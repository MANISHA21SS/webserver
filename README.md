# Developing a Simple Webserver

# AIM:

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```py
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
<h2>4.MERN Stack</h2>
<h2>5.ATP.Net</h2>
</body>
</html>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
## OUTPUT:
### Server output
file:///home/sec/Pictures/Screenshots/vhg.png![image](https://github.com/MANISHA21SS/webserver/assets/147474298/d0033006-5d48-4e95-9bd7-7a3e1b802202)

### Client output
![image](https://github.com/MANISHA21SS/webserver/assets/147474298/e2287c4e-cd81-421f-879c-dd49d78d42d9)


## RESULT:
The program is executed succesfully
