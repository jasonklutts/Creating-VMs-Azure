<p align="center">
<img width="517" height="332" alt="image" src="https://github.com/user-attachments/assets/9d4ab107-9a51-4dc5-a664-93380c696408" />
</p>

# Creating a Windows and Linux Virtual Machine with Microsoft Azure

This tutorial outlines how to create and configure both **Windows** and **Linux (Ubuntu)** virtual machines using **Microsoft Azure**.

---

## Environments and Technologies Used
- Microsoft Azure  
- Virtual Machines (VMs)

---

## Operating Systems Used
- Windows 10 Pro  
- Linux Ubuntu

---

## High-Level Deployment and Configuration Steps
1. Create a **Resource Group**  
2. Create a **Windows 10 VM** inside that Resource Group  
   - Allow Windows VM to create a new **Virtual Network (Vnet)** and **subnet**  
3. Create a **Linux (Ubuntu) VM** inside the same Resource Group  
   - Select the **same Vnet** as the Windows VM  
4. Specify **credentials**, check the **Licensing Agreement**, and click **Review + Create**

---

## Deployment and Configuration Steps

### Step 1: Create Resource Group
<img width="476" height="178" alt="image" src="https://github.com/user-attachments/assets/2bc40877-512c-4431-b045-f55f8bf1518a" />
<img width="550" height="295" alt="image" src="https://github.com/user-attachments/assets/e9b458f5-355f-469e-8f84-36b4dcedc92f" />



From the Azure home page:  
- Go to **Resource Groups** → **Create new**  
- Specify **Subscription**, **Resource Group Name**, and **Region**  
- Click **Review + Create**

---

### Step 2: Create Windows 10 Virtual Machine
<img width="552" height="672" alt="image" src="https://github.com/user-attachments/assets/8325a84a-92a7-4b78-a7bc-7b1dc83a0bf5" />


- Azure Home → **Virtual Machines** → **Create New**  
- Select **Resource Group**, **VM Name**, **Region**, and **Zone**  
- Choose **Windows 10 Pro** image  
- Assign at least **2 vCPUs** and **8–16 GB RAM**

---

### Step 3: Configure Networking for Windows VM
<img width="554" height="721" alt="image" src="https://github.com/user-attachments/assets/b08da6cf-4718-4757-946a-7766bc257472" />


- In the **Networking** tab, specify a **Virtual Network Name**  
- This will later be shared with the Linux VM  
- Leave defaults for the rest, click **Review + Create**

---

### Step 4: Verify Windows VM Deployment
<img width="416" height="697" alt="image" src="https://github.com/user-attachments/assets/3eb21764-a997-4816-99fa-1b6530f42aad" />


After deployment, click the Windows VM to view network info:  
- Operating System  
- RAM Size  
- Public/Private IP Address  
- Virtual Network / Subnet  
- Disk details  

This setup will mirror what is created for the Linux VM.

---

### Step 5: Create Linux Virtual Machine
<img width="622" height="747" alt="image" src="https://github.com/user-attachments/assets/18f336a4-19de-45ef-8864-6e1cef707f78" />


- Go to **Virtual Machines** → **Create New**  
- Select the same **Resource Group**, **Virtual Network**, **Region**, and **Zone**  
- Choose **Ubuntu Server 22.44 LTS - x64 Gen2** image  
- Assign at least **2 vCPUs**

---

### Step 6: Configure Networking for Linux VM
<img width="554" height="730" alt="image" src="https://github.com/user-attachments/assets/049e9787-2f82-4b42-befe-adcec901da04" />
 

- Ensure the **Virtual Network Name** matches the Windows VM’s Vnet  
- Click **Review + Create**

---

### Step 7: Verify Deployment of Both VMs
 <img width="746" height="234" alt="image" src="https://github.com/user-attachments/assets/331f76b1-2373-469f-a6c7-8af8474c688d" />

Once deployed, both Windows and Linux VMs will appear under **Virtual Machines** in the Azure portal.  

✅ **You have successfully deployed Windows and Linux VMs in Microsoft Azure!**
