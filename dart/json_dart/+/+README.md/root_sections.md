## 🚀 Usage

### Bluring Key Fields

```dart
print({'api_key': '12345-my-key-value'}.blured());
```

```json
{api_key: ******************}
```

### Keepeing Significant Fields Only

```dart
const json = <String, dynamic>{
  'null': null,
  'false_bool': false,
  'ok': true,
  'zero_int': 0,
  'positive_zero_double': 0.0,
  'negative_zero_double': -0.0,
  'empty_string': '',
  'empty_list': <int>[],
  'empty_map': <String, dynamic>{},
  'empty_set': <int>{},
};
print(json.jsonWithSignificantFields);
```

```json
{ "ok": true }
```
