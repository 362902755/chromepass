# Hacking Chrome Saves Passwords

### Pre Requisites:
	1. Python 2.7	-  https://www.python.org/downloads/. 
			 (It has to be 2.7 or it won't work)
			 
	2. PyWin32	-  Installable by runing "pip install pypiwin32"
			 or "C:\Python27\Scripts\pip.exe install pywin32"
			 
	3. Requests	-  Installable by runing "pip install requests" 
			 or "C:\Python27\Scripts\pip.exe install requests"
			 
	4. py2exe 	-  https://sourceforge.net/projects/py2exe/files/py2exe/0.6.9/ 
			 (choose the 32-bit version for 2.7)

### Features:

	1. Grabbing all the Google Chrome Saves Passwords
	2. Sending them to the attacker machine via a reverse HTTP connection

Victim will open the server and all the Google Chrome Passwords will be sent to the attacker remotely and saved as a text file on the attacker's computer. The connection is done by reverse-http.

PS: This was originally part of one of my malwares so I had to adjust. I didn't have time to clean it up yet that's why it looks so messy.


# Instructions:


## Local Exploitation (If your target is in the same network as you):

	1. Create server by runing the python script "create_server.py". 
	It will then ask you for your ip, you must type your local ip (ex: 192.168.0.1)
	
	2. Start the client.exe
	
	3. Send the server.exe to your target.
	
	4. Obtain a password text file in the same location as the client with all the Google Chrome Passwords.

## Remote Exploitation (If target is NOT on the same network as you):

	1. Create server by runing the python script "create_server.py". 
	It will then ask you for your ip, you must type your PUBLIC ip (ex: 152.162.93.12). 
	You can obtain your public ip by typing "WhatIsMyIp" on Google.
	
	2. Setup Port forwading. You want to forward the port 80 and 8080 to your machine 
	(look up how to do that if you don't know)
	
	3. Start the client.exe
	
	4. Send the server.exe to your target.
	
	5. Obtain a password text file in the same location as the client with all the Google Chrome Passwords.


## NOTE:
	DO NOT change the name of the python scripts.
	

### Any questions contact me at: MarioNascimento@ITCrashSecurity.com


#### DISCLAIMER: I will not be held responsible for the misuse of these scripts. EDUCATIONAL or PROFESSIONAL use only
