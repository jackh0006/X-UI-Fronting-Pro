# SPDX-License-Identifier: MIT
# X-UI Fronting PRO — Privacy Policy

This tool manages **your** server's HAProxy, certificates, and firewall.
It collects nothing for the author.

## What leaves the device

- **Package mirrors + Let's Encrypt** (cert automation): IP/packages,
  domain validation. Certificates are public in Transparency logs.
- **Upstream 3x-ui installer** (if you choose menu 12): fetched from its
  official source; review it there first.

## What stays local

- HAProxy configs, TLS private keys, encrypted backups, audit logs, UFW
  rules. Keep keys `0600`, backups encrypted, never commit or paste them.
- No analytics, no telemetry, no phone-home in `install.sh`.

## Operator notes

- Your VPS provider sees sizes/timing/destinations — fronting hides which
  domain clients meant from local networks, not activity from the provider.
- Backups are AES-256 **only with a strong passphrase you choose**; a weak
  one is the same as no encryption.

Questions: open an issue (no keys, no configs, no domains you operate).
