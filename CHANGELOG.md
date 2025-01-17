# iProov Biometrics Flutter SDK

## 3.0.0

iProov SDK Biometrics Flutter SDK v3.0.0 is a major update which includes a number of improvements and breaking changes.

Please consult the [Upgrade Guide](https://github.com/iProov/flutter/wiki/Upgrade-Guide#upgrading-to-v30) for detailed instructions on how to upgrade to this new version.

### Flutter

* Cancelling all subscriptions to the `Stream<IProovEvent>` returned from `IProov.launch()` will now cancel any ongoing claim.
* `Options` has been overhauled to support the new SDK options in iOS v10 and Android v8 respectively.
* Fixed an issue where internal plugin errors would not be properly surfaced to the app.

### iOS

* Upgraded SDK to [v10.1.1](https://github.com/iProov/ios/releases/tag/10.1.1).
* Fixed an issue where custom fonts would crash on two consecutive launches.

### Android

* Upgraded SDK to [v8.1.0](https://github.com/iProov/android/releases/tag/v8.1.0).
* Fixed an issue where custom fonts would not be applied correctly.

### API Client

* Improved exception handling.
* The API Client now requires Dart 2.17+.

### Example app

* The example app now builds with sound null safety.

## 2.0.0

iProov SDK Biometrics Flutter SDK v2.0.0 is a major update which includes a number of improvements and breaking changes.

Please consult the [Upgrade Guide](https://github.com/iProov/flutter/wiki/Upgrade-Guide#upgrading-to-v20) for detailed instructions on how to upgrade to this new version.

### Flutter

* `IProov.launch()` now returns a `Stream<IProovEvent>` rather than using callbacks.
* `Options` are now built from `const` constructors rather than setting individual properties.
* Added comprehensive documentation to `Options`.
* Added the following new options, supported in the latest SDK versions:
  * `UiOptions.floatingPromptRoundedCorners`
  * `GenuinePresenceAssuranceUiOptions.readyFloatingPromptBackgroundColor`
  * `GenuinePresenceAssuranceUiOptions.notReadyFloatingPromptBackgroundColor`
  * `GenuinePresenceAssuranceUiOptions.readyOverlayStrokeColor`
  * `GenuinePresenceAssuranceUiOptions.notReadyOverlayStrokeColor`
  * `LivenessAssuranceUiOptions.floatingPromptBackgroundColor`
  * `LivenessAssuranceUiOptions.overlayStrokeColor`
* Fixed an issue where specifying custom certificates for pinning would result in a crash.

### iOS

* Upgraded SDK to [v9.5.0](https://github.com/iProov/ios/releases/tag/9.5.0).

### Android

* Upgraded SDK to [v7.5.0](https://github.com/iProov/android/releases/tag/v7.5.0).

### API Client

* The Dart API client is now provided as a separate module, `iproov_api_client`.
* Upgraded [http](https://pub.dev/packages/http) to v0.13.4.
* Added support for the `/validate` API call.

### Example App

* Fixed an issue where the Android example app wouldn't build due to an error relating to Android embedding.

## 1.1.1

### iOS

* Upgraded SDK to [v9.3.2](https://github.com/iProov/ios/releases/tag/9.3.2).

## 1.1.0

### iOS

* Upgraded SDK to [v9.3.1](https://github.com/iProov/ios/releases/tag/9.3.1).

### Android

* Upgraded SDK to [v7.3.0](https://github.com/iProov/android/releases/tag/v7.3.0).

## 1.0.0

We're pleased to announce that the iProov Biometrics Flutter SDK is now production-ready!

### Flutter

* Added `floatingPromptEnabled` to `UiOptions`.
* Renamed `footerTextColor` to `promptTextColor` in `UiOptions`.
* Removed `font` and `fontResource` from `UiOptions`. Use `fontPath` instead, which is now cross-platform.

### iOS

* Upgraded SDK to [v9.3.0](https://github.com/iProov/ios/releases/tag/9.3.0).
* Updated installation instructions for Cocoapods.
* Added support for custom fonts.

### Android

* Upgraded SDK to [v7.2.0](https://github.com/iProov/android/releases/tag/v7.2.0).
* Added support for custom fonts.

## 0.2.0

### Flutter

* All parameters to `IProov.launch()` are now named parameters.
* API key and secret for the Example app should now be set in `api_keys.dart`.
* Added `flutter_lints` dependency to package and example app.
* Added `headerBackgroundColor`, `footerBackgroundColor`, `headerTextColor` and `footerTextColor` to `UiOptions`.
* General improvements to the Example app.
* Improved coding style and formatting.
* Pinning certificates should now be passed as `List<int>` instead of `String` paths.

### iOS

* Upgraded SDK to [v9.2.0](https://github.com/iProov/ios/releases/tag/9.2.0).
* Passing certificates directly as `List<int>` is now supported.
* Error handling improvements.
* `closeButtonImage` is now supported.

### Android

* Upgraded SDK to [v7.1.0](https://github.com/iProov/android/releases/tag/v7.1.0).
* Passing certificates directly as `List<int>` is now supported.
* Error handling improvements.

## 0.1.0

Initial preview release

* iOS SDK [9.0.1](https://github.com/iProov/ios/releases/tag/9.0.1).
* Android SDK [7.0.3](https://github.com/iProov/android/releases/tag/v7.0.3).