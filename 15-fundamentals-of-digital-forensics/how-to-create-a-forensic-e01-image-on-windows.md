---
title: "Create a Forensic Image (.E01) from Windows Using FTK Imager"
description: "Step-by-step guide to acquiring digital evidence from physical or virtual drives using FTK Imager on Windows systems."
tags: ["forensics", "cybersecurity", "windows", "e01", "ftk-imager"]
author: ["alesanchezr"]
---

# How to Create a Forensic `.E01` Image from a Physical or Virtual Disk (on Windows)

In digital forensics, an `.E01` image allows you to capture the complete contents of a hard drive without altering the original. This file can contain metadata, be split into smaller parts, and be automatically verified using hashes. Below, two ways to generate an `.E01` image are explained: one from a physically connected hard drive, and another from a virtual machine file.

## Creating an Image from a Hard Drive Connected to the Computer (on Windows)

Suppose a hard drive was removed from a suspect computer. The analyst connects it to their workstation using a SATA-USB adapter or an external enclosure. The goal is to make a bit-by-bit copy of that disk without modifying it.

For this, **FTK Imager** will be used, a free tool that allows you to capture disks and generate forensic images in `.E01` format.

### Steps:

1. Download and install [FTK Imager](https://www.exterro.com/ftk-imager).
2. Open the program as administrator.
3. In the top menu, select -> `File → Create Disk Image...`

    ![create-disk-image](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/create-disk-image.png?raw=true)

4. Choose the `Physical Drive` option. A list of connected disks will appear. Select the external disk (make sure it is not your system disk). How do you do this? When you select Physical Drive in FTK Imager, you will see something like:

    ```python
    PhysicalDrive0 - 500GB - WDC WD5000LPCX-...
    PhysicalDrive1 - 120GB - SanDisk SSD PLUS...
    PhysicalDrive2 - 16GB - Generic USB Flash...
    ```

    > **Check if the size matches your external disk. The system disk is usually `PhysicalDrive0`, so you should not select it unless you are absolutely sure it is the external disk (which is almost never the case).**

5. Fill in the case fields (for example: case number, examiner name, analysis description). These can be left blank if this is for practice.

    ![inputs](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/cases-inputs.png?raw=true)

6. For image type, select `E01 (Expert Witness Format)`.

    ![select format](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/format-selection.png?raw=true)

7. Choose a destination folder to save the image.

    ![select format](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/select-img-destination.png?raw=true)

In the configuration options:
   - **Compression**: set the value to `6` (fast).
   - **Fragmentation**: use `1500 MB` to split the image into more manageable parts.

8. Press `Start` to begin acquisition. Make sure to enable the **"Verify images after they are created"** option to ensure the integrity of the copy.

    ![select-file](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/start-img.png?raw=true)

When finished, you will get a series of `.E01`, `.E02`, etc. files, along with a `.txt` file documenting the generated hashes and case details.

## Creating an Image from a Virtual Machine (`.vdi` or `.vmdk` file)

When working with virtual machines, you do not have a physical disk, but a file representing it. In VirtualBox, this file has a `.vdi` extension; in VMware, `.vmdk`. The contents of these files can also be forensically analyzed, but first they need to be converted.

### Step 1: Convert the Virtual Machine File to `.raw`

The `.raw` format is a direct copy of the virtual disk contents. To obtain it, use the `qemu-img` tool.

1. Download QEMU for Windows from [qemu.weilnetz.de](https://qemu.weilnetz.de/w64/).
2. Extract or install QEMU and locate the `qemu-img.exe` file.
3. Open the terminal (CMD or PowerShell) and run the appropriate command according to your disk type:

For VirtualBox:
```bash
qemu-img convert -f vdi -O raw "C:\path\to\file.vdi" "C:\output\image.raw"
```

For VMware:
```bash
qemu-img convert -f vmdk -O raw "C:\path\to\file.vmdk" "C:\output\image.raw"
```

---

### Step 2: Convert `.raw` to `.E01` with FTK Imager

1. Open FTK Imager as administrator.
2. In the menu, select:

   `File → Create Disk Image...`

3. Select the source type, in this case `Image File`:

   ![select-source](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/select-source.png?raw=true)

4. Select the `.raw` file as the source.
    
    ![select-file](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/start-img.png?raw=true)

    > Make sure to enable the **"Verify images after they are created"** option to ensure the integrity of the copy.

5. Then, click **Add** to define the output image type and where it will be saved, select:

    ![format](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/format-selection.png?raw=true)

6. Fill in the case metadata.

    ![inputs](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/cases-inputs.png?raw=true)

7. Choose the destination folder, file name, compression, and fragmentation.

    ![select destination](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/select-img-destination.png?raw=true)

    > Leave the “Use AD Encryption” option unchecked.

8. Press **Finish**, then **Start** to begin creating the image.

## Expected Result

FTK Imager will generate:

- Segmented files: `.E01`, `.E02`, `.E03`, etc.
- A `.txt` file with the verification hash and case metadata

    ![images results](https://github.com/rosinni/cybersecurity-syllabus/blob/main/assets/15-fundamentals-of-digital-forensics/results-e01.png?raw=true)



These files can be analyzed directly with tools like **Autopsy** or reloaded into FTK Imager for exploration. It is important to keep all files together in the same folder and not change their names if you want to maintain the integrity of the evidence.
