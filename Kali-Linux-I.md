
# Basic Commands for Kail Linux

`sudo su`
 switch to root terminal

`cat /etc/*-release`
 to see the release of the OS

1. **ssh** - Secure Shell, used for secure remote access to a system.1.  
2. **ls -** List directory contents.  
3. **pwd** - Print the current working directory.  
4. **cd** - Change directory to a different folder.  
5. **touch** - Create an empty file or update the modified timestamp of an existing file.  
6. **echo** - Print a message or the value of a variable.  
7. **nano** - A simple text editor.  
8. **vim** - A more advanced text editor with many features.  
9. **cat** - Print the contents of a file to the console.  
10. **shred** - Securely delete a file by overwriting its contents.  
11. **mkdir** - Create a new directory.  
12. **cp** - Copy a file from one location to another.  
13. **mv** - Move a file from one location to another, or rename a file.  
14. **rm** - Remove a file.  
15. **rmdir** - Remove a directory if it is empty.  
16. **ln** - Create a link to a file or directory.
17. **clear** - Clear the console.  
18. **useradd** - Add a new user to the system.  
19. **sudo** - Run a command with administrative privileges.  
20. **adduser** - Add a new user to the system with more options than useradd.  
21. **su** - Switch to another user account.  
22. **exit** - Close the current terminal or log out of the current user account.  
23. **sudo passwd** - Change the password for the current user.  
24. **sudo passwd [username]** - Change the password for another user.  
25. **sudo apt** - A package manager used to install, update and remove software packages on Debian-based           systems.  
26. **2sudo apt update & install** - Update package lists and install packages.  
27. **finger** - Display information about a user.  
28. **man** - Display the manual page of a command.  
29. **whatis** - Display a brief description of a command.  
30. **which** - Locate a command and display its path.  
31. **whereis** - Locate the binary, source, and manual page files for a command.  
32. **wget** - Download files from the web.  
33. **curl** - Transfer data to or from a server.  
34. **zip** - Compress files into a zip archive.  
35. **unzip** - Extract files from a zip archive.  
36. **less** - View a file one page at a time.
37. **head** - Display the first lines of a file.  
38. **tail** - Display the last lines of a file.  
39. **cmp** - Compare two files byte by byte.  
40. **diff** - Display the differences between two files.  
41. **sort** - Sort the lines of a file.  
42. **find** - Search for files in a directory hierarchy.  
43. **chmod** - Change the permissions of a file or directory.  
44. **chown** - Change the owner of a file or directory.
37. **head** - Display the first lines of a file.  
38. **tail** - Display the last lines of a file.  
39. **cmp** - Compare two files byte by byte.  
40. **diff** - Display the differences between two files.  
41. **sort** - Sort the lines of a file.  
42. **find** - Search for files in a directory hierarchy.  
43. **chmod** - Change the permissions of a file or directory.  
44. **chown** - Change the owner of a file or directory.
45. **ifconfig** - Configure network interfaces.  
46. **ip address -** Display IP address information.  
47. **ip address | grep eth0** - Display the IP address of the eth0 interface.  
48. **ip address | grep eth0 | grep inet | awk** - Display the IP address of the eth0 interface using awk.  
49. **resolvectl status** - Display the current DNS resolver configuration.  
50. **ping** - Test network connectivity by sending packets to a host.  
51. **netstat** - Display network connections, routing tables, and interface statistics.  
52. **-tulpn** - Display active listening ports and associated programs.  
53. **ss** - Display socket statistics.  
54. **iptables** - Configure and administer the netfilter firewall.  
55. **ufw** - A user-friendly interface to manage iptables firewall rules.
56. **uname** - Print system information, including kernel name, network node hostname, kernel release, and kernel version.  
57. **neofetch** - Display system information in a colorful and visually appealing way.  
58. **cal** - Display a calendar of the current month or year.  
59. **free -** Display the amount of free and used system memory.  
60. **df and df-H** - Display disk usage statistics for a file system.  
61. **ps** - Report a snapshot of current processes.  
62. **top** - Display dynamic real-time information about running processes.  
63. **kill** - Send a signal to terminate a process.  
64. **pkill** - Send a signal to terminate one or more processes based on their name.  
65. **systemctl** - Control the systemd system and service manager.  
66. **history** - Display previously executed commands.  
67. **sudo reboot** - Reboot the system with administrative privileges.  
68. **shutdown** - Shutdown or reboot the system.



# Basic Commands for Network

### host tool

`host -h`
 This is used to print all the options along with host tool

`host nptel.ac.com`
 This is used for showing server names

`host -t ns nptel.ac.com`
 This is used to show all name server of host

`host -l nptel.ac.com <name-server name>`
 This is used to show zone data of a particular server for check the configuration of DNS server or if there have any vulnarability like : asynchronous transfer file range etc.
 If here show **Transfer failed** that means the website is configured properly and it not allow to transfer to zone data.

`host -t ns zonetransfer.me`
 `host -l zonetransfer.me <name-server name>`



### dig tool

`dig -h`
 print all options along dig tool that is used for *DNS Enumaration* 

`dig nptel.ac.com`
 print about the DNS server

`dig nptel.ac.com +short`
 print about the DNS server in short

`dig nptel.ac.com -t ns`
 print about the DNS name server

