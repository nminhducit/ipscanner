# IP Scanner

## Overview

**IP Scanner** is a Windows batch script designed to scan the local network for active devices, display detailed information about each device, and perform various network-related tasks. This script simplifies network management by providing an easy-to-use interface for administrators and network engineers to monitor network activity and gather information about connected devices.

## Features

- **Scan Subnets**: Scans the local network to discover active devices.
- **List Machines**: Displays MAC addresses, IP addresses, and hostnames of connected devices.
- **Progress Indicator**: Shows real-time progress during scanning and other operations.
- **Gather Host Information**: Retrieves details like the adapter name, external IP, internal IP, subnet mask, default gateway, domain/workgroup, and hostname of the host machine.
- **Firewall Configuration**: Ensures network discovery is enabled for accurate scanning.

## Usage

1. **Launch the Script**:
   - Double-click the batch file to start the script.
   - Ensure you run the script with administrative privileges for optimal functionality.

2. **Script Operations**:
   - The script first checks if an instance of IP Scanner is already running. If it is, a notification will be displayed.
   - The script then enables network discovery on the system to facilitate network scanning.

3. **Main Menu**:
   - **Scan Subnets**: Automatically starts scanning the local network to discover devices.
   - **List Machines**: After scanning, displays detailed information about each discovered device including MAC address, IP address, and resolved hostname.
   - **Exit**: Exits the script.

## How It Works

- **Network Scanning**:
  - Uses the `ping` command to send packets to each IP address in the subnet.
  - Collects responses to identify active devices.

- **Listing Machines**:
  - Utilizes `arp -a` to gather MAC addresses and IP addresses.
  - Resolves IP addresses to hostnames using `ping -a`.

- **Host Information**:
  - Retrieves the external IP using a web service (`ifconfig.me`).
  - Gets adapter details, IP address, subnet mask, gateway, and domain information using `WMIC` and `netsh`.

## Requirements

- **Windows OS**: The script is compatible with Windows 8, 10, and 11.
- **Administrative Privileges**: Required for certain network operations and firewall adjustments.
- **Network Connectivity**: Necessary for scanning and retrieving external IP.

## Customization

You can customize the script by modifying the batch file according to your network's needs:

- **Change Scan Range**: Adjust the subnet range in the `:SCANSUBNETS` function.
- **Modify Output**: Customize the displayed information in the `:LISTMACHINES` section.


## Troubleshooting

- **Script Not Running**: Ensure you have administrative rights and that no other instances of the script are running.
- **No Devices Found**: Verify that network discovery is enabled and that the network configuration is correct.
- **Incorrect Host Information**: Ensure your network settings allow for accurate DNS resolution and device communication.

## License

This script is provided as-is without any warranties. You are free to modify and distribute it according to your needs.

---

By [NMINHDUCIT](mailto:nminhducit@gmail.com)

