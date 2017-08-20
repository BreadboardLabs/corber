---
layout: page
title:  "Live Reload"
---

Live reload takes your frameworks standard serve/livereload behaviour to corber apps.

Live reload apps can still access Cordova plugins and work on emulators and physical devices.

**Caveats**

- Live reload is not for production environments. It is not a solution for delivering over the air updates in a production context.

- Your computer and phone/device must be on the same network.

#### Usage

```
  corber serve
  corber --environment=staging --platform=android
```

Some whitelisting may be required in config.xml, which corber will guide you create and tear down.

At a high level, this command builds a cordova container app, and then starts a slightly modified serve process.
Once serve is running, deploy the newly generated app to a device/emulator as explained in [build workflow](/pages/workflow/building).

Code changes should immediately resolve on your device. If you are having further troubles, you likely need to customize the device live-reload url.

#### Additional Android Steps

The whitelist plugin is also required for Android >4.0:
`corber plugin add cordova-plugin-whitelist`

#### Customize the device live-reload url

Livereload works by redirecting the cordova apps window.location from file://index.html to your locally running serve instance.
In general, we detect and automatically set these values for you.

There are times you may need to run live-reload from a remote host and port, or to customize a local url because we are not detecting it correctly.

In all cases below, `<url>` refers to the full url including protocol,
host, and port, e.g. http://localhost:4200


*via commandline arg*

```cli
corber serve --reload-url="<url>"
```

*via .ember-cli*

```json
  reloadUrl: "<url>"
```
