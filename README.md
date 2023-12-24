This program is based on sockets 


it has server and client in the folder , make sure that this program is used under a LAN Network 


The server and clients in the file need a same Gateway which is the router ip address (eg. 10.57.0.1)


Main motive of this program is to control the Games unsing mobile application 
the moblie application is in Remote_10.py program run that program in a mobile connected to wifi 

use :   >>> Pydroid 3 app to run the Remote_10 program 

Steps to run the program :

1. git clone  < link >
2. cd WIFI_Dev_Remote
3. ls
4. pip install -r Requirements.txt
5. nano client.py
6. search for client.connect(('127.0.0.1', 5000))
7. Change 127.0.0.1 to <your ipaddress>
8. python3 multi_server.py
9.
10.
11. Open new tab
12. cd WIFI_Dev_Remote
13. pyinstaller --onedir client.py
14. ls
15. cd dist
16. ls | grep client.exe

17. send the client.exe to target pc
18. run client.exe in target pc

19. go back to terminal
20. ls
21. nano Remote_10.py
22. Search for
    host = socket.gethostbyname(socket.gethostname())
    #host = '10.76.15.246'
    Change it as
    #host = socket.gethostbyname(socket.gethostname())
    host = '<multi_server.py --ipaddress>'     #change the  ip address with the server ip address 
24. Copy whole code of Remote_10.py and now install Pydroid 3 in your mobile
25. 
26. Make sure the mobile is connected to same router as the multi_server.py and client.exe
27. 
28. now past the whole code of Remote_10.py in new folder in Pydroid 3 in mobile
29. 
30. now open a Online car game in Client.exe pc > suggested to open NFS 2018 in pc

31. now you will find a GUI in mobile after running the Remote_10.py in mobile (make sure the multi_server.py and Client.exe are running in different systems)

32. press the buttons on the mobile to control the Game running on the Client.exe system.
