# Smart Traffic Regulation System (Under Development) 

The system currently takes input from a RFID card. RFID card is connected with NodeMCU 12E, which communicates with a web server via Wifi and the web server communicates with a MySQL database. 
The basic feature of the system is to first check if a public vehicle have the up to date documentations, this is achieved through broadcasting the device id from NodeMCU. Each public vehicle will have only one device, that device is linked to all the papers and dates in the database. After the vehicle is cleared server checks the driver by scanned driving license. We demonstrated a driving license through a RFID card.
If the driver has valid license to drive the vehicle, the license will be binded and logged with the vehicle, until the driver again scans to logout. A web interface is displayed on the bus, so that passengers can report any discrepency. 

Future functionalities like GPS tracking, automated speeding detection, bus stop violation detection through image analysis is under development.

# Diagram
![RFIDnodeMCU](https://user-images.githubusercontent.com/57692222/80870775-84f2ab80-8cca-11ea-9a1f-4824c322ddaa.png)

# Codes
1. RFID_nodeMCU folder has the codes needed to run the RFID and NodeMCU module. The code communicates with the custom PHP API and according to the payload uses green/red light to indicate success or failure.
2. PostDemo.php is the custom API that communicates with the RFID reader and database and does all the operations of binding drivers and taking logs.
3. Other codes are for the automated display coded with Ajax. So, front page and logs changes automatically when any change is occured in the database.

# Screenshots

![image](https://user-images.githubusercontent.com/57692222/80871033-0bf45380-8ccc-11ea-9418-6399984480c9.png)

![image](https://user-images.githubusercontent.com/57692222/80871108-96d54e00-8ccc-11ea-81c4-73c77bda64a0.png)


