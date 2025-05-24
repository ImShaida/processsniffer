# processsniffer
A C# process-aware packet sniffer that captures traffic from a specific process and saves it to a .pcap file using SharpPcap and PacketDotNet.

# ProcessSniffer

A C# process-aware packet sniffer for Windows using SharpPcap and PacketDotNet.

## Features
- Capture network packets on any Npcap-enabled interface
- Filter traffic by process name
- Save matched traffic to Wireshark-compatible `.pcap` files

## Usage

```bash
processSniffer.exe -i "\\Device\\NPF_{...}" -p chrome.exe

