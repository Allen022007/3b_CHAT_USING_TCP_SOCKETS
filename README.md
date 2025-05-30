# 3b.CREATION FOR CHAT USING TCP SOCKETS
~~~
Name : W Allen Johnston Ozario
Reg.No : 21222411004
~~~
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### client.py
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server.py
```python
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
## OUTPUT
### client.py
![image](https://github.com/user-attachments/assets/95c92247-61f9-44a3-be34-f4f75c1d6103)

### server.py
![image](https://github.com/user-attachments/assets/385f0e01-6bb5-4cda-9173-b62ac4fdc14c)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
