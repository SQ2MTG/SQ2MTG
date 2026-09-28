# MikroTik Discord Generator — Technical Reference

## Repository status

* GitHub repository: `SQ2MTG/MikrotikDiscordGenerator`
* Private repository
* Language: Python
* Default branch: `main`
* No license metadata declared
* Last push: 2025-07-30

## Function

A Python/Tkinter utility for generating MikroTik `/tool fetch` commands intended to send router status information to Discord.

The project is a command-generation tool rather than a router-side service. Exact generated command syntax and UI fields should be treated as source-verified implementation details.

## Integration

The architecture bridges:

1. MikroTik RouterOS command generation
2. Discord webhook-based status delivery

The generated RouterOS commands should be reviewed before deployment, especially when they contain URLs, headers or authentication parameters.

## Credentials

Repository source previously contained Discord-related credential material. This documentation intentionally omits all secrets. If any exposed credential was ever active, rotate it and move configuration to an external secret mechanism.

## Maintenance

Because this is a private, undated utility project with no declared license, preserve the repository's current internal-use context unless licensing and redistribution rights are established.
