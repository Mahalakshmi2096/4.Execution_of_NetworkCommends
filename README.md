 
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## PROGRAM:
CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000)) 
while True:
    ip=input("Enter the website you want to ping ")
    s.send(ip.encode())
    print(s.recv(1024).decode())
```
SERVER:
```
import socket
from pythonping
import ping
s=socket.socket()
s.bind(('localhost'8000))
s.listen(5) 
c,addr=s.accept()
while True:
    hostname=c.recv(1024).decode() try:
       c.send(str(ping(hostname, verbose=False)).encode())
    except KeyError:
       c.send("Not Found".encode())
```
TRACEROUTE COMMAND:
```
from scapy.all import*
target = ["www.google.com"]
result, unans = traceroute(target,maxttl=32)
print(result,unans)
```

## OUTPUT:

CLIENT:

<img width="953" height="565" alt="image" src="https://github.com/user-attachments/assets/2ef9f85a-c8fb-464e-9d71-b944503df91f" />


SERVER:

<img width="957" height="562" alt="image" src="https://github.com/user-attachments/assets/f1487202-7fbb-4f01-94a8-781a1449c106" />

TRACEROUTE COMMAND:

![image](https://github.com/user-attachments/assets/cfc56bc4-9c7d-47d4-ae32-b97b1b4a9fcb)


## Result
Thus Execution of Network commands Performed 
