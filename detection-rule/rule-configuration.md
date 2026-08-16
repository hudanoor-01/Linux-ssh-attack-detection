# Linux SSH Multiple Failed Logins Detection

## Purpose

Detect multiple failed SSH authentication attempts against a Linux host.

## Log Source

Linux authentication logs collected from `/var/log/secure`.

## Detection Logic

The detection rule monitors failed SSH authentication events and generates an alert when multiple failures occur.


## Detection Rule

Rule type: Threshold

Rule name:

Linux SSH Multiple Failed Logins

Severity:

Medium

The rule triggers when multiple failed SSH authentication events meet the configured threshold.

## Investigation Query

```text
event.category:"authentication" AND message:"Failed password"
