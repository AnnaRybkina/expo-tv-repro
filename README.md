# expo-tv-repro

## react-native-safe-area-context tvOS Bug Reproduction

This project demonstrates an issue with `react-native-safe-area-context` v5.3.0 on tvOS platforms. After the recent update that added new architecture support for macOS, tvOS applications using this package render as a blank white screen.

## How to run

```bash
npm install
npm run prebuild
npm run ios
```

## The Issue

When using `react-native-safe-area-context` v5.3.0 in a tvOS application:

- The app renders only a white screen
- No components are displayed
- No console logs appear, even when placed before any SafeAreaContext usage
- The application appears to crash during initialization

## Environment

- **react-native-safe-area-context**: v5.3.0
- **React Native**: npm:react-native-tvos@0.77.0-0
- **Platform**: tvOS
- **Device/Simulator**: Apple TV 4K

## Reproduction Steps

1. Clone this repository
2. Install dependencies with `npm install`
3. Run `npm run prebuild` to set up the native projects
4. Run `npm run ios` to launch on the tvOS simulator
5. Observe that the screen is blank/white with no rendered content

## Workarounds

```bash
npm install react-native-safe-area-context@5.2.0
```

## Related Information

This issue appears to be related to the new architecture support for macOS added in version 5.3.0. The problem specifically affects tvOS while other platforms continue to work as expected.
