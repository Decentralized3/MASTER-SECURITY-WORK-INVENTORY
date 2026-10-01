# Android Intent Sender — PoC

## Context

During authorized Android testing, ADB was not sufficient for reproducing an application-specific inter-application Intent test.

## Objective

Build a small Android application that could construct and send explicit Intents from a separate application context.

## Work performed

The PoC was developed in Android Studio using Java and the Android build system.

The application was iterated through build errors, installed, launched and used to attempt delivery of explicit Intents to selected components.

## Result

The application became functional and the test buttons executed. Attempts to invoke selected non-exported target components failed with Android security restrictions.

That result was useful: it established the boundary being tested rather than merely assuming that a component was reachable.

## What was learned

A small purpose-built test harness can provide a more realistic test of Android IPC than repeatedly forcing a general-purpose command-line tool to reproduce complex application behavior.

## Publication status

The target-specific version remains private.

A generic version can be published after removing target names, component identifiers and engagement-specific data.
