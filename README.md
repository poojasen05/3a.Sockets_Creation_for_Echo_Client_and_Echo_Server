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

NAME:POOJA.S

REGISTER NUMBER:212223040146

## PROGRAM
##server
~~~
 import socket
 s=socket.socket()
 s.bind(('localhost',8000))
 s.listen(5)
 c,addr=s.accept()
 while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
~~~

##client
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

~~~

## OUPUT
### server
![Screenshot 2024-10-03 134736](https://github.com/user-attachments/assets/e2214461-9b30-483a-98f9-fdac86b232e2)


### client
![Screenshot 2024-10-03 134650](https://github.com/user-attachments/assets/cb1e18b7-4040-4512-b3f5-9fd848fc82b7)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
