# Prototype browser verification

Scope: automated Chromium interaction tests on the offline mock UI. These do not verify production security, persistence, encryption, availability, tenant isolation or GDPR compliance.

| Test | Result | Observed |
|---|---|---|
| T01 Invalid demo MFA | PASS | Demo verification failed. |
| T02 Examiner self-approval blocked | PASS | Denied: requires Moderator persona. |
| T03 Independent question approval | PASS | Approved |
| T04 Early exam access blocked | PASS | Denied: exam is outside its demo window. |
| T05 Submission receipt | PASS | Demo receipt ES-R001; not durable storage. |
| T06 Duplicate submission handled | PASS | Existing demo receipt ES-R001 (no duplicate). |
| T07 Examiner cannot publish | PASS | Denied: requires Registrar persona. |
| T08 Registrar cannot bypass moderation | PASS | Moderation must occur first. |
| T09 Independent publication | PASS | Published |
| T10 Simulated alert | PASS | Synthetic alert ES-INC-01 created; review R01 and incident playbook. |
| T11 Denials audited | PASS | 5 denied events |
| T12 Browser errors absent | PASS | [] |
| T13 Reset clears state | PASS | Not signed in |
