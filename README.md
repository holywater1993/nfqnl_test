# summary
Block a unappropriate URL using NFQUEUE

# reference
Modify the skeleton code of gilgil_netfilter
https://gitlab.com/gilgil/network/wikis/iptables-and-netfilter/netfilter

# before you test
## install libraries below
apt install libmnl-dev
apt install libnfnetlink-dev
apt install libnetfilter-queue-dev

## type commands below on the terminal
iptables -F
iptables -A OUTPUT -j NFQUEUE --queue-num 0
iptables -A INPUT -j NFQUEUE --queue-num 0
