## 🚀 Usage

By default the package uses `https://source.unsplash.com` as source of images.

### Get an image

```dart
// get an image generator
final images = Images(keywords: ['castle']);

// generate an image
final image = await images.next;

// save the generated image as PNG file
const file = 'example_image.png';
final encoder = findEncoderForNamedImage(file)!;
final bytes = encoder.encode(image);
File(file).writeAsBytesSync(bytes);

```

![Output Castle - Thematic Images](https://raw.githubusercontent.com/signmotion/thematic_images/master/images/example_image.png)
