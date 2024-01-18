# Archiving-and-Logging-Data

As the security analyst at Credico Inc., a financial institution, I had to enhance the existing log management system to comply with the Gramm-Leach-Bliley Act.

**Step 1: Create, Extract, Compress, and Manage tar Backup Archives**

In this section, I navigated to the ~/Projects directory and extracted the TarDocs.tar archive. I verified the extraction and excluded the Java directory to create a new tar archive named Javaless_Docs.tar. Additionally, I created an incremental archive named logs_backup.tar.gz.

**Step 2: Create, Manage, and Automate Cron Jobs**

To mitigate CryptoLocker malware, I created a cron job that archives the /var/log/auth.log file every Wednesday at 6 a.m. using gzip compression. I configured the cron job to enhance the system's resilience against ransomware attacks.

**Step 3: Write Basic Bash Scripts**

To adhere to the Gramm-Leach-Bliley Act, I created backup directories and a bash script (system.sh) that executes Linux tools to gather system information. The script saves the results in different text files within their respective directories. I made the script executable and tested it successfully.

**Step 4: Manage Log File Sizes**

Recognizing the need for log rotation to manage log file sizes, I edited the logrotate configuration file to rotate authentication messages weekly, keeping only the seven most recent logs without compressing empty logs and delaying compression.

**Step 5: Check for Policy and File Violations**

To monitor account and authorization log modifications, I verified the auditd service's activity, configured auditd parameters, and created rules to watch specific paths. I restarted the auditd daemon, produced an audit report on user authentications, created a new user, and generated a report on account modifications.

**Step 6: Perform Various Log Filtering Techniques**

To investigate a suspicious login, I wrote journalctl commands for various use cases, including log searches for messages with specific priority levels, checking disk usage, removing archived journal files, and filtering log messages based on priority levels. I automated the last task by creating a daily cron job in the user crontab.

The completion of this assignment demonstrates my proficiency in utilizing various tools and concepts for effective log management and data protection in a financial institution's environment.
