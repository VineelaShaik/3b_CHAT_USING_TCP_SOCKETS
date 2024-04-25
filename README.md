# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
Developed by:Vineela Shaik<br>
RegisterNumber:212223040243<br>
**CLIENT:**
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
**SERVER:**
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
![Screenshot (141)](https://github.com/K-Shanmugaraj/3b_CHAT_USING_TCP_SOCKETS/assets/144870425/35c867dd-1367-46bf-a3d4-77aaf53ed94e)



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
