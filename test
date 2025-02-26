# Automatic Backup of Specific Files Using Scripting and Task Scheduler
Creating an automatic backup of specific files using a shell script and Task Scheduler.
 
## Step 1: Create the Shell Script
 
1. **Create the `.sh` file**:
    - Save the following script code in a file named `backup.sh`:
 
    ```sh
    SCRIPT_DIR=$(dirname "$0")
    SOURCE_DIR="$SCRIPT_DIR/Scripting.md"
    BACKUP_DIR="$SCRIPT_DIR/backup"
    TIMESTAMP=$(date +%Y%m%d%H%M%S)
 
    BACKUP_FILE="backup-$TIMESTAMP.tar.gz"
 
    # Create directory if not exists
    mkdir -p $BACKUP_DIR
 
    # Create a compressed backup of the source directory
    tar -czf "$BACKUP_DIR/$BACKUP_FILE" "$SOURCE_DIR"
    ```
 
    ![Screenshot (45)](https://github.com/user-attachments/assets/3793f6bf-655a-4371-8df3-a30fdfd45e2d)
 
2. **Run the shell script in bash**:
    - Open a terminal and navigate to the directory containing `backup.sh`.
    - Execute the script by running:
      ```sh
      sh activiy1.sh
      ```
    ![Screenshot (47)](https://github.com/user-attachments/assets/666c01b2-c425-4437-972d-7b74a5b1258b)
 
3. **Verify the backup**:
    - A `backup` folder will be created in the script directory, containing the backup file.
    ![Screenshot (48)](https://github.com/user-attachments/assets/b50ce391-5a9b-4e3b-bad0-795e91b2d6a9)
 
## Step 2: View the Backup
 
1. **Extract the backup file**:
    - Navigate to the `backup` folder and extract the `.tar.gz` file using:
      ```sh
      tar -xzf backup-<TIMESTAMP>.tar.gz
      ```
 
    ![Screenshot (49)](https://github.com/user-attachments/assets/fe4d78ea-32aa-4b52-8a4e-b0a8dde1eb81)
    ![Screenshot (50)](https://github.com/user-attachments/assets/fed469b4-e78e-4e6d-a817-1091dccbe8f5)
 
 
2. **View the backed-up file in an IDE**:
    - Open the extracted file in your preferred IDE to verify its contents.
 
    ![Screenshot (52)](https://github.com/user-attachments/assets/a13c2c82-5fd6-4bd3-b1e5-c2c3c562ec2e)
 
## Step 3: Automate the Backup Using Task Scheduler
 
1. **Open Task Scheduler**:
    - Search for "Task Scheduler" in the Start menu and open it.
 
    ![Screenshot (53)](https://github.com/user-attachments/assets/b2e3e5ae-539d-41a2-b671-de5da33ec97b)
 
2. **Create a Basic Task**:
    - Click on "Create Basic Task" in the right-hand pane.
      
    ![Screenshot (54)](https://github.com/user-attachments/assets/7a15e5ef-e1ba-47a6-9892-a0ef0c140614)
    ![Screenshot (55)](https://github.com/user-attachments/assets/3f641165-7646-4a7f-a568-28d1a04fd93a)
 
3. **Select a Trigger**:
    - Choose when you want the task to run (e.g., daily, weekly).
 
    ![Screenshot (56)](https://github.com/user-attachments/assets/ff3e5ae9-c49c-4930-bbbd-e06663de1c71)
    ![Screenshot (57)](https://github.com/user-attachments/assets/6f732ffd-75c9-41ae-b573-427630612640)
 
4. **Select an Action**:
    - Choose "Start a Program" and browse to the location of your `backup.sh` script.
 
    ![Screenshot (58)](https://github.com/user-attachments/assets/1b4a6607-d341-4ca6-9513-6ae60c0d05ca)
    ![Screenshot (59)](https://github.com/user-attachments/assets/fa670074-de39-4152-aea3-b30f27a339a3)
    ![Screenshot (60)](https://github.com/user-attachments/assets/761278ea-cfde-43f7-97de-f9092058ba88)
 
 
5. **Finish the Task Setup**:
    - Review your settings and click "Finish".
 
    ![Screenshot (61)](https://github.com/user-attachments/assets/cb2fc6a6-88fb-4e75-bf29-94f93e2a0b45)
 
6. **Verify the Scheduled Task**:
    - Ensure the task is listed in the Task Scheduler Library and is set to run at the specified time.
 
    ![Screenshot (62)](https://github.com/user-attachments/assets/92cf09cc-4421-442a-b9db-841d94faa1e9)
52.112.125.8
 
