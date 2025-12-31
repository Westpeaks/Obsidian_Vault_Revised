![[InternetAPIErrorCodes.png]]

## Common API Errors and How to Resolve Them

### 1. HTTP 400 Bad Request

**Description:**

- A 400 Bad Request indicates that the client-side input is incorrect or malformed. This means that the server cannot process the request and it is typically due to syntax error. In the example below, the user input is missing a comma. 
  
  ![[UserCommaError.webp]]
**Solution:**

Correct syntax errors. 

### 2. HTTP 401 Unauthorized

**Description:**

- A 401 Unauthorized error occurs when the request has invalid credentials. The request has no valid authorization. For example, it is missing a secret key or token. This could be caused by incorrect authentication credentials, username or password, missing or inaccurate authorization headers, or incorrect access permissions.

**Solution:**

- Ensure that the call includes the appropriate key or OAuth Token.

```API
GET /admin/users HTTP/1.1  
Host: example.com  
Authorization: Bearer valid_token
```
### 3. HTTP 404 Not Found

**Description:**

- This indicates that the requested resource does not exist on the server side (**Ex.** you request a user that does not exist). 

**Solution:**

- Correct the syntax of the request to gather the right data. 

### 4. 500 Internal Server Error

**Description:**

- This is a generic error indicating that an unexpected condition has occurred. This makes the server unable to complete the request. 

**Solution:**

- Server logs should help track down the issue. 
- Debugging steps:
	- Review server logs for detailed error messages.
	- Ensure all dependencies and configurations are correctly set.
	- Handle exceptions in the server code.

## Other Common Errors

#### 402 Payment Required Error

The 402 Payment Required Error occurs when the client must pay to access the requested resource. This error is not commonly encountered in REST API development.

#### 403 Forbidden Error

The 403 Forbidden Error occurs when the client cannot access the requested resource. This error can be caused by incorrect access permissions, missing or inaccurate authorization headers, or external restrictions blocking access to the API endpoints. 

To troubleshoot this error, ensure you have adequate permissions for making requests on the API endpoints in question. Additionally, you should verify that you are using the correct authorization headers and that no external restrictions block access to the API endpoints.

#### 408 Request Timeout Error:

Occurs when the server takes too long to respond to the client's request. To troubleshoot it, double-check the URL and ensure it’s correct, check your internet connection, and then reload the web page.

#### 502 Bad Gateway Error

Occurs when the server acting as a gateway or proxy receives an invalid response from the upstream server. To troubleshoot it, ensure you use the correct domain name and the server is reachable. Also, check your firewall logs to see if you are blocking any traffic.

#### 504 Gateway Timeout Error

This occurs when the server acting as a gateway or proxy takes too long to receive a response from the upstream server. To troubleshoot the error, verify your internet connection is working and that you are sending valid data parameters within the request.

#### 507 Insufficient Storage Error

Occurs when the server cannot store the representation needed to complete the request. To troubleshoot it, subscribe to a better package that offers more storage or optimise your current repository if there is excess page traffic.

#### 508 Loop Detector Error

This occurs when the server detects an infinite loop, which could be caused by too many redirects preventing the requested resource from rendering. To troubleshoot the error, look for the API call(s) causing the loop and forward it to your API provider for assistance.

# Links:

[Troubleshooting Common API Errors and How to Fix Them](https://medium.com/@2957607810/troubleshooting-common-api-errors-and-how-to-fix-them-6aa0419cb32d)

#api

2025111327