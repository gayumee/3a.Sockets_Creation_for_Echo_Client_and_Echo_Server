# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.

Name: T. Gayathri
Reg No: 212223100007

## PROGRAM
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())

```
## OUTPUT
## CLIENT 
![image](https://github.com/gayumee/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149037327/d2ef538b-61a4-4efc-8163-4c423de36c7a)
## SERVER
![Screenshot 2024-04-29 075645](https://github.com/gayumee/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149037327/471afe25-ab8c-4723-9708-fe08a9a96d3a)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
