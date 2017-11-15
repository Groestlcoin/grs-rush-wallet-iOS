# GRSJS
An GRS wallet based on the JSWallet written in React Native.

## Dependencies
You will need to have Node.js, React Native and XCode installed to compile this app for iOS.

Follow the instructions here to get started:
https://facebook.github.io/react-native/docs/getting-started.html

## Initial setup
After you have installed react-native run the following commands from the project root.

npm install
yarn
react-native link react-native-qrcode-scanner
react-native link react-native-simple-toast
react-native link react-native-camera
react-native link react-native-torch

## Instructions
Before you compile the app you should always run the copyAssets script located in the root directory. This will copy asset files to the ios folder so it is bundled in the production builds. This is important if you have made changes to the src/assets/jswallet files.

To compile and test production build of the app you should run the following commands whilst standing in the Project folder:
react-native bundle --entry-file index.js --platform ios --dev false --bundle-output ios/main.jsbundle --assets-dest ios
./copyAssets
react-native run-ios --configuration Release

You can also run the app by opening the Xcode project in the ios folder.