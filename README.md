<p align="center">
<img width="200" alt="kali-logo" src="https://github.com/user-attachments/assets/e20f3fee-7e75-4b99-964b-6dfc827da8b6" />
</p>

<h1>Website Spoofing & Credential Harvesting Lab (SET Toolkit)</h1>

<p>
This lab demonstrates a real-world social engineering attack using website spoofing to capture user credentials.
Using Kali Linux and the Social-Engineer Toolkit (SET), a cloned login page is hosted to simulate a phishing attack.
</p>

<h2>Key Objectives</h2>

<h4>Social Engineering Simulation</h4>
- Simulate a phishing attack using a spoofed website  

<h4>Credential Harvesting</h4>
- Capture user credentials through a cloned login page  

<h4>Security Awareness</h4>
- Understand how attackers exploit user trust  

---

<h2>Environments and Technologies Used</h2>

- Kali Linux  
- Social-Engineer Toolkit (SET)  
- VirtualBox / VMware  
- Windows VM  
- Networking (Host-Only / NAT)  

<h2>Operating Systems Used</h2>

- Kali Linux  
- Windows 10 / Windows Server  

---

<h1>Scenario</h1>

<h3>&#9312; Website Spoofing Attack (Credential Harvesting)</h3>

<h4>Background:</h4>
<p>
An attacker aims to trick a user into entering their credentials into a fake login page that mimics a legitimate website.
The attacker uses SET Toolkit to clone a trusted site (Google) and capture login credentials.
</p>

---

<p><strong>Launch Kali Linux and Elevate Privileges</strong></p>

<pre>
sudo su 
</pre>

<p><strong>Retrieve the IP address:</strong></p>

<pre>
ifconfig
</pre>

<img width="603" height="181" alt="Screenshot highlight 2026-04-01 202726" src="https://github.com/user-attachments/assets/6cbe3f6b-6296-43d1-b684-4b4664ac2562" />

---

<p><strong>Launch Social-Engineer Toolkit</strong></p>

<pre>
setoolkit
</pre>

<p><strong>Select the following options:</strong></p>

<ul>
<li>Social-Engineering Attacks</li>
<li>Website Attack Vectors</li>
<li>Credential Harvester Attack Method</li>
<li>Web Templates</li>
<li>Google</li>
</ul>

<img width="355" height="212" alt="Screenshot 2026-04-01 200752" src="https://github.com/user-attachments/assets/b9d3a445-be1b-4e6f-8b05-1f07e7f1575e" />

<img width="356" height="282" alt="Screenshot 2026-04-01 200829" src="https://github.com/user-attachments/assets/416efaa6-1776-4593-96dd-32df5be6ce29" />

<img width="349" height="190" alt="Screenshot 2026-04-01 200917" src="https://github.com/user-attachments/assets/732f1354-22f5-40db-9267-3c4e7cb7557c" />

<img width="318" height="105" alt="Screenshot 2026-04-01 201056" src="https://github.com/user-attachments/assets/346a806e-6a93-4010-b935-e63e8523cc59" />

---

<p><strong>Configure the Credential Harvester</strong></p>

<p>
Enter the Kali machine's IP address to host the fake login page.
SET Toolkit will clone the Google login page and start a listener to capture credentials.
</p>

<img width="698" height="33" alt="Screenshot 2026-04-01 201028" src="https://github.com/user-attachments/assets/068ae8d5-f673-42a6-8a4e-b48bbfbef57d" />
<img width="493" height="104" alt="Screenshot 2026-04-01 201452" src="https://github.com/user-attachments/assets/ef2630e7-9b1b-4bed-bf2f-78609d89b12d" />

---

<p><strong>Simulate Victim Interaction</strong></p>

<p>
In a real-world attack, this link would be disguised as a legitimate-looking URL to trick the user.
For demonstration purposes, we will directly navigate to the Kali machine's IP address:
</p>

<pre>
http://&lt;Kali-IP&gt;
</pre>

<p><strong>Enter test credentials:</strong></p>

<ul>
<li>Email: example@domain.com</li>
<li>Password: Password1234</li>
</ul>

<img width="783" height="589" alt="Screenshot 2026-04-01 201825" src="https://github.com/user-attachments/assets/4f132ed6-d571-4204-8534-02a50c2f93f8" />

---

<p><strong>Captured Credentials</strong></p>

<p>
Return to the Kali terminal to observe the captured credentials.
The SET Toolkit logs all submitted data from the spoofed login page.
</p>

<img width="506" height="281" alt="Screenshot 2026-04-01 201921" src="https://github.com/user-attachments/assets/134aec38-e63c-4f12-b3ba-a4b8d8baf6dc" />

---

<h4>Considerations:</h4>

<ul>
<li>Users may not verify URLs before entering credentials</li>
<li>Cloned websites can appear identical to legitimate ones</li>
<li>Social engineering exploits human behavior rather than technical vulnerabilities</li>
<li>Multi-factor authentication (MFA) can reduce risk</li>
</ul>

---

<h2>Security Implications</h2>

<p>This lab highlights how attackers can:</p>

<ul>
<li>Trick users into revealing sensitive information</li>
<li>Use legitimate-looking pages to gain trust</li>
<li>Capture credentials without exploiting software vulnerabilities</li>
</ul>

---

<h2>Final Thoughts</h2>

<p>
This lab demonstrates how effective social engineering attacks can be in compromising user credentials.
Understanding these techniques is critical for both offensive security learning and defensive awareness.
Organizations should implement user training, phishing detection, and strong authentication methods.
</p>

---

<h2>Disclaimer</h2>

<p>
This project was conducted in a controlled lab environment for educational purposes only.
Do not attempt these techniques on real users or systems without proper authorization.
</p>
