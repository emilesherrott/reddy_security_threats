## Injection

### What is injection?
- Injection is an attacker's attempt to send data to an application in a way that will change the meaning of commands being sent to an interpreter.

### How does it work?
- It is carried out by cyber criminals or people who want access to sensitive data for malicious purposes.  
- It can be carried out by rival companies in order to decrease an organisation's performance and make it less of a threat in competitive sense. For example, a company could lose users due to them seeming untrustworthy from a data breach, or they could lose data which directly impacts the company financially.  
- It could be carried out by ethical hackers in order to expose vulnerabilities in a company's software or databases. This allows the company to improve their security to prevent a malicious attack in the future.  

### What issues / problems does it cause?
- Injection attacks can cause data loss, data corruption, security breaches, and possibly the loss of control of the target host and the release of sensitive information linked to the host.

### Mitigations
1. Use of prepared statements (with parameterized queries). 
I.e - when making sql queries to a database, we wouldn't define any variables we are using directly in the code (e.g if we were searching for data from a specific email, we should not explicityely define a variable equal to that email beforehand). Queries should also be parameterised, meaning we would not use string-literals to directly input information into the query, as this opens up the query to being modified. 

2. Using DCL (Data control language) to limit access to certain queries. 
I.e - ensuring that DELETE or UPDATE queries cannot be used within an SQL database - this can further prevent attackers from making changes to data or extracting it. 

3. Don't trust any user input.  
Treat all user input as untrusted. Any user input that is used in an SQL query introduces a risk of an SQL injection. Treat input from authenticated and/or internal users the same way that you treat public input.

4. Adopt the latest technologies.  
Older web development technologies don't have SQLi protection. Use the latest version of the development environment and language and the latest technologies associated with that environment/language. For example, in PHP use PDO instead of MySQLi.

5. Continuous scanning and Penetration testing.  
Continuous web application scanning involves regularly running automated vulnerability scanning tools to identify and assess any potential vulnerabilities in a system.  
Penetration testing involves simulating an attack on a system to identify and exploit vulnerabilities.  
