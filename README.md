# 2a_Stop_and_Wait_Protocol

Name : MOHAN RAJ.C

Register Number : 212223040114
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
```
###client

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   i=input("Enter a data: ")
   c.send(i.encode())
   ack=c.recv(1024).decode()
   if ack:
     print(ack)
     continue
   else:
     c.close()
     break
```
###server
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
```
## OUTPUT

![321714703-62d050ea-29aa-4bbc-ac06-4aa1a7ec6c58](https://github.com/Mohanraj2006/2a_Stop_and_Wait_Protocol/assets/152195759/ee9220a1-63e8-407f-8afb-eccba52aba9e)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
