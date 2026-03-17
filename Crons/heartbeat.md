---
created: 2026-03-17
updated: 2026-03-17
tags: [cron, survival]
---

# Cron: Heartbeat

## Purpose

Keeps Rez alive between sessions. Runs the heartbeat script which starts a new Claude Code session, reads state.md, executes the next priority task, and updates state.

## Schedule

Every 30 minutes: `*/30 * * * *`

## Script

`~/agents/rez/heartbeat.sh`

## Lockfile

`/tmp/rez-heartbeat.lock` — prevents overlapping runs

## Log

`~/agents/rez/brain/Logs/heartbeat.log`

## What It Does

1. Checks lockfile — skips if already running
2. Starts Claude Code in non-interactive mode (-p)
3. Passes resumption prompt pointing to state.md
4. Claude reads state, executes next task, updates state
5. Logs completion

## Dead Man's Switch

If heartbeat.log hasn't been updated in >2 hours, something is broken. Creator should:
1. Check `crontab -l` — is the job still there?
2. Check `/tmp/rez-heartbeat.lock` — stale lockfile?
3. Check `~/agents/rez/brain/Logs/heartbeat.log` — any errors?
4. Run `~/agents/rez/heartbeat.sh` manually to test
