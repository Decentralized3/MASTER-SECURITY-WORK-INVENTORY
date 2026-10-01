# Bug-Bounty & Authorized Testing

This section records real-world security testing separately from laboratory work.

## Why it is separate

A lab demonstrates technique.

An authorized engagement adds another constraint: **scope, disclosure rules, report status and evidence matter.**

For that reason, the repository does not turn every observation into a vulnerability claim.

## Current records

### Viator
Android application testing in a Bugcrowd context.

### TheFork Manager
Android configuration/static analysis and a limited Firebase endpoint check. The recovered evidence shows the database instance was already deactivated; no data access was demonstrated.

### Luno
Verification of candidate findings supplied by an AI pentesting system. The work included manual analysis of DNS, headers and 403 behavior. Several candidates were not confirmed.

### ZeeshanUsmani ecosystem
Web/API reconnaissance and validation. No confirmed high/critical finding is established in the recovered material.

### Pillowfort
Application reconnaissance and configuration/library review. No confirmed vulnerability is established.

## Disclosure rule

Before a target-specific record becomes public, verify:

- program authorization
- scope
- report/submission status
- triage outcome
- disclosure policy
- whether target names/details may be published

Never publish credentials, tokens, cookies, user data, raw scan dumps or confidential reports.
