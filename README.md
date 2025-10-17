# SteamKill

SteamKill is a Bash script designed to monitor network activity for a specified game port. If no activity is detected, it automatically terminates the game. The script also dims your screen to zero brightness while running and restores it to normal upon termination.

# Description

This script is primarily intended for use with VRChat and is useful for those who want to automatically terminate the game when they disconnect from their wireless headset. It continuously checks for network activity on a specified port and reacts accordingly, allowing you to enjoy uninterrupted gameplay until you close the associated app (like WiVRn).

# Requirements

- **Linux Mint 22.04** (tested)
- **xfce terminal**
- **xrandr** (for screen brightness control)
- **tcpdump** (for monitoring network packets)
- **run-wivrn script** (optional)

## Installation

1. **Install Required Software**:
   Make sure you have the necessary software installed:
   ```bash
   sudo apt install x11-xserver-utils tcpdump
   ```

2. **Create the Script File**:
   Create a text file for the script. For example, on your Desktop:
   ```bash
   nano ~/Desktop/steamkill
   ```

3. **Copy the Script**:
   Copy the script code into the file and save it.

4. **Make the Script Executable**:
   Run the following command to make the script executable:
   ```bash
   chmod +x ~/Desktop/steamkill
   ```

5. **Run the Script**:
   To execute the script, you can run:
   ```bash
   /home/user/Desktop/run-wivrn && sudo /home/user/Desktop/steamkill
   ```

## Configuration

You can configure the following parameters in the script:

- `PORT`: The port to listen on (default is `9757`).
- `INTERFACE`: The network interface to use (default is `enp1s0`).
- `CONSECUTIVE_FAILS`: The number of consecutive counts required to terminate the game (default is `6`).
- `COUNT_DURATION`: The duration in seconds for counting packets (default is `10`).
- `GAME`: The name of the game to terminate conditionally (default is `VRChat`).
- `SLEEP_DURATION`: Sleep duration between checks (default is `1` second).
- `PACKAGES`: The number of packets to limit the specified timeframe (default is `100`).

The default settings should work effectively, but you may adjust them based on your needs.

## Acknowledgments

- Thanks to **xytovl** for creating **WiVRn**, an awesome open-source project for Linux gaming.
- Special thanks to **ChatGPT** for assisting in the creation, debugging of this script and description.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

