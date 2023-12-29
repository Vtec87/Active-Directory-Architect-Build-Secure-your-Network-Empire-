# Active-Directory-Architect-Build-Secure-your-Network-Empire-

# Active Directory Architect: Building and Securing Your Network Empire
Picture this: You, seamlessly navigating the intricate realm of virtual networks, building connections that transcend the ordinary. Ready to dive in?
*By Victor P. Sr*

*Unlock the Power of Network Management.*

Welcome to Victor P. Sr.'s Home Active Directory Lab, where cybersecurity expertise and hands-on learning converge. Guided by essential tools like Oracle VirtualBox, Server 2019 ISO, Windows 10 ISO, and unleashed PowerShell scripts, I reveal the intricacies of constructing an Active Directory within a virtualized environment.

- **Master Network Configurations:**
Embark on a journey where networking mastery awaits. Ever wondered how to craft resilient virtual environments seamlessly? This lab is your gateway to unlocking the secrets of network configurations.

**Target Audience:**
   - Tailored for individuals with a foundational understanding of networking concepts, this lab is ideal for those familiar with virtualization basics and operating system fundamentals.

**Intriguing Opening:**
   - Picture this: You, seamlessly navigating the intricate realm of virtual networks, building connections that transcend the ordinary. Ready to dive in?

**Estimated Time:**
   - Plan for a dynamic 3-4 hour experience, adjusting as needed based on your familiarity with networking concepts.

**Skills and Tools:**
   - Prepare for the journey by ensuring Oracle VirtualBox is installed. Download the Windows 10 and Server 2019 ISOs [here](example_link) and [here](example_link). Familiarity with essential tools like PowerShell will enhance your experience.

**Troubleshooting Tips:**
   - Hone your troubleshooting skills by enabling virtualization in BIOS during Oracle VirtualBox installation. Ensure a seamless ISO download by maintaining a stable internet connection. Validate network configurations during DHCP setup to prevent potential IP conflicts.

**Specific Learning Outcomes:**
   - Delve into the intricacies of crafting a robust domain controller with Active Directory. Configure dual network adapters for seamless connectivity. Master DHCP setup for automated IP assignments. Script a PowerShell marvel, creating 1,000 users in Active Directory.

**Extension Activities:**
   - For those seeking an extra challenge, fortify your virtual environment with security configurations, delve into redundancy strategies, or explore advanced scripting possibilities. Advanced users may experiment with VLANs or delve into script-driven wonders.

**Visuals:**
   - Benefit from illustrative visuals that guide you through each step. Visual aide for a more intuitive learning experience.
![Screenshot 2023-11-13 115809](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/3d8e0110-7b6e-4f98-ae41-70b910ef8c3f)

Table of Contents
Objective 1: Setting Up the Virtualization Platform

Installing Oracle VirtualBox
Preparing for OS Installation: Downloading ISOs
Objective 2: Creating the Domain Controller VM

Configuration Overview
Server 2019 Installation and Active Directory Setup
Objective 3: DHCP Setup and PowerShell Script

Setting Up DHCP
PowerShell Script for User Creation
Objective 4: Creating a Client VM

Verifying DNS and Joining the Domain
Conclusion and Closing Thoughts

