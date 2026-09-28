# Reminder Bot — Technical Reference

## Overview

A small Python automation project for sending scheduled Discord reminders for a recurring club day.

## Components

* `reminder-today.py` — sends the reminder for the current club day.
* `reminder-tomorrow.py` — sends the reminder for the following day.
* `crontab` — scheduling configuration.

## Message delivery

The scripts use Python `requests` to POST a Discord webhook payload containing:

* a reminder message mentioning `@everyone`;
* an embed title;
* an embed description with the meeting time and location.

The repository is therefore a simple webhook-based notification service rather than a persistent Discord bot.

## Scheduling

Execution is intended to be delegated to cron. The repository contains a ready-made `crontab` file.

## Security note

The current source contains a Discord webhook URL directly in the Python scripts. That credential should be considered exposed and rotated; future deployments should load it from an environment variable or another secret store.

## Source

Repository: `SQ2MTG/reminder-bot`
