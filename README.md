# Ubuntu-VPN-Server-PPTP
Set up Your Own PPTP VPN Server On Ubuntu Linux

1. Install pptpd
	apt-get update
	
	apt-get install pptpd
2. Adding DNS Servers
	nano /etc/ppp/pptpd-options

	ms-dns 8.8.8.8
	
	ms-dns 8.8.4.4

3. Adding VPN User Accounts
	nano /etc/ppp/chap-secrets

	user1 pptpd user1-password *
	
	user2 pptpd user2-password *
4. Allocating Private IP for VPN Server and Clients
	nano /etc/pptpd.conf

	localip 192.168.1.1
	
	remoteip 192.168.1.100-200
5. Enable IP Forwarding
	nano /etc/sysctl.conf
	
	net.ipv4.ip_forward = 1
6. Start PPTPD
	systemctl start pptpd
	
	systemctl enable pptpd
7. Port Forwarding
	Server IP : 10.11.32.122
	
	Public IP : 14.171.28.17
	
	1723
	
	47
  
  ---
  Link:
  https://www.youtube.com/watch?v=eb7T6qNCU_w&t=18s&ab_channel=NetVN
  https://drive.google.com/file/d/1iS8tlIE33hxsat8ww-r_037xnxxwGA0d/view