**Objective** **1**: Setting Up the Virtualization Platform
Installing Oracle VirtualBox
Start by downloading Oracle VirtualBox to create the foundation for our virtual machines.
[Download Oracle.](https://www.virtualbox.org/wiki/Downloads) 

Note: If you've already installed VirtualBox, proceed to the next section.

VirtualBox Configuration

Next Steps: After installing VirtualBox, proceed to create a new virtual machine to stay on track and engaged in the learning process.

Preparing for OS Installation: Downloading ISOs
Before diving into the OS installation, download the necessary ISO files from the official sources:

[Download Windows 10 ISO.](https://www.microsoft.com/en-us/software-download/windows10)
[Download Server 2019 ISO.](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)
Estimated Time: ??- Download time may vary based on your internet connection. Please plan accordingly.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/288e5da6-ec14-4bba-8942-0d4d1d663337)


This lab promises not just knowledge but an immersive journey where networking becomes an art, and you are the master artist. Are you ready to create virtual landscapes that transcend the ordinary? Let's dive in!

**Crafting the Domain Controller VM - Simplified Setup**

Let's delve into creating our primary virtual machine, the Domain Controller, for our Active Directory lab. I'll break it down into simple steps for you.

**Setting Up the Virtual Machine:**
1. **Dual Network Adapters:**
   - Our Domain Controller VM will have two network adapters. Think of them like giving our virtual machine two ways to connect, just like your computer can connect through Wi-Fi or a cable.
   - The first adapter is like the Wi-Fi, allowing our VM to connect to the internet and reach beyond its virtual home.
   - The second adapter is like a secret passage, connecting our VM securely to the VirtualBox's private network.

Here's a bit more detail:
- **Domain Controller (DC):** This is our virtual server, managing who gets in and ensuring things stay safe.
- **Virtual Network:** Imagine this as a private club within VirtualBox, where our VMs can chat and share without any unwanted guests.

These dual adapters are like having a front door and a back door to our virtual space, making it strong and secure.

**Visual Aid:**
Below is a simple diagram to give you a visual:

```
         +-----------------------------+
         |        Domain Controller         |
         |                                 |
         |  +-------------+     +-------------+  |
         |  |   Wi-Fi (Internet)    |     |   Secret Passage (Private Network) |  |
         |  +-------------+     +-------------+  |
         +-----------------------------+
```


**Diagram Description:**
In the diagram, the Domain Controller is at the center. It has two connections, one to the Wi-Fi (representing the internet) and the other to the Secret Passage (representing the private network within VirtualBox).
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/06ce6595-bcf3-4e75-8732-843fb1dcfcbb)

Stay tuned because the next guide will take you through each step, making it as simple as following a recipe. Picture a virtual world that's just like the real deal, and we're about to make it happen together. Ready for the next steps? Let's keep this virtual journey rolling! 🚀

**Troubleshooting Tips:**
- If your VM is having trouble connecting to the internet, double-check the Wi-Fi (Internet) adapter settings. You can troubleshoot using [this guide](link-to-wifi-troubleshooting).
- If the private network isn't working, ensure the Secret Passage (Private Network) adapter is correctly configured in VirtualBox settings. Further troubleshooting steps can be found [here](link-to-network-troubleshooting).

These tips should help if you encounter any hiccups along the way.

**Setting Up Server 2019 and Activating Active Directory**

Now that our Domain Controller VM is up and running, let's dive into the installation of Server 2019 and the essential configurations.

**Step-by-Step Guide:**
- **Install Windows Server 2019:**
   - Smoothly go through the Server 2019 installation process.
   - Assign IP addresses for an organized internal network, while external connections flow effortlessly through the home network/router.

- **Name the Server and Initialize Active Directory:**
   - Give your server a unique identity.
   - Install "Active Directory," the core of network security and authentication.
   - Kickstart the creation of your domain, establishing the groundwork for a controlled and secure networking environment.

- **Configure Internet Access Routing:**
   - Dive into detailed routing configurations, ensuring smooth internet access for clients on the private network through the Domain Controller.

In essence, this phase covers the fundamentals of constructing a robust Active Directory domain. Think of each step as a unique stroke, forming a canvas that reflects real-world network infrastructures. Get ready to blend theory with hands-on application as we shape our virtual environment into a seamless realm of connectivity. The journey begins, and the Active Directory domain takes form!

*Estimated Time:* Allocate 1-2 hours for a thorough understanding and execution.

*Visual Support:* Look forward to screenshots and diagrams included in the guide.

*Who Should Follow:* This guide is tailored for enthusiasts with a basic grasp of virtualization and networking concepts. For those unfamiliar with specific terms, refer to the glossary provided.

