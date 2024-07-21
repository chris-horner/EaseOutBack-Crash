# EaseOutBack Crash Demo

[EaseOutBack](https://developer.android.com/reference/kotlin/androidx/compose/animation/core/package-summary#EaseOutBack()) easing throws

```
java.lang.IllegalArgumentException: The cubic curve with parameters (0.34, 1.56, 0.64, 1.0) has no solution at 0.99999994
```

in tweens where the duration is 1700ms or longer. This began some time after `1.7.0-alpha01` for `androidx.compose.animation:animation-core`.

Most likely caused by [this change](https://android-review.googlesource.com/c/platform/frameworks/support/+/2844994), this project serves as a simple reproduction of the crash.