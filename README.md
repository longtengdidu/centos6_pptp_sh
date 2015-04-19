# centos6_pptp_sh


iptables -A INPUT -m state --state NEW -m tcp -p tcp --dport 1723 -j ACCEPT
iptables -A INPUT -m state --state NEW -m udp -p udp -dport 1723 -j ACCEPT
iptables -I INPUT -p tcp --dport 1723 -jACCEPT 
iptables -I INPUT -p udp --dport 1723 -jACCEPT 
/etc/init.d/iptables save
/etc/init.d/iptables restart