Telnet Server/Client
How to run and use
Prog3svr is a simple communication program via Telnet protocol. 
Following is a tutorial for running and using it.
Step 1. Running Telnet server
Like other ordinary server programs, you can simply run this one on Linux.
There is a command format;
./prog3svr <svr_port>
For example, if you are going to bind server on port 5677, you can enter command like this;
./prog3svr 5677
If terminal says “bash: ./prog3svr: Permission denied”, enter the following command.
chmod +x prog3svr
 

Step 2. Connect to server on Windows
Both Windows and Linux support command ‘telnet’ as a tool to connect to any TCP servers.
But according to research on stackoverflow and other telnet sites,  Windows telnet has so many problems unlike linux’s one, because of its unpredictable behavior.
So I recommend you to use Putty instead of it.
To connect to server via telnet with Putty, just follow the below steps.
1. Run Putty and connect to server via telnet.
If your server’ IP address and port are 100.100.100.4 and 5677, you can do like this.
 
If you click Open, server accepts your request and connection succeeds.
 
2. Enter the commands to use.
If you are going to register with the name “user1”, you can use JOIN command.
JOIN user1
You can check if user registration is succeeded by using LIST command.
LIST
 
You can also send message to one or all joined users.
With MESG command, you can send message to one user. For example, if you are going to send message “Hello, testuser3.” to testuser3, you can enter the following command.
MESG testuser3 Hello, testuser3.
 

If testuser3 sends reply “How are you?”, it is displayed with the sender’s name.
 
Sending to all joined user is similar to previous one. This can be performed with BCST command.
BCST Hello everyone!
At this moment, all users receive this message.
 
If you want to quit, use QUIT command.
QUIT
