<a id="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/sbeam-dev/sumigoe">
    <img src="imgs/sumigoe_4x.png" alt="Logo" width="300px">
  </a>

<h3 align="center">Sumigoe</h3>

  <p align="center">
      <img alt="CircleCI" src="https://dl.circleci.com/status-badge/img/circleci/LvQj2CqzhDWWNx8EgFaC2c/VsotN4jDBvVzNKRMRuvXZy/tree/main.svg?style=svg">
      <img alt="GitHub Release" src="https://img.shields.io/github/v/release/sbeam-dev/sumigoe">
    <br />
      Companion app for voice therapy/training
    <br />
    <a href="https://github.com/sbeam-dev/sumigoe/wiki"><strong>Documentation and FAQs</strong></a>
    <br />
  </p>
</div>


## Features

- **Real-time pitch and resonance (formants) tracking**
- **Live visualizations and statistics for your voice**
- **In-app recording and playback**
- **Cross-platform**: Supports Linux, Windows, macOS, and Android.
- **Fully local and private**: ML models are bundled with the app and all analysis runs locally, Internet is not needed at all.

## Getting Started

1. Go to the [releases page](https://github.com/sbeam-dev/sumigoe/releases/latest).
2. Download the file for your platform from the table below.

| Platform | File | Notes |
|---|---|---|
| Linux (Debian/Ubuntu) | `sumigoe_<version>_amd64.deb` | Requires Ubuntu 24.04+ or equivalent (glibc 2.39) |
| Linux (other distros) | `sumigoe_<version>_x86_64.AppImage` | Needs FUSE (`libfuse2` on most distros) |
| macOS (Apple Silicon) | `Sumigoe_<version>_aarch64.dmg` | Intel Macs are not supported yet |
| Windows | `Sumigoe_<version>_x64.msi` or `Sumigoe_<version>_x64-setup.exe` | `.msi` is smaller if Webview (Edge) is already installed |
| Android | `sumigoe_<version>_arm64-v8a.apk` | For Android phones |

After installing, grant the app **microphone** access when prompted.

### Note on installation warnings

Sumigoe's code-signing is not recognized by Apple/Microsoft/Google yet (For example, Apple developer ID requires a payment.), so your OS will show security warnings on Windows, macOS, and Android. This is expected for open-source apps. If you downloaded the file from the official [releases page](https://github.com/sbeam-dev/sumigoe/releases) and the checksum matches, it is safe to proceed.

See below for platform-specific guide:

<details>
<summary><strong>Windows</strong></summary>

When you run the installer, Windows may show <em>"Windows protected your PC"</em> (Microsoft Defender SmartScreen):

1. Click **More info**.
2. Click **Run anyway**.

</details>

<details>
<summary><strong>macOS</strong></summary>

On first launch, macOS may refuse to open the app with <em>"Sumigoe cannot be opened because it is from an unidentified developer"</em> or <em>"Sumigoe is damaged and can't be opened"</em> (the latter appears on newer macOS versions for unsigned apps downloaded from the internet):

1. Open the DMG and drag **Sumigoe** into **Applications**.
2. In Finder, **right-click (or Control-click) the app and choose Open**, then confirm **Open** in the dialog. You only need to do this once.
3. If macOS still reports the app as damaged, clear the quarantine flag in Terminal:
   ```sh
   xattr -cr /Applications/Sumigoe.app
   ```

</details>

<details>
<summary><strong>Android</strong></summary>

Because the APK is sideloaded (not from Google Play) and signed with a self-issued certificate:

1. Tap the downloaded APK. Android will ask to allow installs from that app (your browser or file manager): tap **Settings** and enable **Allow from this source**, then go back and tap **Install**.
2. Google Play Protect may warn that the app is unknown or ask to scan it. Choose **Install anyway** / **More details → Install anyway**.
3. On first launch, allow the **microphone** permission when prompted.

</details>

## Contributing

If you are not a developer, please use Github [discussions](https://github.com/sbeam-dev/sumigoe/discussions) for bugs, suggestions and experience sharing.

If you are a developer and would like to contribute, please post issues or PRs at [Tangled repository](https://tangled.org/superaidesu.tngl.sh/sumigoe-app).


## License

This project is licensed under Apache 2.0 license.
