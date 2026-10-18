# NexSpeak Nightly

Nightly builds of the [NexSpeak](https://github.com/Duell10111/NexSpeak) desktop app, a
Discord-like Matrix client with voice and video calls.

This repository only holds the [releases](https://github.com/Duell10111/NexSpeak-nightly/releases);
the code, issues and discussions live in [Duell10111/NexSpeak](https://github.com/Duell10111/NexSpeak).
How to use the app is described in the [documentation](https://nexspeak.readthedocs.io), including a
page on [nightly builds](https://nexspeak.readthedocs.io/en/latest/nightly.html).

> [!WARNING]
> Nightlies are built automatically from `main` and are not tested by hand. Expect bugs. For
> everyday use, take a [stable release](https://github.com/Duell10111/NexSpeak/releases/latest).

## How nightlies are made

- A build runs at night only if the app changed since the last nightly and CI passed for that
  commit, so there is no new release on quiet days.
- Each release names the commit it was built from.
- Versions look like `0.1.1-nightly.20261018.42`: the next patch version, the build date and a run
  number. They sort above the last stable release and below the next one.
- Only the newest 7 nightlies are kept.

## Install

Download the file for your platform from the
[latest nightly](https://github.com/Duell10111/NexSpeak-nightly/releases):

| Platform | File |
|---|---|
| macOS (Apple Silicon and Intel) | `.dmg` |
| Windows | `.exe` |
| Linux | `.AppImage` or `.deb` |

**NexSpeak Nightly** installs next to the stable NexSpeak app: it has its own name, settings, login
and `nexspeak-nightly://` links, so both can run at the same time.

The builds are not signed yet ([details](https://nexspeak.readthedocs.io/en/latest/install.html#unsigned-builds)):

- macOS: Gatekeeper blocks the first start. Open it via System Settings → Privacy & Security →
  "Open Anyway", or run `xattr -dr com.apple.quarantine "/Applications/NexSpeak Nightly.app"`.
- Windows: SmartScreen warns; choose "More info" → "Run anyway".

## Updates

NexSpeak Nightly updates itself to the newest nightly from this repository (never during a call).
Stable installs never receive nightlies. On macOS, automatic updates only work once the builds are
signed; until then, install new nightlies by hand.

## Feedback

Please report bugs in the [main repository](https://github.com/Duell10111/NexSpeak/issues) and
mention the nightly version (shown in the release title).

## License

NexSpeak is licensed under the
[AGPL-3.0-or-later](https://github.com/Duell10111/NexSpeak/blob/main/LICENSE).
