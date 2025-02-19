# React Native Dimensions API Width Issue on Android

This repository demonstrates a bug where the `Dimensions` API in React Native returns 0 or an incorrect width value for the screen on Android devices. The issue is intermittent and might not always be reproducible on demand.

## Bug Description
The `Dimensions.get('window').width` or `Dimensions.get('screen').width` methods sometimes return 0 or a value that doesn't match the actual screen width. This leads to layout problems and unexpected behavior in the application.

## How to Reproduce
1. Clone this repository.
2. Run the app on an Android emulator or device.
3. Observe the console logs and the layout of the app. Note that the incorrect width issue is not guaranteed to occur every time you run the app.

## Solution
The provided solution uses a combination of event listeners and state updates to ensure the correct dimensions are available before rendering components that depend on the screen dimensions. This solution can reduce the chances of the app rendering with an incorrect width.