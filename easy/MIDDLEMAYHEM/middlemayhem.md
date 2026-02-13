# MiddleMayhem Lab Report

<img width="940" height="681" alt="image" src="https://github.com/user-attachments/assets/60312297-7c53-4f54-b19a-4142fe789085" />

- Q1) Access the Website in the browser, present it in the bookmark, and identify the JavaScript framework and version used.
  - Accessing the website shows the Javascript framework and version used at the footer

<img width="940" height="488" alt="image" src="https://github.com/user-attachments/assets/a9542a55-e55b-4718-9612-a45c42bdcd29" />

- Q2) Using Splunk, Find the attacker’s IP address
  - Using trial and error on source IPs, we see the attacker's IP address clearly

- Q3) Analyze the SIEM logs to determine how many unique URIs were accessed by the attacker.
  - Using | to apply the source IP count to the stats command, it shows a unique number of URIs accessed by the attacker

<img width="940" height="379" alt="image" src="https://github.com/user-attachments/assets/c5c2576f-4020-484e-92ec-51280d036af0" />

- Q4) Explore the site and identify two specific locations that could reveal internal structures or potential access points not meant for public eyes. Provide the two relative URLs.
  - Clicking on robots on the homepage leads to another webpage containing URLs not meant for public eyes

<img width="940" height="455" alt="image" src="https://github.com/user-attachments/assets/07a8ae01-a110-47ca-9966-2eacaf9bd07b" />

- Q5) Based on the Framework and Version, what recent CVE could be used to bypass authorization?
  - Searching next.js middleware authorization bypass reveals the CVE that could be used

<img width="940" height="607" alt="image" src="https://github.com/user-attachments/assets/4e754835-ae60-48e9-9647-f5c8b264ffac" />

- Q6) Find the relevant HTTP header in the SIEM logs that indicates CVE exploitation. Provide the header name.
  - Checking Splunk with the attacker IP, it shows the http header in the details under event

- Q7) What interesting URI did the attacker access after exploiting the CVE?
  - Right under the header, the URI is mentioned which the attacker tried gaining access to after exploiting the CVE

- Q8) The attacker tried uploading a reverse shell. Find out the IP and port to which the target would connect once the connection is established.
  - Just above the header, inside http_file_data, the ip address along with the port number is mentioned which is connected to the shell.sh file

<img width="940" height="429" alt="image" src="https://github.com/user-attachments/assets/6dd23492-5153-481d-b2a5-a06d7b047d6b" />

- Q9) After compromising the WebApp server, the attacker attempted lateral movement. Identify the technique used, as recorded in the SIEM logs.
  - After searching password it was known that via ssh, there was a bruteforce attempt to gain root access

- Q10) Identify the user account that achieved successful lateral movement to another server.
  - Searching password shows the password used to achieve successful lateral movement to another server
