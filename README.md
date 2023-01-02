# Developing a Simple Webserver

# AIM:

Name : B.Vijay kumar Ref.no:22007124

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

content ="""
<html>
<body>
<h1>WELCOME</h1>
<h2>Name: B Vijay Kumar</h2>
<h2>Reference no:22007124</h2>
<h3>LIST OF FRAMEWORKS</h3>
<h4>-laravel</h4>
<h4>-meteor</h4>
<h4>django</h4>
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
![image](./djangoframeworks.png)
# RESULT:

The program is executed succesfully
