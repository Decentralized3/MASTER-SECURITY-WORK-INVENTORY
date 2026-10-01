# Android Application Security — Authorized Testing Record

> Target-specific operational details are intentionally omitted.

## Context

Android application security testing was performed against an in-scope mobile application in a Bugcrowd context.

## Objective

Move from static observations to dynamic validation of security-relevant Android components and behavior.

## Work performed

The work progressed through several stages:

1. Reviewed the APK through MobSF and decompiled application artifacts.
2. Examined the AndroidManifest and component exposure.
3. Enumerated activities/receivers and tested Intent/deep-link behavior with ADB.
4. Investigated selected broadcasts and application components.
5. Attempted runtime instrumentation with Frida.
6. Built a small Android Intent Sender application to test inter-application component invocation.

## What was actually demonstrated

The custom PoC built and ran. Attempts to invoke selected non-exported components produced the expected Android security restrictions rather than successful external access.

Frida attachment and process spawning were achieved, but some hooks failed because application context was not available at the time of the hook. A delayed approach was explored, but the recovered record does not establish a successful final data extraction.

## What was not established

The static analysis produced several candidate observations, including component exposure and configuration-related items. None of these are presented here as confirmed vulnerabilities because the recovered evidence does not establish exploitability and impact.

## What was learned

The work progressed from:

**static analysis → component enumeration → runtime instrumentation → custom IPC testing**

The important lesson was that a static security observation needs dynamic validation before it becomes a finding.

## Evidence

Recovered evidence includes MobSF material, decompiled classes, manifest/configuration files, ADB output, Frida output, build logs and the local PoC project.

## Publication status

The original target, decompiled application material, component identifiers and operational artifacts remain private. A genericized IPC testing example can be documented separately.
