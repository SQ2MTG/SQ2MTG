# Reminder Bot — technical reference

## Purpose

Reminder Bot is a historical private Python project for Discord reminders.

Repository metadata and previous source review indicate scheduled reminder scripts such as `reminder-today.py` and `reminder-tomorrow.py`, intended to be invoked by cron or another scheduler.

## Runtime model

The documented project model is simple:

`scheduler/cron → reminder script → Discord webhook/message delivery`.

The repository is old and does not currently expose a README in the default branch, so exact dependencies, webhook format and message templates should be treated as source-verification items.

## Security

Discord webhook credentials are sensitive. Any credential previously present in source/configuration must not be copied into this documentation. If an old webhook is still active, rotate it and move the replacement to protected runtime configuration.

## Status

Treat this as a historical project until the current source and deployment requirements are revalidated.
