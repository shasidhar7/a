# Automatic Backup of Specific Files Using Scripting and Task Scheduler
Creating an automatic backup of specific files using a shell script and Task Scheduler.
 
## Step 1: Create the Shell Script
 
1. **Create the `.sh` file**:
    - Save the following script code in a file named `activity1.sh`:
 
    ```sh
    # Backup 
    SOURCE_DIR="/d/Mindsprint/Day 11"
    backup_dir="/d/backup"
    timestamp=$(date +"%Y-%m-%d_%H-%M-%S")
    Backup_file="backup_$timestamp.tar.gz"

   # Create Directory if not exist
   mkdir -p "$backup_dir"

   # Convert tar file
   tar -czf "$backup_dir/$Backup_file" "$SOURCE_DIR"


    ```

    <img width="695" alt="Screenshot 2025-02-26 214746" src="https://github.com/user-attachments/assets/d54d3823-0ed2-4398-b796-9d88302033c8" />


 
2. **Run the shell script in bash**:
    - Open a terminal and navigate to the directory containing `activity1.sh`.
    - Execute the script by running:
      ```sh
      sh activiy1.sh
      ```
 
3. **Verify the backup**:
    - A `backup` folder will be created in the script directory, containing the backup file.
    <img width="960" alt="Screenshot 2025-02-26 214923" src="https://github.com/user-attachments/assets/6a56fd91-1ef5-428d-ab79-b8038e487f09" />

 
## Step 2: View the Backup
 
1. **Extract the backup file**:
    - Navigate to the `backup` folder and extract the `.tar.gz` file using:
      ```sh
      tar -xzf backup-<TIMESTAMP>.tar.gz
      ```
 
    <img width="960" alt="Screenshot 2025-02-26 215052" src="https://github.com/user-attachments/assets/736d4faf-25a6-41e0-a037-770f8f2ff27a" />

 
 
2. **View the backed-up file in an IDE**:
    - Open the extracted file in your preferred IDE to verify its contents.
 
    <img width="960" alt="Screenshot 2025-02-26 215233" src="https://github.com/user-attachments/assets/d740e508-dcfd-4efc-a995-7b96ee27a85b" />

 
## Step 3: Automate the Backup Using Task Scheduler
 
1. **Open Task Scheduler**:
    - Search for "Task Scheduler" in the Start menu and open it.
 
 
2. **Create a Basic Task**:
    - Click on "Create Basic Task" in the right-hand pane.
      
<img width="960" alt="Screenshot 2025-02-26 215346" src="https://github.com/user-attachments/assets/30ed055d-8bda-46fa-8ce4-555a11a26f31" />
<img width="556" alt="Screenshot 2025-02-26 223508" src="https://github.com/user-attachments/assets/6e2c87db-768b-4937-934d-d8c0933d792f" />
 
3. **Select a Trigger**:
    - Choose when you want the task to run (e.g., daily, weekly).
 
![Screenshot (2)](https://github.com/user-attachments/assets/84d4724b-b0a4-43f3-b7eb-4bea6375d2c7)
![Screenshot (3)](https://github.com/user-attachments/assets/da10078c-54e1-40df-a05d-056c9c51bfdc)
 
4. **Select an Action**:
    - Choose "Start a Program" and browse to the location of your `backup.sh` script.
 
![Screenshot (4)](https://github.com/user-attachments/assets/26896693-6c94-4e41-81b7-1320ab5efe50)
![Screenshot (5)](https://github.com/user-attachments/assets/e7ebae6f-5732-4b43-989d-066dc8ae62d6)
 
 
5. **Finish the Task Setup**:
    - Review your settings and click "Finish".
 
 
6. **Verify the Scheduled Task**:
    - Ensure the task is listed in the Task Scheduler Library and is set to run at the specified time.
 
![Screenshot (6)](https://github.com/user-attachments/assets/b783b244-f6d3-4012-8be7-144d8c838c07)
 
