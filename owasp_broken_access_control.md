## Objectives that will learn:
+   Understand what Broken Access Control is and its impact.
+   Identify Broken Access Control vulnerabilities in web applications.
+   Exploit these vulnerabilities in a controlled environment.
+   Understand and apply measures to mitigate and prevent these vulnerabilities.


### Broken Access Control Introduction

    What is IDOR?
    Ans: Insecure Direct Object References

    What occurs when an attacker can access resources or data belonging to other users with the same level of access?
    Ans: Horizonal Privilege Escalation

    What occurs when an attacker can access resources or data from users with higher access levels?
    Ans: Vertical Privilege Escalation

    What is ABAC?
    Ans: Attribute-Based Access Control

    What is RBAC?
    Role-Based Access Control

____
### Assessing the web application
    What is the type of server that is hosting the web application? This can be found in the response of the request in Burp Suite.
    Ans: Apache

    What is the name of the parameter in the JSON response from the login request that contains a redirect link?
    Ans: redirect_link

    What Burp Suite module allows us to capture requests and responses between ourselves and our target?
    Ans : proxy

    What is the admin’s email that can be found in the online users’ table?
    Ans: admin@admin.com

_____
### Exploiting Web Application
    What kind of privilege escalation happened after accessing admin.php?
    Ans: vertical

    What parameter allows the attacker to access the admin page?
    Ans: isadmin

    What is the flag in the admin page?
    THM{I_C4n_3xpl01t_B4c}

________