**In a Nutshell:**
By completing this guide, you'll gain the skills to install Server 2019, set up Active Directory, and configure routing for seamless internet access. The visual aids and hands-on approach ensure you understand not just the theory but the practical application of these crucial concepts.

In the upcoming steps, I'll walk you through implementing DHCP on the domain controller, ensuring that when we create a Windows 10 machine, it effortlessly obtains an IP address, establishing a streamlined and efficient network infrastructure. Stay tuned for the next phase of our virtualization journey!
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/070de0a7-83cc-4b5b-9b8c-f5a5cff4b138)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/b98b0bfd-86cd-4adf-94ee-8276b7094b11)

The final step before creating the client virtual machine on the domain controller involves running a PowerShell script. This script will automate the creation of 1,000 users in the "Active Directory."
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/f0066a81-cbab-486e-b821-754ccf61df7e)

After creating the users, the next step involves setting up another VM and installing Windows 10 on it. This VM will be connected to a private VirtualBox network. I'll name this machine "Client1," join it to the domain, and then log into it using one of my domain accounts.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/d60e11c9-0890-41d8-bc41-1613dd747eb7)
First, I launch my VM to create a DC (Domain Controller).
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/edd52b69-25ff-4e8c-9c5a-e66bb446d283)

Before installing my 2019 server, I adjusted my OS settings by going to the advanced settings and changing the shared clipboard and Drag'nDrop to "Bidirectional." I made this adjustment to enable bi-directional clipboard sharing, allowing me to use copy (Ctrl+C) and paste (Ctrl+V) seamlessly between my work and the Virtual Machine. Additionally, it enables me to drag files between them for smoother interaction.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/30699822-ab5a-4e5a-8234-bff74135f49e)

Next, I navigated to my network settings. As a reminder, I'm setting up the Domain Controller first, and for that, I need two Network Interface Cards (NICs).

- For the first NIC, I dedicated it to the internet, and it will run NAT (Network Address Translation). This helps with internet connectivity.
- The second NIC is dedicated to the internal VMware network. 
  - To add this second NIC, I went to my Network settings.
  - Selected the Adapter.
  - Attached it to the internal network.
  - Made sure to enable it.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/cd6043e0-6c2b-4466-bfd4-6140b5a4952c)
After completing these steps, I proceeded with the Windows setup.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/4f3c8c31-8cc1-4a51-afde-d14b9af7a6a6)
- After Server 2019 installation, I configured the password for my admin account.
- Upon reaching the Windows environment:
  - Note: The Ctrl + Alt + Delete option differs in a VM.
  - Since I had a PC, I navigated to "Input" > "Keyboard" and chose Ctrl + Alt + Delete as the option.
 
  - ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/766c9d31-d3b9-44e3-9641-7a60f0bd5b4e)

- After logging into the server, my next step was to install "VM guest additions" for an improved experience in VM.
- I initiated this process by going to "Devices" and selecting "Guest Additions CD images."

![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/b227d8f3-d194-4304-80bc-429c2d300fae)
Following that, I navigated to Explorer and selected "This PC." From there, I clicked on the Guest Additions for my VM box.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/29f47175-f171-4380-993e-fd76f1b0eb6c)

Once inside the VM box Guest Additions, I conducted a search and opened the "amdx64" file.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/a741fb35-569e-456d-bde2-d1c1e2cd1d11)
This screenshot illustrates how the program should appear while running.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/b5d17295-400c-4de1-a610-ab1787091a50)
"After completing the necessary configurations, I proceeded to manually reboot the Server VM, and then I navigated to my VM to initiate the shutdown process."
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/1b860bb7-576d-4edb-81f0-894a471736cc)
Certainly! Here's the revised information with bullet points for clarity:

- **Reboot Observations:**
  - After rebooting the Server VM:
    - Mouse performance improved; no lag was observed.
    - Screen resolution adjustment worked seamlessly.

- **Setting Up IP Addresses for NICs:**
  - Identified two NICs from the diagram.
  - Focused on configuring IP addresses for NIC 2 (Internal), as NIC 1 (connected to the Internet) automatically received an IP address from the home router.

