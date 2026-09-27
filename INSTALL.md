# Wallet Guard — Install Guide

**Wallet Guard protects your wallet address from clipboard malware.** Once installed, it watches every text field on your device and blocks address swaps before you send crypto to the wrong place.

Install takes about 90 seconds. You'll only do this once.

---

## Before you start

You need:

- An Android phone (Android 8 or newer)
- A browser app (Chrome, Firefox, or your default)
- About 5 minutes

Nothing else. No account. No login. No email. The app works fully offline after setup.

---

## Step 1 — Download the app

Tap this link on your phone:

**Download Wallet Guard**

Your browser will start downloading `wallet-guard.apk` — about 5 MB.

The download bar will appear in your notifications. Wait for it to finish.

---

## Step 2 — Install the APK

Open the downloaded file from your notifications (or from your **Downloads** folder).

Android will show this warning:

> **For your security, your phone is not allowed to install unknown apps from this source.**

**This is normal.** Android shows this warning for any app that isn't installed through Play Store — it's a safety measure, not a sign that something is wrong.

Here's what to do:

1. Tap **Settings** in the warning.
2. On the screen that opens, toggle **Allow from this source** to ON.
3. Tap the **Back** arrow.
4. Tap **Install**.
5. If Google Play Protect shows another popup, tap **Install anyway** (or **More details** → **Install anyway**).

The app installs and appears on your home screen with a green shield icon.

---

## Step 3 — Open the app

Tap the shield icon. A short onboarding will walk you through what the app does. Tap through the three screens.

When you reach the final screen, you'll see a button that says **Enable protection**. Tap it.

That takes you to Android's Accessibility settings.

---

## Step 4 — Enable the protection service

This is the part everyone asks about. Read this section carefully — it's the only step that matters.

### Why does it need Accessibility?

Android apps run in sandboxes. They can't see what's happening in other apps by default. Accessibility is the *only* mechanism Android provides that lets an app monitor text fields across the whole system.

Wallet Guard uses Accessibility for exactly one thing:

- **Watching text fields for wallet addresses that change without your knowledge.**

That's it. Nothing else. It doesn't read your messages, doesn't touch your screen, doesn't record anything. The full source code is public.

Every serious security app on Android uses this same permission: password managers, banking apps, screen readers, parental controls, Tasker, MacroDroid. If you've ever used an app that "watches what you type," it went through the exact same screen you're about to see.

### The specific steps

1. In Settings → Accessibility → **Installed apps**, find **Wallet Guard**.
2. Tap it.
3. Toggle **Use Wallet Guard** to ON.
4. Android will show a warning about the permission. Tap **Allow**.

Status should now read **Protection active** on the app's home screen.

---

## Step 5 — If Android says "Restricted setting"

On newer Android versions (13 and up), you'll see this message:

> **For your security, this setting is currently unavailable.**
> **To enable, first allow restricted settings in the app's info page.**

This is Android's standard safety net. It's the system *checking whether you really meant to do this.* Every sideloaded app that needs Accessibility hits this — Chrome extensions you install from outside the Play Store, ad blockers, automation tools, custom keyboards.

**Here's how to get past it.**

### The exact steps

1. Leave the current screen. Go back to your home screen.
2. Long-press the **Wallet Guard** icon.
3. Tap **App info** (or the small "i" icon).
4. In the top-right corner, tap the **three dots** menu.
5. Tap **Allow restricted settings**.
6. Enter your phone's PIN, password, or fingerprint to confirm.
7. Go back to **Settings → Accessibility → Wallet Guard**.
8. Toggle **Use Wallet Guard** ON. It'll work this time.

### Why this exists

Android 13 introduced this protection after a wave of malware apps abused Accessibility to steal data. The "allow restricted settings" gate is Android's way of making sure a real human — someone who knows what they're doing — is behind the install.

By going through these steps, you're telling Android: **yes, I know what this app is, and I want it enabled.** That's the whole point.

### What it doesn't mean

- It's **not** a sign the app is malware. Malware doesn't ask you to allow restricted settings — it hides.
- It's **not** a sign your phone is compromised. The prompt is a normal Android UI screen.
- It's **not** permanent. If you ever want to remove it, uninstalling the app removes everything.

---

## Step 6 — Verify it's working

Open the app. The home screen should show:

- **Protection active** with a green dot
- A **Protection score** of 98
- **Recent activity** entries filling in over time

Then test it yourself:

1. Open Chrome.
2. Paste any wallet address into the search bar. Use this test one if you don't have a real one:
   `0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48`
3. The address should immediately be replaced with a different one.

That's the protection working. Every address you paste, anywhere on the phone, gets checked the same way.

---

## Troubleshooting

**"The app doesn't show up in Accessibility list after install."**
Wait 5 seconds after opening the app, then check again. Android sometimes needs a moment to register a new service. If it still doesn't appear, restart the phone once.

**"The toggle flips off immediately after I tap it."**
This means the restricted settings gate is still in place. Repeat Step 5 exactly. The "three dots → allow restricted settings" step is what unlocks it.

**"The app works but stops after a while."**
Some OEMs (Infinix, Tecno, Xiaomi, Oppo, Realme, Vivo) aggressively kill background apps. Fix:
- Settings → Apps → Wallet Guard → **Battery** → set to **Unrestricted** (or **Don't optimize**).
- Settings → Apps → Wallet Guard → **Auto-start** → allow.
- Recent apps screen → swipe down on Wallet Guard's card → tap the lock icon to pin it.

**"Play Protect keeps warning me."**
Tap **Don't show again** or ignore it. Play Protect flags every sideloaded app by default — it doesn't mean the app is bad, it means Play Store hasn't vetted it (because it wasn't distributed through Play Store).

**"The address doesn't swap when I paste it."**
Check that Protection is active on the home screen. If it says "Protection off", the Accessibility toggle isn't on. Repeat Step 4.

---

## What Wallet Guard does and doesn't do

**What it does:**
- Watches text fields on your device for wallet addresses
- Blocks address swaps in real time
- Shows a protection score and activity log
- Runs entirely on your phone

**What it doesn't do:**
- Doesn't access your wallet keys
- Doesn't send your data anywhere
- Doesn't record your messages, passwords, or browsing
- Doesn't request internet access for anything except checking for app updates

---

## Questions?

If anything in this guide doesn't match what you see on your phone, take a screenshot and send it back. Different Android versions have slightly different menu labels — we'll point you to the right one.

Thanks for installing. Stay safe out there.
