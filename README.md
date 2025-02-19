# Milo

## Table of contents 
- [Installation](#installation)

## Installation
### [Flutter Setup on Windows](#flutter-setup-on-windows) 
### [Flutter setup on MacOs](https://github.com/ShaikAbuAhmed/Ahmed-portfolio/blob/main/README.md#flutter-setup-on-macos-1)

## Flutter Setup on Windows
This guide provides step-by-step instructions to install Flutter and all necessary dependencies for developing mobile applications on a Windows system.

### Step 1: Download and Install Git
Flutter requires Git to be installed on your system. Follow these steps:
1. Visit the [official Git website](https://git-scm.com/download/win).
2. Download the appropriate version for your Windows system.
3. Run the installer and follow the default installation steps.
4. **Important:** Select **"Use Git and optional Unix tools from Command Prompt"** during installation.
5. Complete the installation and restart your system if necessary.

### Step 2: Download and Install Flutter
1. Go to the [official Flutter website](https://flutter.dev/).
2. Click on **Get Started** and select **Windows**.
3. Download the latest Flutter SDK as a ZIP file.
4. Extract the ZIP file and move the `flutter` folder to a directory (e.g., `C:\SRC\flutter`).

### Step 3: Add Flutter to System Path
1. Open the Windows search bar and type **"env"**, then select **"Edit the system environment variables"**.
2. Click **Environment Variables**.
3. Under **User Variables**, find and select the `Path` variable, then click **Edit**.
4. Click **New** and add the path to the Flutter `bin` folder (e.g., `C:\SRC\flutter\bin`).
5. Click **OK** and close all dialog boxes.
6. Restart your system or reopen the command prompt.

### Step 4: Verify Flutter Installation
1. Open **Command Prompt** and run the following command:
   ```sh
   flutter doctor ```
3. You should see Flutter and Windows options as [✅]
2. If you see errors, they may relate to missing dependencies such as the Android toolchain.

### Step 5: Install Android Studio
Flutter requires Android Studio for Android development:
1. Download Android Studio from the [official website](https://developer.android.com/studio).
2. Run the installer and follow the setup wizard.
3. **Ensure you install the Android Virtual Device (AVD) and Android SDK.**
4. Launch Android Studio and complete the setup wizard.

### Step 6: Configure Android SDK and Emulator
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

### Step 7: Final Verification
1. Open **Command Prompt** and run:
   ```sh
   flutter doctor
   ```
2. Ensure all checks [✅] are complete we are having an option to choose between Visual Studio and Android Studio So No worries if Visual studio Comes [❌].

### Conclusion
Your Windows system is now ready for Flutter development. You can create new Flutter projects and run them on an emulator or real device. For any issues, refer to the [official Flutter documentation](https://docs.flutter.dev/get-started/install/windows).

Happy coding!


## Flutter setup on MacOs
This guide provides step-by-step instructions to set up Flutter and the required tools for both Android and iOS development on macOS.

### Step 1. Install Git
Git is required for Flutter development. It is installed automatically with Xcode, but you can also install it separately:

```sh
xcode-select --install
```

For Apple Silicon (M1, M2, etc.), run the following command in the terminal:

```sh
sudo softwareupdate --install-rosetta --agree-to-license
```

### Step 2. Install Flutter SDK
1. Visit the [Flutter official website](https://flutter.dev/docs/get-started/install/macos).
2. Download the appropriate Flutter SDK version based on your Mac's architecture (Intel or Apple Silicon).
3. Extract the downloaded `.zip` file and move it to a preferred location, e.g., `~/Developer/flutter`.

### Step 3. Add Flutter to System Path
To permanently add Flutter to your system path:

1. Determine the shell you are using:

   ```sh
   echo $SHELL
   ```

2. Open the respective profile configuration file:
   - For `zsh` (default on macOS Catalina and later):
     ```sh
     nano ~/.zshrc
     ```
   - For `bash`:
     ```sh
     nano ~/.bash_profile
     ```

3. Add the following line (update the path accordingly):
   ```sh
   export PATH="$PATH:/Users/your-username/Developer/flutter/bin"
   ```
4. Save the file and apply changes:
   ```sh
   source ~/.zshrc  # or source ~/.bash_profile
   ```

5. Verify the installation:
   ```sh
   flutter --version
   ```

### Step 4. Install Xcode (for iOS Development)
1. Download and install Xcode from the Mac App Store.
2. Accept the Xcode license agreement:
   ```sh
   sudo xcodebuild -license
   ```
3. Install required command-line tools:
   ```sh
   sudo xcode-select --install
   ```
4. Verify Xcode installation:
   ```sh
   flutter doctor
   ```

### Step 5. Install Android Studio (for Android Development)
1. Download [Android Studio](https://developer.android.com/studio) and install it.
2. Open Android Studio and complete the setup wizard.
3. Install the required SDK components:
   - Open `SDK Manager` (from `More Actions` in the welcome screen).
   - Under `SDK Platforms`, install the latest Android SDK.
   - Under `SDK Tools`, install:
     - Android SDK Command-line Tools
     - Android Emulator
     - Android SDK Build Tools
     - Android SDK Platform Tools
4. Accept Android licenses:
   ```sh
   flutter doctor --android-licenses
   ```
5. Verify installation:
   ```sh
   flutter doctor
   ```

### Step 6. Setup iOS Simulator
1. Open Xcode.
2. Navigate to `Xcode` > `Settings` > `Components`.
3. Install an iOS Simulator.
4. Run an iOS simulator:
   ```sh
   open -a Simulator
   ```

### Step 7. Setup Android Emulator
1. Open Android Studio.
2. Go to `More Actions` > `Virtual Device Manager`.
3. Create a new device (e.g., Pixel 6).
4. Choose the latest Android version and install it if necessary.
5. Enable hardware acceleration (recommended):
   ```sh
   sudo sysctl -w hw.virtualization=1
   ```
6. Start the emulator:
   ```sh
   emulator -avd your_emulator_name
   ```

### Step 8. Verify Flutter Installation
Run the following command to check if everything is set up correctly:
```sh
flutter doctor
```
You should see checkmarks for Flutter, Xcode, Android Studio, and the required dependencies.

## Conclusion
Your Windows system is now ready for Flutter development. You can create new Flutter projects and run them on an emulator or real device. For any issues, refer to the [official Flutter documentation](https://docs.flutter.dev/get-started/install/macos/mobile-ios).

Happy coding!