- **Manual IP Address Configuration for NIC 2:**
  - Right-clicked on the network icon.
  - Selected "Change adapter options."

- **Emphasis on NIC 1 and NIC 2:**
  - Emphasized that NIC 1 requires no manual IP address assignment.
  - Stressed the importance of manually assigning an IP address to NIC 2 for internal network connectivity.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/79c7d005-5617-4940-9beb-b12dfe84aae6)

"At this juncture, I needed to identify my network connection. To do so, I right-clicked on the first network, opened 'Status,' and selected 'Details.' Subsequently, I located my IPv4 address, which was 10.0.2.15. Once identified, I assigned the name 'INTERNET' to this network."
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/cf69804a-2e46-4a03-8926-cd9b5f35fba9)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/df58659a-d058-44c2-9497-89fb7295f5d3)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/ab1d9bc8-04c9-4715-8f76-50a133f2b544)
- **Renaming and Checking NICs:**
  - Checked the 1st network by right-clicking and opening status > details.
  - Identified the IPv4 address (e.g., 10.0.2.15) and renamed it to “INTERNET.”

- **Identifying Internal Adapter:**
  - Checked the 2nd Ethernet adapter by examining its properties.
  - Noted that it was unable to find a DHCP server and was auto-assigned the IP address 169.254.155.46.
  - Renamed the 2nd Ethernet adapter to “X_Internal_X” and updated the PC name to “DC” (domain controller).

- **Assigning IP Address:**
  - Went to Network icon > Change adapter options.
  - Highlighted and right-clicked the 2nd “X_Internal_X” adapter.
  - Accessed Properties > IPv4 > Configure.
  - Added the IP address 172.16.0.1.
  - Subnet mask was automatically set to 255.255.255.0.

- **Default Gateway Consideration:**
  - Opted not to use a default gateway for this NIC.
  - Explained that the domain controller itself would serve as the default gateway.
  - Clarified that as it has two NICs (one on the “Internet” and the other on the “Internal”), only the NIC connected to the “Internet” requires a default gateway.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/eb512b6c-16a3-4b6a-9d96-4a33239f3946)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/70927486-e2f9-40e5-99f6-291fbf368862)
When I install Active Directory, it automatically installs DNS, making this server use itself as the DNS server. To achieve this, I can simply use its own IP address.

![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/8047427e-cfb3-4765-bda6-76ba6a7fe814)
-Alternatively, I can enter the loopback address, which is 127.0.0.1, a generic address that refers to the server itself.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/09f7586e-bfd7-4637-9ab4-51738dbdf721)

Returning to the diagram, I've completed the following steps:
1. Configured IP addressing for the NIC connected to the internal network, which is currently empty.
2. The next task on the agenda is to install "Active Directory Domain Services" (ADDS) and proceed to create a domain.
3. ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/7535be71-4f0d-41bb-8612-5b882e85112f)

My next step in creating ADDS involves opening my server and selecting "Add Roles and Features."
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/2011a61f-b839-40e5-8797-5ef4f5925247)

Upon reaching this point, I chose the server where I intend to install Active Directory services. I selected the specific server I will be using and proceeded to set up Active Directory.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/999ca3c8-e78b-42bd-b6e4-518ef54fa222)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/c2d84171-3d7f-4125-ad63-2b73f98abe36)

Click on "Add features," and then proceed to the next step to initiate the installation process.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/5356ea4b-9976-4826-a748-cd7145221ed2)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/6e9f6caf-1308-4b28-8c31-7adb301b1af7)

After completing the Active Directory (AD) installation, I proceeded to the "Post-deployment Configuration" to create the domain. By selecting "Promote this server to a domain controller," I accessed the "Add a new forest" tab. Here, I designated a name for the domain, choosing "mydomain.com" for this instance.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/d105dfe3-ca5a-443f-b49a-15673972033f)