`dig nptel.ac.com -t mx`
 print about the DNS mail server

`dig axfr zonetransfer.me <name-server name>`
 print about the DNS records along with the name and mail server



### dnsenum tool

`dnsenum -h`

`dnsenum nptel.ac.com`

`dnsenum zonetransfer.me`

`densrecon -h`



### namp tool

`nmap`
 print all the options along with the namp tool

`nmap -PE <target ip address>`
 print the general **ICMP Seep**

`nmap -PE -sn <target ip address>`

`nmap -PE -sn <target ip address> --reason`

`nmap -PE -sn <target ip address> --reason --packet-trace`

`nmap -PE -sn <target ip address> --reason --packet-trace --disable-arp-ping`

`nmap -PP -sn <target ip address> --reason --packet-trace --disable-arp-ping`

`nmap -PM -sn <target ip address> --reason --packet-trace --disable-arp-ping`

`nmap -PS -sn <target ip address> --reason --packet-trace --disable-arp-ping`

`nmap -PA -sn <target ip address> --reason --packet-trace --disable-arp-ping`

`nmap -PU -sn <target ip address> --reason --packet-trace --disable-arp-ping`

`nmap -PE <target ip address> --reason --packet-trace --disable-arp-ping`
 for all the sweep cases by sending all types of packets

`nmap -sT <target ip address> --reason --packet-trace --disable-arp-ping`
 This is used to **TCP SYN** Scan along by sending _ICMP Echo, ICMP non-echo, TCP synchronisation and TCP acknowledgment packets_ with packet information 

`nmap -sS <target ip address> --reason --packet-trace --disable-arp-ping`

`nmap -sT -p22 <target ip address> --reason --packet-trace --disable-arp-ping`
 here **-p22** means port number 22

`nmap -b <target server ip address> <client ip address>`
 to FTP Bounce scan

`nmap -v -b <target server ip address> <client ip address>`

`nmap -p22 -Pn -v -b <target server ip address> <client ip address>`
 here **-Pn** is used for scaning on open parts and don't show the closed ports in result

`namp -O <target ip address>`

`namp -O <target ip address> --reason --packet-trace --disable-arp-ping

`nmap -sV <target ip address>`
 for version detections running on target

`nmap -sT <target ip address>`

`nmap -p22 <target ip address>`
 scan for part 22

`nmap -p22,21,8080 <target ip address>`
 scan for port number 21, 22, 8080

`nmap -p1-10 <target ip address>`
 scan for port 1 to port 10

`namp <target ip address> --reason --packet-trace --disable-arp-ping
 here **-r** is used for stop the randomisation of scanning of port

`namp -A <target ip address> --reason --packet-trace --disable-arp-ping
 here **-A** is used for Aggressive Search which will detect OS, versions and other things



### proxychains tool

`leafpad /etc/proxychains4.conf`
 to view the configuration file of proxychains tool

`proxychains firefox`
 to open firefox using poxychains


### macchanger tool

`manchanger -h`
 to show all options along macchanger tool

`macchanger -s eth0`

`sudo macchanger -r eth0`

`sudo macchanger -s eth0`

`sudo macchanger -p eth0`


### remote login service
 to execute application on target system

`telnet <target ip address>`
 to remote the target system

`ssh <target ip address> -l <target username>`

`ssh <target username>@<target ip address>`
 *<target username@target ip address>:~$* `sudo apt-get install macchengar`




### crunch tool

`crunch`

`crunch <minimum password length> <maximum password length> <keywords of password>`

`crunch 4 4 -t ,@%^`
 here 
		 , means upper charecter in first position
		 @ means lower charecter in second position
		 % means number in third position
		 ^ means special charecter in forth position

`crunch 1 5 -p abcd`

`crunch 1 5 12345 > sample.txt`
 all posible word list store in smaple.txt file



### hydra tool

`hydra`

`hydra -L username.txt -P password.txt <target ip address> ssh`
 here
		 username.txt has all possible username wordlist
		 password.txt has all possible password wordlist
		 ssh means which service we will use
 


### enum4linux tool
 it is used for user enumeration

`enum4linux`

`enum4linux -U <target ip address>`
 This is used to enumerate all the users available in target 

`enum4linux -P <target ip address>`
 This is used to see the Password Policy information of target machine


### rpcclient tool
 it is used for user enumeration

`rpcclient`

`rpcclient -U "" <target ip address>`
 This is used for connect with target system using username null thourgh rpcclient
	*rpcclient $>*  `querydominfo`
	*rpcclient $>*  `enumdomusers`
	*rpcclient $>*  `queryuser msfadmin`



### ftp tool
 it is used as file transfer service

`ftp <target ip address>`
 *ftp>*  `ls`
 *ftp>*  `ls -l`
 *ftp>*  `put sample1.txt`
  to create file on target system
 *ftp>*  `ls`
 *ftp>*  `get sample2.txt`
  to transfer file from target system to our machine
 *ftp>*  `delete smaple2.txt`
  to delete file from target system





# Malware Scanning & Virus Scanning

`namp --script http-malware-host <host>`

`lynis`

`lynis audit system`

`sudo apt-get install listbugs`

`sudo apt-get install apt-listchanges`

`leafpad /etc/login.defs`
 this is configuration file of password policy

