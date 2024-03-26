# Active

## Description

This tool is a simple port scanner, which will tell you if the port is open or closed. 


### What is a port?
    A port serves as a gateway for programs to send and receive data over a network, ensuring that data reaches the intended program on a device. 

### What is port scanning?
    Port scanning involves checking a computer or network's ports to determine which ones are open or closed, revealing available services and potential vulnerabilities.

### Why is port scanning important in pentesting?
    Port scanning is vital in penetration testing (pentesting) as it helps identify open ports and services on a target system. This information allows pentesters to assess the security of the network, find potential entry points, and simulate real-world attacks, enabling organizations to improve their defenses.

### How does the program work?
    The program is a port scanner that lets users specify a target host and range of ports to scan. It establishes connections using TCP or UDP sockets to check if the ports are open or closed and then reports the status of each port.


# How to run

Ensure you have Python installed by running the following commands:

    sudo apt update
    sudo apt install python3

# Usage
```
$ python3 tinyscanner.py --help

usage: tinyscanner.py [-h] [-p P] [-u] [-t] host

Simple port scanner

positional arguments:
  host        The target host to scan

options:
  -h, --help  show this help message and exit
  -p P        Range of ports to scan
  -u, --udp   Perform UDP scan
  -t, --tcp   Perform TCP scan
```
```
$ python3 tinyscanner.py -u 127.0.0.1 -p 80-83

Port 80 is open
Port 81 is open
Port 82 is open
Port 83 is open
```
```
$ python3 tinyscanner.py -t 127.0.0.1 -p 80-83

Port 80 is closed
Port 81 is closed
Port 82 is closed
Port 83 is closed
```