- Entered password for the configuration.
- Clicked "Next" through the subsequent steps until reaching the final screen.
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/3f7126df-ad4f-492f-bc22-2ad29cdba32e)
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/f626986c-a1bb-4ab0-b716-a8b98e54477f)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/db4ba0c7-1255-45f0-ba4c-8ded30a23848)
- Installed as shown on the screen below.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/599953c2-338d-494c-a3eb-f2e05cf4d845)
So now I logged in with my new built-in admin  with password as shown below
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/1497b794-ebfe-4bb7-8bf7-9cca6bacff40)
- Went to Start > Administrative tools > Active Directory > Active Directory User & Computers
- Created a dedicated domain admin account instead of using the built-in administrator account.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/cd01abd3-1b2f-43cd-ae73-4ae7605d65e3)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/e8c2e600-5e1a-4191-a3bf-7cffbf86cad9)
- Hovered over "mydomain"
- Right-clicked and selected "New" > "Organizational Unit (OU)"
- Created an organizational unit (OU) to place my admin account in.
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/a457c307-0e0e-4870-8f0c-09a9a657ab87)
- Typed "_ADMINS"
- Unchecked the box below
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/4f79a0d0-b77b-461c-96ec-c693fad9bec2)
-- Right-clicked on the new folder "_ADMINS"
- Selected "USER"
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/36fa3431-683f-4281-89d0-03d83caec858)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/8881fda4-6f53-4cec-979f-e7548a049c35)
- Used the exact same password as created.
- Checked the box "Password never expires" as it is a lab environment.
- Successfully created the account.
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/84ceea8a-50d9-4be3-b798-4963595e1094)
- Right-clicked on the domain account.
- Searched for properties.
- Navigated to "Member of" tab.
- Clicked on "Members of."
- Added "domain admins."
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/d1e2f12b-25d5-480a-8678-3218c627ca94)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/cc17b941-fccf-4985-8459-07bcc95d98df)
- Right-clicked on the new folder "_ADMINS."
- Selected "USER."
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/c8e3e435-4843-4d02-a916-76556e66d477)
- After logging into the account, my task, as per my diagram, is to install RAS/NAT (*Remote Access Service/Network Address Translation*), which is a remote access server network. The purpose of this is to create a Windows 10 client, enabling it to be on a private VPN (Virtual Private Network) while still accessing the internet through the domain controller.
- ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/bf301e0e-d8f4-4997-be39-2c46bf5ae0e0)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/c154e221-dd38-4f2f-8d4e-dc9ce9a74c0f)
I will also install (NAP) *Network Access Point* like RAS and NAT on the domain controller to allow our clients to do that. To achieve this, I will go to Server Manager > Add roles and features > Next > Next. (*Note: I noticed my server...)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/7e41051f-088f-40ad-a897-38970590b6d8)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/8a510695-ebdf-49d1-9127-888d57479d59)
came back to the page to add roles. I checked the box for remote access, clicked next until I got to install Routing.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/ec779bf3-7d34-4c4d-bd66-54ca41688f36)
I proceeded with the installation until I reached the point to install routing, as illustrated below.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/b3d21610-0ad3-4adf-8b21-4675275148be)
Once this![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/f0d29588-92a6-47f0-8b1b-1a2f53534921)
 was completed, I returned to Server Manager, accessed "Tools," and then navigated to "Routing and Remote Access."
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/135747e1-ba02-47c9-a2dc-af4cbceab96b)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/02b3ba17-6407-4bd6-8660-a959afe44c9d)
I proceeded to install NAT, following the process until I reached and clicked “Upon this public interface to connect to the internet,” as shown below.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/3fe6adfd-9eeb-42c9-be02-20ca65439917)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/89bcca60-4f38-42c0-9dbf-5bcfe7950c95)
I confirmed the completion of my task by observing the icon change on my DC (local) to a green color, indicating successful configuration.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/2177a3d1-1ade-4931-a1fe-486a944da22b)

