# Windows-Server-2025-on-Hyper-V
This guide provides a step-by-step process to install Windows Server 2025 on a Hyper-V virtual machine.

## Prerequisites

- A host machine with **Hyper-V enabled** (Windows 10 Pro/Enterprise or Windows 11 or Windows Server 2016/2019/2022).
- **Windows Server 2025 ISO** downloaded from the [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter).
- Sufficient system resources (recommended: 4 GB RAM, 2 CPUs, and 60 GB disk space for a smooth experience).

## Table of Contents

1. [Enable Hyper-V](#enable-hyper-v)
2. [Set up a New Virtual Machine](#set-up-a-new-virtual-machine)
3. [Configure the Virtual Machine](#configure-the-virtual-machine)
4. [Install Windows Server 2025](#install-windows-server-2025)
5. [Complete Initial Setup](#complete-initial-setup)

---

### Step 1: Enable Hyper-V

If you haven’t enabled Hyper-V on your host machine, follow these steps:

1. Open **Control Panel** → **Programs** → **Turn Windows features on or off**.
2. Check the box next to **Hyper-V** and its sub-features:
   - **Hyper-V Management Tools**
   - **Hyper-V Platform**
3. Click **OK** and restart your computer if prompted.

### Step 2: Set up a New Virtual Machine

1. Open **Hyper-V Manager**.
2. In the **Actions** panel, click **New** → **Virtual Machine**.

 ![image](https://github.com/user-attachments/assets/a59f064d-4f9d-4b69-ac9b-64c38fcbe1a1)



3. In the **New Virtual Machine Wizard**, click **Next**.

### Step 3: Configure the Virtual Machine

1. **Specify Name and Location**
   - Give your VM a name, such as “Windows Server 2025.”
2. **Assign Memory**
   - Set the startup memory (recommended: at least 4096 MB for Windows Server 2025).
   - Optionally, enable **Dynamic Memory** if your system supports it.
  
 ![image](https://github.com/user-attachments/assets/1fa4cffd-b1d6-4b63-95b2-1c2cb871dc98)


     
3. **Configure Networking**
   - Select an existing virtual switch or create a new one.
4. **Connect Virtual Hard Disk**
   - Choose to **Create a virtual hard disk**.
   - Set the size (recommended: 60 GB or more).
   - (Optional) Choose a different location to store the VM files.


 ![image](https://github.com/user-attachments/assets/55a3c580-2eef-4193-ba47-d34a17ba9c05)


     
5. **Installation Options**
   - Select **Install an operating system from a bootable image file**.
   - Browse and select the **Windows Server 2025 ISO**.


  
 ![image](https://github.com/user-attachments/assets/760ba6a0-fb4d-451f-9b6e-d7b520e91d4e)

     

### Step 4: Install Windows Server 2025

1. Start the new VM:
   - In **Hyper-V Manager**, right-click the new VM and select **Connect**.
   - In the **Virtual Machine Connection** window, click **Start**.
2. Windows Setup will start. Follow the on-screen prompts:
   - Select **Language**, **Time**, and **Keyboard Layout**.
   - Click **Next**, then **Install Now**.
  
   
   ![image](https://github.com/user-attachments/assets/d4bd9d89-b4d0-44ba-8f49-3f32459da25d)

3. Choose your preferred **Windows Server 2025 edition** and click **Next**.

 ![image](https://github.com/user-attachments/assets/fe7b08dd-a1c3-483c-9368-ce43690bde01)


4. Accept the license terms and select **Next**.
5. Select **Custom: Install Windows only (advanced)**.
6. Choose the virtual drive created earlier, then click **Next** to start the installation.

### Step 5: Complete Initial Setup

1. After installation, the system will reboot, and you’ll be prompted to set up an administrator password.
2. Enter a secure password and press **Enter**.

 ![image](https://github.com/user-attachments/assets/e7bcaf84-35e2-47c5-880a-f3c76cf3c8ea)
  
3. Once setup is complete, log in with the administrator credentials you just created.

### Additional Configuration

For optimal performance, consider configuring:

- **Network settings** to join a domain or set a static IP.
- **Windows Updates** to keep your server secure.
- **Roles and Features** as per your project needs.

---

## Conclusion

You now have Windows Server 2025 running on a Hyper-V virtual machine. Enjoy exploring and configuring your new server!
