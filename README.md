# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

DATE :27-04-2023

AIM :

To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.


ALGORITHM :

1.Import the necessary modules in python

2.Create a socket connection to using the socket module.

3.Send message to the client and receive the message from the client using the Socket module in server.

4.Send and receive the message using the send function in socket.


PROGRAM :

CLIENT:
```
Developed by: E.NAVEEN KUMAR
Register no: 212222220029
```

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
SERVER:

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

OUTPUT :

CLIENT:

![EX CL8](https://github.com/NAVEENKUMAR4325/EX-8/assets/119479566/6691f4cd-31e9-4018-96dd-ed73b92e5be3)

SERVER:

![EX SE8](https://github.com/NAVEENKUMAR4325/EX-8/assets/119479566/01101b7e-bb43-4841-845f-fdc653f49209)




RESULT :

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
