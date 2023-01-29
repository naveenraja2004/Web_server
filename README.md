# Developing a Simple Webserver

# AIM:

Name=Naveen raja N.R=22008936

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler

content =
"""
<html>
<body>
<h1>Welcome to the webserver </h1>
</body>
</html>
"""
class WebHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
    
server_address=('',8000)
httpd=HTTPServer(server_address,WebHandler)
print("Web server running...")
httpd.serve_forever()    
```
# OUTPUT:
![out2](https://user-images.githubusercontent.com/118707204/215314178-ed5f7b3f-2b58-4583-9f48-0f9997bf5b31.png)


# RESULT:

The program is executed succesfully
