# ScreenDim

Cordova/Phonegap plugin for enabling/disabling screen dim.

## Usage

````html
<script src="cordova.js"></script>
<script src="screendim.js"></script>
<script>
    // turn off the default screen dimming
    document.getElementById('turnoff').addEventListener('touchstart', function (e) {
        cordova.screenDim.disable();
    });

    // turn it back on
    document.getElementById('turnon').addEventListener('touchstart', function (e) {
        cordova.screenDim.enable();
    });

    // toggle it
    document.getElementById('toggle').addEventListener('touchstart', function (e) {
        cordova.screenDim.toggle();
    });
</script>
````

## Installation

```
cordova plugin add <this repo url>
```

## What/Why

Mobile devices typically have an idle timer - a time limit when the screen will
start to dim to conserve power.

By default this is a good thing - you don't want any old app keeping your screen
on and killing your power. However, in certain cases you may want to disable
this dimmer - for example, if you have a chess game where the user would be
expected to think about her move, without touching the screen, for some extended
period of time.

This plugin should be used for that purpose - disable the screen dimmer for some
part of your app, and enable it again once you're done.

## Supported Platforms

* iOS
* Android

## LICENSE

MIT

## Changelog

1.0.3 Update for cordova >= 3.6.x (Android)
1.0.2 Update for cordova >= 3.6.x (iOS)
1.0.1 Update for cordova 3.0.x (Android/iOS)
1.0.0 Initial release (Android/iOS)
