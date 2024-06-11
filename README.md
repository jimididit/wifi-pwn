# Wi-Fi Deauthentication Script

This project contains a script to perform a Wi-Fi deauthentication attack using a network interface controller (NIC) in monitor mode.
**Note:** This script is for educational purposes only. Do not use it against any network that you don't own or have authorization to test.

## Prerequisites

- **System**: Linux (Debian-based distribution recommended)
- **Tools**: `aircrack-ng`, `iw`, `wireless-tools`
- **Python**: Python 3.x

## Project Structure

```
.
├── wifi_pwn.py
└── README.md
```

## Setup Instructions

### 1. Install System Dependencies

Ensure you have the following system packages installed:

```sh
sudo apt update
sudo apt install -y aircrack-ng iw wireless-tools
```

### 2. Clone the Repository

Clone this repository to your local machine:

```sh
git clone https://github.com/jimididit/wifi_pwn.git
cd wifi_pwn
```

### 3. Set Up Python Environment

There are no additional Python packages required for this script. If you have other scripts or future extensions that require Python packages, you can list them in `requirements.txt` and install them using:

```sh
pip install -r requirements.txt
```

### 4. Run the Script

Make sure the script is executable:

```sh
chmod +x wifi_pwn.py
```

Run the wifi_pwn.py script with superuser privileges:

```sh
sudo ./wifi_pwn.py
```

## Usage Instructions

### Initial Setup

1. **Superuser Check**:
    - The script will check if it is running with superuser privileges. If not, it will prompt you to run it with `sudo`.

2. **CSV Backup**:
    - The script will move any existing CSV files in the current directory to a backup folder to prevent data loss.

### User Input

3. **MAC Address Exclusion**:
    - The script will prompt you to enter MAC addresses of devices that you do not want to deauthenticate. Enter these addresses as a comma-separated list.

4. **Wi-Fi Band Selection**:
    - The script will prompt you to select the Wi-Fi bands to scan:
        - `0` - 2.4GHz
        - `1` - 5GHz
        - `2` - Both 2.4GHz and 5GHz

### Network Interface Configuration

5. **Network Interface Selection**:
    - The script will list available network interface controllers and prompt you to select one to use for monitoring.

6. **Monitor Mode**:
    - The selected NIC will be set to monitor mode, and the script will begin scanning for networks.

### Network Selection

7. **Network Selection**:
    - The script will display detected Wi-Fi networks and prompt you to select one for the attack.

### Deauthentication Attack

8. **Capture Clients**:
    - The script will capture clients connected to the selected network.

9. **Perform Attack**:
    - The script will perform deauthentication attacks on the captured clients.

### Cleanup

10. **Reset NIC**:
    - After the attack, the script will reset the NIC to managed mode and restart network services.

## Disclaimer

This script is for educational purposes only. Do not use it against any network that you don't own or have authorization to test.

## License

This project is licensed under the MIT License.
