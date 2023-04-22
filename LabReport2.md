# Part 1

**StringServer Code**

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String bruh ="";
    public String handleRequest(URI url) {
        if(url.getPath().equals("/add-message")){
            String[] parameters = url.getQuery().split("=");
            bruh+= parameters[1]+ "\n";
            return bruh;
        }
        else{
            return "404 not found";
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
```

![](localWebsite.png)
* The methods called from the code is the *handleRequest* method, it is called when we to add a message to the server.
* A relevant argument in the *handleRequest* if we want to add a message it checks the URL for the "/add-message" query.
* The value from String s changes. Before it I added "bruh moment" it was "Hello \nHow are you" then after the method *handleRequest* gets called it changes to "Hello\nHow are you\nbruh moment".

