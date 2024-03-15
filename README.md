# EX01 Developing a Simple Webserver
## Date:15/03/2024

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
     <head>
          <title>TOP 5 SOFTWARE COMPANIES </title>
     </head>     
     <body>
     <center>
     <caption align="center"><b>TOP 5 SOFTWARE COMPANIES</b></caption>
     </center>
     <table align="center" width="500" cellspacing="2" cellpadding="4" border="5" bgcolor="black"
          <tr align="center">
             <th bgcolor=" blue">S.NO</th>
             <th bgcolor=" blue">COMPANY</th>
             <th bgcolor=" blue">REVENUE</th>
             <th bgcolor=" blue">R&D SPEND</th>
             <th bgcolor=" blue">PERCENTAGE OF R&D</th>
          </tr>
          <tr align="center">
            <td bgcolor="light blue">1</td>  
            <th bgcolor="light blue">AMAZON.com</th>
            <td bgcolor="light blue">$177,866m</td>  
            <td bgcolor="light blue">$23,015m</td>
            <td bgcolor="light blue">0.2%</td>  
          </tr>
          <tr align="center">
            <td bgcolor="blue">2</td>  
            <th bgcolor="blue">ALPHABET</th>
            <td bgcolor="blue">$110,855m</td>  
            <td bgcolor="blue">$16,625m</td>
            <td bgcolor="blue">0.0%</td>
          </tr>  
          <tr align="center">
            <td bgcolor="light blue">3</td>  
            <th bgcolor="light blue">FACEBOOK</th>
            <td bgcolor="light blue">$40,653m</td>  
            <td bgcolor="light blue">$7,754m</td>
            <td bgcolor="light blue">0.0%</td>
          </tr> 
          <tr align="center">
            <td bgcolor="blue">4</td>  
            <th bgcolor="blue">SALESFORCE.com</th>
            <td bgcolor="blue">$10,480m</td>  
            <td bgcolor="blue">$1,632.2m</td>
            <td bgcolor="blue">0.8%</td>
          </tr> 
          <tr align="center">
            <td bgcolor="light blue">5</td>  
            <th bgcolor="light blue">NETFLIX</th>
            <td bgcolor="light blue">$11,692m</td>  
            <td bgcolor="light blue">$11,052.8m</td>
            <td bgcolor="light blue">0.0%</td>
          </tr> 
    </table>
    </html>  


                    
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![webserver 2](https://github.com/keerthanasivakumar02/simplewebserver/assets/150827397/5c85f172-6e16-4260-b187-6d229b451a6f)

![webserver 3](https://github.com/keerthanasivakumar02/simplewebserver/assets/150827397/755c2566-e54c-40ce-adc3-306cacb206ab)



## RESULT:
The program for implementing simple webserver is executed successfully.
