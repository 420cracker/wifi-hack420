# Wifi-Hack420
This project demonstrates a Native Portal + Deauthentication Attack on a WiFi network using Kali Linux. The attack forces users to disconnect from a real WiFi network and connect to a fake access point (AP) with the same SSID (network name). When they attempt to log in, their credentials are captured.
# Hardware Requirements
- Laptop or PC with Kali Linux installed
- Wireless network adapter that supports monitor mode & packet injection (e.g., ALFA AWUS036NHA)
# Software requirements 
- Kali Linux (Latest Version)
- Sparrow-WiFi (For Reconnaissance)
- Airgeddon (For WiFi Attack)
# Tools to install
- sudo apt install sparrow-wifi
- sudo apt install airgeddon
# Implementation
# step1
open terminal and type "sudo sparrow-wifi"
Go to "falcon" option and click on "advance scan"

![Image](https://github.com/user-attachments/assets/8e244a09-f4f5-4277-a77f-9e6ffebaed2b)
# step2
click on "create monitering interface" and then click "yes". It will turn on moniter mode so you can perform further process

![Image](https://github.com/user-attachments/assets/2a25b05d-8f3b-43c6-819b-39871fe0b74c)

Now, Your moniter mode is on and you can scan for available wifi networks in your area.Click on scan and scanning will be started.

![Image](https://github.com/user-attachments/assets/8cbf80c0-3c98-4f67-ac5c-9614e698ea8f)

# step3 
- You will see some wifi networkes in the table with a lot of information like mac address,ssid,security,frequency,signal strength,bandwidth etc...
- It is recomended that you should select a wifi network with higher signal strength like in my case "vivo1823" have -33 signal strength which is higher then that of others.
- The client station indicates the clients connected to associated wifi networks. 
![Image](https://github.com/user-attachments/assets/e7fb1d21-e3da-4206-bac9-017bd8c82e4c)

# step4 
After selecting your target, exit the tool and open airgeddon tool by typing "sudo airgeddon"

# step5 
Tool will be opened and looks like this.

![Image](https://github.com/user-attachments/assets/f0eef71f-e0c6-4f8c-b94d-cc6f49521ce2)

Press "enter" to continue.

![Image](https://github.com/user-attachments/assets/617ac1b6-d122-42a3-87d3-e8a82d69c61a)

# step6
This will check for required packages and confirm it. If you are not installed the packages it will ask you to install them. Just click enter to install them or install manually.
click "enter" to continue.
![Image](https://github.com/user-attachments/assets/617ac1b6-d122-42a3-87d3-e8a82d69c61a)

Tool will ask you to select network interface. I have 2nd moniter interface. You have to select your moniter interface.

![Image](https://github.com/user-attachments/assets/badd867b-e420-4d85-8b94-25ab770aeb97)

# step7
Airgeddon tool shows you a list of attacks.
type "7" and click "enter".

![Image](https://github.com/user-attachments/assets/ab24d027-b9c2-4a71-8298-a6aba862f0f9)


Type "9" for captive portal attack and click "enter".

![Image](https://github.com/user-attachments/assets/c168113b-901e-48ba-8649-b9209b4537ca)

Type "1" for first method and click "enter".

![Image](https://github.com/user-attachments/assets/ee31db8b-9db3-4e48-958a-1725cf0de7c8)

It will ask you for handshake file, But we've not captured handshake file so we will type "N" and press "enter"

![Image](https://github.com/user-attachments/assets/88fca76c-1967-4e7b-8aec-27193f48d06c)


It will ask to enable "Dos persuit mode". Simply type "N" and continue.

![Image](https://github.com/user-attachments/assets/25e75ede-fa5a-4e16-9121-1ab11a2c27f2)

# step8
Airgeddon tool will search and show you available wifi networks in your area and clients connected to wifi networks.

![Image](https://github.com/user-attachments/assets/3db7e6b5-20ac-4afc-b18a-8463202b84b0)

Press ctrl+c to stop scanning.

# step9
Now select your target here to capture handshake file.

![Image](https://github.com/user-attachments/assets/acd1b993-f241-42ac-a381-80f5eb5e7a93)

Hit enter to continue & handshake capture process will start.
It will disconnect all clients connected to target wifi and then force to reconnect with target. When client reconnect with wifi, The handshake file is captured.

![Image](https://github.com/user-attachments/assets/94c54e52-b570-4707-9aae-ad1537b1bee7)

# step10
Now, Handshaks file is captured. Type path to save captured handshake file or hit "enter" to save it to default folder.

![Image](https://github.com/user-attachments/assets/d01bb8f5-3e84-4c06-8239-380dcdbaf5d1)

# step11
Finaly, Handshake file is captured and saved successfully. It's time to use captive portal attack.
Type the path to save hacked password.

![Image](https://github.com/user-attachments/assets/4a4d0fc6-771d-4ada-a89b-40c836f0d702)

# step12
Select your language.
![Image](https://github.com/user-attachments/assets/cb2c7483-6830-43cc-b663-10182f23fabe)

Type "Y" for advanced captive portal.

![Image](https://github.com/user-attachments/assets/1ebe4e2b-4885-4be6-9afb-cf0f07c42cb0)

The attack process will begin, just wait to connect with client to get password.

![Image](https://github.com/user-attachments/assets/a93cc12a-0a8d-42c3-b571-7c54ae4343b4)

# step13
- At this point, The clients connected to your target wifi network will be automaticaly disconnected from real Access point and reconnect with our fake network that looks like to the target wifi network.
- A notificatoin will receive on client's mobile screen that you have not internet connection.

![Image](https://github.com/user-attachments/assets/451b79aa-e619-4605-bed9-2e952dc9dfa1)

Now, When client click on the notification, It will redirect him to our fake capitive portal and ask him to enter wifi password to continue.

![Image](https://github.com/user-attachments/assets/68f80d0b-8de5-40dc-b7fa-beb34a4e046b)

After enterning password, The tool will verify password with the handshake file which we captured in previous step.
If password does not match with handshake file It will ask to enter password again.
When password mactch, It shows like this:

![Image](https://github.com/user-attachments/assets/40f4f765-a498-482d-b851-6094670ead94)

# step14
When client enters correct password, The password will be captured and stored in a txt file and show you like this:

![Image](https://github.com/user-attachments/assets/bafa054a-24d2-4f79-ae29-13bfcb30eac7)

# step15
Now go to the location that you give to save txt file in previous step. You will see a txt file which contains wifi password.
Open it which looks like this:)

![Image](https://github.com/user-attachments/assets/a2b05975-0edd-4c06-a42b-6732d937f1b3)


BOOM :) You have got the password.


# Warning :
This project is only for educational purpose & i does not promote any illegal activity. I done this project on my own network.
So i am not responsible for any illegal use of this project.
# Design By :
This project is created and uploaded by #Muhammad Haris Haroon.
