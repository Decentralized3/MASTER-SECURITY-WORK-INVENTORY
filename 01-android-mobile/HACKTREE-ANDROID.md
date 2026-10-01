# Android Intent & IPC Labs

## Context

Hands-on CTF practice using a deliberately vulnerable Android application. The work focused on understanding how Android Intent handling, state, nested Parcelable data and application logic interact.

## Flag 4 — State Machine

### Objective

Drive the application's state machine through the required Intent actions.

### Work performed

The decompiled activity and supporting classes were examined. ADB was used to send the required actions in sequence.

The observed transitions were:

`INIT → PREPARE → BUILD → GET_FLAG`

Logcat confirmed each transition.

### Result

The state machine was successfully driven to the final state. The decrypted flag itself was not captured in the available evidence.

### What was learned

The final behavior depended on the exact state/tag sequence used by the application. Reaching the final state and obtaining the protected output were separate problems.

---

## Flag 5 — Intent in Intent

### Objective

Understand and reproduce an activity expecting a nested Intent inside a Parcelable extra.

### Work performed

The activity and its Intent-dumping utility were examined. Several approaches were tried:

- ADB string extras
- nested Intent analysis
- Frida experimentation
- examination of the expected Parcelable structure

### Result

The activity could be launched, but the required nested structure was not successfully delivered. The ADB approach failed because a string extra could not reproduce the required Parcelable type. A Frida attempt failed while manually instantiating the activity.

### What was learned

Android IPC testing depends on the actual object type and structure being delivered. A textual representation of an Intent is not equivalent to a nested Parcelable Intent.

### Status

Incomplete.

## Evidence

The recovered work includes decompiled Java, ADB/logcat output and Frida session output.

## Publication

Safe as a CTF/lab write-up when target-specific challenge details are appropriate for disclosure. No real-world target or bounty claim is attached to this record.