To set up the DHCP server on our domain controller and define the scope information, follow these steps:

1. Navigate to the domain server.
2. Click on "Add roles."
3. Proceed by selecting "Next."
4. Choose "DHCP Server" and also select "Add features."
5. After this, restart your system. *Note: The CPU will restart automatically.*

   ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/49db9fa1-c6a8-439b-bf0e-aa364b8be922)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/cd49c156-934f-4e0a-8813-665c7c53f44d)
After completing the DHCP server installation, close the window.

To configure the DHCP settings, follow these steps:

1. Go back to Server Manager.
2. Navigate to Dashboard > Tools > DHCP.
3. DHCP enables computers on the network to automatically obtain their IP addresses.
4. Create a scope for IP addresses in the range of 172.16.0.100 with the specified subnet mask.
5. Open the DHCP server and observe that both IPv4 and IPv6 are currently down.
6. Right-click on IPv4 and select "New Scope."
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/d8b70757-effe-4fda-a8e5-35ee763f401e)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/f8acc57b-c015-4b52-a59f-9174609d27b1)
Include the following details for clarity:

1. Naming the Scope:
   - Name the scope after the IP range, for instance, "172.16.0.100-200."

2. IP Range Selection:
   - Specify the IP range, and in this case, begin with the starting address 172.16.0.100.

3. Exclusions:
   - Confirm that no exclusions are required for this setup.

4. Proceed:
   - Continue with the configuration process, moving forward without any exclusions.
   ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/1a889755-94a5-4f1e-924a-d815c9f221f3)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/865b71ab-1259-4592-9a15-2ad94130537f)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/32e56136-71bb-48c4-a569-778d8aba2dde)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/2a7cbf7f-c8b7-4e21-9c9a-7b840085c34c)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/864d047b-474f-475e-887e-3fa2dd4b706f)
After completing the DHCP scope configuration, follow these steps for a smooth update:

1. Authorization and Refresh:
   - Hover over the DC Server in the DHCP console.
   - Right-click and choose "Authorize."
   - Refresh the DHCP server.

2. Status Update:
   - After authorization and refresh, check the status of IPv4 and IPv6.
   - Confirm that the status for both IPv4 and IPv6 has been successfully updated.

These steps ensure that your DHCP server is properly authorized and updated with the new configuration.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/64a619c7-fe4f-44c2-bd83-1ec13d96e243)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/9a262d94-f41e-41d7-8a37-538336861384)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/de83fab1-7ab0-48dd-8816-38f1ba8f099a)
To configure internet browsing on the domain controller, follow these steps:

1. Navigate to Server Manager.

2. Click on "Configure this Local Server."

3. Look for the Internet Explorer Enhanced Security Configuration section.

4. Disable Internet Explorer Enhanced Security:
   - If it's enabled, find the option to disable it.
   - Follow the prompts or settings to turn off Internet Explorer Enhanced Security.

This configuration change will allow you to browse the internet from the domain controller without the constraints of enhanced security.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/16c11ba5-f907-407a-8abd-54e1e1d2ee50)

To create multiple users in Active Directory using PowerShell scripts, follow these steps:

1. Disable Internet Explorer Enhanced Security:
   - In Server Manager, go to "Configure this Local Server."
   - Locate the Internet Explorer Enhanced Security Configuration section.
   - Turn off Internet Explorer Enhanced Security.

2. Open Internet Explorer:
   - Use Internet Explorer to navigate to the script repository at https://github.com/joshmadakor1/AD_PS.

3. Download and Extract the Script:
   - Download the script from the repository by saving the file to your desktop.
   - Extract the contents of the downloaded file. You should find a folder named "AD_PS-master."

4. Open PowerShell:
   - Launch PowerShell to run the script.

5. Navigate to the Script Folder:
   - Use the `cd` command to navigate to the extracted script folder:
     ```
     cd Desktop\AD_PS-master\Names
     ```

6. Run the Script:
   - Run the PowerShell script to create multiple users:
     ```
     .\CreateADUsers.ps1
     ```

