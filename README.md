# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
## OUTPUT:
## Find out the ip address of the attackers system
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/998e46c1-56bd-4f10-94c8-4e45d7d9730f)
## Invoke msfconsole:
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/274f55a6-b8a1-41af-8409-0565b2ae8a43)
## Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/a529566c-ac93-4e83-ae57-4014fd67b9f5)
## Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/8cc78305-7214-4b48-8311-02f811e896e1)
## nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later. scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/a748017a-744f-4cb5-80f0-346946e3c67b)
## Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/424b1a1f-c570-4c06-8461-e9bbc9b3a9ca)
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/e46473d6-be65-4117-92f2-efbab2d33b3a)
## Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/1a36ece6-13cf-4aa5-9dc0-4bd2398bf116)
## The info command provides information regarding a module or platform image
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/52046ae1-bb5d-44fe-9023-6146b1461252)
## Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/0f457997-f305-4ed6-9aee-4bd5d5e50379)
## Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/adbc1886-f9ad-4f83-93e6-5de0e79550d9)
## use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/e5d08cf6-b7b6-4c5e-a0a8-02b5b74d4d73)
## Use the set rhosts command to set the parameter and run the module, as follows:
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/235268c0-7daa-4943-9227-cf93b1bb0b33)
## After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/b43cc3bf-fb8c-4eb6-8bc8-a30505b8cfb9)
## set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true
![image](https://github.com/MARXINLIJO/Metasploit-for-reconnaissance/assets/145742540/e66ba29e-5510-4a66-801c-1187c3f0c91d)
## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
