# LocalHost

This is a simple Node.js code that creates an HTTP server using the built-in http module. The server listens on port 8080 and responds with a "Hello world!" message in HTML format whenever a request is made to it.

Code Explanation
Let's break down the code step by step:

const { createServer } = require('http');

This line imports the createServer function from the http module. It allows us to create an HTTP server.

const server = createServer((request, response) => {
    response.writeHead(200, { 'Content-Type': 'text/html' });
    response.write('<h1>Hello world!</h1>');
    return response.end();
});

Here, we use the createServer function to create an HTTP server. It takes a callback function as an argument, which will be executed whenever a request is made to the server. The callback function receives two parameters: request and response.

request: Represents the incoming HTTP request made by a client.
response: Represents the server's response to the client.
In the callback function, we perform the following tasks:

Use response.writeHead to set the HTTP status code to 200 (OK) and specify the content type as 'text/html'.
Use response.write to write the HTML content '<h1>Hello world!</h1>' to the response.
Finally, we call response.end() to indicate that the response is complete and should be sent back to the client.

server.listen(8080);

This line tells the server to start listening on port 8080. The server will be able to receive incoming HTTP requests on this port.
