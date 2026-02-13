# Anakus Lab Report

<img width="940" height="542" alt="image" src="https://github.com/user-attachments/assets/135aa56a-62ba-4d92-9ec9-9c64429dea0b" />

- Q1) Using Detect it Easy, what is the SHA256 hash of the malware in question (lnrvmp.dll), and what language was it written in? Feel free to utilize VirusTotal to garner more information (Format: SHA256, Language)
  - The initial detect-it-easy scan will reveal the sha256 hash of the malware in question as well as the language it was written in

<img width="940" height="396" alt="image" src="https://github.com/user-attachments/assets/fd5a69e3-76b0-4d20-9987-a1a912b39f2c" />

- Q2) The total entropy value in Detect it Easy gives us a general indication of the randomness across the entire file, but the presence of a highly entropic-packed section indicates a portion of the file containing data that has been compressed—packed. Usually, an entropy above 7.2 is considered malicious, what is the name of this section in question? (Format: .xxxx)
  - Using detect-it-easy, under the Entropy section it reveals what section is with entropy of 7.2 or higher

<img width="940" height="604" alt="image" src="https://github.com/user-attachments/assets/2724230c-a19f-490a-af86-e531b5f33361" />
<img width="940" height="581" alt="image" src="https://github.com/user-attachments/assets/39fe682f-8dd6-4f7c-bc7d-95f5aec9c25c" />

- Q3) Given the file’s entropy level, reputation on VirusTotal, and weird characteristics, it is clear that is malicious. However, attackers will sometimes use the names of security companies in their malware to bypass detection. In this case, what product name is this malware impersonating? (Format: Product Name)
  - A virustotal OSINT scan shows what malware this file is trying to impersonate

<img width="940" height="525" alt="image" src="https://github.com/user-attachments/assets/a4e3c23a-8070-4347-aa0a-4236f9aebe6f" />

- Q4) Using SigCheck, let's see if the file has been signed with a code-signing certificate—proving its validity. Include the “Verified” status and “Signing date” also known as Link Date (Format: Status, X:XX PM X/X/XXXX)
  - Running sigcheck reveals when the file was signed and whether it was verified or not

<img width="711" height="229" alt="image" src="https://github.com/user-attachments/assets/bee6a4ec-5586-41b5-95d2-b5d4e0c67120" />

- Q5) Let’s look at the alleged malware “hataker.exe”. Judging from its hash, it is not apparent on most malware platforms—albeit, it does not exclude its maliciousness. Turn on Windows Defender and run the malware until it picks it up. What is the name given to this alleged, malicious trojan-type program? (Format: Trojan:full name)
  - Running the malware gives a warning about it being potentially a malware

- Q6) Interestingly, now knowing the trojan type for the “hataker.exe”, we can safely assume the attacker was planning to initiate a connection from the victim’s endpoint to its command and control server. What is this method called? (Format: Xxxxxxx Xxxxx)
  - Initiating a connection from the victim's end to its C2 server is known as reverse shell

<img width="664" height="494" alt="image" src="https://github.com/user-attachments/assets/b0a6775f-7def-44ca-b92d-e970c56d01f9" />

- Q7) Sticking to the same context, let’s dissect the malware further. What dynamic domain is the malware “hataker.exe” using to establish a connection back to the attacker’s system? (Format: Domain name)
  - Running Wireshark, it reveals from what IP address reveals the host name containing the dynamic domain which is being used to establish a connection back to the attacker's system

<img width="940" height="593" alt="image" src="https://github.com/user-attachments/assets/f415dc18-fb83-470d-af0c-5567b477de6f" />

- Q8) Using Timeline Explorer, look at the “Threat Logs” from the incident, how many high-risk alerts were tracked? (Format: Count)
  - Using timeline explorer, shifting the level column to the filter section, it shows for each level how many alerts were tracked

<img width="940" height="515" alt="image" src="https://github.com/user-attachments/assets/637f4fb9-5fd8-4d28-9f9f-d0e733e3b900" />

- Q9) What are the two “Rule Titles” with the highest count under the high-risk alerts level group—in respective order? (Format: Rule Title 1, Rule Title 2)
  - Shifting the rule title column and putting it under the level filter, it reveals two titles with the highest count

<img width="940" height="522" alt="image" src="https://github.com/user-attachments/assets/20cc3a05-00bb-4f4d-bef6-516052253e9a" />

- Q10) Examine the last “Rule Title” for the high-risk alerts level group: what MITRE ID does this correspond to and what is the TgtGrp in question? (Format: TechniqueID, TgtGrp)
  - Corresponding the rule title with MITRE ATT&CK framework, it can be shown what technique id correlates to it and the target group is mentioned in the tool itself

<img width="940" height="576" alt="image" src="https://github.com/user-attachments/assets/e68ddd8b-1e63-4a84-abba-9707d0807b49" />

- Q11) Looking at the medium-risk level alerts, what is the “Rule Title” and count of the popular alert group? (Format: Rule Title, Count)
  - Use the filter on the medium-risk level threats and see which is the most popular alert group

<img width="940" height="353" alt="image" src="https://github.com/user-attachments/assets/36846f5e-d45b-46a8-a8cd-509cfc354750" />

- Q12) What function was used for the password spray attack? Lists its MITRE ID for this type of attack as well (Format: powershell-function, TXXXX.xxx)
  - Under "manipulation of user computer or group security principals across AD", it is shown what function was called for the password spray attack. The mitre id is available on Google on the website
