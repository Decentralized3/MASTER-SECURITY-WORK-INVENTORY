# Web & Application Security Work

## Earlier lab practice

The recovered history supports practical web/application-security lab work involving:

- request interception
- API testing
- authentication/session testing
- authorization testing
- SQL injection
- XSS
- CSRF
- IDOR
- business-logic testing

These should be represented as **lab practice**, not professional penetration-testing engagements, until the original lab records are recovered.

## ZeeshanUsmani ecosystem

The recovered testing included:

- subdomain and DNS/CNAME analysis
- Next.js application mapping
- API testing
- input-validation tests
- mass-assignment checks
- directory/API fuzzing
- source/JavaScript review
- Cloudflare behavior analysis
- GoHighLevel/LeadConnector funnel testing

Several hypotheses were tested and rejected. For example, a suspected Gemfury takeover did not survive verification because the actual CNAME resolved to AWS App Runner. Additional API parameters were ignored by the server, and Cloudflare consistently blocked several automated requests.

### Result

No confirmed high/critical vulnerability is established by the recovered record.

### Value of the work

The important technical development was learning to verify a hypothesis against the actual infrastructure rather than treating scanner output or an interesting response as a finding.

## Pillowfort

The recovered record includes application-surface mapping, Firebase configuration review, response analysis and client-library identification.

No confirmed vulnerability is established.

Operational tokens and live configuration values are excluded from this repository.

## Publication

Target-specific operational data remains private unless the applicable program permits disclosure. Sanitized methodology and lessons can be published.
