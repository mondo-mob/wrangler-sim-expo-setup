## Expo for Wranglers

These instructions are for wranglers who wish to set up their MacBooks for running iOS and/or Android simulators with Expo Go and/or Expo Development Builds.


## Prerequisites

### Expo 

You'll need to create an Expo account at https://expo.dev and be granted access to any particular Expo/RN projects you want to run.

### Common setup

1. Install Xcode via the AppStore
2. Once completed, open Xcode. It will likely install more components.
3. Open a Terminal, you will be pasting a series of commands (below) into this terminal. You should wait for each command to complete before continuing. You'll know it's complete once you see the cursor again.
4. Install Homebrew 
```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
This command will prompt for a password. Enter the password of your current mac user. 
After installation Brew will likely ask you to run a couple of commands to add Brew to your path.
5. Install `n`
```shell
brew install n
```
6. Install node 16
```shell
sudo n 16
```
7. Install git
```shell
brew install git
```
8. Clone this repository somewhere appropriate, if you're not sure where just use your home directory
```shell
cd ~
git clone https://github.com/mondo-mob/wrangler-sim-expo-setup.git
```
9. Change directory into the repository that was cloned in the last step above. For example:
```shell
cd ~/wrangler-sim-expo-setup
```
10. Install NPM modules
```shell
npm i
```
11. Login to Expo
```
npx expo login
 ```
12. Configure XCode
    - Open Xcode and click on the Xcode --> Preferences menu
    - Click the `Locations` tab
    - If no `Command Line Tools` open is selected, click on the select dropdown to select one (there should be a single item in there to select)

### Android setup (if required)
1. Install Android Studio
```shell
brew install --cask android-studio
```
2. ... SDK setup, emulator installation etc ....

## Expo Go

This will install Expo Go onto a simulator/emulator.
Once installed you can open your project specific url.

### iOS Simulator

1. Start Expo
```shell
npm start:expo-go
```
2. Press `i` to open an iOS simulator and install Expo Go on it
3. Expo Go should be installed onto the simulator now. Open the simulator and paste your Expo project link into Safari, which should open your app.

You can switch devices using the `Simulators` menu.

### Android emulator

1. Start desired emulator from Android Studio

2. Download Expo Go apk file from https://expo.dev/tools

3. Drag apk file onto running simulator to install.

## Expo Development Builds

### iOS simulator

iOS Simulators require a specific simulator build to be created.
This must already be made created by the development team before running the steps below.

1. Configure application
   - Within app.json change the `owner` and `slug` properties to match the desired Expo project. 
2. Install simulator build
```
npx eas-cli build:run -p ios
```
3. If prompted `Existing EAS project found... Configure this project?` Choose `yes`.
4. Select the build you wish to install
5. (If prompted), select the simulator you wish to install onto
6. Once installed you can open the development build application on the simulator and then open the desired project url via the "Enter URL manually" option.

These steps can be repeated to install newer builds as required.

### Android simulator
1. Start desired emulator from Android Studio

2. Download desired Development build apk from Expo console.

3. Drag apk file onto running simulator to install.


