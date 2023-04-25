# Lab Report 2

##Code for StringServer

~~~
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String string = "";

    public String handleRequest(URI url){
        if (url.getPath().equals("/")){
            return String.format("%s", string);
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")){
                String[] parameters = url.getQuery().split("=");
                string = string + "\n" + parameters[1];
                return String.format("%s", string);
            }
            return "404 Not Found!";
        } 
        
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

## Using add-message

![Image]Hello.jpg
![Image}How.jpg
