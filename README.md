# VocalFX

Releases of **VocalFX**, a real-time vocal effects app for Windows 10/11. Sing into your microphone and add
reverb, echo, EQ, compression, voice style (pitch and voice weight), double tracking and harmony live, hear
yourself on headphones with low latency, and send the processed voice to Discord, OBS or game voice chat through
a virtual audio cable. Music or a YouTube video from an app you choose can be sent along with your voice.
Basic and advanced modes, Korean and English.

## Download
Open the [latest release](../../releases/latest) and download `VocalFX-windows-<version>.zip`.

## Updates
The app includes an automatic update system.

Every time you open VocalFX it checks this repository for a new version. If there is one, it downloads it on
the start screen, verifies its checksum, installs it in the same folder and restarts into the new version, so your
shortcuts and taskbar pin keep working. If audio is already running the update waits for **Restart now** or the
next launch. You can turn this off in **Settings → Updates**.

`VocalFX-update-<version>.zip` is used by the automatic updater. You don't need to download it.

## Installation
1. Download `VocalFX-windows-<version>.zip`
2. Extract it to a folder you can write to (for example `Documents\VocalFX` or `D:\Apps`), not `Program Files`
3. Run `VocalFX\VocalFX.exe`

> Windows may show "Windows protected your PC" because the app isn't signed. Choose **More info** → **Run anyway**.

> Do not run the app directly inside the ZIP file. Extract it first.

### Using it in Discord / OBS
1. Install a virtual audio cable once, for example [VB-CABLE](https://vb-audio.com/Cable/) (donationware by VB-Audio; not bundled with VocalFX). Reboot after installing.
2. In VocalFX choose your microphone, your headphones (monitor output) and `CABLE Input (VB-Audio Virtual Cable)` (virtual mic output), pick the **Reference Live Vocal** preset and press **Start**.
3. In Discord → Voice & Video, set the input device to `CABLE Output (VB-Audio Virtual Cable)` and turn off Noise Suppression, Echo Cancellation and Automatic Gain Control, otherwise Discord removes the reverb and echo.
4. In OBS add an *Audio Input Capture* source with `CABLE Output (VB-Audio Virtual Cable)`.
5. Optional: under **Send app audio** pick the app playing music (for example the browser with YouTube) so Discord listeners hear it too. Discord's and VocalFX's own audio are never sent (needs Windows 11 or Windows 10 build 20348+).

## Notes
- Use headphones for monitoring: speakers feed your voice back into the microphone. Monitoring always starts off.
- Your voice is processed only on your PC. VocalFX doesn't record or upload audio and has no account or telemetry. The only network access is the update check against this repository.
- Settings and presets are kept in `%APPDATA%\VocalFX`.
- `VocalFXProbe.exe` is a command-line tool for checking audio devices (`VocalFXProbe --list`).

If you encounter a problem, please report it so it can be fixed in a future update.
