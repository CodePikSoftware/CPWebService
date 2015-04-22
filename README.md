# CPWebService
Java SE Web Services Library to send HTTP GET, POST requests, send File Attachments and receive HTTP responses easily from any web server.

# Installation
1. Import the CPWebService.jar libary into your JavaSE Project
2. Import the support libraries into your Java SE Project

#Syntax
The CPWebSerice will use following basic syntax to send any HTTP GET, POST Request to a web address.

  CPWebService login = new CPWebService("http://yoururl/", new codepik.CPWebServiceResponse() {
          
            @Override
            public void getAPIResponse(CPResponse output) {
            //Executed when the response is recieved
                System.out.println(output.getResponseCode()); //Prints the Response code
                System.out.println(output.getResponseText()); //Prints the Response Body
                
                
            }
        });
  
  //Optional : add parameters to the request body      
  login.addParameter("parameter1","value");
  login.addParameter("parameter2","value");
  
  //send the request to the server URL provided
  login.run();


