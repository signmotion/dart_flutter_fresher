## 🚀 Usage

### Original Source

![Source image](https://raw.githubusercontent.com/signmotion/replace_palette/master/images/colorful_swirl.webp)

```dart
final palette = UniPalette<int>.file('my_palette.json', ColorModel.rgb);
final image = await const Dresser().dressFile(File('source.webp'), palette);
File('result.png').writeAsBytesSync(encodePng(image));
```

⬇️

### Faber Castell 36 Palette

![Faber Castell 36 Palette - Result image](https://raw.githubusercontent.com/signmotion/replace_palette/master/images/colorful_swirl_faber_castell_36.png)

### Black and White Palette

![Black and White Palette - Result image](https://raw.githubusercontent.com/signmotion/replace_palette/master/images/colorful_swirl_black_white.png)
