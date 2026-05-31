# SOC-Project-Malicious-Traffic-Analysis-with-Wireshark



This repository contains a traffic analysis exercise performed with **Wireshark**.  
The objective was to identify an infected Windows client, extract host and user information, and uncover the Command and Control (C2) infrastructure used in the attack.

---

##  Key Findings

- **IP address of the infected Windows client:** `10.1.17.215`  
- **MAC address of the infected Windows client:** `00:0d:b7:26:4a:74`  
- **Host name of the infected Windows client:** `DESKTOP-L8GSC53`  
- **User account name from the infected Windows client:** `BLUEMOONTUESDAY\usuario`  
- **Likely domain name for the fake Google Authenticator page:** `google-authenticator.burleson`  
- **IP addresses used for C2 servers for this infection:** `X.X.X.X` (external IP with 13,546 packets, plus any other repeated external IPs)

---

##  Methodology

1. **Client Identification**  
   - Applied the filter `ip.addr == 10.1.17.215` to isolate traffic from the suspected host.  
   - Confirmed IP, MAC, and hostname using DHCP, NBNS, and LLMNR traffic.

2. **User Account Discovery**  
   - Inspected Kerberos packets (`AS-REQ` and `TGS-REQ`).  
   - Extracted the user account name from `cname → name-string`.

3. **Phishing Domain Detection**  
   - Used the filter `http || dns`.  
   - Found DNS queries pointing to `google-authenticator.burleson`, a domain mimicking Google Authenticator.

4. **C2 Infrastructure Identification**  
   - Applied the filter `ip.dst != 10.1.17.0/24` to focus on external traffic.  
   - Leveraged **Statistics → Endpoints** to identify external IPs with high packet counts.  
   - Confirmed beaconing behavior (13,546 packets) indicating C2 communication.

---

##  Evidence

Screenshots of the analysis are stored in the `screenshots/` directory.  
The full report with detailed explanations is available in [`report.pdf`](report.pdf).

---

##  Conclusion

The analysis successfully identified:  
- The infected Windows client and its user account.  
- The phishing domain used to impersonate Google Authenticator.  
- The external IP addresses acting as C2 servers.  

This project demonstrates practical SOC skills in traffic analysis, threat detection, and incident investigation using Wireshark.
