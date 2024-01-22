# React-Native Maestro Application Setup Documentation

## Developer Information
- **Name:** Ammaar Sohail
- **Roll no:** 2029207
- **Email-id:** ammaarsohail19@gmail.com

## Introduction

This documentation provides a step-by-step guide to set up a React-Native Maestro application. The process includes installing Node.js, configuring the React Native environment, setting up Visual Studio Code, Android Studio, and configuring WSL2 for Android development.

## Prerequisites

Ensure the following are installed on your computer before proceeding:

1. **Node.js and npm (Node Package Manager)**
2. **React Native environment**
3. **Visual Studio Code (VS Code)**
4. **Android Studio**

## Step 1: Setting Up Node.js and npm

1. **Install Node.js and npm:**
   - Visit the Node.js official website.
   - Download and run the installer.
   - Follow the installation instructions.

2. **Verify Installation:**
   - Open a terminal or command prompt.
   - Run the commands: `node -v` and `npm -v`.
   - Ensure version numbers are displayed.

## Step 2: Setting Up React Native Ignite Environment

1. **Install React Native CLI:**
   - Open a terminal.
   - Run: `npm install -g react-native-cli`
   - Run: `npm install -g react-native-ignite`

2. **Create Ignite application:**
   - Run: `Ignite new MyApp`
   - Check connection with the simulator: `npm start`
  
     ![WhatsApp Image 2024-01-22 at 05 30 41_d3571edd](https://github.com/Ammaar19/Midas_2029207/assets/117352598/f66d1c97-6822-499e-81f7-4885859b9038)


## Step 3: Setting Up Maestro

1. **Install WSL2 for Windows:**
   - Open a terminal.
   - Run: `wsl --install`
   - Follow on-screen instructions and restart the computer.

2. **Install JAVA:**
   - After restarting, open the WSL2 terminal.
   - Run: `sudo apt install openjdk-11-jdk`

## Step 4: Android Setup in WSL2

- Download Android command line tools zip from the official site.
- Set up tools in WSL2 using provided commands.
- Update `~/.bashrc` with necessary environment variables.
- Install basic Android utilities and platform tools.

## Step 5: Install and Use Maestro

- Install Maestro with: `curl -Ls "https://get.maestro.mobile.dev" | bash`
- Check Maestro version: `maestro --version`
- Configure ADB in WSL2.
- Write your first Maestro code using provided examples.

## Writing Your First Maestro Code

Refer to the official documentation for sample flows and test commands [here](https://maestro.mobile.dev/getting-started/run-a-sample-flow).

To run a sample application:
```bash
Maestro download-samples
cd ./samples
adb install sample.apk
maestro test android-flow.yaml
```

For a custom application, use the provided sample code and modify as needed.

```yaml
#flow: Login
#intent:
# Open up our app and use the default credentials to login
# and navigate to the demo screen

appId: com.midas
---
- clearState
- launchApp
- assertVisible: "Sign In"
- tapOn:
    text: "Tap to sign in!"
- assertVisible: "Your app, almost ready for launch!"
- tapOn:
    text: "Let's go!"
- assertVisible: "Components to jump start your project!"
```

For opening Wikipedia through Maestro:
```bash
maestro test wiki-flow.yaml
```

**Result:**
The WSL Terminal should display successful results, and the emulator should reflect the expected behavior.
![image](https://github.com/Ammaar19/Midas_2029207/assets/117352598/cb63c9c5-d9bb-4afc-9793-14753f536118)

![image](https://github.com/Ammaar19/Midas_2029207/assets/117352598/0687dd42-867d-428d-913c-0ce1b11baf75)

#Feel free to explore further in the provided documentation and customize your Maestro application.
