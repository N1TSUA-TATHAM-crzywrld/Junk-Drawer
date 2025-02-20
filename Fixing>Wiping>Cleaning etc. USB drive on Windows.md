# 🛠️ Fixing, Wiping, and Cleaning a USB Drive on Windows
 > [!NOTE]
 > For situations where a USB drive isn't visible in File Explorer or appears unmounted despite being connected.

Follow these steps to clean and prepare your USB drive using the Command Prompt:

1. **Open Command Prompt (Terminal):**
   - Press `Windows key + X` and select **Command Prompt** from the menu.
   - *Alternatively:* Press `Windows key + R`, type `cmd`, and press Enter.

2. **Launch DiskPart:**
   - In the Command Prompt, type `diskpart` and press Enter.

3. **List All Disks:**
   - Type `list disk` and press Enter to display all connected disks.

4. **Identify the USB Disk:**
   - To determine which disk corresponds to your USB drive:
     - Unplug the USB drive.
     - Type `list disk` again and note the listed disks.
     - Reconnect the USB drive.
     - Type `list disk` once more and identify the new disk that appears. This is your USB drive.
   - **Caution:** Ensure you correctly identify the USB drive to avoid modifying the wrong disk.

5. **Select the USB Disk:**
   - Once identified (e.g., Disk 2), type:
     ```
     select disk 2
     ```
   - Press Enter. A confirmation message will indicate the selected disk.

6. **Clean the USB Disk:**
   - Type `clean` and press Enter. This command removes all partitions and data from the selected disk.

7. **Convert to MBR (Master Boot Record):**
   - Type `convert mbr` and press Enter. This initializes the disk with the MBR partition style.

8. **Create a Primary Partition:**
   - Type `create partition primary` and press Enter.

After completing these steps, your USB drive has been cleaned and is ready for formatting. To format the drive:

- Open **File Explorer**.
- Locate the USB drive, which should now appear as an unformatted disk.
- Right-click on the drive and select **Format**.
- Choose your desired file system (e.g., NTFS or FAT32) and perform the formatting.

**Note:** Formatting will erase all data on the USB drive. Ensure you have backups of any important data before proceeding.

---

*This guide provides a straightforward method to clean and prepare a USB drive using built-in Windows tools.*
