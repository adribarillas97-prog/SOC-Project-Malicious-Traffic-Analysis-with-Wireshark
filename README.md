# Incident Investigation: Malware Infection and C2 Traffic Analysis Using Wireshark



This repository contains a traffic analysis exercise performed with **Wireshark**.  
The objective was to identify an infected Windows client, extract host and user information, and uncover the Command and Control (C2) infrastructure used in the attack.

---

##  Key Findings

- **IP address of the infected Windows client:** `10.1.17.215`  
- **MAC address of the infected Windows client:** `00:0d:b7:26:4a:74`  
- **Host name of the infected Windows client:** `DESKTOP-L8GSC53`  
- **User account name from the infected Windows client:** `BLUEMOONTUESDAY\usuario`  
- **Likely domain name for the fake Google Authenticator page:** `google-authenticator.burleson`  
- **IP addresses used for C2 servers for this infection:** `10.1.17.215` (external IP with 13,546 packets, plus any other repeated external IPs)

---

##  Task Answers


1. What is the IP address of the infected Windows client?  
10.1.17.215

   <img width="1007" height="593" alt="image" src="https://github.com/user-attachments/assets/a95bf38d-4ba9-467e-ba03-e642057e00dd" />

---

2. What is the MAC address of the infected Windows client?  
00:0d:b7:26:4a:74

<img width="490" height="638" alt="image" src="https://github.com/user-attachments/assets/cf4d6107-23e1-423c-95f9-d43cde066cad" />

---


3. What is the host name of the infected Windows client?  
DESKTOP-L8GSC53

<img width="868" height="318" alt="image" src="https://github.com/user-attachments/assets/5566e114-e01e-4601-b315-4c7fce0e0052" />

---

5. What is the user account name from the infected Windows client?  
BLUEMOONTUESDAY\usuario

<img width="345" height="188" alt="image" src="https://github.com/user-attachments/assets/37f731d4-e3f5-4f90-b001-bd44cce5b60c" />

---

6. What is the likely domain name for the fake Google Authenticator page?  
google-authenticator.burleson

<img width="938" height="326" alt="image" src="https://github.com/user-attachments/assets/f3c8c6e9-79d5-495a-ac75-486bcca016c4" />

---

7. What are the IP addresses used for C2 servers for this infection?  
[External IP with 13,546 packets]

<img width="907" height="547" alt="image" src="https://github.com/user-attachments/assets/e3b3a02e-4180-48c4-8e31-895083d0edb9" />


----

##  Evidence

Screenshots of the analysis are stored in the
The full report with detailed explanations is available in [report.pdf](report.pdf).


---

##  Conclusion

The analysis successfully identified:  
- The infected Windows client and its user account.  
- The phishing domain used to impersonate Google Authenticator.  
- The external IP addresses acting as C2 servers.  

This project demonstrates practical SOC skills in traffic analysis, threat detection, and incident investigation using Wireshark.
