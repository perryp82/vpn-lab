# Azure Virtual Machine and VPN Lab

This tutorial walks you through setting up a virtual machine in Microsoft Azure, testing VPN connections, and observing the changes in IP addresses and website behavior.

---

## Part 1: Create a Virtual Machine in Azure

1. **Access Your Public IP Address**
   - On your own machine, browse to [WhatIsMyIPAddress](https://whatismyipaddress.com/).
   - Take note of your public IP address and save it in a text file for reference.

2. **Create a Resource Group**
   - Log into your Azure Portal: [Azure Portal](https://portal.azure.com/).
   - Navigate to **Resource Groups** and click **Create**.
   - Provide the following:
     - **Resource Group Name**: `MyAzureVPNLab`
     - **Region**: Select a region near you.
   - Click **Review + Create**, then **Create**.

3. **Create a Virtual Machine**
   - Navigate to **Virtual Machines** in the Azure Portal and click **Create**.
   - Select **Azure Virtual Machine**.
   - Fill out the following:
     - **Name**: `MyWindowsVM`
     - **Region**: Choose a region in a different geographic location or country from your current location.
     - **Image**: Windows 10 Pro.
     - **Size**: Select a size that fits the free tier if applicable.
     - **Administrator Username and Password**: Set your credentials.
   - Ensure **Inbound Port Rules** allow RDP (Remote Desktop Protocol).
   - Click **Review + Create**, then **Create**.

4. **Log into the Virtual Machine**
   - After the VM is created, navigate to it in the Azure Portal.
   - Copy the **Public IP Address** of your VM.
   - Use Remote Desktop to connect to the VM:
     - **Remote Desktop Address**: Enter the Public IP Address of the VM.
     - **Username and Password**: Use the credentials you created earlier.
   - Once connected, open a web browser on the VM.

5. **Check the VM's Public IP Address**
   - In the VM, browse to [WhatIsMyIPAddress](https://whatismyipaddress.com/).
   - Take note of the VM's public IP address and save it in a text file.

---

## Part 2: Sign Up for ProtonVPN and Test the VPN Connection

1. **Sign Up for ProtonVPN**
   - On your actual computer, go to [ProtonVPN Sign-Up](https://account.protonvpn.com/signup?plan=free&language=en).
   - Create a free account.

2. **Download ProtonVPN Client**
   - In your VM, go to [ProtonVPN Download](https://protonvpn.com/download/).
   - Download and install the ProtonVPN client.

3. **Log Into ProtonVPN**
   - Open the ProtonVPN client in the VM.
   - Log in using your ProtonVPN account credentials: [ProtonVPN Login](https://account.protonvpn.com/login).

4. **Connect to a VPN Server**
   - In the ProtonVPN client, choose a VPN server in a country different from both your actual computer's location and your VM's region (e.g., Japan).
   - Connect to the VPN server.

5. **Check the VPN's Public IP Address**
   - In the VM, browse to [WhatIsMyIPAddress](https://whatismyipaddress.com/).
   - Take note of the new IP address and save it in a text file.

6. **Test Website Behavior**
   - In the VM, browse to sites like:
     - [Google](https://www.google.com)
     - [Disney](https://www.disney.com)
     - [Amazon](https://www.amazon.com)
   - Observe if the language or URL changes based on the VPN server's location.
   - Take notes on any differences.

---

## Notes and Observations

- Save all IP addresses and observations in a text file for documentation purposes.
- Compare the behavior of websites and the changes in IP addresses to understand the effects of geographic location and VPN usage.
