---
title: Privacy Policy
---

_Last updated: November 18, 2026_

This app is a Bluetooth client for the parking lift/garage controllers at the
Palatine building. It is designed to work entirely on your device.

## What we collect

**Crash reports and anonymous diagnostics — nothing else.** The app has no
accounts, no analytics, and no advertising SDKs. Talking to the parking
controller is all Bluetooth Low Energy, directly between your device and the
controller in front of you. The only network traffic is crash and diagnostic
reporting to [Sentry](https://sentry.io), which we use to find bugs and make
opening and closing the gate more reliable:

- **Crash reports.** If the app crashes or hits an unexpected error: the stack
  trace, app version, device model, and operating-system version.
- **Gate-operation diagnostics.** For each open / request-space / close: which
  action it was, whether it succeeded, how many attempts it took, how long each
  step took, the category of any failure (for example "connection timed out" or
  "controller reported maintenance mode"), the controller's status codes, the
  Bluetooth signal strength, and an identifier for the controller (a hash that
  identifies the building's controller, not you).
- **Performance data** about app start-up and screen loading.

These reports are tied to a random identifier for this installation of the
app, not to your name, email, phone number, or any account. They never include
your parking credentials, the gate PIN you type, the QR code, the names you give
spots or controllers, your location, or screenshots or recordings of the
screen. Reports are kept by Sentry for at most 90 days.

## What stays on your device

- **Parking spot credentials.** When you scan (or paste) the QR code for your
  parking spot, the app decrypts it on-device and stores the resulting
  credential in the operating system's secure credential store — the **iOS
  Keychain** or the **Android Keystore** (via `expo-secure-store`). It is never
  transmitted anywhere except to the parking controller over Bluetooth, and
  only when you press a button to open, request, or close. It is never included
  in crash or diagnostic reports.
- **Controller names and preferences.** Any names you assign to discovered
  controllers, and which ones you have disabled, are stored locally.
- **Debug log.** The in-app debug console keeps a record of the bytes exchanged
  with the controller for the current session. It is shown only to you and is
  not uploaded.

You can remove all of this at any time by deleting the spot in the app, or by
deleting the app.

## Permissions the app asks for

| Permission | Why |
|---|---|
| **Bluetooth** (on Android, "Nearby devices") | To find and talk to your parking controller. This is the entire function of the app. |
| **Camera** | To scan the parking QR code when adding a spot. Frames are processed on-device for QR detection and are never stored or transmitted. |

The app does not ask for location. Android historically required a location
permission for any Bluetooth scan; this app declares that its scans are never used
to derive your location, so on Android 12 and later no location permission is
requested at all. On Android 11 and older the system still requires one to return
Bluetooth scan results — it is used for nothing else, and no location is read,
stored, or transmitted.

## Children

The app is not directed at children and collects no personal data from anyone.

## Third parties

Crash reports and diagnostics are processed by **Sentry** (Functional Software,
Inc.) on our behalf, only to operate and improve this app; see
<https://sentry.io/privacy/>. Nothing is shared with, or sold to, anyone else,
and nothing is used for advertising or tracking.

## Changes

If this policy changes, the updated version will be posted at the same link,
with a new "last updated" date.

## Contact

Questions: contact@canarialabs.com
