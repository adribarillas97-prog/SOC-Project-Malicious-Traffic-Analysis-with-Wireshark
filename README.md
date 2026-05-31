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

   <img width="1007" height="593" alt="image" src="https://github.com/user-attachments/assets/48d0ff4e-f7b5-45e6-b0d1-51fca5779e4f" />

10.1.17.215
  

3. What is the MAC address of the infected Windows client?  
00:0d:b7:26:4a:74

4. What is the host name of the infected Windows client?  
DESKTOP-L8GSC53

5. What is the user account name from the infected Windows client?  
BLUEMOONTUESDAY\usuario

6. What is the likely domain name for the fake Google Authenticator page?  
google-authenticator.burleson

7. What are the IP addresses used for C2 serv

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
