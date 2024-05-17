# Sample TCPDUMP (Scenerio)
You are a cybersecurity analyst working at a company that specializes in providing IT services for clients. Several customers of clients reported that they were not able to access the client company website www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you attempt to visit the website and you also receive the error “destination port unreachable.” To troubleshoot the issue, you load your network analyzer tool, tcpdump, and attempt to load the webpage again. To load the webpage, your browser sends a query to a DNS server via the UDP protocol to retrieve the IP address for the website's domain name; this is part of the DNS protocol. Your browser then uses this IP address as the destination IP for sending an HTTPS request to the web server to display the webpage  The analyzer shows that when you send UDP packets to the DNS server, you receive ICMP packets containing the error message: “udp port 53 unreachable.” 
![image](https://github.com/ALNorman/Analysis-DNS-ICMP-Traffic/assets/169396450/476a50b9-b872-4a09-aeb4-35b363f141ff)

# Report of Findings
Cybersecurity Incident Report: 
Network Traffic Analysis

The UDP protocol reveals that port 53 was unreachable when trying to access company site yummyrecipesforme.com. This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message UDP port unreachable. The port noted, port 53 is used by the DNS to resolve domain names to IP addresses and vice versa. 

The time these incidents occurred is between 1:24 - 1:28pm. We became aware of the incident after recieveing reports from several customer clients they were not able to access the company site. The network security team responded and began running tests with the network protocol analyzer tool tcpdump. The resulting logs revealed that port 53, which is used by the DNS was not reachable. We are continuing to investigate the root cause of the issue to determine how we can restore secure access to the web portal. Our next steps include checking the firewall configuration to see if port 53 is blocked and contacting the system administrator for the web server to have them check the system for signs of an attack. The most likely issue is an attacker was attempting to redirect users to malicious websites, intercept sensitive information or launch DDoS attacks.




