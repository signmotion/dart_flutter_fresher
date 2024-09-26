## 🚀 Usage

### ImageProvider to UI Image

```dart
await AssetImage('1.jpg').uiImage
```

### Package Image to Widget Image

```dart
Image(...).widgetImage
```

### Any formatted raw bytes to Widget Image

```dart
bytes.widgetImage
```

### ImageProvider to PNG raw bytes

```dart
AssetImage('nature.webp').pngUint8List
```

Supports the image providers:

- `AssetImage`
- `FileImage`
- `MemoryImage`
- `NetworkImage`
- any providers from [pub.dev](https://pub.dev/packages?q=image+provider) inherited from `ImageProvider`

Can detect [all formats](https://github.com/brendan-duncan/image/blob/main/doc/formats.md) from the package [image](https://github.com/brendan-duncan/image).

See folders `example` and `test` for more use cases.

## 🔄 Available Converters

```dart
import 'dart:ui' as ui;
import 'package:flutter/widgets.dart' as widget;
import 'package:image/image.dart' as image;
```

|               | extension name  |     | image.Image | ui.Image | widget.Image | ImageProvider | Uint8List |
| ------------- | --------------- | --- | :---------: | :------: | :----------: | :-----------: | --------- |
| image.Image   | `imageImage`    |     |             |    ✅    |      ✅      |      ✅       | ✅        |
| ui.Image      | `uiImage`       |     |     ✅      |          |      ✅      |      ✅       | ✅        |
| widget.Image  | `widgetImage`   |     |     ✅      |    ✅    |              |      ✅       | ✅        |
| ImageProvider | `imageProvider` |     |     ✅      |    ✅    |      ✅      |               | ✅        |
| Uint8List     | `uint8List`     |     |     ✅      |    ✅    |      ✅      |      ✅       |           |

## 📸 Screenshots

[<img src="https://raw.githubusercontent.com/signmotion/flutter_image_converter/master/images/screenshots/1.webp" width="600"/>](https://raw.githubusercontent.com/signmotion/flutter_image_converter/master/images/screenshots/1.webp)
[<img src="https://raw.githubusercontent.com/signmotion/flutter_image_converter/master/images/screenshots/2.webp" width="600"/>](https://raw.githubusercontent.com/signmotion/flutter_image_converter/master/images/screenshots/2.webp)
[<img src="https://raw.githubusercontent.com/signmotion/flutter_image_converter/master/images/screenshots/3.webp" width="600"/>](https://raw.githubusercontent.com/signmotion/flutter_image_converter/master/images/screenshots/3.webp)

## 💛 Thanks

While working on projects, I meet people who make the project better with their outsider and professional view. I want to write down their names here..... and I'd be happy to add your name as well.

⭐ [C Davis aka faithoflifedev](https://github.com/faithoflifedev): [Support web platform](https://github.com/signmotion/flutter_image_converter/pull/1)

⭐ [eibaan](https://reddit.com/user/eibaan)
