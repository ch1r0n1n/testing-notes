FFUF
- SUBDOMAIN	
	- ffuf -u http://FUZZ.mydomain.com -c -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt -fs 0

- VHOST
	- Ffuf -w [wordlist file'subdomains-top1miillion]:FUZZ -u [URL] -H 'Host: FUZZ.[domain]

- DIRECTORY
	- ffuf -w /root/Desktop/tools/SecLists/medium.txt -u http://192.168.70.32/FUZZ -fc 403 -o [filename]

- PARAMETER
	- ffuf -u 'http://MACHINE_IP/sqli-labs/Less-1/?FUZZ=1' -c -w 
	-/usr/share/seclists/Discovery/Web-Content/burp-parameter-names.txt -fw 39 
	-/usr/share/seclists/Discovery/Web-Content/raft-medium-words-lowercase.txt -fw 39 	 
	-/ffuf -u  http://hackxpert.com/RXSS/GET/00.php?FUZZ=tesdf -w params.txt -t 1 

- VALUE
	- /ffuf -u  http://hackxpert.com/RXSS/GET/00.php?FUZZ=tesdf -w params.txt -t 1
	- ffuf -u 'http://MACHINE_IP/sqli-labs/Less-1/?id=FUZZ' -c -w 					
	-/usr/share/seclists/Discovery/Web-Content/raft-medium-words-lowercase.txt -fw 39 			

- NMAP NSE
	-/usr/share/nmap/scripts
	- Nmap -p[port] -sV[enumerate version] --script=[script] 

- DIRSEARCH
	- dirsearch -w /root/Desktop/tools/SecLists/medium.txt -u http://[IP] -x 400,403,404,500,503,504 -o