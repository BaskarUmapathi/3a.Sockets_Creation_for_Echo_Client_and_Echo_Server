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
## PROGRAM:
### SERVER:
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

### CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 

```

## OUTPUT:
### SERVER : 
![image](https://github.com/BaskarUmapathi/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151434098/93c732b7-355e-4098-8efd-11874c1a5b17)

### CLIENT : 
![image](https://github.com/BaskarUmapathi/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151434098/4f44af6b-9dd3-449b-828c-6d1ef3b7bc05)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
