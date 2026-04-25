# Privacy Policy

**Product:** Sheru desktop application
**Publisher:** AivionLabs
**Contact:** [hello@aivionlabs.com](mailto:hello@aivionlabs.com)
**Last updated:** 2026-04-25

---

## Summary

Sheru is a fully offline, local-first desktop application. **AivionLabs does not collect, receive, store, or process any personal data from your device.** Everything Sheru reads — your hardware, processes, mail, calendar, and files — stays on your machine.

---

## 1. What Sheru accesses locally

To provide its features, Sheru reads the following data on your device. None of this is transmitted to AivionLabs or any third party:

| Data category | What is accessed | Why |
|---|---|---|
| **System metrics** | CPU, memory, disk, network, temperature sensors, running processes | System monitoring and chat responses |
| **Network** | Local gateway, connected devices via ARP scan | Network awareness feature |
| **Mail** | Email content from Outlook, Apple Mail, Gmail, or IMAP | Mail summarisation and search |
| **Calendar** | Events from Outlook, macOS Calendar, or Google Calendar | Calendar queries |
| **Files** | File metadata and content | File search and open — only with explicit per-file user consent |
| **Bluetooth / USB** | Connected device names and identifiers | Device listing feature |
| **Audit log** | A record of actions taken by the agent | Stored locally at `~/.sheru/logs/`; never transmitted |

---

## 2. Third-party services

### 2.1 Gemini API (optional)

If you choose to use the Gemini fallback for natural language processing, queries are sent to Google's Gemini API using **your own API key**. AivionLabs does not act as an intermediary and does not see or store these queries. Refer to [Google's Privacy Policy](https://policies.google.com/privacy) for how Google handles API data.

### 2.2 Google OAuth (Gmail and Google Calendar)

If you connect Gmail or Google Calendar, Sheru initiates a standard OAuth 2.0 flow. The resulting access and refresh tokens are stored **only in your system keychain** (macOS Keychain, Windows Credential Manager). AivionLabs never receives, stores, or processes these tokens.

Sheru requests read-only OAuth scopes:
- `https://www.googleapis.com/auth/gmail.readonly`
- `https://www.googleapis.com/auth/calendar.readonly`

---

## 3. Data storage

All data Sheru produces or caches is stored locally on your device:

| Location | Contents |
|---|---|
| `~/.sheru/config.toml` | Auth token, user preferences |
| `~/.sheru/logs/` | Append-only audit log |
| System keychain | OAuth tokens (Gmail, Google Calendar) |

No data is synced to cloud storage, AivionLabs servers, or any external service.

---

## 4. Telemetry and analytics

Sheru contains **no telemetry, no analytics, and no crash reporting**. AivionLabs receives no information about your usage, errors, or behaviour.

---

## 5. AivionStudio pairing

Sheru supports optional pairing with AivionStudio via a 4-digit code (`POST /api/v1/pair`). This endpoint only accepts connections from `127.0.0.1` / `::1` (your own machine) and rotates the pairing code every 30 minutes. No data is transmitted outside your local network during pairing.

---

## 6. GDPR (European Users)

Because Sheru does not transmit personal data to AivionLabs, **AivionLabs does not act as a data controller or processor of your personal data** under the GDPR.

You, as the owner of your device, are the sole controller of data on it.

Your rights under GDPR that may be relevant:

- **Right of access:** All data is on your device — you can inspect it directly.
- **Right to erasure:** Uninstall Sheru and delete `~/.sheru/` to remove all locally stored data.
- **Right to portability:** Data in `~/.sheru/` is in plain TOML and text formats — readable and portable.

If you have GDPR questions or concerns, contact us at [hello@aivionlabs.com](mailto:hello@aivionlabs.com).

---

## 7. Children's privacy

Sheru is not directed at children under 13 (or under 16 in the EU). We do not knowingly collect any data from children.

---

## 8. Changes to this policy

We will post updates to this file in this repository with a revised date. For material changes, we will note them in the [Changelog](https://github.com/AivionLabs/sheru/blob/main/CHANGELOG.md).

---

## 9. Contact

**AivionLabs**
Email: [hello@aivionlabs.com](mailto:hello@aivionlabs.com)
Website: [aivionlabs.com](https://aivionlabs.com)
