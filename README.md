# Developing a Simple Webserver
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation
### Step 2:
Design of webserver workflow
### Step 3:
Implementation using Python code
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver

## PROGRAM:
```
content = """
<!DOCTYPE html>
<html>
<head>
<title>My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Frameworks</h1>
<h2>1.Django</h2> 
<h2>2.MEAN Stack</h2>
<h2>3.React</h2>
<h2>4.Angular</h2>
<h2>5.Express</h2>

</body>
</html>
"""

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print('Get request received...')
        self.send_response(200)
        self.end_headers()
        self.wfile.write(content.encode()) 

print("This is my webserver")
server_address =('',80)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```



## OUTPUT:

### Server Side Output

![image](https://user-images.githubusercontent.com/118351569/206891524-844f55e1-5c75-4571-9230-0733c99fd55b.png)



### Client Side Output

![image](https://user-images.githubusercontent.com/118351569/206891561-3a0c6e49-e300-4af1-9876-ccc4c2e393a6.png)







## RESULT:

Thus the webserver is developed to display about top five programming languages.
