NMAP NSE
- nmap -p135,139,445 -sV --script=smb-vuln-*

ENUM4LINUX
- enum4lniux -a {IP}

RPCCLIENT
- rpcclient -U "" {IP}
	- If we have a username we can insert it in the quotes
	- Commands in rpcclient terminal
			1.  srvinfo
			2. 	enumdomusers
			3. 	getdompwinfo
			4. 	querydominfo
			5. 	netshareenum
			6. 	netshareenumall

SMBCLIENT
			1. smbclient -L {IP}
			2. Smbclient -L {IP} -U Administrator
			3. smbclient //{IP}/tmp
			4. smbclient \\\\{IP}\\ipc$ -U john
			5. smbclient \\\\{IP}\\ADMIN$ -U john
			6. smbclient //{IP}/ipc$ -U john
			7. smbclient /{IP}/admin$ -U john
			8. smbclient \\\\{IP}\\[SHARE NAME]$ -U [USERNAME]