# oss-audit-24BCE10824

# oss-audit-24BCE10824
Capstone project containing shell scripts for the Open Source Software Audit of the Apache HTTP Server.

# Open Source Software Audit
**Student Name:** NISHTHA MAURYA
**Roll Number:** 24BCE10824  
**Chosen Software:** Apache HTTP Server

## Project Overview
This repository contains five custom Bash shell scripts written for an Ubuntu Linux environment as part of an open-source audit of the Apache HTTP Server. 

## Description of Scripts
* **`script1.sh` (System Identity Report):** Dynamically retrieves core Linux host identity metrics (Kernel, OS, Uptime) using command substitution.
* **`script2.sh` (FOSS Package Inspector):** Verifies the APT installation status, version, and architecture of the Apache package.
* **`script3.sh` (Disk and Permission Auditor):** Loops through and audits standard system directories and the `/etc/apache2` configuration folder for storage size and ownership permissions.
* **`script4.sh` (Log File Analyzer):** Parses log files line-by-line using a conditional while-read loop to flag and count specific system errors.
* **`script5.sh` (Manifesto Generator):** An interactive prompt that generates a personalized open-source philosophy text file using user input and string concatenation.

## Dependencies Required
To run these scripts successfully, ensure the following dependencies are met on your system:
* **Operating System:** Ubuntu / Debian-based Linux distribution (or Windows Subsystem for Linux).
* **Environment:** Standard Bash shell.
* **Software Dependency:** The **Apache HTTP Server** must be installed on the system (`sudo apt install apache2`). Without this, Script 2 and Script 3 will report that the software and its configuration directories (`/etc/apache2`) are missing.

## Step-by-Step Instructions to Run the Codes

**Step 1: Open your Terminal**
Launch your Ubuntu Linux terminal (or WSL environment).

**Step 2: Navigate to the Directory**
Use the `cd` command to navigate to the folder where you have downloaded or cloned these script files.

**Step 3: Grant Execution Permissions**
By default, Linux text files are not executable. You must grant execution rights to each script before running it for the first time using the `chmod` command. 
```bash
chmod +x script1.sh
chmod +x script2.sh
chmod +x script3.sh
chmod +x script4.sh
chmod +x script5.sh.
```

**Step 4: Execute the Scripts**
Run the scripts by prefixing the filename with ./ (which tells Linux to look in the current directory).

To run Script 1, 2, 3, or 5:
```bash
./script1.sh
```
Special Instruction for Script 4 (script4.sh):
Script 4 is a Log File Analyzer that requires a target file to read. You must pass a file path as an argument when you run it.

To test it, first create a dummy log file:
```bash
echo -e "System booted\nWarning: high memory\nError: connection timeout\nError: Apache failed" > testlog.txt
```
Then, run the script against the test file:
```bash
./script4.sh testlog.txt
```
