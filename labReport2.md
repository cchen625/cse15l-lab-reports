Part 1:
~~~

import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int msgCount = 0;
    String str = "";

    public String handleRequest(URI url) {
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                System.out.println(parameters[1]);
                if (parameters[1].contains("+")) {
                    String[] words = parameters[1].split("\\+");
                    String phrase = "";
                    for (String word: words) {
                        phrase = phrase + " " + word;
                    }
                    msgCount++;
                    String temp = String.format("\n%d. %s", msgCount, phrase);
                    str = str + temp;
                    return str;
                }
                else {
                    msgCount++;
                    String temp = String.format("\n%d. %s", msgCount, parameters[1]);
                    str = str + temp;
                    return str;
                }
        }
        }
        return "404 Not Found!";
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
~~~
