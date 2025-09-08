#  Ex.No.2    TestDisk: Open-Source Data Recovery Tool

## Aim :
To use TestDisk step by step to recover a missing partition and repair a corrupted one.



## 🛠️ Installation
Linux (Debian/Ubuntu): sudo apt-get install testdisk

macOS (Homebrew): brew install testdisk

Windows: Download the executable from the official CGSecurity website.

## Procedure

### 1. Create a Log File
- Launch TestDisk from your terminal or command prompt using sudo testdisk (or testdisk_win.exe on Windows).

- Select the [Create] option to generate a log file of the recovery session. This is helpful for future reference or troubleshooting.
<br>
<br>
<p align="center">
<img width="1245" height="409" alt="Screenshot 2025-09-08 235101" src="https://github.com/user-attachments/assets/045385ac-0011-4a5a-a80f-4a887116b61f" />


</p>
<br>
<br>

### 2. Select the Drive to Analyze
- TestDisk will display a list of all detected storage devices.

- Use the Up/Down arrow keys to highlight the drive that contains your lost data.

<br>
<br>
<p align="center">
<img width="882" height="669" alt="Screenshot 2025-09-08 235119" src="https://github.com/user-attachments/assets/59ad8971-91b7-45de-91e9-f0026d99f41a" />

</p>
<br>
<br>

- Select [Proceed] to move to the next step.

### 3. Choose the Partition Table Type
- TestDisk will automatically suggest the most likely partition table type (e.g., Intel/PC, EFI GPT).

- The default value is usually correct. Confirm the selection by pressing Enter.
<br>
<br>
<p align="center">
<img width="799" height="459" alt="Screenshot 2025-09-08 235132" src="https://github.com/user-attachments/assets/91e0c0bd-a3dd-4b3b-adf8-90f4f4eaebd2" />


</p>
<br>
<br>

### 4. Analyze Current Partition Structure
- From the main menu, choose [Analyse] and press Enter.
<br>
<br>
<p align="center">
<img width="670" height="419" alt="Screenshot 2025-09-08 235143" src="https://github.com/user-attachments/assets/10bea8b9-737b-43a8-b1e0-f46691867058" />

</p>
<br>
<br>

- This will display the current partition table and check for errors or missing partitions.

### 5. Perform a Quick Search
- After the analysis, you will be prompted to perform a [Quick Search].

<br>
<br>
<p align="center">
<img width="786" height="649" alt="Screenshot 2025-09-08 235156" src="https://github.com/user-attachments/assets/c53f1bfb-4d52-4f93-a18d-b4797e66f06c" />

</p>
<br>
<br>

- Select it and press Enter to scan the drive for lost partitions.

- Once a partition is found, you can press p to list its files. Deleted files and folders often appear in red.

- Press q to return to the search results.

  ### 6. Perform a Deeper Search
- If the Quick Search fails to find your lost partitions, select [Deeper Search].

-<br>
<br>
<p align="center"> 
<img width="750" height="441" alt="Screenshot 2025-09-08 235205" src="https://github.com/user-attachments/assets/81e40aec-be89-4ea3-b9f0-fa6cc02b8d40" />

</p>
<br>
<br>

- This process can take a long time, as it scans the entire drive, block by block, to find remnants of partition structures.

- Again, use p to preview files and confirm if a found partition is the one you are looking for.

### 7. Modify Partition Status
- After finding the correct partitions, use the Left/Right arrow keys to set their status.

- Use **Left/Right arrow keys** to change status:  
  - **P**: Primary  
  - ***:** Bootable  
  - **L**: Logical  
  - **D**: Deleted

    <br>
<br>
<p align="center">
<img width="772" height="659" alt="Screenshot 2025-09-08 235216" src="https://github.com/user-attachments/assets/7123b7d6-c0db-4634-8915-ad1ab2f23f89" />

</p>
<br>
<br>

- Ensure that the partitions you want to recover are marked as Primary or Logical (and not deleted).

### 8. Write the Partition Table
- Once you are confident the partition structure is correct, select [Write] from the menu.

<br>
<br>
<p align="center">
<img width="698" height="675" alt="Screenshot 2025-09-08 235231" src="https://github.com/user-attachments/assets/c258533c-b671-4427-b090-f0e9a86470a2" />

<br>
<br>

- Confirm the operation by pressing y (for yes). This will write the new partition table to your disk.

<br>
<br>
<p align="center">
<img width="777" height="443" alt="Screenshot 2025-09-08 235248" src="https://github.com/user-attachments/assets/64b5ee7a-0e65-4d96-948f-1cc1197291a8" />

</p>
<br>
<br>


- WARNING: This is a permanent change. Double-check your selections before writing.

### 9. Recover Files
- If you just need to recover a few files without fixing the partition table, you can do so from the file list (after pressing p).

- Navigate to the folder containing your desired files.

- Use the colon : key to select the files you want to recover.

- Press the uppercase C key to copy the selected file(s).

- Navigate to a safe destination on a different storage device and press uppercase C again to paste.

### 10. Exit and Restart
- Once your task is complete, select [Quit] to exit the program.

- If you wrote a new partition table to the drive, it is recommended to restart your computer to allow the operating system to recognize the changes.
