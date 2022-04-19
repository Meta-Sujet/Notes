```dart
  final Function selectHandler;

  final VoidCallback selectHandler;

```

if the function you're passing around takes NO parameters, arguments (e.g. selectHandler won't receive any arguments, hence we use `VoidCallback`).