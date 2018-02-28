# Backup Android folders using rsync

## Installation

- Install Termux and Termux:API (e.g. from
  [F-Droid][https://f-droid.org/]).
- [Activate the storage in
  Termux][https://wiki.termux.com/wiki/Internal_and_external_storage].
- Install the dependencies `apt install rsync openssh jq`.
- Generate ssh key `ssh-keygen`.
- Copy ssh key to destination `ssh-copy-id user@host`.
- Copy `android-rsync-backup` (e.g in your home folder).
- Edit variables `src`, `dest` and `ssid` in `android-rsync-backup` script.

## Manual backup

Run the script from Termux: `~/android-rsync-backup` or add the script to homescreen
with Termux:Widget.

## Periodic backup with cron

- Activate cron `crond`
- Add `android-rsync-backup` to `crontab`
- Set `ACQUIRE WAKELOCK` for Termux

## Activate the backup using Tasker

See Termux:Task.
