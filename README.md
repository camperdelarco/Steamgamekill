# SteamGameKill README

## Overview

**SteamGameKill** is a Bash script designed for Linux users, primarily designed for managing VRChat sessions, but it can work with any steam game. The script monitors uses DBus to listen for the WIVRn headset disconnection message before terminating the user specified game. It also dims your screen while active and restores brightness upon termination.

## Features

- **Automatic Game Termination:** Monitors headset activity and terminates VRChat when the headset is disconnected.
- **Screen Dimming:** Dims the screen to zero brightness when the script runs and restores it when stopped with `CTRL+C`.
- **Start Avahi and WIVRn without duplicates** auto starts both processes after checking they aren't already running on your computer.

## Tested Equipment

- **Operating System:** Linux Mint 22.04
- **Terminal:** XFCE Terminal (to run the script)
- **Dependencies:**
  - `xrandr` (for controlling screen brightness)
  - `avahi-daemon` (for mDNS service)
  - `flatpak` (to run WiVRn)

## Installation

1. **Install Required Software:**
   Open your terminal and run:
   ```bash
   sudo apt install x11-xserver-utils avahi-daemon flatpak
   ```

2. **Create the Script File:**
   Create a Bash script file on your Desktop or any target folder of your choice:
   ```bash
   nano ~/Desktop/SteamGameKill
   ```

3. **Copy the Script:**
   Copy the script code into the file and save it.

4. **Make the Script Executable:**
   Run the following command:
   ```bash
   chmod +x ~/Desktop/SteamGameKill
   ```

5. **Run the Script:**
   To execute the script, run:
   ```bash
   /home/user/Desktop/SteamGameKill
   ```

## Configuration

You can configure the following parameters directly in the script:

- **GAME:** The name of the game to terminate (default is `VRChat`).
- **DIM_SCREEN:** Enable or disable screen dimming (default is `false`).

Other parameters can be adjusted based on your specific needs, including network interface and monitoring settings.

## Usage

- **Start the Script:** Launch the script as described in the installation section.
- **Stop the Script:** Use `CTRL+C` to stop the script and restore screen brightness.

## Acknowledgments

- Thanks to all contributors of WiVRn for their work on Linux gaming projects.
- Special thanks to **xytovl** for his patience and assistance on the Linux VR Adventures Discord server.
- Thanks to ChatGPT for the help in writing this script and the README

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
