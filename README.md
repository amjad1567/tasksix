# Packet Capture for ICMP Ping

## Overview

This repository contains a packet capture file (`ping.pcapng`) that demonstrates ICMP (Internet Control Message Protocol) traffic resulting from a simple ping test. The capture was taken using Wireshark on Kali Linux and includes packets from four ICMP Echo Requests and four ICMP Echo Replies.

## Instructions

### Capturing Packets

1. **Start Wireshark:**
   - Open a terminal in Kali Linux.
   - Run Wireshark with root privileges:
     ```bash
     sudo wireshark
     ```
   - In Wireshark, select the `eth0` interface to start capturing packets.

2. **Ping Command:**
   - Open a new terminal window.
   - Execute the following command to ping `google.com` four times:
     ```bash
     ping -c 4 google.com
     ```

3. **Observe Packets:**
   - Return to Wireshark to view the captured packets.
   - Apply the filter `icmp` to see only ICMP packets.

4. **Save the Capture:**
   - Go to `File` > `Save As` in Wireshark.
   - Save the file as `ping.pcapng`.

### File Description

- `ping.pcapng`: This file contains the packet capture for the ICMP ping test. It includes:
  - Four ICMP Echo Request packets.
  - Four ICMP Echo Reply packets.

## Uploading the Capture

To upload the capture file to the `tasksix` folder in this repository:

1. Copy the `ping.pcapng` file to the `tasksix` directory in your local repository.
2. Commit the changes and push to GitHub:
   ```bash
   cd path/to/your/repo
   mkdir -p tasksix
   cp /path/to/ping.pcapng tasksix/
   git add tasksix/ping.pcapng
   git commit -m "Add ICMP ping capture"
   git push
  
