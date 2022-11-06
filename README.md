## Export Service Client Generation

This is the configuration file used by AutoRest to generate the service clients

---

## Getting Started

### Step 1: Download Node.js Installer
<!-- [Node.js web site](https://nodejs.org/en/download/). -->
In a web browser, navigate to the
<a href="https://nodejs.org/en/download/" target="_blank">Node.js web site</a>. 
Click the Windows Installer button to download the latest default version. 
At the time this article was written, version 10.16.0-x64 was the latest version. 
The Node.js installer includes the NPM package manager.

### Step 2: Install Node.js and NPM from Browser
A. Once the installer finishes downloading, launch it. Open the **downloads** link in your browser and click the file or, browse to the location where you have saved the file and double-click it to launch.

B. The system will ask if you want to run the software – click **_Run_**.

C. You will be welcomed to the Node.js Setup Wizard – click **_Next_**.

D. On the next screen, review the license agreement - Click **_Next_**.

E. The installer will prompt you for the installation location - Click **_Next_**.

F. Select components to include or remove from the installation - Click **_Next_**.

G. Finally, click the **_Install_** button to run the installer. When it finishes, click **_Finish_**.

### Step 3: Install AutoRest using NPM:

A. Using a Termonal, console or Power Shell, **_Run_** the following:

> npm install -g --production autorest@3.0.6274 --verbose


### Step 4: Verify Installation of Node.js, NPM and AutoRest

A. Open a command prompt (or PowerShell) and enter the following:

> node -v

B. You can do the same to verify **_NPM_**:

> npm -v

C. To verify the **_AutoRest_** installation, enter the following:

> autorest --info

| Type      | Extension Name                    | Version  | Location
|-----------|-----------------------------------|----------|-------------------------------------------------------------------|
| core      | @autorest/core                    | 3.0.6274 | C:\Users\dhopk\.autorest\@autorest_core@3.0.6274                  |
| extension | @microsoft.azure/autorest.csharp  | 2.3.91   | C:\Users\dhopk\.autorest\@microsoft.azure_autorest.csharp@2.3.91  |
| extension | @microsoft.azure/autorest.modeler | 2.3.55   | C:\Users\dhopk\.autorest\@microsoft.azure_autorest.modeler@2.3.55 |


### Step 5: Generate the service clients

A. From the ./$(project-folder)/swagger/doc folder, **_Run_**:

> autorest readme.md --version=3.0.6274 --verbose

B. To see additional help and options, **_Run_**:

> autorest --help

---

# Configuration Options (yaml)
Below is the yaml code to capture the operational command line options.

```yaml
# Specify the version of Autorest to use
# NOT WORKING - version: V3

# Core Settings and Switches
clear-output-folder: true
input-file: swagger.json
output-folder: Generated-csharp

# Core Functionality for CSharp
csharp:
  namespace: DataStation.Exchange.Export.Server
  library-name: DataStation.Exchange.Export.Service
  add-credentials: true
```

