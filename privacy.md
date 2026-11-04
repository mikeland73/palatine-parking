---
title: Privacy Policy
---

_Last updated: November 4, 2026_

This app is a Bluetooth client for the parking lift/garage controllers at the
Palatine building. It is designed to work entirely on your device.

## What we collect

**Nothing.** The app has no servers, no accounts, no analytics, and no
advertising SDKs. It makes no network requests of any kind — all communication
is Bluetooth Low Energy, directly between your device and the parking
controller in front of you.

## What stays on your device

- **Parking spot credentials.** When you scan (or paste) the QR code for your
  parking spot, the app decrypts it on-device and stores the resulting
  credential in the operating system's secure credential store — the **iOS
  Keychain** or the **Android Keystore** (via `expo-secure-store`). It is never
  transmitted anywhere except to the parking controller over Bluetooth, and
  only when you press a button to open, request, or close.
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

The app is not directed at children and collects no data from anyone.

## Third parties

There are none. No data is shared with, or sold to, anyone.

## Changes

If this policy changes, the updated version will be posted at the same link,
with a new "last updated" date.

## Contact

Questions: mikeland86@gmail.com
