---
layout: page
title:  "ember-cordova-platform"
---

#### Summary

This Ember service provides information about the current platform. Heavily inspired and partially forked from [Ionic Platform](http://ionicframework.com/docs/api/utility/ionic.Platform/).

#### Installation

```
ember install ember-cordova-platform
```

#### Service Name

```js
  Ember.inject.service('service:ember-cordova/platform');
```

#### API

|    | Description |
|----|-------------|
|navigator | proxy for window.navigator object|
|ua | proxy for window.navigator.userAgent object|
|platforms | array of all platforms found (e.g. WebView, iOS)|
|isHybrid | bool - is Cordova, PhoneGap or Crosswalk |
|isCordova | bool |
|isIPad | bool |
|isIOS | bool |
|isAndroid | bool |
|isWindowsPhone | bool|
|isEdge | bool|
|isCrosswalk | bool|
|platform | string. either ios, android, windowsphone, edge,
crosswalk or navigator.platform|
|version | number |
|device | proxy for window.device|
