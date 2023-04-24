# CSE 15L Lab Report 2

## Part 1

`StringServer` code:

import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
    String str = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format(str);
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    str += parameters[1] + "\n";
                    return String.format(str);
                }
            }
            return "404 Not Found!";
        }
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}

Screenshots of using `/add-message`:

![Image](firefox_0424_0007_56.png)

The methods called in the screenshot above are `parseInt(args[0])` for `int port`, which parses what is inputted into `args[0]` when the command `java StringServer 4000` is ran on the terminal. 4000 will be the port `StringServer` runs on. Then `Server.start(port, new Handler());` method is ran which starts a webserver with the port and a new `Handler` class. The `Handler` class then runs the method `HandleRequest`, which takes in the parameter `URI url`. 

![Image](firefox_0421_2335_47.png)

