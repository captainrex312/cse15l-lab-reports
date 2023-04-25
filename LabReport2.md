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

![Image](Hello.jpg)

1) Which methods in your code are called?\
- The method called is: 'handleRequest(URI url)' of the 'Handler' class.\
2) What are the relevant arguments to those methods, and the values of any relevant fields of the class?\
- The argument 'URL' is a url object representing the incoming request with the path '/add-message' and query string 'Hello.'\
3) How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.\
- The field 'string' is originally an empty string, but is updated to "Hello" once the command is run.\

![Image](How.jpg)

1) Which methods in your code are called?\
- The method called is: 'handleRequest(URI url)' of the 'Handler' class.\
2) What are the relevant arguments to those methods, and the values of any relevant fields of the class?\
- The argument 'URL' is a url object representing the incoming request with the path '/add-message' and query string 'How are you.'\
3) How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.\
-The field 'string' is originally the string "Hello", but is updated to "Hello" followed by "How are you" once the command is run.\

## Choosing a bug from Lab 3
