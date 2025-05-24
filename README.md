# processsniffer
A C# process-aware packet sniffer that captures traffic from a specific process and saves it to a .pcap file using SharpPcap and PacketDotNet.

## Features
- Capture network packets on any Npcap-enabled interface
- Filter traffic by process name
- Save matched traffic to Wireshark-compatible `.pcap` files

## Usage

```bash

processsniffer.exe
[*] Available Interfaces:
[0] Name: \Device\NPF_{************************}
    Description: WAN Miniport (Network Monitor)

[1] Name: \Device\NPF_{************************}
    Description: WAN Miniport (IPv6)

[2] Name: \Device\NPF_{************************}
    Description: WAN Miniport (IP)

processSniffer.exe -i <interface> -p <processName.exe>

e.g\\

processsniffer.exe -i "\Device\NPF_{0511*****************}" -p Copilot.exe
[*] Starting capture on: MediaTek Wi-Fi 6 MT7921 Wireless LAN Card
[*] Saving matched packets to: Copilot_capture.pcap
[*] Press Enter to stop...
[+] Matched packet: 10.0.0.2:40250 -> 2.19.193.26:443
[+] Matched packet: 10.0.0.2:40251 -> 2.19.193.26:443
[+] Matched packet: 2.19.193.26:443 -> 10.0.0.2:40250
[+] Matched packet: 10.0.0.2:40250 -> 2.19.193.26:443
