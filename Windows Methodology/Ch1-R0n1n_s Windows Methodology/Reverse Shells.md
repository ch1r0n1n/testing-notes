1. Setup netcat listener with rlwarp
	1. Why rlwarp?
		a) Allows history and auto-completion. Just for convenience if we get a sucky shell.
2. If we're using a reverse shell script against a target with port 445 open, set the LHOST port to 445
	1.Why port 445?
		b)This connects to the Windows SMB port (A port Windows recognizes and it open to allow for network communication / traffic) which is essentially an open port we can talk to Windows on.