# Release Guide

This document provides step-by-step instructions on how to build and release a new version of the project.

## Building

### **1. Install Flutter and Setup Development Environment**

1. Install the **Flutter** extension in VS Code.
   - This will install additional tooling required for development.
2. When prompted, install the **Flutter SDK**.
   - For this project, the SDK is installed in the project directory.
   - The installation process will update your environment so that the SDK is added to your system **PATH**.

### **2. Running and Testing Locally**

1. Open **PowerShell** in the workspace directory.
2. Run the application with:
   ```powershell
   flutter run
   ```

### **3. Building for Release**

1. Open a terminal in the project workspace.
2. Run the following command to build the Windows release files:
   ```powershell
   flutter build windows
   ```

This will generate the necessary files for distribution in the `build\windows\x64\runner\Release\` directory.

## Preparing a Release

### **1. Navigate to the Build Directory**

Open **PowerShell** or **Command Prompt** and run:

```powershell
cd build\windows\x64\runner\Release\
```

This ensures you are in the correct directory where the build files are located.

### **2. (Optional) Zip the Files**

To package all files into a single ZIP archive for easier distribution:

```powershell
Compress-Archive -Path * -DestinationPath Elastic_5468_vX.Y.Z.zip
```

Replace `X.Y.Z` with the appropriate version number.

## Creating a Release on GitHub

### **1. Go to the Repository on GitHub**

1. Open a web browser and navigate to the repository at [SummitRobotics/elastic-dashboard](https://github.com/SummitRobotics/elastic-dashboard).
2. Click on **"Releases"** (found in the right sidebar under "Code").
3. Click **"Draft a new release"**.

### **2. Enter Release Information**

1. In the **"Tag version"** field, enter the version number (e.g., `vX.Y.Z`).
   - If the tag does not exist, GitHub will create it.
2. Add a **title** (e.g., `Version X.Y.Z`).
3. Provide a **description** of the release.

### **3. Upload Release Files**

1. Click **"Attach binaries"** and select either:
   - The entire `Elastic_5468_vX.Y.Z.zip` file (preferred).
   - Individual files from `build\windows\x64\runner\Release\`.

### **4. Publish the Release**

Click **"Publish Release"** to finalize the release.

## **Verifying and Sharing**

1. Check the **Releases** section to confirm the uploaded files.
2. Copy and share the **release link** with users.

---

This guide ensures a smooth release process for the project. Update as needed!

