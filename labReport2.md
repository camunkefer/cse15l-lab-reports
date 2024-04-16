# Part 1
## Code for `ChatServer`
```
import java.io.IOException;
import java.net.URI;
class Handler implements URLHandler {
    String s = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format(s);
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    s = s + parameters[2]+ ": " + parameters[1].substring(0, parameters[1].indexOf("&")) + "\n";
                    return String.format(s);
                }
            }
            return "404 Not Found!";
        }
    }
}
class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```
## Screenshots of using `/add-message`
### Screenshot 1
![Image](Screenshot 2024-04-16 102947.png)
### Screenshot 2
![Image](Screenshot 2024-04-16 102735.png)
