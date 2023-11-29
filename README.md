# Developing a Simple Webserver
NAME: SAI VISHAL D REF.NO.:23013576

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
``````

from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
<title>Webserver</title>
</head>
<body>
<h1>Top Five Web Application Development</h1>
<h3>1.Django</h3>
<h3>2.MEAN Stack</h3>
<h3>3.React<h3>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()

``````
# OUTPUT:
![Screenshot 2023-11-29 110021](https://github.com/SaiVishal1105/Web_server/assets/145742557/dca830c4-abc8-4b39-a65f-69a78f09c626)

# RESULT:

The program is executed succesfully
