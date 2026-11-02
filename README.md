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
## PROGRAM
developed by T.Goshanrajan (212225040098)
## Client
```python
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## Server
```python
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```

## OUPUT

<img width="1293" height="297" alt="Screenshot 2026-11-02 091108" src="https://github.com/user-attachments/assets/3bfddbe2-0ed1-4e58-9646-b64e252b3d1b" />
<img width="1295" height="257" alt="Screenshot 2026-11-02 091141" src="https://github.com/user-attachments/assets/c6e03682-2aa9-4a94-bab1-626752c45b25" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
