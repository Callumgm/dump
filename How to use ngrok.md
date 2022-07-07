# Port forwarding using ngrok

Navigate to the installed folder and make sure it has the executable file `ngrok` in it.


cd to the folder and run:
```
ngrok tcp 12000
```

The port number used above should be same port as the server.
You should see the following after executing the above command:

<img src="https://github.com/Viren-Patil/TCP_Chatroom_GUI/blob/master/snapshots/ngrok.png">

Observe the highlighted line. It says the access to **tcp://0.tcp.ngrok.io:19171** will be forwarded to **localhost:12000**

This basically means that when client will try to access **tcp://0.tcp.ngrok.io:19171** it will be forwarded to you system's **localhost:12000**

Open a terminal and run:
```
ping 0.tcp.ngrok.io
```
Note that I haven't used the *tcp://* part of the domain name and neither the *:19171* while doing ping


## Creating client payload
```
IP = ngrok IP
Port = ngrok Port
```
**Notice the port number that I have used.** Yes you read it right. It will **not be** 12000, instead it will be the port number on which **ngrok is listening which is 19171** as it is evident from the image [above](#port-forwarding-using-ngrok).




## Creating the server
```
IP = 127.0.0.1
port = 12000
```
Make sure to keep the port number same as the one you had used while running *ngrok* command [previously](#port-forwarding-using-ngrok).



## Conclusion

If you did everything alright then the application should run just fine.

To use the BotNet, you run the server and do the port forwarding using ngrok and use the IP & Port when creating client file


## Error fixes

Make sure webcam server is running on a diffrent port than the botnet server


