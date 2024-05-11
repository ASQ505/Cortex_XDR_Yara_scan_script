# Yara Rule Matching Script for Cortex XDR

This script allows you to perform Yara rule matching within your Cortex XDR environment. It's particularly useful for Incident response, compromise assessments, or periodic scans.

## Original Developer
This script was originally created by hruuttila@paloaltonetworks.com.
https://github.com/bricerenaud/xdr_yara_rule_matching

## Modifications
Several modifications have been made to the script to improve its performance and compatibility:

### v0.1
- Script creation by hruuttila@paloaltonetworks.com.

### v0.2
- Added settings for "nice" and "ionice".
- Implemented base85 encoding for Yara Interpreter.
- Introduced Yara search options.
- Added a message for "no match" scenario.
- Modification by brenaud@paloaltonetworks.com.

### v0.3
- Modified to be compatible with Yara rules containing escape characters.
- Added UTF-8 encoding for better compatibility.
- Modification by abdu.ma10@hotmail.com.

## Installation

To use this script, follow these steps to upload it directly to the Cortex XDR console:

1. **Access Cortex XDR Console:** Log in to your Cortex XDR console.

2. **Navigate to Response / Action Center / Scripts Library:** Go to the Scripts Library within the Response or Action Center section.

3. **Paste Yara Rules:** Before creating the script, ensure to paste all your Yara rules into the provided section in the script file (`yararule` variable).

4. **Upload the Script:**
   - Click on the **New Script** button.
   - Choose the script file from your local machine and upload it.
   - Give your script a descriptive name.
   - Set the Supported OS to **Windows**.
   - Configure the Timeout to a suitable value, starting with 600 seconds as a good practice. Depending on your Yara search, you may need to adjust this value later.
   - Set Input to **Run by entry point** with `main` as the entry point. `root_path` should be specified as a string.
   - Set Output Type to **Auto Detect**.

5. **Create the Script:**
   - After configuring the script settings, click on **Create** to upload and save the script.

By following these steps, you'll have the script ready to run within your Cortex XDR environment.

## Source of Original Script
The original script can be found at [https://github.com/bricerenaud/xdr_yara_rule_matching](https://github.com/bricerenaud/xdr_yara_rule_matching).

## Usage
To execute your script on specific Windows machines, navigate to the Scripts Library menu, and right-click on your script. Choose the "Run" option. provide the "ROOT_PATH" for your search in the field (for example, "C:\Users"), click on RUN.

