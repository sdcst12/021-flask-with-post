## SDSS Computing Studies Python Assignment
### Flask!

Objectives:
* To create a basic flask server that receives form data
* To have a flask server respond to a post request
* Create a client python file that can make a post request to a server

### POST Requests
There are two standard methods by which a server can serve a request/response: GET and POST.

GET requests are the ones that are made in the URL, and are generally made using a browser. When you go to Google and search for cats, you can use this URL: https://www.google.com/search?q=cats  
This is an example of a GET method, where the information to be sent is included in the URL.

POST Requests are hidden. This is very important when you don't want sensitive data (such as passwords or cryptographic keys) to be displayed or visible in the URL.  We instead embed data inside the request itself which is received by the server.

Today, we will be looking at some important commands in both a flask SERVER program, and a python CLIENT program.

### Server Considerations
We need to include a couple new items. Look at the file postServer.py as your example.

```from flask import request```
This is required to retrieve the form data from your post request
```payload = request.form```
This is where we actually retrieve the payload from the request.  It does need to be converted to a dictionary for us to use.

## Client Considerations
We need to import the requests module in order to mak a server request by GET or POST from a python program.
One of the methods in the requests module is the .post() method.  While it has many important arguments/parameters, the most important one is the URL of the server.  Another optional argument is "data" which will include any form data that you need to send.  This is generally of a type tuple or list or dictionary.
In our example file client.py we are making a post request using a dictionary.

