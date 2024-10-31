## 🚀 Usage

```dart
void initState() {
  super.initState();
  magic = MagicDraw();
  // init code, see `example/lib/main.dart`
}

late final MagicDraw magic;

Widget build(BuildContext context) => MaterialApp(
  home: Scaffold(
    body: SafeArea(child: magic),
  ),
);
```

[<img src="https://raw.githubusercontent.com/syrokomskyi/magic_draw/master/images/screenshots/1.gif" width="600"/>](https://raw.githubusercontent.com/syrokomskyi/magic_draw/master/images/screenshots/1.gif)
