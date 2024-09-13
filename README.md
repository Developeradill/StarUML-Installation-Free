# StarUML-Installation-Free
## Overview

This guide helps users bypass the StarUML license validation by modifying the license-checking script in the `app.asar` file. By following this procedure, you will be able to run StarUML without requiring a license key. This process involves using Node.js and the `asar` package to unpack and repack the `app.asar` file in the StarUML installation directory.

## Prerequisites
- StarUML installed on your system (Download from [here](https://staruml.io/))
- Node.js installed (Download from [here](https://nodejs.org/en))
- Basic knowledge of command-line operations

## Steps

### 1. **Install Node.js**
Download and install Node.js from the official website.

### 2. **Set Up the Environment**
1. Create a new folder on your desktop named `New Asar`.
2. Go to the StarUML installation folder (`C:\Program Files\StarUML\resources`) and copy the `app.asar` file.
3. Paste the `app.asar` file into the `New Asar` folder.

### 3. **Install ASAR**
Open a command prompt and install the ASAR package by running:

npm install -g asar

### 4. **Extract the app.asar File**
In the command prompt, navigate to the New Asar folder on your desktop:

cmd:
cd Desktop\New Asar

Then, extract the app.asar file by running:

cmd:
asar extract app.asar app

###5. **Modify the License Manager**
Navigate to the extracted folder: New Asar/app/src/engine and locate the license-manager.js file. 
Open this file in a text editor and replace its content with the code provided in this repository (Licence file).

###6. **Repack the app.asar File**
After editing the license-manager.js file, go back to the command prompt and run:

cmd:
asar pack app app.asar

This will repack the modified files into a new app.asar file.

###7. **Replace the Original app.asar File**
Copy the newly created app.asar file and replace the original one located in: C:\Program Files\StarUML\resources.

###8. **Open StarUML**
Start StarUML, and it should work without requiring license validation.


**Disclaimer**
This repository is for educational purposes only. Bypassing software licenses may violate terms of service and local laws. Use this guide responsibly.
