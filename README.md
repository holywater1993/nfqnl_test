# summary
Block a unappropriate URL using NFQUEUE<br>
<br>
# reference
Modify the skeleton code of gilgil_netfilter<br>
https://gitlab.com/gilgil/network/wikis/iptables-and-netfilter/netfilter<br>
<br>
# before you test
## install libraries below
apt install libmnl-dev<br>
apt install libnfnetlink-dev<br>
apt install libnetfilter-queue-dev<br>
<br>
## type commands below on the terminal
iptables -F<br>
iptables -A OUTPUT -j NFQUEUE --queue-num 0<br>
iptables -A INPUT -j NFQUEUE --queue-num 0<br>
