# 4a. Execution_of_NetworkCommands
## NAME: RENICK FABIAN RAJESH
## REG NO: 212224230227
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Algorithm for PING:
```
Step 1: start the program.
Step 2: Include necessary package in java.
Step 3: To create a process object p to implement the ping command.
Step 4: declare one Buffered Reader stream class object.
Step 5: Get the details of the server
5:1: length of the IP address.
5:2: time required to get the details.
5:3: send packets, receive packets and lost packets.
5.4: minimum, maximum and average times.
Step 6: print the results.
Step 7: Stop the program.
```

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

## PING
## PROGRAM:
## Client: 
```
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost'8000))
s.listen(5)
c,addr=s.accept()
while True:
   hostname=c.recv(1024).decode()
   try:
      c.send(str(ping(hostname, verbose=False)).encode())
   except KeyError:
      c.send("Not Found".encode())
```
## Server: 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   ip=input("Enter the website you want to ping ")
   s.send(ip.encode())
   print(s.recv(1024).decode())
```

## Output
![Screenshot 2025-04-30 121016](https://github.com/user-attachments/assets/806720d0-224e-4925-a651-ae9d3e860a9d)
![Screenshot 2025-04-30 121050](https://github.com/user-attachments/assets/dbb061f1-3f0e-4e73-add7-1b4be74dcabb)


## Result
Thus Execution of Network commands Performed 
