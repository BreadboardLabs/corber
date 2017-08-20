---
layout: page
title:  "ember-cordova-statusbar"
---

#### Summary

This service provides functions to customize the iOS and Android status bar. Currently better beta.

#### Installation

```
ember install ember-cordova-statusbar
```

#### Usage

Service Name:

```js
Ember.inject.service('service:ember-cordova/statusbar');
```

#### API

| Name  | Description |
|---------|-------------|
|hide()| hide the status bar|
|show()| show the status bar|
|isHidden| bool|
|isVisible| bool|
