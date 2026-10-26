# VocalFX

Releases of **VocalFX**, a real-time vocal effects app for Windows 10/11. Sing into your microphone and add
Krisp-class AI noise removal (DeepFilterNet 3), reverb, echo, EQ, compression, voice style (pitch, voice weight and auto-tune), double tracking and harmony live, hear
yourself on headphones with low latency, and send the processed voice to Discord, OBS or game voice chat through
a virtual audio cable. Music or a YouTube video from an app you choose can be sent along with your voice.
Basic and advanced modes, Korean and English. Closing the window keeps VocalFX running in the system tray.
PC sound removal cancels music, videos and Discord voices that leak from your headphones or speakers into the mic.

## Download
Open the [latest release](../../releases/latest) and download **`VocalFX-Setup-<version>.exe`** (installer).
`VocalFX-windows-<version>.zip` is the portable version.

## Updates
The app includes an automatic update system.

Every time you open VocalFX it checks this repository for a new version. If there is one, it downloads it on
the start screen, verifies its checksum, installs it in the same folder and restarts into the new version, so your
shortcuts and taskbar pin keep working. If audio is already running the update waits for **Restart now** or the
next launch. You can turn this off in **Settings → Updates**.

`VocalFX-update-<version>.zip` is used by the automatic updater. You don't need to download it.

## Installation
1. Download and run `VocalFX-Setup-<version>.exe`. It installs for your user only (no administrator rights), adds Start menu and desktop shortcuts and an uninstaller.
2. Keep **Install VB-CABLE** checked if you want to use VocalFX as a microphone in Discord / OBS. The installer downloads VB-Audio's official package, checks its signature and opens VB-Audio's own setup: click **Install Driver**, confirm the administrator prompt, and restart your PC once afterwards. (VB-CABLE is donationware by VB-Audio · www.vb-cable.com — donations are welcome.)
3. No Visual C++ Redistributable is needed.

> Windows may show "Windows protected your PC" because the installer isn't signed. Choose **More info** → **Run anyway**.

Portable: extract `VocalFX-windows-<version>.zip` to a folder you can write to (not `Program Files`) and run `VocalFX\VocalFX.exe`.

### Using it in Discord / OBS
1. Install a virtual audio cable once: the installer's VB-CABLE option, or [VB-CABLE](https://vb-audio.com/Cable/) by hand (donationware by VB-Audio). Reboot after installing.
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
