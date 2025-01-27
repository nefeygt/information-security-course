# h2 Kill Chain

## x) Read and summarize:
1. Abstract and Introduction
  - Briefly talks about and explains the technical terminology used and teaches what they are being used for (Abstraction part).
  - Talks about "Advanced Persistent Threat" (APT), and the brief history of that by mentioning and describing the key events throughout this whole period.
  - Goes into a bit detail about APT and and gives information about what this paper is talking about and mentioning how we as defenders can develop resilient mitigations against intruders.
  - Finalizes the introduction part by mentioning briefly about the different sections of the paper.
2. Related Work
  - Explains how phase-based models (Find, Fix, Track, Target, Engage, Assess (F2T2EA) from military strategies) inspired the kill chain concept.
  - References past efforts like the Mandiant exploitation lifecycle and insider threat models. They focus on post-compromise phases, and emphasizes the importance of acting earlier in the kill chain.
3. Intelligence-Driven Computer Network Defense
  - Introduces a risk management strategy where defenders analyze adversaries' capabilities, objectives, tactics.
  - Talks about the the indicator life cycle, breaking down intrusions into actionable intelligence using the three indicator. Atomic indicators, computed indicators, behavioral indicators.
  - Talks about the phases of kill chain and stopping even one of them will end the attack completely.
    - Reconnaissance
    - Weaponization
    - Delivery
    - Exploitation
    - Installation
    - Command and Control (C2)
    - Actions on Objectives
4. Case Study
  - Tells a story of a real attack on Lockheed Martin in 2009 involving three hacking attempts over a month.
  - Attackers used phishing emails with weaponized PDFs to exploit known vulnerabilities in Adobe Acrobat.
  - Highlights the importance of analyzing both successful and unsuccessful intrusions to improve resilience.
5. Summary
  - Sums up how the kill chain helps defenders break down attacks into phases. So it makes it easier to identify weaknesses and disrupt threats.
  - Talks about potential areas for further research, like the cost-benefit ratio of efforts and broader applications of the kill chain beyond cyber espionage.  

## a) Tactics, tools and procedures:
  1. Tactic:  It represents the adversary's tactical goal. Why? They do an action.
    - Credential Access (aiming to steal credentials like usernames and passwords).
  2. Technique: This describes How? an adversary achieves a tactical goal by performing an action.
    - Brute Force (tries a lot of combinations in an order aiming to find the correct one).
  3. Sub-technique: It provides a more specific description of the adversarial behavior used to achieve a goal.
    - Password Guessing (a sub-technique of Brute Force).
  4. Procedure: It is the specific implementations adversaries use for techniques or sub-techniques.
    - An adversary using a publicly available tool to automate password guessing attempts against an organization's VPN portal.

## b) Installing Linux: Done.

## c) Attack Story:


### Technical Words Learned:
kill chain, incident response, intrusion detection, intelligence, threat, APT, computer network defense, 

### References:
Karvinen 2024: Information Security Course, https://terokarvinen.com/information-security/
Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains
MITRE ATT&CK Matrix, https://attack.mitre.org/
