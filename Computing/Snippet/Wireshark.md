host 172.18.5.4
net 192.168.0.0/24
net 192.168.0.0 mask 255.255.255.0
src net 192.168.0.0/24
src net 192.168.0.0 mask 255.255.255.0
dst net 192.168.0.0/24
dst net 192.168.0.0 mask 255.255.255.0
port 53
host www.example.com and not (port 80 or port 25)
host www.example.com and not port 80 and not port 25
