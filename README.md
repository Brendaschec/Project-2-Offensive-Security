#Project 2 Offensive-security
Project 2-Offensive Security
Challenges for Project 2 - Day 1


Flag 1

Category: Easy
On the Welcome.php page, enter a reflected XSS payload where it says "Put Your Name Here." The successful payload will make a pop up appear. When you close out the pop-up, Flag 1 will appear!



Flag 2


Category: Intermediate


On the Memory-Planner.php webpage, the flag will appear if you enter an XSS payload in the "Choose Your Character" field to make a pop-up.


Note: Input validation makes this one more challenging.


Click here for a hint
Input validation code is removing the case insensitive word "script"








Flag 3

Category: Easy
Access the Comments.php page and make a pop-up appear to find Flag 3.



Flag 4


Category: Advanced


Vulnerability: Sensitive data exposure.


Click here for a hint
Watch your head(er).






Flag 5

Category: Easy
In the second field on the Memory-Planner.php page, conduct a local file inclusion (LFI) exploit by loading the file to access this flag.



Flag 6


Category: Intermediate


Vulnerability: LFI (advanced). Load a php file to access the flag.


Click here for a hint
Memory Planner : Choose your location.






Click here for a hint
Input validation requires .jpg somewhere in the file name.






Flag 7


Category: Advanced


Vulnerability: SQL injection (on the Login.php page)


Click here for a hint
Enter the payload in the second field on the user login page.






Click here for a hint
Try lots of different SQL injection payloads. Check out this webpage for ideas: https://github.com/payloadbox/sql-injection-payload-list






Click here for a hint
Try adding a blank space at the end of your payload!






Flag 8


Category: Easy


This flag is on the Login.php page.


Free Hint: HTML


Click here for a hint
Highlight the page, or view the source code, and the answer may appear.






Flag 9

Category: Easy

Vulnerability: Sensitive data exposure

Free Hint: Standard used by websites to communicate with web crawlers and other web robots.



Flag 10


Category: Easy


Vulnerability: Command injection


Click here for a Hint
Networking.php: DNS check






Click here for a Hint
View the contents of the vendors.txt file with your payload.






Flag 11


Category: Intermediate


Vulnerability: Command injection (advanced)


Click here for a Hint
MX record checker






Click here for a Hint
Access the vendors.txt file again. Now the input validation doesnt allow ";" or "&", so try a different method.






Flag 12


Category: Advanced


Vulnerability: Brute force attacks


Click here for a Hint
Also the admin login






Click here for a Hint
Flag 10 or 11 can help you find the user. Now brute force the password!






Flag 13


Category: Expert


Vulnerability: PHP injection


Click here for a Hint
Flag 9 will help you find this flag.






Click here for a Hint
Research and try different PHP injection payloads to find this flag.






Flag 14


Category: Advanced


Vulnerability: Session management


Click here for a Hint
Finding Flag 12 will take you to the page where this Flag exists.






Click here for a Hint
Burp Repeater would work, but Burp Intruder would make it easier to run this around 100 times.






Flag 15


Category: Advanced


Vulnerability: Directory traversal


Click here for a Hint
On the disclaimer page.






Click here for a Hint
Use Flag 10 Exploit to find the hidden directory.






Click here for a Hint
Challenges for Project 2 - Day 2


Flag 1

Category: Reconnaissance
Use a Dossier open source tool found within OSInt Framework to find information about the WHOIS domain for the website totalrekall.xyz. Look for Flag1."



Flag 2

Category: Reconnaissance
Flag 2 is the IP address of totalrekall.xyz.



Flag 3


Category: Reconnaissance


SSL certificate research about totalrekall.xyz will lead you to Flag 3.


Click here for a Hint
crt.sh








Flag 4

Category: Scanning
Run an Nmap or Zenmap scan on your network to determine the available hosts. Your network begins with 192.168.13. The flag is the count of hosts returned (not including the host you are scanning from).



Flag 5

Category: Scanning
Run an agressive scan against the discovered hosts. The flag is the IP address of the host running Drupal.



Flag 6

Category: Scanning
Run a Nessus scan against the host that ends with .12. View the details of the one critical vulnerability. The flag is the ID number at the top right of the page.



Flag 7


Category: Exploit


Use an RCE exploit through Metasploit to exploit the host that ends with .10. Using the results from the agressive Nmap scan, try to to determine which exploit works. You may have to try many before finding the one that works. Once you have access to the host, search that server for Flag 7.


