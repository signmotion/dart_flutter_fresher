## Motivation

Sometimes we want to use nice packages from pub.dev on the CLI or server side.
But (sometimes) the needed package has dependencies on Flutter...

I created `pure_dart_ui` to address this injustice in a single line (see `Usage` section below).

## 🌟 Features

### Classes independed of the Flutter SDK

- `Color`
- `Offset`
- `Rect`
- `Size`

### Functions independed of the Flutter SDK

- `clampDouble`
- `lerpDouble`

## 🚀 Usage

Add the package `pure_dart_ui` to `pubspec.yaml` and import the library:

```dart
import 'package:pure_dart_ui/pure_dart_ui.dart';
```

Or, if you want to fix the error stream when you run `dart main.dart`, then replace the line

```dart
// replace this import and be happy
import 'dart:ui';
```

with the line above in the desired 3rd-party package.

Use the classes and functions in this package same way you used `Flutter dart:ui`.

In other words, you can create your own application or use a 3rd-party package with [dart:ui features](https://api.flutter.dev/flutter/dart-ui/dart-ui-library.html) based on a pure Dart, without depending on the Flutter SDK.

### Use `Color`

```dart
const color = Color(0xffa1b2c3);
```

## Similar Projects

- [universal_io](https://pub.dev/packages/universal_io)
  A cross-platform `dart:io`.
- [universal_html](https://pub.dev/packages/universal_html)
  A cross-platform `dart:html`.
