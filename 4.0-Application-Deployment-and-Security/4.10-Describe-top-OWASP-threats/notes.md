<!-- cSpell:ignore  OWASP,CSRF,SQLninja,SQLmap,SAST,-->

# Top OWASP threats

## What's OWASP?

* Open Web Application Security Project (OWASP)
* Provides tools, code projects and documentation projects

## XSS

* A script which is embedded within comments or CSS code
* Make sure you sanitize all code which doesn't need to be there
* Can be used to execute a script within the website URI

## SQL injections

* Code injection technique
* Inject SQL statements to dump database or manipulate data
* Requires the SQL database to have a vulnerability exploited

### SQL injections - web pages

* The most common form of web hacking
* Placement of malicious code in SQL statements
* Often occurs when user needs to input data such as username,but instead they give a SQL statement

### Detection of SQL injections 

* Use open source tools such as SQLmap or SQLninja
* Static Application Security Testing (SAST) is designed to analyze code and scan for security flaws
* Automate testing to make it regular and affective

### Preventing SQL injections 

* Database firewalls 
    * Can be used to permit only certain traffic to access your database
    * Detect SQL injections based on number of queries from a particular host 
* Prepared statements can be use in conjunction with variable binding
    * Attackers are unable to change the intent of a query
* Stored procedures
    * Stored in the database itself, then called from the application
    * Auditors look for *sp_execute*, *execute* or *exec* uses within an SQL server
    * This can cause some web applications to have 'db_owner' rights to the database
* Whitelist input validation
    * Names of tables or columns should come from the application/code, rather than the user
    * Always append a data conversion before it's appended to he query
    * Considered a secondary defence
* Escaping all user-supplied input
    * Last ditch attempt if other options are not feasible
    * Usually used to retrofit legacy code
    * Typically not very cost affective

## CSRF

* Cross site request forgery (sea surf)
* Attacker intends for user to execute their code
* Aimed at a site whereby a user is already authenticated (think a bank etc)
* This can be leveraged even if a user doesn't click on a link etc if the site is vulnerable to XSS.