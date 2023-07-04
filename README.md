# Jailbreak/Root Detection Bypass in Flutter

This script is designed to bypass security checks that are implemented using the IOSSecuritySuite module in iOS applications and Rootbear in Android Application. For iOS, it intercepts two exported functions, one that checks if the device is jailbroken and the other that checks if the code is running in an emulator, and modifies in the runtime to bypass these checks. 

## How to Use

**Prerequisites**

- Frida needs to be installed on the device or emulator where the application is running.

**Steps**

1. Start the application on the device or emulator where Frida is installed.
2. Launch the terminal on your computer and navigate to the directory where the script is located.
3. Ensure frida can communicate with the device by running the following command:`frida-ps -Uai`
4. Load the script by running the following command:`frida -U -l flutter-jb-bypass-ios-short.js <process_name/app_name>`
5. Wait for the script to intercept the exported functions and modify in the runtime. A success message will be displayed once bypassed.

**To-Do**

- [ ]  Frida script to bypass Rootbeer root detection checks in Android (Work in progress)
