# SPDX-License-Identifier: MIT
# AGENTS.md — AI contributor guide for X-UI-Fronting-Pro

You touch people's servers as root. Be conservative.

## Hard rules

1. **Never break a working panel.** `bash -n` + `shellcheck -S error`
   clean. Prefer docs over code churn.
2. **Fail closed on downloads.** The bootstrapper must verify every fetched
   payload (non-empty + marker) before `exec`. Never weaken that gate.
3. **No secrets in repo.** No TLS keys, backup passphrases, configs,
   domains under management.
4. **Non-destructive is a promise.** Config merges keep unknown blocks;
   rollback must exist for every mutating menu action. Test the merge logic
   mentally — no live panel here.
5. **Honest fronting language.** SNI routing hides intent from local nets,
   not activity from providers. Never `unhackable / invisible / NSA-proof /
   most advanced`. The vs-3x-ui table states complementarity, not supremacy.
6. **Version-proof texts.** No hardcoded versions outside code constants;
   releases cut only by tag with canonical asset names. Keep MIT.

## Workflow

- Small diffs, verification noted per change.
- End every answer with: files changed, how to verify, open risks.
  If you cannot follow a rule, stop and ask the human.
