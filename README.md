# Installing EC Time Tracker

Pick the section that matches your operating system. All downloads are on the
[Releases page](https://github.com/waqasajaz/attendance-and-time-tracking-releases/releases).

---

## macOS

> Works on Intel and Apple Silicon Macs.

1. Download the right `.dmg` for your Mac:
   - **Apple Silicon (M1/M2/M3/M4)** → `EC Time Tracker-<version>-mac-arm64.dmg`
   - **Intel** → `EC Time Tracker-<version>-mac-x64.dmg`

2. Double-click the `.dmg`, then drag **EC Time Tracker** into the **Applications** folder.

3. Open **Terminal** (Spotlight: `Cmd + Space` → "Terminal") and run:

   ```bash
   xattr -cr "/Applications/EC Time Tracker.app"
   ```

   This removes macOS's "downloaded from the internet" tag. You only need to run it once.

4. Open **EC Time Tracker** from the Applications folder or Launchpad.

### If you see "EC Time Tracker is damaged and can't be opened"

That means you skipped step 3. Run the `xattr` command above and try again.

---

## Linux (Debian / Ubuntu / Mint / Pop!\_OS)

1. Download `EC Time Tracker-<version>-linux-amd64.deb` from the Releases page.

2. Open a terminal in the folder where the file was saved (usually `~/Downloads`) and run:

   ```bash
   sudo apt install ~/Downloads/EC.Time.Tracker-*-linux-amd64.deb
   ```

   Enter your password when prompted.

3. Launch **EC Time Tracker** from the application menu, or run it from a terminal:

   ```bash
   ec-time-tracker
   ```

### Upgrading to a new version

Just install the new `.deb` the same way — `apt` will upgrade in place:

```bash
sudo apt install ~/Downloads/EC.Time.Tracker-*-linux-amd64.deb
```

### Uninstalling

```bash
sudo apt remove --purge ec-time-tracker
```

---

## Linux (any other distro — Fedora, Arch, openSUSE, etc.)

Use the AppImage. It runs anywhere without installation.

1. Download `EC Time Tracker-<version>-linux-x86_64.AppImage` from the Releases page.

2. Make it executable and run it:

   ```bash
   chmod +x ~/Downloads/EC*-linux-x86_64.AppImage
   ~/Downloads/EC*-linux-x86_64.AppImage
   ```

3. To integrate it into your app menu (optional), use a tool like
   [AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher) or
   move the file to `~/Applications` and right-click → "Add to favorites" in your file manager.

---

## Windows

1. Download `EC Time Tracker-<version>-win-x64.exe` from the Releases page.

2. Double-click the installer.

3. If Windows SmartScreen shows a blue "Windows protected your PC" dialog, click
   **More info** → **Run anyway**. (This appears because the build isn't yet signed
   with a code-signing certificate; the dialog will disappear once signing is set up.)

4. Follow the wizard: choose an install location → click **Install** → **Finish**.
   The app launches automatically.

### Upgrading

If EC Time Tracker is already running, close it first (right-click the icon in the
system tray → Quit, or end it in Task Manager). Then run the new installer.

### Uninstalling

Open **Settings → Apps → Apps & features**, find **EC Time Tracker**, click **Uninstall**.

---

## Troubleshooting

### macOS: app crashes immediately

Open Terminal and run:

```bash
"/Applications/EC Time Tracker.app/Contents/MacOS/EC Time Tracker"
```

Copy the output and report it as an issue.

### Linux: nothing happens when I click the icon

Run from terminal to see the error:

```bash
ec-time-tracker
```

### Windows: installer says "integrity check has failed"

The download is corrupt. Delete the `.exe` and re-download from the Releases page.
If it still fails, try a different browser or download via `curl`/`wget`.

---

## Getting help

If something doesn't work, please open an issue at
<https://github.com/waqasajaz/attendance-and-time-tracking-releases/issues>
with:

- Your OS and version (e.g. "macOS Sonoma 14.5", "Ubuntu 24.04")
- Which file you downloaded
- The exact error message or screenshot
