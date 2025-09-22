Step1: Finding local Ip address using cmd “ipconfig”.(As i am using Windows)
Step2: Scanning for open ports using “nmap -A <ip>” save it as capture.txt
Step3: Run Wireshark
Step4: Capture packets 
Step5: Filter using cmd “ip.addr == <ip>” and save it as capture.pcapng
Step6: Compare the packet protocols with nmap and find the available open ports 
Step7: Search for common vulnerabilities for the open ports such as 
1)Port 135/tcp (msrpc - Microsoft RPC)
	EternalBlue (MS17-010)
	MS08-067
2)Port 139/tcp (netbios-ssn - NetBIOS Session Service)
	MS08-067
	MS08-030
3)Port 445/tcp (microsoft-ds - Microsoft-DS)
	EternalBlue (MS17-010)
	MS08-067
4)Port 2179/tcp (vmrdp - VMware Remote Display Protocol)
	CVE-2021-21985
	CVE-2021-21984
5)Port 5357/tcp (wsdapi - Web Services for Devices API)
	CVE-2020-1380
	CVE-2020-1350
6)Port 7070/tcp (realserver - RealServer)
	CVE-2014-0160
	CVE-2013-1977
