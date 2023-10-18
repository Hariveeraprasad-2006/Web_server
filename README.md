# Developing a Simple Webserver
Name : Hari Veera Prasad

ID : 23009466

 Dept : AIML 
# AIM:

Develop a webserver to display about top five web application development frameworks.

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
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>

<h1>1. Django</h1>
<h1>2. MEAN Stack</h1>
<h1>3. React</h1>
<h1>4. Ruby on Rails</h1>
<h1>5. Angular</h1>

</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received")
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my web server")
server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()
```

# OUTPUT:
![image](https://github.com/Hariveeraprasad-2006/Web_server/assets/145049988/4fd6a4ed-0205-44dc-8795-6163fd151d3b)

# RESULT:

The program is executed succesfully.
