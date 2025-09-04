# Automation_Scripts
All my automation and scripting ideas 


HTB Open VPN connection 
As a  Jr. storage/ system admin, I interact with design & use automation daily. when using HTB with a kail vm it dawned on me that this is a wonderful opportunity to use automation when labbing to get straight to the meat and potatoes of learning how to pen test.
This guide explains how to create and use a simple bash script to connect to a Hack The Box VPN.

Step 1: Download the VPN Config File
First, log in to the Hack The Box website and download the OpenVPN configuration file. This file will have a .ovpn extension. The script assumes you will save it in your ~/Downloads directory.

Step 2: Create the Script
Create a new text file and save the following code inside it. You can name the file vpn_connect.sh.

#!/bin/bash

# This script automates the process of connecting to a Hack The Box VPN.

# Navigate to the Downloads directory.
# This script assumes your configuration file is in the Downloads folder.
cd ~/Downloads

# Run openvpn with elevated privileges.
# Replace "your_vpn_config_file.ovpn" with your actual file name.
sudo openvpn --config "your_vpn_config_file.ovpn"

Step 3: Make the Script Executable
Open your terminal and navigate to the folder where you saved the script. Then, run the following command to give the script permission to run:

chmod +x vpn_connect.sh

Step 4: Run the Script
You can now run the script from your terminal using this command:

./vpn_connect.sh

The script will automatically navigate to your Downloads folder, start the OpenVPN process, and prompt you for your user password to continue. After you enter your password, the script will handle the VPN connection for you.

