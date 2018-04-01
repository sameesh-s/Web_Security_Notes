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

Chapter 2: Core Defense Mechanisms
----------------------------------
The fundamental security problem with all web applications: That all user input is untrusted.
* Handling user access to the application's data and functionality to prevent users from gaining unauthorized access
* Handling user input to the application's functions to prevent malformed input from causing undesirable behavior.
* Handling attackers to ensure that the application behaves appropriately when being directly targeted, taking suitable defensive and offensive measures to frustrate the attacker.
* Managing the application itself by enabling administrators to moniter its activities and configure its functionality.
Handling User access
--------------------
* Authentication
* Session management
* Access control
Handling User Input
-------------------
* Varieties of Input
Approches to Input Handling  
---------------------------
* Reject known Bad (Blacklisting)
[NOTE] Attacks that exploit the handling of NULL bytes arise in many areas of web application security. In contexts where a NULL byte acts as a string delimiter, it can be used to terminate a filename or a query to some backend component. In contexts where NULL bytes are tolerated and ignored (for example, within HTML in some browsers), arbitrary NULL bytes can be inserted withing blocked expressions to defeat some blacklist-based filters.
* Accept Known Good(extremely effective - white listing)
* Sanitization (Instead of rejecting, It remove the malcious content)
* Safe Data Handling (SQL injection avoid using parameterized query)
* Semantic checks
* Boundary Validation (Validation on server side)
* Multistep Validation and Canonicalization
Handling Attackers
------------------
* Handling errors
* Maintaining audit logs
=> All events relating to the authentication functionality, such as successful and failed login, and change of password.
=> Key transactions, such as credit card payment and fund transfers
=> Access attemptes that are blocked by the access control mechanisms
=> Any requests containing known attack strings that indicate overtly malicious intentions.
* Alerting administrators
* Reacting to attacks
* Alerting administrators
=> Usage anomalies, such as large numbers of requests being received from a single IP address or user, indicating a scripted attack.
=> Business anomalies, such as an unusual number of funds transfers being made to or from a single bank account
=> Requests containing known attack strings
=> Requests where data that is hidden from ordinary users has been modified
* Reacting to Attacks(slow response, terminate attacker's session)
* Managing the Application
=> Weaknesses in the authentication mechanism may enable an attacker to gain  administrative access, effectively compromising the entire application.
=> Many applications do not implement effective access control of some of their administrative functions. An attacker may find a means of creating a new user account with powerful privilages.
=> Administrative functionality often involves displaying data that originated from ordinary users. Any cross-site scripting flaws within the administrative interface can lead to comporomise of a suer session that is guranteed to have powerful privileges.
=> administrative functionality is often subjected to less rigorous security testing, because its users are deement to be trusted, or because pen testers are given access to only low-privliaged accounts. 

  
