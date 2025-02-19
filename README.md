# Milo
## Table of contents 
- [Installation](#installation)
## Installation
### [Flutter Setup on Windows](#Flutter Setup on Windows) 
### [Flutter setup on Macos](### Flutter Setup on Windows)
## Flutter Setup on Windows
This guide provides step-by-step instructions to install Flutter and all necessary dependencies for developing mobile applications on a Windows system.
## Step 1: Download and Install Git
Flutter requires Git to be installed on your system. Follow these steps:
1. Visit the [official Git website](https://git-scm.com/download/win).
2. Download the appropriate version for your Windows system.
3. Run the installer and follow the default installation steps.
4. **Important:** Select **"Use Git and optional Unix tools from Command Prompt"** during installation.
5. Complete the installation and restart your system if necessary.

## Step 2: Download and Install Flutter
1. Go to the [official Flutter website](https://flutter.dev/).
2. Click on **Get Started** and select **Windows**.
3. Download the latest Flutter SDK as a ZIP file.
4. Extract the ZIP file and move the `flutter` folder to a directory (e.g., `C:\SRC\flutter`).

## Step 3: Add Flutter to System Path
1. Open the Windows search bar and type **"env"**, then select **"Edit the system environment variables"**.
2. Click **Environment Variables**.
3. Under **User Variables**, find and select the `Path` variable, then click **Edit**.
4. Click **New** and add the path to the Flutter `bin` folder (e.g., `C:\SRC\flutter\bin`).
5. Click **OK** and close all dialog boxes.
6. Restart your system or reopen the command prompt.

## Step 4: Verify Flutter Installation
1. Open **Command Prompt** and run the following command:
   ```sh
   flutter doctor
3. You should see Flutter and Windows options as [✅]   ```
2. If you see errors, they may relate to missing dependencies such as the Android toolchain.

## Step 5: Install Android Studio
Flutter requires Android Studio for Android development:
1. Download Android Studio from the [official website](https://developer.android.com/studio).
2. Run the installer and follow the setup wizard.
3. **Ensure you install the Android Virtual Device (AVD) and Android SDK.**
4. Launch Android Studio and complete the setup wizard.

## Step 6: Configure Android SDK and Emulator
1. Open Android Studio and navigate to **More Actions > SDK Manager**.
2. Under **SDK Platforms**, select the latest stable Android version.
3. Under **SDK Tools**, ensure the following are selected:
   - Android SDK Build-Tools
   - Android SDK Platform-Tools
   - Android SDK Command-line Tools
4. Click **Apply** to install the selected tools.
5. Open **Virtual Device Manager** under **More Actions**.
6. In latest versions One Sample Model device comes bydefault if you need custom Virtual Device Follow mentioned below steps.
7. Click **Create Device** and select a device template (e.g., Pixel 6 or pixel fold).
8. Download and install the latest Android system image.
9. Select **Hardware** acceleration if available in latest Versions it comse Bydefault.
10. Click **Finish** to create the virtual device.
11. Start the emulator by clicking the **Play** button.

## Step 7: Final Verification
1. Open **Command Prompt** and run:
   ```sh
   flutter doctor
   ```
2. Ensure all checks are complete we are having an option to choose between Visual Studio and Android Studio So No worries if Visual studio Comes [❌].

## Conclusion
Your Windows system is now ready for Flutter development. You can create new Flutter projects and run them on an emulator or real device. For any issues, refer to the [official Flutter documentation](https://docs.flutter.dev/get-started/install/windows).

Happy coding!

## Flutter Setup on Windows
