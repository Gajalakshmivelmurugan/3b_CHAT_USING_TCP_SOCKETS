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
client
```
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
server
```
import socket 
s=socket.socket() 
s.connect(('localhost',9000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
![Screenshot 2024-10-16 130645](https://github.com/user-attachments/assets/00457cc7-6722-4ff8-ac99-4bb2916a553a)
![Screenshot 2024-10-16 130700](https://github.com/user-attachments/assets/f0efb424-4f86-488b-814a-031535850511)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
