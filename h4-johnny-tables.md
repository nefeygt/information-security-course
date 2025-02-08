
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

2. Munroe: xkcd 327: Exploits of a Mom: It's a funny and short comic to emphasize the importance of SQL injection and sanitizing. I learned about sanitizing during my frontend and backend courses back in Turkey and since then I really do care about an work while knowing the importance of sanitization.

## a) Goat (Install WebGoat 2023.4.): I followed the steps on the Tero's webpage and successfully downloaded and ran the app. I accessed it on the localhost and port 8888.

## b) F12. Solve Webgoat 2023.4: General: Developer tools: I followed the steps on WebGoat to learn more and practice on the developer tools and I solved the interactive problem and I really enjoyed it. The second one was a bit harder and more complex to do it but was also more fun.
1. ![image](https://github.com/user-attachments/assets/4648c181-2df9-4b1c-9fe7-cf768bc73af3)
2. ![image](https://github.com/user-attachments/assets/49646423-8252-47fe-a389-a61db461e39b)



## c) Not outdated. Update all operating system and all applications in your Linux:

## d) Sequel. Solve SQLZoo:
1. 0 SELECT basics:
2. 2 SELECT from World, from first two subtasks: "1. You can use WHERE..." and "2. Find the countries...".


## e) Solve Portswigger Labs: Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data. Explain how and why! How can you find the vulnerabitiy? What each part of the exploit does?:

## m) Voluntary bonus: WebGoat: SQL Injection:

## n) Voluntary bonus: solve some Portswigger labs marked as Apprentice (easy level):


### References:
Karvinen 2024: Information Security Course, https://terokarvinen.com/information-security/ <br>
A01:2021 - Broken Access Control, https://owasp.org/Top10/A01_2021-Broken_Access_Control/
A05:2021 - Security Misconfiguration, https://owasp.org/Top10/A05_2021-Security_Misconfiguration/
A06:2021 - Vulnerable and Outdated Components, https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/
A03:2021 - Injection, https://owasp.org/Top10/A03_2021-Injection/
Munroe: xkcd 327: Exploits of a Mom, https://xkcd.com/327/
Install WebGoat 2023.4, https://terokarvinen.com/2023/webgoat-2023-4-ethical-web-hacking/
