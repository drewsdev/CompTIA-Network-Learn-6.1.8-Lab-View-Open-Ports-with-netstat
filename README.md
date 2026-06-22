# CompTIA-Network-Learn-6.1.8-Lab-View-Open-Ports-with-netstat
## CompTIA CertMaster Learn v9.1

In this lab, your task is to complete the following:

* Use Zenmap to scan for open ports running VNC. Use the table below to help you identify the computer.  
* Go to the suspect computer and uninstall VNC.  
* From the suspect computer, run netstat -l to verify that the ports for VNC are closed.  

|  IP Address  | Computer  |
|:------------:|-----------|
| 192.168.0.30 | Exec      |
| 192.168.0.31 | ITAdmin   |
| 192.168.0.32 | Gst-Lap   |
| 192.168.0.33 | Office1   |
| 192.168.0.34 | Office2   |
| 192.168.0.46 | IT-Laptop |
| 192.168.0.48 | Support   |

![WireShark](/Screenshot_1.png)  
![netstat](/Screenshot_2.png)

Explanation

While completing this lab, use the following information:

|  IP Address  | Computer  |
|:------------:|-----------|
| 192.168.0.30 | Exec      |
| 192.168.0.31 | ITAdmin   |
| 192.168.0.32 | Gst-Lap   |
| 192.168.0.33 | Office1   |
| 192.168.0.34 | Office2   |
| 192.168.0.46 | IT-Laptop |
| 192.168.0.48 | Support   |

Complete this lab as follows:

1. Use Zenmap to scan for open ports running VNC.  
  a. From the Favorites bar, select Zenmap.  
  b. In the Command field, type nmap -p 5900 192.168.0.0/24.  
  c. Select Scan.  
  d. From the results, find the computer with port 5900 open.  
2. Uninstall VNC from the suspect computer.  
  a. From the top navigation tabs, select Floor 1 Overview.  
  b. Under Support Office, select Support.  
  c. From the Favorites bar, select Terminal.  
  d. At the prompt, type netstat -l and press Enter to confirm the port is open on the machine.  
  e. Type dnf list vnc and press Enter to find the package name.  
  f. Type dnf erase libvncserver and press Enter.  
  g. Press y and press Enter to uninstall the package.  
3. Type netstat -l and press Enter to confirm that the port has been closed on the machine.
