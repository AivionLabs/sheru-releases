# Security Policy

## Supported versions

| Version | Supported |
|---|---|
| 0.1.x (Beta) | Yes |

---

## Reporting a vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Email: [hello@aivionlabs.com](mailto:hello@aivionlabs.com)
Subject: `[SECURITY] Sheru — <brief description>`

Include:
- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Your name or handle (if you'd like credit in the release notes)

We aim to acknowledge reports within **48 hours** and will work with you on a coordinated disclosure timeline.

---

## Security model

Sheru runs a local FastAPI sidecar at `http://127.0.0.1:61209`. All endpoints (except `/api/v1/ping` and `/api/v1/healthz`) require the `X-Sheru-Token` header.

- The token is generated on first run and stored in `~/.sheru/config.toml` (mode `0600`).
- `POST /api/v1/pair` (AivionStudio pairing) is token-free but only accepts connections from `127.0.0.1` / `::1`.
- The pairing code rotates every 30 minutes.

**Network exposure:** The sidecar only binds to `127.0.0.1`. It is not accessible from other machines on your network.

---

## Scope

Security issues in the following areas are in scope:

- Authentication bypass on the local API
- Privilege escalation beyond the running user's permissions
- Unauthorised access to mail or calendar content
- OAuth token leakage

Out of scope: vulnerabilities in third-party dependencies (report to upstream), issues requiring physical access to the device.

---

## Known limitations

- The Python sidecar runs with your user's full filesystem permissions. It does not run in a sandbox.
- Mail and calendar connectors access credentials stored in the system keychain — protect your device login accordingly.
- File access requires explicit user consent per file, but the consent prompt is shown in the Sheru UI and could be missed if you are not paying attention.
