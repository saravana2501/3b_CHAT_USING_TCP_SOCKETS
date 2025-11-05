# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
# client:
```
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept() 
address={"6A:08:AA:C2":"192.168.1.100","8A:BC:E3:FA":"192.168.1.99"}; 
while True: 
            ip=c.recv(1024).decode() 
            try: 
                c.send(address[ip].encode()) 
            except KeyError: 
                c.send("Not Found".encode())
```
# server:
```import socket
s=socket.socket() 
s.connect(('localhost',9000)) 
while True: 
    ip=input("Enter MAC Address : ")  
    s.send(ip.encode()) 
    print("Logical Address",s.recv(1024).decode())
```

## OUPUT:
# client:
![Screenshot 2025-04-18 110204](https://github.com/user-attachments/assets/6b28a67c-3382-4cfe-a258-3725907b035d)


# server:
![Screenshot 2025-04-18 110056](https://github.com/user-attachments/assets/0c14c86f-da30-4020-8531-d84f69cae751)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
