## Motivation

1. We need to keep the file paths consistent in live cross-platform projects. I mean the dividers for Linux and Windows. I used to use [path](https://pub.dev/packages/path) extensively (thanks to the [authors](https://pub.dev/publishers/dart.dev/packages)), but we got some boilerplate with it.

2. **WFile** contains some abstractions, for ex. `Broker`, and its implementation: `text`, `image`, `xml` for `filesystem`. It helps to share data.

3. Many JSON files are very simple. I often use repetitive code to read them. You can now replace Dart's idioms with this line: `f.readAsJsonMap()` or `f.readAsJsonList()`.

4. Also when reading the image file, we can get the alpha channel guarantee if it is needed.

Additionally with **WFile** you can write just

```dart
f.writeAsImage(image, 'path/to.webp');
```

instead of

```dart
final encoder = findEncoderForNamedImage(p);
if (encoder == null) {
  throw Exception('Not found an encoder for file `$p`.');
}
final bytes = encoder.encode(image);
File(p).writeAsBytesSync(bytes);
```

Thanks [s00prtr00pr](https://reddit.com/user/s00prtr00pr).

## 🚀Usage

### Read Files

```dart
const sourcePath = 'path/prefix';
// const sourcePath = ['path', 'prefix'];
final f = WFile(sourcePath);

// get a varios content from files with respect to [sourcePath]
f.readAsText('text.txt');
f.readAsTextLines('lines.txt');            // <String>[...]
f.readAsBytes('bytes.bin');
f.readAsImage('images/1/happy.png');       // path/prefix/images/1/happy.png
f.readAsImage(['images', 1, 'happy.png']); // path/prefix/images/1/happy.png
f.readAsJsonMap('map.json');               // <- { ... }
f.readAsJsonList('list.json');             // <- [ ... ]
f.readAsXml('data.xml');                   // <- <data attr="...">...</data>
```

### Write Files

```dart
const sourcePath = 'path/prefix';
// const sourcePath = ['path', 'prefix'];
final f = WFile(sourcePath);

// get a varios content from files with respect to [sourcePath]
f.writeAsText(content, 'text.txt');
f.writeAsBytes(content, 'bytes.bin');
f.writeAsImage(content, 'images/1/happy.png');       // path/prefix/images/1/happy.png
f.writeAsImage([content, 'images', 1, 'happy.png']); // path/prefix/images/1/happy.png
f.writeAsJsonMap(content, 'map.json');               // { ... }
f.writeAsJsonList(content, 'list.json');             // [ ... ]
f.writeAsXml(content, 'data.xml');                   // <data attr="...">...</data>
```

### Copy Files

```dart
f.copy('path/source.file', 'path/destination.file');
```

You can use a relative path.

### Identify a File Type

```dart
final f = WFile('image.webp');

f.application(); // false
f.audio();       // false
f.binary();      // true
f.font();        // false
f.image();       // true
f.text();        // false
f.video();       // false
```

### Identify the MIME type

```dart
f.mime();  // image/webp
```
