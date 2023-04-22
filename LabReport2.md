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

**1st `/add-message` ScreenShot**
![](localWebsite.png)
* The methods called from the code is the *handleRequest* method, it is called when we to add a message to the server.
* A relevant argument in the *handleRequest* if we want to add a message it checks the URL for the "/add-message" query.
* The value from String s changes. Before it I added "bruh moment" it was "Hello \nHow are you\n" then after the method *handleRequest* gets called it changes to "Hello\nHow are you\nbruh moment".

**2nd `/add-message` ScreenShot**
![](localWebsite2.png)
* The methods called from the code is the *handleRequest* method, it is called when we to add a message to the server.
* Just like the previous screenshot the relevant argument in the *handleRequest* if we want to add a message it checks the URL for the "/add-message" query.
* The value from String s changes. Before it I added "123" it was "Hello\nHow are you\nbruh moment\n" then after the method *handleRequest* gets called it changes to "Hello\nHow are you\nbruh moment\n123\n".

#Part 2
**Failure-inducing Input**
```
public void testReverseInPlace2() {
    int[] input2 = {1,2,3};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{3,2,1} , input2);
}
```
**Pass-inducing Input**
```
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
}
```
**Symptom as JUnit**
