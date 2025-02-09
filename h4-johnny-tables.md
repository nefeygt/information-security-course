
# h4 Johnny Tables

## x) Read and summarize:
1. OWASP: OWASP 10 2021:
   - A01:2021 - Broken Access Control:
      - Explains some terminology and gives statistics about this topic.
      - Briefly talks about various ways of this to happen (SQL injection techniques etc.)
      - Again briefly talks about how this can be interrupted.
      - Gives an example attack so it's more understandable, I liked the way that it gives actual code example.
   - A05:2021 - Security Misconfiguration:
      - Explains the rise in rankings due to increased use of configurable software with stats.
      - Lists common misconfigurations: default accounts, verbose error messages, unnecessary features enabled, outdated security settings, etc.
      - Prevention focuses on hardening processes (automated configurations, minimal platforms), regular audits, and security headers.
      - Example attacks include leaving sample apps with known flaws on various places. The scenarios show how simple oversights can lead to major breaches, which makes the risks tangible.
   - A06:2021 - Vulnerable and Outdated Components:
      - Highlights the challenge of managing third-party components, especially with no CVEs directly mapped. Stats include a default exploit score of 5.0.
      - Describes risks like unpatched libraries, undocumented dependencies, and slow update cycles.
      - Suggests fixes like automated inventory tools, patch management, and sourcing components securely.
      - Example attack uses a specific technique to show how unpatched components allow remote code execution. It’s eye-opening how outdated code can linger dangerously.
   - A03:2021 - Injection:
      - Drops to third place but still critical, with SQLi and XSS as major culprits (19% max incidence rate).
      - Explains injection flaws via unfiltered user input, dynamic queries, and ORM misuse. Broad scope: SQL, NoSQL, OS commands, etc.
      - Prevention emphasizes parameterized APIs, input validation, and escaping special characters.
      - Example attacks show raw SQL and Hibernate queries concatenated with user input, allowing attackers to inject malicious code. The code snippets make it clear how small coding mistakes create huge holes—kinda scary but super instructive!

2. Munroe: xkcd 327: Exploits of a Mom: <br>

It's a funny and short comic to emphasize the importance of SQL injection and sanitizing. I learned about sanitizing during my frontend and backend courses back in Turkey and since then I really do care about an work while knowing the importance of sanitization.

## a) Goat (Install WebGoat 2023.4.): <br>

I followed the steps on the Tero's webpage and successfully downloaded and ran the app. I accessed it on the localhost and port 8888.

## b) F12. Solve Webgoat 2023.4: General: Developer tools: <br>

I followed the steps on WebGoat to learn more and practice on the developer tools and I solved the interactive problem and I really enjoyed it. The second one was a bit harder and more complex to do it but was also more fun.
1. ![image](https://github.com/user-attachments/assets/4648c181-2df9-4b1c-9fe7-cf768bc73af3)
2. ![image](https://github.com/user-attachments/assets/49646423-8252-47fe-a389-a61db461e39b)

## c) Not outdated. Update all operating system and all applications in your Linux: <br>

I looked it up from google and learned that only two commands are enough to achieve this so I ran them and rebooted the system. It took a bit longer than I expected.
![image](https://github.com/user-attachments/assets/b0395ea0-b32f-4026-8def-de277bad8509)


## d) Sequel. Solve SQLZoo: <br>

I solved three levels starting from: 0 SELECT basics to 2 SELECT from World. These were easy and I actually solved these a year ago for my SQL course back in Turkey. I did more advanced stuff with SQL during that course so these were so easy for me. But I realized that I need some practice with SQL while trying to solve the hard questions because it's been a long time since I used it last time.

## e) Solve Portswigger Labs: Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data. Explain how and why! How can you find the vulnerabitiy? What each part of the exploit does?:
1. How does it work?
   1. Finding the injection point first:
      - The lab application filters products by category via a URL parameter.
      - This parameter is likely used directly in a SQL query without proper sanitization.
   2. Testing to find a vulnerability:
      - Append a single quote ' to the category value to break the SQL syntax: https://0ae20062045e6dae80e5b7e600fb00dc.web-security-academy.net/filter?category=Gifts'
      - And then the results is like this: ![image](https://github.com/user-attachments/assets/b5551d26-11a7-4318-be2b-f2b647b7342f)
      - Server returns a database error, it confirms improper input handling
   3. Creating the exploit:
      - Inject ' OR 1=1-- into the parameter.
      - So my final URL looks like this: https://0ae20062045e6dae80e5b7e600fb00dc.web-security-academy.net/filter?category=Gifts%27%20OR%201=1--%20
      - And this URL forces the webpage to this query: SELECT * FROM products WHERE category = 'Gifts' OR 1=1-- '
      - And therefore we succesfully get the results from this security leak and lack of sanitization: ![image](https://github.com/user-attachments/assets/4c5fb69e-f4e9-4913-8f74-0cc873edc83f)
2. Why does it work?: <br>
The application fails to sanitize user input, allowing us to manipulate the SQL query. The payload ' OR 1=1-- ensures the WHERE clause is always true, bypassing filters and exposing hidden data. And finally we access to the databsae

## m) Voluntary bonus: WebGoat: SQL Injection: <br>
I also wanted to check this and I liked it, here are the screenshots of the interactive parts of this work:
1. ![image](https://github.com/user-attachments/assets/4700c2dc-ac99-4d2b-aaea-16ebb11b806d)
2. I got this one after trying for a couple of minutes and learning the logic: ![image](https://github.com/user-attachments/assets/947454d2-0200-4e85-9c8c-42c8b220ea57)
3. I used the same logic for this one: ![image](https://github.com/user-attachments/assets/5a2da820-c0a2-4dcd-a791-a1b70c9892fd)
4. This one was about understanding and knowing the syntax. ![image](https://github.com/user-attachments/assets/4c846059-a41e-4e6d-8232-24d4f8b20ddb)

## n) Voluntary bonus: solve some Portswigger labs marked as Apprentice (easy level): <br>
This one was easier then we former lab. We bypass the password check by entering "--". So when we write "administrator'--" as the username and leave the password blank or write anything in the the system automatically logs us in as the administrator. ![image](https://github.com/user-attachments/assets/eb497928-4c56-4a73-9d39-15e2626d8c66)


### References:
Karvinen 2024: Information Security Course, https://terokarvinen.com/information-security/ <br>
A01:2021 - Broken Access Control, https://owasp.org/Top10/A01_2021-Broken_Access_Control/ <br>
A05:2021 - Security Misconfiguration, https://owasp.org/Top10/A05_2021-Security_Misconfiguration/ <br>
A06:2021 - Vulnerable and Outdated Components, https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/ <br>
A03:2021 - Injection, https://owasp.org/Top10/A03_2021-Injection/ <br>
Munroe: xkcd 327: Exploits of a Mom, https://xkcd.com/327/ <br>
Install WebGoat 2023.4, https://terokarvinen.com/2023/webgoat-2023-4-ethical-web-hacking/ <br>
0 SELECT basics, https://sqlzoo.net/wiki/SELECT_basics <br>
1 SELECT name, https://sqlzoo.net/wiki/SELECT_names <br>
2 SELECT from World, https://sqlzoo.net/wiki/SELECT_from_WORLD_Tutorial <br>
Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data, https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data <br>
Lab: SQL injection vulnerability allowing login bypass, https://portswigger.net/web-security/sql-injection/lab-login-bypass <br>
