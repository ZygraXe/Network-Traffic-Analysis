## HTTP Credential Exposure Analysis

### Filter Used

http


### Description
HTTP protocol transmits data in plaintext without encryption. When users submit login credentials over HTTP, sensitive information such as usernames and passwords can be intercepted by attackers monitoring the network.

### Analysis Performed
A login attempt was made on an HTTP-based website while network traffic was being captured using Wireshark. The captured packets were analyzed to inspect HTTP POST requests.

### Observation
The login request was transmitted in plaintext, and the submitted username and password were visible directly within the HTTP packet payload. This demonstrates how attackers can easily steal credentials on unsecured networks.

### Impact
- Exposure of user credentials
- Risk of account compromise
- Increased likelihood of credential reuse attacks
- Loss of confidentiality

### Security Risk Level
High

### Mitigation
- Enforce HTTPS using TLS encryption
- Implement HTTP Strict Transport Security (HSTS)
- Avoid transmitting credentials over unsecured HTTP
- Use secure authentication mechanisms

### Conclusion
This analysis highlights the critical importance of encrypting web traffic. Using HTTP for authentication exposes sensitive data and poses a serious security risk.
