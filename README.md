

# DO NOT USE - REDUNDANT
Expo Go .apk and .ipa files can simply me downloaded from https://expo.dev/tools


---



These instructions are for wranglers who wish to set up their MacBooks for running iOS and/or Android simulators with Expo Go installed on them.

You'll need to create an Expo account at https://expo.dev and be granted access to any particular Expo/RN projects you want to run. 

### Prerequisites / common setup

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
8. Clone this repository somewhere approriate, if you're not sure where just use your home directory
```shell
cd ~
git clone https://github.com/mondo-mob/wrangler-sim-expo-setup.git
```
9. Open Xcode and click on the Xcode->Preferences menu
10. Click the `Locations` tab
11. If no `Command Line Tools` open is selected, click on the select dropdown to select one (there should be a single item in there to select)

### Starting iOS simulator and Expo Go

1. Change directory into the repository that was cloned in the last step above. For example:
```shell
cd ~/wrangler-sim-expo-setup
```
2. Install NPM modules
```shell
npm i
```
3. Start Expo
```shell
npm start
```
4. Press `i` to open an iOS simulator and install Expo Go on it
5. Expo Go should be installed onto the simulator now. Open the simulator and paste your Expo project link into Safari, which should open your app.

You can switch devices using the `Simulators` menu.

### Android simulators setup

1. Install Android Studio
```shell
brew install --cask android-studio
```
2. ... SDK setup, emulator installation etc ....

### Starting Android simulator and Expo Go

As above but press `a` instead of `i` to open an Android simulator.

### Gotchas

... ?? copy/paste on Android

### Useful simulator shortcuts

... ?? reloading etc
