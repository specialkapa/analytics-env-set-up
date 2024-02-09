# Python Analytics Environment Setup

## Introduction
This repository is dedicated to hosting a PowerShell script designed to be used 
on a Virtual Machine (VM) during startup. The purpose of the script is to 
automate the setup of a Python environment tailored for analytics work. This is 
particularly useful for projects requiring a consistent and automated setup 
process for analytics environments on new VM instances.

## Prerequisites
- Windows-based Virtual Machine
- PowerShell access on the VM

## Setup Instructions

### Automated Environment Setup on VM Startup
1. Place the `init-python-env.ps1` script in a designated startup directory or 
   configure it to run at startup using your VM's task scheduler or startup 
   script settings.
2. Upon VM startup, the script will automatically execute, performing the 
   following actions:
   - Creation of a Python virtual environment.
   - Installation of Python packages specified in `requirements.txt`.
   - Cloning of [jupyter-starter-kit](https://bitbucket.org/ghb-credit-risk/jupyter-starter-kit/src) repository.
   - Creation of jupyter shortcuts

### Manual Setup (Optional)
For manual setup or testing, follow these steps:
1. Copy the `init-python-env.ps1` and `requirements.txt` files to your VM.
2. Open PowerShell as an administrator.
3. Navigate to the directory containing the script.
4. Execute the script by running:
   
   ```powershell
   .\init-python-env.ps1
   ```