This script will execute and create a batch of sample users in Active Directory. Note that running PowerShell scripts should be done with caution, especially in a production environment.

![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/d1a605c8-df0a-4fd4-92d3-d1f18d0fafb6)

To add users into Active Directory using your name and the created list, follow these steps:

1. Open the PowerShell Script:
   - Navigate to the folder where you extracted the PowerShell script.

2. Modify the Script:
   - Open the PowerShell script file (e.g., `CreateADUsers.ps1`) in a text editor.

3. Edit User Information:
   - Within the script, you should find sections specifying user information.
   - Replace the placeholder values with your desired user details (e.g., your name, usernames, passwords).

4. Save Changes:
   - Save the changes to the script file after editing.

5. Run the Script:
   - Open PowerShell and navigate to the folder containing the modified script.
   - Run the modified script to add users to Active Directory:
     ```powershell
     .\CreateADUsers.ps1
     ```

This will execute the script with your specified user details and add the users to Active Directory. Ensure that the provided information is accurate and follows any requirements or constraints set in your Active Directory environment.

![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/553b5682-c7b2-46ba-a5c7-9b7d63700b2c)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/c20d6044-9de9-458b-a689-a7c1eb6adaed)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/c001918c-7f48-48a8-b541-04517ced5dac)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/e798eefe-b3fc-4f1e-8c7f-aa6f8b6a11cb)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/e635860b-910d-4cc7-88b5-322d1be65cdc)
"After completing the Active Directory session, I've successfully automated the creation of over 1,000 users in the system and added them to Active Directory."
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/57a43dc2-70ef-4ea3-a511-e0ff2356319e)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/2e013e67-7157-4e4d-b1e4-5bb98773a22d)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/f45eee61-e28f-4b1d-8503-2e88d6c3e0d5)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/12cc8304-bf32-4297-b591-c5b865fa0a1c)

- **Create New VM Client:**
  - Verify that the DNS server is functioning correctly by successfully pinging the internet.
  - Confirm connectivity from the client all the way to the default gateway, which is the Domain Controller.
  - Ensure that the Domain Controller is properly handling NAT (Network Address Translation) and forwarding traffic to the internet.
  - Validate bidirectional ping functionality from the internet back to the Domain Controller.
  ![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/54601a3f-0a6d-458a-a2e4-a7835bc8bcd5)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/99bdd0e3-8067-4002-b8c7-4db63ac3406e)

![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/60bc08b2-ea0e-4e6a-9f97-6345bac0f3f3)
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/c7138c61-6b87-4e25-9e20-05d8156aba90)
Confirmed: Successfully joined "Client4" to the "mydomain" in Active Directory. This implies that any account, including admin access, can now be utilized to access the joined client.
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/959f5410-72a6-4606-a24e-a5b083c703cd)
This screenshot demonstrates the capability to utilize my admin access to access Windows 10 on "Client4".
![image](https://github.com/Vtec87/Active-Directory-Architect-Build-Secure-your-Network-Empire-/assets/115051912/194f0b6a-d0a7-40a5-bd5c-cfa03704df69)
Referring back to my diagram, I successfully established a mini Corporate Network.
In conclusion, the entire infrastructure has been successfully built and is operational, demonstrating seamless connectivity within the network.
**Before You Dive In**
n:**
- **[Checklist](#link-to-checklist):** Ensure you have everything ready. It's like a checklist before a trip.
- **[Prerequisites](#link-to-prerequisites):** Make sure you have the necessary software and configurations to avoid any bumps in the road.




**Troubleshooting Tips:**
   - Sometimes, the path isn’t as smooth. I’ve got your back with [tips to tackle common challenges](#link-to-troubleshooting).

**A Note on Detail:**
   - In some steps, I'll break it down a bit more for a crystal-clear understanding. For our seasoned explorers, I'll keep it light. Look out for the details where they matter most!

Ready for the adventure? Let's paint our canvas and shape our Active Directory domain! 🚀
