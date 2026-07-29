# ownCloud iOS + React Native

Experimental fork of [ownCloud iOS](https://github.com/owncloud/ios-app) testing brownfield
support for existing iOS codebases. Commits serve as reference for integrating
React Native without refactoring the project structure.

Uses Expo's brownfield isolated approach.

## Integration steps
1. **Create Expo app**: the React Native screen is prebuilt once in the shared [expo-brownfield-shared-ios](https://github.com/briones-agent/expo-brownfield-shared-ios) Swift Package (product `ExpoBrownfieldPackage`, module `ExpoBrownfieldKit`).
2. **Install expo-brownfield**: add the remote Swift Package to the `ownCloud` app target (init the `ios-sdk` submodule first).
3. **Integrate**: `ownCloud/ExpoIntegration.swift` adds a floating "Expo" button on an overlay `UIWindow` that presents `ReactNativeViewController(moduleName: "main")`; `AppDelegate` calls `ExpoIntegration.bootstrap()` at launch. iOS deployment target bumped to 16.4.

<details><summary>ownCloud iOS</summary>

# [ownCloud](https://owncloud.org) iOS App

## 📲 Download

Our iOS app is free for downloading available on the AppStore

<a href="https://apps.apple.com/app/id1359583808?itsct=apps_box_badge&amp;itscg=30200" style="display: inline-block; overflow: hidden; border-radius: 13px; width: 250px; height: 83px;"><img src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83&amp;releaseDate=1561593600" alt="Download on the App Store" style="border-radius: 13px; width: 250px; height: 83px;"></a>

####  🌎 https://ownCloud.com

| Account List                                                 | File List                                                    | File Actions                                                 | Preview Files                                                | Quick Access                                                 | Settings                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="doc/images/en-US/iPhone 11 Pro Max-11_ios_accounts_list_demo.png" alt="Simulator Screen Shot - iPhone 11 Pro"> | <img src="doc/images/en-US/iPhone 11 Pro Max-20_ios_files_list_demo.png" alt="Simulator Screen Shot - iPhone 11 Pro"> | <img src="doc/images/en-US/iPhone 11 Pro Max-21_ios_files_actions_demo.png" alt="Simulator Screen Shot - iPhone 11 Pro"> | <img src="doc/images/en-US/iPhone 11 Pro Max-22_ios_files_preview_pdf_demo.png" alt="Simulator Screen Shot - iPhone 11 Pro"> | <img src="doc/images/en-US/iPhone 11 Pro Max-40_ios_quick_access_demo.png" alt="Simulator Screen Shot - iPhone 11 Pro"> | <img src="doc/images/en-US/iPhone 11 Pro Max-60_ios_settings_demo.png" alt="Simulator Screen Shot - iPhone 11 Pro"> |

## 😍 Features

* 🦋 Using the current iOS frameworks
* ⭐️ Exclusively built for iOS
* 🛠 Written in Swift
* 📂 Seamless integration with iOS files for improved collaboration
* 🕹 Multi-select with drag and drop features for efficient file management
* 👑 Using iPadOS features for pro users
* ✅ Certificate management and password manager integration for boosting security
* 🏳️‍🌈 Multiple UI themes with dark and light colors
* 🚢 Free on the AppStore
* 🇪🇺 Localised in many languages
* 📱iOS 11+
* 🧩 License: [GPLv3](https://github.com/owncloud/ios-app/LICENSE)

## 🛠 Build our App

To build our App, please read our [SETUP.md](https://github.com/owncloud/ios-app/blob/master/SETUP.md)

```
$ read SETUP.md
```

## 📖 Documentation & Help

The documentation for the app can be viewed here: [iOS Documentation](https://doc.owncloud.com/ios-app/)

Support and help can be found here: [Docs & Guides](https://owncloud.com/docs-guides/)

## 🇪🇺 Translate

The App is translated in many languages. If your language is missing or if you want to improve a string, you are welcome!
This can be done in [Transifex](https://www.transifex.com/signup/?join_project=owncloud).


## 💡 Found a bug or have some ideas for improvement?

- 💬 Open a new issue on [Github](https://github.com/owncloud/ios-app/issues/new)
- 🐥 Don't forget to follow us on [Twitter](https://twitter.com/owncloud) 

## 📋 Start Contributing

Make sure you read [SETUP.md](https://github.com/owncloud/ios-app/blob/master/SETUP.md) when you start working on this project. Basically: Fork this repository and contribute back using pull requests to the master branch.
Easy starting points are also reviewing [pull requests](https://github.com/owncloud/ios-app/pulls) and working on [good first issue](https://github.com/owncloud/ios-app/labels/good%20first%20issue).

## ☁️ ownCloud Classic

[Learn](https://owncloud.org/news/how-to-set-up-an-owncloud-in-3-minutes/), how you can easily setup your own ownCloud server in 3 minutes or test our ownCloud iOS app with our demo server:

- [Download](https://apps.apple.com/app/id1359583808) our iOS App
- Add account 

### Demo credentials

| Server URL | demo.owncloud.com |
| ---------- | ----------------- |
| User       | demo              |
| Password   | demo              |



</details>
