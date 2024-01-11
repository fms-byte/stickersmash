# To Publish apk from Expo App, run the following command:

```bash
npm install -g eas-cli
```

```bash
eas build --platform android --profile preview
```
## Create 'eas.json' file in the root directory of the project with the following content:
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