## 🔎 Lab

**Discover how to view information about your hardware on your computer:**

- **For Windows:**

1. Press **`win + r`** on your keyboard and enter **msinfo32** in the window to view internal information such as the processor, software version, and amount of **RAM**.

2. Press **`win + r`** on your keyboard and enter **cmd** in the window. It will open the Windows terminal, and enter the command **systeminfo**; you will get information from the hostname to the BIOS version.

3. In the same terminal, enter the command ***wmic memphysical get MaxCapacity***, ***MemoryDevices.***

    > The command will return the maximum amount of RAM supported by the motherboard and the number of available slots. This is a very useful command if you plan to upgrade your computer's RAM. The maximum amount (MaxCapacity) is expressed in Kb, so you will have to divide by 1024 to transform it into Mb and again divide by 1024 to get the amount in Gigabytes.
