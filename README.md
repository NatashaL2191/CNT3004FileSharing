# CNT3004 – Socket-Based Networked File Sharing Cloud Server Project

This project implements a multithreaded, socket-based file sharing system using Python.

## 📁 Project File Structure

```bash
CNT3004_FileSharing/
├── server/
│ ├── server.py # Main server file 
│ ├── init.py
│ ├── utils/
│ │ ├── init.py
│ │ 
│ └── storage/
│ └── (server-side files saved here)
│
├── client/
│ ├── client1.py # Client 1 (different function set)
│ ├── client2.py # Client 2 (different function set)
│ ├── init.py
│ └── shared/
│ └── commands.py # (optional) shared functions between clients
│
├── analysis/
│ ├── performance_test.py # Measure file transfer or response times
│ └── network_load.txt # Output logs from testing
│
├── docs/
│ ├── diagrams/
│ │ └── architecture.png # Diagram showing server-client interaction
│ └── report.pdf # Written report / explanation of design
│
├── tests/
│ ├── test_server.py
│ ├── test_client1.py
│ └── test_client2.py
│
├── .gitignore
├── README.md
└── requirements.txt
```

## How to Run

### Server (Computer #1)
```bash
python server/server_main.py
```

### Client (Computer #2 or #3)
```bash
python client/client_main.py
```

### Connect Command
In the client terminal:
```
connect <server_ip> <port>
```
Example:
```
connect 192.168.1.10 5000
```

## Features
- Authentication with encryption
- Upload, download, delete, directory, and subfolder operations
- Performance logging and analysis

## Network Setup Guide
1. Connect all computers to the same network (e.g., campus Wi-Fi or LAN).
2. Find the server computer’s IP address:
   - Windows: `ipconfig`
   - macOS/Linux: `ifconfig`
3. Clients use that IP when connecting (e.g., `connect 192.168.1.10 5000`).
4. Ensure firewall allows inbound connections on the selected port (default 5000).

## Authors
- Add team members here
