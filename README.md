# Sheru — Releases

This repository hosts the official binary releases of **Sheru**, the offline desktop agent by [AivionLabs](https://aivionlabs.com).

> **Product page:** [aivionlabs.github.io/sheru-releases](https://aivionlabs.github.io/sheru-releases)
> **Source code:** [github.com/AivionLabs/sheru](https://github.com/AivionLabs/sheru)

---

## What is Sheru?

Sheru is a local desktop agent that monitors your machine and lets you talk to it in plain language. It reads your hardware, processes, network, mail, and calendar — all locally, all private. No cloud. No API keys. No telemetry.

Named after a loyal Bangla watchdog.

---

## Download

Binaries are published here as releases become available. Find the folder for your platform:

| Platform | Folder | Status |
|---|---|---|
| macOS (Apple Silicon + Intel) | [`macOs/`](./macOs/) | Beta |
| Windows 11 | [`Windows/Windows11/`](./Windows/Windows11/) | Planned |
| Linux | [`Linux/`](./Linux/) | Planned |

> **Beta access:** Sheru is currently in closed beta. If you received an invite, download instructions are in your invite email.

---

## Installation

### macOS

1. Download the `.dmg` file from the [`macOs/`](./macOs/) folder (latest version).
2. Open the DMG and drag **Sheru.app** to your Applications folder.
3. Launch Sheru from Applications.
4. On first launch, macOS may ask for accessibility and mail permissions — these are required for local monitoring.

### Windows

Coming in a future release. See [github.com/AivionLabs/sheru](https://github.com/AivionLabs/sheru) for progress.

---

## Privacy

Sheru is built on a single principle: **your data never leaves your machine.**

- No telemetry, no analytics, no crash reporting
- Mail and calendar content is read locally and never transmitted
- OAuth tokens (Gmail, Google Calendar) are stored in your system keychain
- All configuration and logs are kept in `~/.sheru/` on your device

See the full [Privacy Policy](./PRIVACY.md) for details. For GDPR inquiries, contact [hello@aivionlabs.com](mailto:hello@aivionlabs.com).

---

## Security

To report a vulnerability, **do not open a public issue**. Email [hello@aivionlabs.com](mailto:hello@aivionlabs.com) with subject `[SECURITY] Sheru — <description>`.

See [SECURITY.md](./SECURITY.md) for the full disclosure policy.

---

## License

Sheru is licensed under the [MIT License](https://github.com/AivionLabs/sheru/blob/main/LICENSE).

Built by [AivionLabs](https://aivionlabs.com).
