## This is a simple React Native App that uses Expo to build and publish the app to Expo App Store.

## To Publish apk from Expo App, run the following command in Terminal:

### Install Expo CLI:
```bash
npm install -g eas-cli
```
### Create 'eas.json' file in the root directory of the project with the following content:
```js
{
  "build": {
    "preview": {
      "android": {
        "buildType": "apk"
      }
    },
    "preview2": {
      "android": {
        "gradleCommand": ":app:assembleRelease"
      }
    },
    "preview3": {
      "developmentClient": true
    },
    "preview4": {
      "distribution": "internal"
    },
    "production": {}
  }
}
```
### Login to Expo account:
```bash
eas login
```
### Check if you are already logged in:
```bash
eas whoami
```
### Build the app:
```bash
eas build --platform android --profile preview
```