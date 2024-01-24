# The code for the `ChatServer.java` file is found below:
```
    import java.io.IOException;
    import java.net.URI;
    import java.util.ArrayList;
    class Handler implements URLHandler{

        ArrayList<String> messages = new ArrayList<>();

        public String handleRequest(URI url){
            if(url.getPath().contains("/add-message")){
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")){
                    String[] message = parameters[1].split("&");
                    messages.add(String.format(parameters[2]+": " + message[0]).replace("+", " "));
                }
            }
            String runningString = "";
            for (String message: messages){
                runningString = String.format(runningString + message + "\n");
            }
            return runningString;
            }
        
    }



    class ChatServer{
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

Hi
