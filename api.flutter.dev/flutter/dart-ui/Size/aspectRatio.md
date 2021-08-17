# aspectRatio property

> [double](https://api.flutter.dev/flutter/dart-core/double-class.html) aspectRatio

The aspect ratio of this size.

This returns the [width](https://api.flutter.dev/flutter/dart-ui/Size/width.html) divided by the [height](https://api.flutter.dev/flutter/dart-ui/Size/height.html).

If the [width](https://api.flutter.dev/flutter/dart-ui/Size/width.html) is zero, the result will be zero. If the [height](https://api.flutter.dev/flutter/dart-ui/Size/height.html) is zero (and the [width](https://api.flutter.dev/flutter/dart-ui/Size/width.html) is not), the result will be [double.infinity](https://api.flutter.dev/flutter/dart-core/double/infinity-constant.html) or [double.negativeInfinity](https://api.flutter.dev/flutter/dart-core/double/negativeInfinity-constant.html) as determined by the sign of [width](https://api.flutter.dev/flutter/dart-ui/Size/width.html).

See also:

- [AspectRatio](https://api.flutter.dev/flutter/widgets/AspectRatio-class.html), a widget for giving a child widget a specific aspect ratio.
- [FittedBox](https://api.flutter.dev/flutter/widgets/FittedBox-class.html), a widget that (in most modes) attempts to maintain a child widget's aspect ratio while changing its size.

## Implementation

```dart
double get aspectRatio {
  if (height != 0.0)
    return width / height;
  if (width > 0.0)
    return double.infinity;
  if (width < 0.0)
    return double.negativeInfinity;
  return 0.0;
}
```

