# Aatu Zhaatu - Flutter WebView App

A cross-platform Flutter application that wraps the Aatu Zhaatu website in a native mobile app. This app provides a seamless experience for accessing the website on Android, iOS, Windows, macOS, Linux, and web browsers.

---

## 📋 Table of Contents

- [Features](#features)
- [Supported Platforms](#supported-platforms)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Building & Running](#building--running)
- [Project Structure](#project-structure)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)

---

## ✨ Features

- **Cross-Platform Support**: Run on Android, iOS, Windows, macOS, Linux, and Web
- **WebView Integration**: Seamlessly embed the Aatu Zhaatu website using `webview_flutter`
- **Error Handling**: Graceful error messages when content fails to load
- **Loading States**: Visual feedback during page loading
- **Material Design**: Modern UI following Material Design 3 principles
- **JavaScript Support**: Full JavaScript execution for interactive website features
- **Android Debugging**: Built-in support for remote debugging via Chrome DevTools

---

## 🎯 Supported Platforms

| Platform | Status | Support Level |
|----------|--------|---|
| Android | ✅ | Full - Tested & Optimized |
| iOS | ✅ | Full |
| Windows | ✅ | Full |
| macOS | ✅ | Full |
| Linux | ✅ | Full |
| Web | ✅ | Full |

---

## 📦 Prerequisites

Before you begin, ensure you have installed:

- **Flutter SDK**: Version 3.3.0 or higher
  - [Download Flutter](https://flutter.dev/docs/get-started/install)
- **Dart SDK**: Included with Flutter
- **Platform Requirements**:
  - **Android**: Android SDK (API level 20 or higher) and Android Studio
  - **iOS**: Xcode 12.0 or later
  - **Windows**: Visual Studio 2019 or later (with C++ tools)
  - **macOS**: Xcode and CocoaPods
  - **Linux**: Required development libraries
  - **Web**: Any modern web browser

### Verify Installation

```bash
flutter --version
flutter doctor
```

---

## 🚀 Installation

### 1. Clone or Download the Project

```bash
# If using git
git clone <repository-url>
cd application_test

# Or extract the project folder
```

### 2. Install Dependencies

```bash
flutter pub get
```

This downloads all required packages listed in `pubspec.yaml`:
- `webview_flutter` (^4.9.0) - Core WebView functionality
- `webview_flutter_android` (^3.16.0) - Android-specific optimizations

### 3. Verify Setup

```bash
flutter doctor -v
```

Ensure all required components are installed for your target platform.

---

## ⚙️ Configuration

### Change the Website URL

To point the app to a different website, edit `lib/main.dart`:

```dart
// In the _WebsiteScreenState class
static const String _websiteUrl = 'https://your-website-url.com';
```

### Customize App Title

Update the app title in `lib/main.dart`:

```dart
title: 'Your App Title',  // Change from 'Aatu Zhaatu'
```

And in the AppBar:

```dart
title: const Text('Your App Title'),
```

### Customize Theme Colors

Modify the theme in `MyApp`:

```dart
colorScheme: ColorScheme.fromSeed(seedColor: Colors.blue), // Change color
```

---

## 🔨 Building & Running

### Run in Development Mode

```bash
# Android
flutter run -d <android-device-id>

# iOS
flutter run -d <ios-device-id>

# Web
flutter run -d chrome

# Windows
flutter run -d windows

# macOS
flutter run -d macos

# Linux
flutter run -d linux
```

### List Connected Devices

```bash
flutter devices
```

### Build Release Versions

```bash
# Android APK
flutter build apk --release

# Android App Bundle (for Play Store)
flutter build appbundle --release

# iOS
flutter build ios --release

# Windows
flutter build windows --release

# macOS
flutter build macos --release

# Linux
flutter build linux --release

# Web
flutter build web --release
```

---

## 📁 Project Structure

```
application_test/
├── lib/
│   └── main.dart              # Main app code with WebView setup
├── android/                    # Android-specific code
├── ios/                        # iOS-specific code
├── windows/                    # Windows desktop app code
├── macos/                      # macOS app code
├── linux/                      # Linux desktop app code
├── web/                        # Web build configuration
├── test/                       # Test files
├── pubspec.yaml               # Project dependencies
├── analysis_options.yaml      # Dart analysis settings
└── README.md                  # This file
```

---

## 🐛 Troubleshooting

### Android Issues

**Issue**: WebView blank or not loading

**Solution**:
```bash
flutter clean
flutter pub get
flutter run
```

**Enable Android Debugging**:
1. Connect Android device via USB
2. Enable USB Debugging on device
3. Run the app: `flutter run`
4. Open Chrome and go to `chrome://inspect` to debug

### iOS Issues

**Issue**: Pod installation fails

**Solution**:
```bash
cd ios
rm Podfile.lock
pod install
cd ..
flutter run
```

### General Issues

**App crashes on startup**:
```bash
flutter clean
flutter pub get
flutter pub upgrade
flutter run
```

**Version conflicts**:
```bash
flutter upgrade
flutter pub outdated
flutter pub upgrade
```

---

## 🔍 Key Features in Detail

### Loading State
The app displays a loading indicator while content is being fetched.

### Error Handling
If the website fails to load, users see:
- Error code and description
- Helpful error message
- Ability to navigate back

### Navigation
- Supports all user interactions on the website
- Back/forward buttons work within the WebView
- External links handled appropriately

### JavaScript Support
Full JavaScript execution is enabled for interactive website features.

---

## 📝 Development

### Adding New Features

1. In `_WebsiteScreenState`, modify the `WebViewController` configuration
2. Add new UI elements to the `build()` method
3. Test on multiple platforms: `flutter run -d <device>`

### Logging

Debug output is available via:
```bash
flutter logs
```

Look for `debugPrint()` messages in the console.

---

## 🤝 Contributing

To contribute improvements:

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Make your changes
3. Test on multiple platforms
4. Submit a pull request

---

## 📄 License

This project is licensed under the MIT License. See LICENSE file for details.

---

## 📚 Resources

- [Flutter Documentation](https://flutter.dev/docs)
- [WebView Flutter Package](https://pub.dev/packages/webview_flutter)
- [Material Design 3](https://m3.material.io/)
- [Dart Language Guide](https://dart.dev/guides)

---

## ✉️ Support

For issues or questions:
1. Check the [Troubleshooting](#troubleshooting) section
2. Review the [Flutter Documentation](https://flutter.dev/docs)
3. Check the [WebView Flutter Issues](https://github.com/google/webview_flutter/issues/)
