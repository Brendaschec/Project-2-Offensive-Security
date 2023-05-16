# offensive-security
Project 2-Offensive Security
hallenges for Project 2 - Day 1


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
