# Spoofer
An old project I decided to rework and document the code
Nothing too complex, a very bare bones ARP based IP spoofer I made to understand the workings of a network connection.

This project is a Python script that uses the scapy library to spoof the MAC address and IP address of a network device and perform a 'man in the middle' attack. It allows the user to intercept and modify the network traffic between a target device and the router. It also has a function to restore the original network configuration when the script is stopped.

#### Features of this project:
* Spoofing the MAC address and IP address of any network interface on the device using scapy.
* Taking user input via the command line using the argparse module to specify the target device and the router.
* Sending and receiving raw network packets using scapy and access and modify the fields in the packets.
* Performing a 'man in the middle' attack by sending spoofed ARP packets to the target device and the router, tricking them to send their traffic to the attacker.
* It can restore the original MAC address and IP address of the network interface and the ARP tables of the target device and the router when the script is terminated.

#### Challenges faced in this project:
* Learning how to use the scapy library to manipulate network packets and protocols at a low level.
* Implementing the logic and algorithm for the MAC address and IP address spoofing and the 'man in the middle' attack techniques.
* Accurately addressing the fields in the network packets and modifying them to perform the attack.
* Handling the exceptions and errors that may occur during the network operations.

#### Learning Outcomes:
* Python programming, especially using the scapy and argparse modules.
* Network security concepts, such as MAC address spoofing, IP address spoofing, and 'man in the middle' attacks.
* Network analysis and troubleshooting tools, such as Wireshark and Nmap.
* Project management and documentation best practices in a code.

# Usage
```
python 3 ./pySpoofer.py -t/--target (Target IP) -g/--gateway (Router IP) [-h/--help (Help)]
```

# Dependecies
Scapy:
```
  pip3 install scapy
```

Windows/Linux (if you don't already have npcap):
[winpcap](https://www.winpcap.org/install/default.htm) [deprecated] / [npcap](https://nmap.org/npcap/) [recommended]
