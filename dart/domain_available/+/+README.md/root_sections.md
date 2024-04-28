## 🖥️ How It Works

Use [Instant Domain Search Check](https://instantdomainsearch.com) for check domain name.

## 🚀 Usage

### Check

```dart
final checked = await DomainAvailable('openai.com').firstRegisteredStatus();
print('The ${checked.domain} is ${checked.registeredStatus}.');
```

```text
> The openai.com is taken.
```

### Sanitize

```dart
print('https://www.happy.com/path_to/page'.sanitizeDomain);
```

```text
> happy.com
```
