Tags: [[Troubleshooting]] [[API]] [[HTTP]] [[Fundamentals]] [[Internet]] 
<h2>API</h2>
An API, or Application Programming Interface, is a set of rules, protocols, and tools that allows different software applications to communicate with each other. It defines the methods and data formats that applications can use to request and exchange information.

APIs are used extensively in software development to enable integration between different systems, services, or platforms. They abstract the underlying complexity of systems and provide a standardized way for developers to interact with them.

<h2>HTTP</h2>
HTTP stands for Hypertext Transfer Protocol. It is a protocol used for transferring hypertext documents, such as HTML files, over the internet. HTTP is the foundation of data communication on the internet.

- Server/client relationship
- Stateless - independent calls
- Uniform Resource Identifier - URIs are used to identify resources on the web, such as web pages, images, or files. A URI typically consists of a scheme (e.g., http:// or https://)
- **Connection Establishment**: HTTP operates over TCP/IP (Transmission Control Protocol/Internet Protocol) and uses TCP connections to establish communication between clients and servers.
- **Secure Version (HTTPS)**: HTTPS (Hypertext Transfer Protocol Secure) is an extension of HTTP that uses encryption (usually SSL/TLS) to secure communication between clients and servers. HTTPS is commonly used for transmitting sensitive data
<h3>Common HTTP Codes</h3>
1. **1xx Informational**: These status codes indicate that the server has received the request and is continuing the process.
    
    - 100 Continue: The server has received the initial part of the request and is awaiting the rest.
    - 101 Switching Protocols: The server is switching protocols as requested by the client (e.g., upgrading to WebSocket).
2. **2xx Success**: These status codes indicate that the request was received, understood, and processed successfully.
    
    - 200 OK: The request was successful.
    - 201 Created: The request has been fulfilled, and a new resource has been created.
    - 204 No Content: The server successfully processed the request but is not returning any content.
3. **3xx Redirection**: These status codes indicate that further action needs to be taken by the client to complete the request.
    
    - 301 Moved Permanently: The requested resource has been permanently moved to a new URL.
    - 302 Found (Moved Temporarily): The requested resource has been temporarily moved to a different URL.
4. **4xx Client Errors**: These status codes indicate that there was a problem with the client's request.
    
    - 400 Bad Request: The server cannot process the request due to a client error (e.g., malformed syntax).
    - 401 Unauthorized: The client needs to authenticate to gain access to the resource.
    - 403 Forbidden: The client does not have permission to access the requested resource.
    - 404 Not Found: The requested resource could not be found on the server.
5. **5xx Server Errors**: These status codes indicate that there was a problem with the server while processing the request.
    
    - 500 Internal Server Error: A generic error message indicating that something went wrong on the server.
    - 502 Bad Gateway: The server, while acting as a gateway or proxy, received an invalid response from the upstream server.
    - 503 Service Unavailable: The server is currently unable to handle the request due to temporary overload or maintenance.