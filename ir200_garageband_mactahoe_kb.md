```markdown
# BOSS IR-200 + GarageBand Setup on macOS Tahoe
**Knowledge Base Article — Blues Rig Recording Setup**

Tested on: MacBook Air M4 · macOS Tahoe (26) · GarageBand 10.4.12 · IR-200 Driver v1.0.1

---

## Overview

This guide documents the exact steps required to get a BOSS IR-200 Amp & IR Cabinet Simulator working as a USB audio interface with GarageBand on macOS Tahoe. This setup is non-obvious because the IR-200 requires an Aggregate Device in macOS even though it is a full 4-in/4-out USB audio device — it will not appear as a selectable input on a GarageBand track without this step.

---

## Hardware & Software Required

- BOSS IR-200 Amp & IR Cabinet Simulator
- MacBook Air (Apple Silicon) running macOS Tahoe (26)
- USB-A to Micro-USB cable (data-capable — charge-only cables will not work)
- USB-C adapter/hub with an active (lit) button — **the button must be ON/lit** or the Mac will not recognise the IR-200
- GarageBand 10.4.12 or later
- BOSS IR-200 USB Driver v1.0.1 for macOS 14+ (download from boss.info/support)

---

## Step 1 — Set IR-200 USB Mode to VENDOR

Before anything else, confirm the IR-200 itself is configured correctly for Mac use.

1. Press **[MENU]** on the IR-200
2. Navigate to **SYSTEM → USB MODE**
3. Set to **VENDOR** (not GENERIC — GENERIC is for iOS only)

> This setting must be VENDOR or the Mac driver will not recognise the device, regardless of what else you do.

---

## Step 2 — Driver Installation

### Pre-install checklist
- Quit GarageBand and all other audio applications
- **Unplug the IR-200 USB cable from the Mac** — do not connect it until after the reboot
- If reinstalling: run the uninstaller first (found at Applications → BOSS → IR-200 Driver → Uninstaller), then reboot before installing fresh

### Install
1. Double-click **IR200_USBDriver14.pkg** to launch the installer
2. If prompted to allow access to your Downloads folder, click **OK**
3. If a security warning appears, go to **System Settings → Privacy & Security** and change "Allow apps downloaded from" to **App Store and identified developers**, then re-run the installer
4. When installation completes, click **Restart** — do not skip the reboot

### After reboot
1. Let the Mac fully load to the desktop
2. Make sure the USB-C adapter button is **ON/lit**
3. Plug the IR-200 USB cable into the Mac
4. Power on the IR-200
5. When the "allow USB device" popup appears, click **Allow** immediately — do not dismiss or delay this
6. Wait 10 seconds

### Verify driver is working
Go to **System Settings → Sound → Input** — IR-200 should appear as an input device. If it does not appear, try unplugging and replugging into a different USB port on the adapter.

> Note: At this stage the IR-200 will appear as an Input device only. It will NOT yet appear as an Output device in System Settings. This is normal — the Aggregate Device step below fixes this.

---

## Step 3 — Create an Aggregate Device in Audio MIDI Setup

macOS requires devices used simultaneously for input and output to be combined into a single Aggregate Device. Even though the IR-200 is a full 4-in/4-out device, GarageBand will not offer it as a track input unless this step is completed.

1. Open **Finder → Applications → Utilities → Audio MIDI Setup**
2. Click the **+** button at the bottom left
3. Select **Create Aggregate Device**
4. In the device list on the right, tick the checkbox next to **IR-200 only**
   - Leave MacBook Air Microphone unchecked
   - Leave MacBook Air Speakers unchecked
   - Your speakers are connected to the IR-200 hardware outputs — you do not want Mac speakers involved
5. Set **Clock Source** to **IR-200**
6. Confirm it shows **4 ins / 4 outs**
7. Double-click the name at the top and rename it **IR-200 Agg**

---

## Step 4 — Configure GarageBand

1. Open GarageBand
2. Go to **GarageBand → Settings → Audio/MIDI**
3. Set **Input Device** → **Aggregate Device** (or whatever you named it)
4. Set **Output Device** → **Aggregate Device**
5. Close Settings

### On your track
1. Select your audio track
2. At the bottom left, open the **Input** dropdown — IR-200 inputs will now appear
3. Select **Input 1** for mono or **Input 1/2** for stereo
4. Make sure the orange **Monitoring** button is lit
5. Check **System Settings → Privacy & Security → Microphone** and confirm GarageBand has microphone access enabled

### Verify signal
Pluck a string — you should see the level meter jump in GarageBand.

---

## Ongoing Use — Important Rules

These rules come directly from the BOSS driver documentation and must be followed every session:

- **Always connect IR-200 and power it on BEFORE opening GarageBand**
- **Never restart or sleep the Mac while IR-200 is connected** — disconnect USB first, reconnect after Mac has fully restarted
- **If Mac goes to sleep with IR-200 connected**, after waking: quit all audio apps, power cycle the IR-200, reconnect USB
- **Never disconnect USB during playback or recording** — may cause GarageBand or macOS to crash
- **If the IR-200 stops being recognised**, try unplugging and replugging into a different USB port
- **Never update macOS with IR-200 connected** — disconnect first, then update, then reinstall the driver after

---

## Why This Works This Way

The IR-200 is a full 4-in/4-out USB audio device. However, macOS will not present it as a GarageBand-selectable input unless it is also configured as an output device simultaneously. Rather than selecting MacBook speakers as the output (which routes audio to the wrong place), the correct solution is to create an Aggregate Device using IR-200 alone. This lets macOS treat it as a unified input/output interface, which GarageBand then accepts as a valid audio device. Your physical speakers remain connected to the IR-200 hardware outputs (TRS → RV-6 → Master Volume → Speakers) and are unaffected by this configuration.

---

## Troubleshooting

| Symptom | Fix |
|---|---|
| IR-200 not visible in System Settings | Check USB-C adapter button is ON/lit; try different USB port |
| IR-200 visible in Settings but not in GarageBand track input | Aggregate Device not set up, or GarageBand input/output not pointing to Aggregate Device |
| No signal in GarageBand meter | Check orange monitoring button is lit on track; check Input is set to IR-200 (not No Input); check GarageBand has Microphone access in Privacy & Security |
| Driver won't install | Set Privacy & Security → Allow apps from "App Store and identified developers"; Control-click installer and choose Open |
| IR-200 disappeared after Mac sleep | Quit GarageBand, power cycle IR-200, reconnect USB |
| IR-200 SYSTEM USB MODE must be VENDOR | Press MENU → SYSTEM → USB MODE → set to VENDOR |
```