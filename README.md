# RSub1-iOS-App

This is a PoC-implementation of the RSub1-App using the Nearby Messages library. It shares your presence (as an anonymous name) with nearby devices, and displays names from nearby devices. It continues to work in the background using BLE; it uses audio only in the foreground.

The repo is a fork of this [googlesamples](https://github.com/googlesamples/ios-nearby/tree/master/messages/NearbyBackgroundExample) repo.

## Prerequisites

### Xcode

[Xcode][xcode] is the IDE of choice for most iOS developers, and the only one officially supported by Apple. There are some alternatives, of which [AppCode][appcode] is arguably the most famous, but unless you're already a seasoned iOS person, go with Xcode. Despite its shortcomings, it's actually quite usable nowadays!

To install, simply download [Xcode on the Mac App Store][xcode-app-store]. It comes with the newest SDK and simulators, and you can install more stuff under _Preferences > Downloads_.

[xcode]: https://developer.apple.com/xcode/
[appcode]: https://www.jetbrains.com/objc/
[xcode-app-store]: https://itunes.apple.com/us/app/xcode/id497799835

### CocoaPods

This workspace includes external dependencies, so in order to install them [CocoaPods][cocoapods] offers easy and fast integration. Install it like so:

    sudo gem install cocoapods

After installing cocoapods, you run

    pod install

to retrieve the external dependencies.

After this step you can open the Xcode workspace. Make sure to always open the Xcode workspace instead of the project file when building your project.

    open App.xcworkspace

### Google Nearby Messages API Key

To use the Nearby Messages API you need a Google Nearby Messages API Key.

1. In your [Google Developers Console](https://console.developers.google.com),
 1. Enable the Google Nearby Messages API.
 1. Create an API key for iOS, and enter your app's bundle ID.
1. Insert your API key into `AppDelegate.m`.

### Xcode-Project

In order to build and run the app on a test device you need to do some extra things:

- Insert a bundle ID into your target's settings (select the project in the Project Navigator, select the target, select the General tab, and insert your bundle ID into the Bundle Identifier field).
- Select a developer certificate (select the project in the Project Navigator, select the target, select the General tab, and select a certificate from your developer account. Maybe you need a paid developer account for this to work).

