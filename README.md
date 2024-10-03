# Hacking-Wireless-Networks

**Objectives:**

- Wi-Fi Packet Analysis
- Crack WEP and WPA2 Wi-Fi networks

---
# Perform wireless traffic analysis

**1. Wi-Fi packet analysis using Wireshark**

1. Launch Wireshark
2. Open file [Wireshark: Open Capture File window appears, navigate to E:\CEH-Tools\CEHv12 Module 16 Hacking Wireless Networks\Sample Captures, select WEPcrack-01.cap and click Open.]
3. The WEPcrack-01.cap file opens in Wireshark window showing you the details of the packet for analysis. Here you can see the wireless packets captured which were otherwise masked to look like ethernet traffic.

Here 802.11 protocol indicates wireless packets.

You can access the saved packet capture file anytime, and by issuing packet filtering commands in the Filter field, you can narrow down the packet search in an attempt to find packets containing sensible information.

In real time, attackers enforce packet capture and packet filtering techniques to capture packets containing passwords (only for websites implemented on HTTP channel), perform attacks such as session hijacking, and so on.

You can also use other wireless traffic analyzers such as AirMagnet WiFi Analyzer PRO (https://www.netally.com), SteelCentral Packet Analyzer (https://www.riverbed.com), Omnipeek Network Protocol Analyzer (https://www.liveaction.com), CommView for Wi-Fi (https://www.tamos.com), and Capsa Portable Network Analyzer (https://www.colasoft.com) to analyze Wi-Fi traffic.

---
# Perform Wireless Attacks

Aircrack-ng is a network software suite consisting of a detector, packet sniffer, WEP, and WPA/WPA2-PSK cracker and analysis tool for 802.11 wireless networks. The program runs on both Linux and Windows.

**1. Crack a WEP network using Aircrack-ng**

1. Parrot
2. Places
3. Desktop
4. The Desktop window appears, navigate to the CEHv12 Module 16 Hacking Wireless Networks folder and copy Sample Captures and Wordlist folders.
5. Now, navigate to the Desktop and press Ctrl+V to paste the copied folders (Sample Captures and Wordlist). Close the Desktop window.
6. Click the MATE Terminal icon at the top of the Desktop window to open a Terminal window.

1. `sudo su`
2. In the Parrot Terminal window, type `aircrack-ng '/home/attacker/Desktop/Sample Captures/WEPcrack-01.cap'` and press Enter.
3. By issuing the above command aircrack-ng will crack the WEP key of the CEHLabs as shown in the screenshot.
![image](https://github.com/user-attachments/assets/48c4670b-1bf3-4963-83a3-440db7c018bc)

**2. Crack a WPA2 Network using Aircrack-ng**

1. `sudo su`
2. In the Parrot Terminal window, type aircrack-ng -a2 -b [Target BSSID] -w /home/attacker/Desktop/Wordlist/password.txt '/home/attacker/Desktop/Sample Captures/WPA2crack-01.cap' and press Enter. Here, the BSSID of the target is 20:E5:2A:E4:38:00.

![image](https://github.com/user-attachments/assets/b1fd8fe3-e577-4f2b-8703-e48490bb89a2)

3. The result appears, showing the WPA handshake packet captured with airodump-ng. The target access point’s password is cracked and displayed in plain text next to the message KEY FOUND!, as shown in the screenshot.

You can also use other tools such as Elcomsoft Wireless Security Auditor (https://www.elcomsoft.com), Portable Penetrator (https://www.secpoint.com), WepCrackGui (https://sourceforge.net), Pyrit (https://github.com), and WepAttack (http://wepattack.sourceforge.net) to crack WEP/WPA/WPA2 encryption.






