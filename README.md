# Expo Linking.getInitialURL() Inconsistent null Return

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` API where it inconsistently returns `null` even when a deep link is used to launch the application.  This makes it challenging to reliably handle deep links during the app's initial launch.

## Problem Description

The `Linking.getInitialURL()` function is used to retrieve the initial URL that launched the app.  However, in certain scenarios, it returns `null` despite a deep link being successfully passed.  The randomness makes it difficult to identify root causes and implement robust error handling.  This issue prevents reliable deep-linking functionality within Expo applications.

## Reproduction

The `bug.js` file demonstrates the problematic behavior.  Running this app and opening it with a deep link, you'll see how `getInitialURL` may sometimes return null.

## Solution

The `bugSolution.js` file presents a potential workaround, utilizing a combination of `Linking.addEventListener` and additional checks to ensure reliable handling of initial URLs, mitigating the problem of `null` returns.

## Technologies Used

* Expo
* React Native
* Javascript