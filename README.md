# osx-mojave-subpixel-enable
Apple’s macOS Mojave disables subpixel antialiasing, also known as font smoothing, by default. On a MacBook Air or a desktop Mac hooked up to a non-Retina display, upgrading will make your fonts look worse.

``` shell
defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO
```

Log out and log back in for your changes to take effect. Thanks to Dean Herbert for reporting this to us.

While subpixel font smoothing is disabled by default, you can re-enable it with a terminal command. There are four possible settings: 0 (disabled), 1 (light smoothing), 2 (medium smoothing), and 3 (heavy smoothing).

``` shell
defaults -currentHost write -globalDomain AppleFontSmoothing -int {0,1,2,3}
```
