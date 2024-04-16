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
![Image](Screenshot%202024-04-16%20102947.png) <br>
* Methods in my code that were called are `handleRequest`, then `getRequestURI()`. `handleRequest` inside the `handler` class calls `getPath` and `getQuery`. <br>
* `handleRequest` has `exchange.getRequestURI()` as an argument. It has `s` as a field which is the string that is outputted onto the screen of the website and gets updated within `handleRequest`'s body. `getRequestURI` has no arguments and will simply get the URI which is `http://localhost:4000/add-message?s=Hello&user=Cameron` to be inputted as an argument in `handleRequest`. Inside `handleRequest`, it will call  `getPath` which is `/add-message` and `getQuery` which is `?s=Hello&user=Cameron` to be used to process the paths and queries and see how `s` needs to be updated. <br>
* `s` in `handleRequest` is a value that changes from this specific request. `handleRequest` goes into the path of the URL, and if it contains `/add-message` which it does, will update the value of `s` according to what the query has for user and message. Since the query is `?s=Hello&user=Cameron`, `s` gets updated to `"Cameron: Hello\n"` <br>
### Screenshot 2
![Image](Screenshot%202024-04-16%20102735.png) <br>
* Methods in my code that were called are `handleRequest`, then `getRequestURI()`. `handleRequest` inside the `handler` class calls `getPath` and `getQuery`. <br>
* `handleRequest` has `exchange.getRequestURI()` as an argument. It has `s` as a field which is the string that is outputted onto the screen of the website and gets updated within `handleRequest`'s body. `getRequestURI` has no arguments and will simply get the URI which is `http://localhost:4000/add-message?s=Hi!!&user=Brianna` to be inputted as an argument in `handleRequest`. Inside `handleRequest`, it will call  `getPath` which is `/add-message` and `getQuery` which is `?s=Hi!!&user=Brianna` to be used to process the paths and queries and see how `s` needs to be updated. <br>
* `s` in `handleRequest` is a value that changes from this specific request. `handleRequest` goes into the path of the URL, and if it contains `/add-message` which it does, will update the value of `s` according to what the query has for user and message. Since the query is `?s=Hi!!&user=Brianna`, `s` gets updated to `"Cameron: Hello\n Brianna: Hi!!\n"` <br>
# Part 2
## command line of your computer, `ls` with the absolute path to the private key
![Image]()  <br>
## command line of the ieng6 machine, run `ls` with the absolute path to the public key
![Image]()  <br>
## A terminal interaction - log into your ieng6 account without being asked for a password
![Image]()  <br>
# Part 3
What I learned from lab in week 2 is that you can update a webpage by adding paths and queries to the end of it. This is a really cool and fun feature that I can play arround with. I also leanred about the differnt parts of a URL.