Click here for a Hint
Search for Tomcat JSP








Flag 8

Category: Exploit
Use an RCE exploit through Metasploit to exploit the host that ends with .11. You will use the "Shocking" exploit. You may have to try many exploits before you find the one that works.

Free Hint 1: You will need to set the TARGETURI option to /cgi-bin/shockme.cgi Once you have access to the host, search that server for Flag 8.

Free Hint 2: Check your sudo privileges.



Flag 9


Category: Exploit


On the same server that you exploited to find Flag 8, continue to search for Flag 9.


Click here for a Hint
Look for suspicious usernames.








Flag 10


Category: Post Exploitation


Use an RCE exploit through Metasploit to exploit the host that ends with .12. Using the results from the Nessus scan, try to determine which exploit works. You may have to try many before you find the one that works. Once you have access to the host, search for a file which contains the flag. You will need to use a Meterpreter feature to access the flag within the file


Free Hint - It may look like you get an error when you connect to the host, but the session was actually created.  Search how to manually connect to your session.


Click here for a Hint
Use Meterpreter to download the file to your machine, then extract the contents within the file to get the flag.








Flag 11

Category: Post Exploitation
Use an RCE exploit through Metasploit to exploit the host that ends with .13. Using the results from the Nmap scan, try to to determine which exploit works. You may have to try many before you find the one that works. Once you have access to the host, use a Meterpreter command to determine  user that the Meterpreter server is running as on the host The username is the flag



Flag 12

Category: Post Exploitation
Exploit the host that ends with .14. The exploit to access this host does NOT use a CVE. The hint for this exploit was displayed when viewing Flag 1. With this information, try and guess the password to access the host. Once you have accessed this host, use a privilege-escalation vulnerabilty to access the final flag.

Free Hint: CVE-2019-14287

Flag 1: OSINT


Category: Reconnaisance


Using OSINT, search for GitHub repositories belonging to totalrekall. Search the repository for user credentials. The flag is a user's cracked password.


Click here for a hint
Check the totalrekall GitHub repo here: https://github.com/totalrekall








Flag 2: HTTP Enumeration


Category: Reconnaisance


The Windows network has a subnet of 172.22.117.0/24. The flag is in a file within a website on the internal network. Use the credentials that you found in Flag 1 to access this flag.


Click here for a hint
Check your port scan for any IP with port 80 open, and try the credentials that you cracked from GitHub in Flag 1.








Flag 3: FTP Enumeration


Category: Reconnasiance


Utilize FTP to access the file containing the flag.


Free Hint: Run an "agressive" scan to determine a method for accessing this file.


Click here for a hint
Google "anonymous access FTP."








Flag 4: Metasploit


Category: Exploitation


Find a machine that is running the SLMail service. Determine an exploit to run using Metasploit. Don't forget to set your LHOST to the IP address of your local machine within the same subnet! Once you have exploited the machine, look for flag4.txt.


Click here for a hint
SLMail is exploitable via Metasploit. The flag is in the immediate directory once your shell opens.








Flag 5: Common Tasks


Category: Post-Exploitation


You just gained access to Win10. What task should you consider doing first, in case you lose access to the machine?


Free Hint: Consider evaluating unnecessary scheduled tasks.


Click here for a hint
Review the section on scheduled tasks.








Flag 6: User Enumeration


Category: Post-Exploitation


Continue exploiting the same machine. The flag is the plaintext password of a specific user.


Click here for a hint
When dumping LSASS, make sure to check for local users and domain user credentials!








Flag 7: File Enumeration


Category: Post-Exploitation


Continue on the same machine. Sometimes the answer is in "public," plain sight.


Click here for a hint
A series of folders under C:\\Users are always public.








Flag 8: User Enumeration pt.2


Category: Post-Exploitation


Using credentials you found on the Win10 machine, laterally move to WinDC. Look for accounts on the new machine.


Click here for a hint
lsadump::cache








Flag 9: Escalating Access


Category: Lateral Movement


Continue to enumerate the new machine, and you will be rewarded with this flag in the heart of its file system.


Click here for a hint
When performing file enumeration, always start at C:\\ or /root.








Flag 10: Compromising Admin


Category: Post-Exploitation


The password hash of the user Administrator.


Free Hint: Look at Day 3's lessons to determine a method.


Click here for a hint
