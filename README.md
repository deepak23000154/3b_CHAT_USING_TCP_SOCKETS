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
## client
```

import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
     msg=input("Client > ")
     s.send(msg.encode())
     print("Server > ",s.recv(1024).decode())
```
## server
```
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
          ClientMessage=c.recv(1024).decode()
          print("Client > ",ClientMessage)
          msg=input("Server > ")
          c.send(msg.encode())
 ```         
## OUTPUT
## client
![Screenshot 2024-11-11 002055](https://github.com/user-attachments/assets/51a12b28-f83d-4f7e-b0f5-25cef87f8371)
## server
![Screenshot 2024-11-11 002111](https://github.com/user-attachments/assets/7a392681-1967-4e68-aa6a-3b872d7b3165)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
