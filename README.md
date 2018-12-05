# Project 8 - Pentesting Live Targets
Time spent: 16 hours spent in total

Vulnerability Cross-Site Request Forgery(CSRF)

<a href="https://imgur.com/WnrcAW8"><img src="https://i.imgur.com/WnrcAW8.gif" title="source: imgur.com" /></a>

Steps Taken:

For this challenge I went the user list edit and hit update. I Used Burp to send post request to the repeater, change first name, last name and username clicked go and refresh. When I went back to the user list, the inputs I entered in Burp displayed as the gif shows it 

Vulnerability: Insecure Direct Object Reference(IDOR)

<a href="https://imgur.com/4ZBeOfc"><img src="https://i.imgur.com/4ZBeOfc.gif" title="source: imgur.com" /></a>
Steps Taken:

For this challenge I went to “Find a Salesperson” and then clicked on one of the Salesperson in the list. I changed the id in the URL to a different number, and the name of the Salesperson changed to a different name


Vulnerability: Session hijacking  
 
<a href="https://imgur.com/edm0VhP"><img src="https://i.imgur.com/edm0VhP.gif" title="source: imgur.com" /></a>
Steps Taken:
1.	Logged as an admin
2.	Use a PHP script that was provided “public/hacktools/change_session_id.php” to find the current session ID or set it the session ID to a new one.
3.	Visited chrome browser and I was able to login as the gif shows


Vulnerability: SQLI

<a href="https://imgur.com/nlbAg93"><img src="https://i.imgur.com/nlbAg93.gif" title="source: imgur.com" /></a>
Steps Taken:
1.	I went to a salesperson page and replaced id by <<    ‘OR SLEEP (5) = 0- -‘    >> and then refreshed the page. The gif shows a successful SQL injection after refreshing the page 
2.	The URL looks like this:  
<<   /blue/public/salesperson.php?id=%27%200R%20SLEEP (5) =0--%27   >>


Vulnerability: Cross Site Script (XSS)

<a href="https://imgur.com/Kle2EWk"><img src="https://i.imgur.com/Kle2EWk.gif" title="source: imgur.com" /></a>

Steps Taken:
1.	I went Contact Us and then and type in the feedback section:
And typed              <script> alert (‘found XSS’); </script> and then submit
2.	It will show that the message “Feedback Received” after that I clicked login and then feedback
3.	From there the pop window will show a successful XSS attack


Vulnerability: User Enumeration

<a href="https://imgur.com/AUylXUW"><img src="https://i.imgur.com/AUylXUW.gif" title="source: imgur.com" /></a>
Steps Taken:

1.	I tried to log in using my name and random password, and got a message that “login was unsuccessful”
2.	 When I tried to login with the username ‘pperson’ the message I received “login was unsuccessful” in bold format


