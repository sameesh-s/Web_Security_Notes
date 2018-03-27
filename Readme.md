Chapter 1: Web Application (In) Security
-----------------------------------------
Vulnerabilities in web applications arise because of a single  core problem: users can submit arbitrary input.
Chapter 2: Core Defense Mechanisms
-----------------------------------
* Broken authentication
* Broken access controls
* SQL injection
* Cross-site scripting
* Information leakage
* Cross-site request forgery
The core security problem: Users can submit arbitrary input.
* Users can interfere with any piece of data transmitted between the client and the server, including request parameters, cookies, and HTTP headers. Any security controls implemented on the client side, such as input validation checks, can be easily circumvented.
* Users can send requests in any sequence and can submit parameters at a different stage than the application expects, more than once, or not at all. Any assumption developers make about how users will interact with the application may be violated.
* Users are not restricted to using only a web browser to access the application Numerous widley available tools operate alongside, or independently of, a browser to help attack web applications . These tools can make requests that no browser would ordinarily make and can generate huge numbers of requests quickly to find and exploit problems.
eg:
* Modifying a session token transmitted in an HTTP cookie to hijack the session of another authenticated user.
* Removing certain parameters that normally are submitted to exploit a logic flaw in the application's processing.
* Altering some input that will be processed by a back-end database to inject a malicious database query and access sensitive data

Key Problem Factors
--------------------
* Underdevelped Security Awareness
* Custom Development
* Decceptive Simplicity
* RapidlyEvolving Threat Profile
* Overextended Technologies
  
