## Course_Outline 

-   Broken Access Control
-   Cryptographic Failures
-   Injection
-   Insecure Design
-   Security Misconfiguration
-   Vulnerable and Outdated Components
-   Identification and Authentication Failures
-   Software and Data Integrity Failures
-   Security Logging & Monitoring Failures
-   Server-Side Request Forgery (SSRF)

#### Port Scanning 
    nmap 10.10.56.150 
    Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-05-07 07:48 +0630
    Nmap scan report for 10.10.56.150
    Host is up (0.25s latency).
    Not shown: 990 closed tcp ports (conn-refused)
    PORT     STATE SERVICE
    22/tcp   open  ssh
    80/tcp   open  http
    81/tcp   open  hosts2-ns
    82/tcp   open  xfer
    83/tcp   open  mit-ml-dev
    84/tcp   open  ctf
    85/tcp   open  mit-ml-dev
    8087/tcp open  simplifymedia
    8088/tcp open  radan-http
    8089/tcp open  unknown


### Broken Acess Control

**Insecure Direct Object Reference**  

    Look at other users' notes. What is the flag?

    http://10.10.56.150/note.php?note_id=0

    flag{fivefourthree}

**Cryptographic Failures (Challenge)**

    Have a look around the web app. The developer has left themselves a note indicating that there is sensitive data in a specific directory. 

    What is the name of the mentioned directory?

    Ans: /assets
    ____

    Navigate to the directory you found in question one. What file stands out as being likely to contain sensitive data?

    Ans: webapp.db

    ______

    Use the supporting material to access the sensitive data. What is the password hash of the admin user?

    Ans: 6eea9b7ef19179a06954edd0f6c05ceb

    _______

    Crack the hash.
    What is the admin's plaintext password?

    Ans: 	qwertyuiop
    ____

    Log in as the admin. What is the flag?

    Ans: THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl}

### Command Injection

    What strange text file is in the website's root directory?
    Ans: drpepper.txt

    How many non-root/non-service/non-daemon users are there?
    Ans: 0

    What user is this app running as?
    Ans: apache

    What is the user's shell set as?
    Ans: /sbin/nologin

    What version of Alpine Linux is running?
    Ans: 3.16.0

-----------

### Inscure Design


    What is the value of the flag in joseph's account?
    Ans: THM{Not_3ven_c4tz_c0uld_sav3_U!}

    What is the database file name (the one with the .db extension) in the current directory?
    Ans: todo.db

    import os; print(os.popen("ls -l").read())

    Modify the code to read the contents of the app.py file, which contains the application's source code. What is the value of the secret_flag variable in the source code?

    Ans: THM{Just_a_tiny_misconfiguration}
_______

### Vulnerable and Outdated Components-Lab
    What is the content of the /opt/flag.txt file?
    Ans: THM{But_1ts_n0t_my_f4ult!}
______

### Identification and Authentication Failures Pratical
    What is the flag that you found in darren's account?
    Ans: fe86079416a21a3c99937fea8874b667 

    What is the flag that you found in arthur's account?
    Ans: d9ac0f7db4fda460ac3edeb75d75e16e 

____

### Software Integrity Failures
    What is the SHA-256 hash of https://code.jquery.com/jquery-1.12.4.min.js?

    Ans: sha256-ZosEbRLbNQzLpnKIkEdrPv7lOy9C27hHQ+Xp8a4MxAQ=

### Data Integriy Failures
    Try logging into the application as guest. What is guest's account password?
    Ans: guest

    What is the name of the website's cookie containing a JWT token?
    Ans: jwt-session

    What is the flag presented to the admin user?
    Ans: THM{Dont_take_cookies_from_strangers}

_______

### Security Logging and Monitoring Failtures
    What IP address is the attacker using?
    Ans: 49.99.13.16

    What kind of attack is being carried out?
    Brute Forces

_______

### Sever Side request Forgery
    Explore the website. What is the only host allowed to access the admin area?

    Ans: localhost

    Check the "Download Resume" button. Where does the server parameter point to?
    Ans: secure-file-storage.com

    Using SSRF, make the application send the request to your AttackBox instead of the secure file storage. Are there any API keys in the intercepted request?
    Ans: THM{Hello_Im_just_an_API_key}

-----------------