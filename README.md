Cordova Vue demo with hot reload

## Setup

```sh
yarn && cd frontend yarn

yarn dev
```
## Generate APK sign key

```sh
keytool -genkeypair -v -keystore ~/.android/key-123456.keystore -alias my-key-alias -keyalg RSA -keysize 2048 -validity 10000
```

## Reference

- https://segmentfault.com/a/1190000021499982
- https://github.com/nanogiants/cordova-plugin-hot-reload

