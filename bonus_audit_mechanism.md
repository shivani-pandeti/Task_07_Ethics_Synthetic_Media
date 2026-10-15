# Bonus: How Ledgerline Would Check That the Policy Is Followed

A policy only matters if someone checks that people follow it. This section explains how Ledgerline Analytics would do that for the policy in `phase_b_policy.md`, and which checks can really be measured.

---

## 1. Keep a Log

Every synthetic narration is recorded in a log with:

- Project name and Project Lead
- Who verified the script, and when
- When the audio was made, and which tool was used
- The file's SHA-256 hash
- Whether C2PA metadata was present before delivery
- The consent record, if a real person's voice was used

If a narration is not in the log, it counts as a violation.

## 2. Quarterly Audit

Every three months, the Responsible Use Lead (RUL) and one partner (not the sales partner) review a random sample of narrations: at least 5, or all of them if there were fewer.

They check:

| Check | Can it be measured? |
|---|---|
| Was the script verified before the audio was made? | Yes. Compare the dates. |
| Is the spoken disclosure at the start and every 60 seconds? | Yes. Listen to it. |
| Does the original file still have C2PA metadata? | Yes. Use the same check from my Phase A. |
| Does the file match the hash in the log? | Yes. |
| Was consent valid on that date? | Yes. Check the consent record. |
| Are all the caveats from the written report in the script? | Mostly. |
| Did the voice sound more certain than the analysis? | No. It only sounds measurable. |

## 3. Compare the Tool's History With the Log

Each quarter, the RUL downloads the history from the firm's voice-tool accounts and compares it with the log. Anything made but not logged is investigated.

This only works for company accounts. It cannot see anything made on a personal account.

## 4. Ways to Report Problems

- **Staff:** an anonymous form to report a violation, or to report feeling pressured to lend their voice.
- **Clients and the public:** a contact address for reporting suspicious audio that claims to come from Ledgerline.
- Nobody is punished for reporting in good faith.

## 5. A Rough Check on Tone

Twice a year, two staff members who did not work on a project read the written report and listen to the narration. They rate how certain each one sounds, from 1 to 5. If the audio sounds much more certain than the report, the team reviews it.

This is based on opinion, so it is only a starting point for discussion, never a reason for discipline.

## 6. Yearly Review and Expiry Date

- Once a year, an outside lawyer reviews the policy against new laws.
- Once a year, staff answer an anonymous survey asking whether they have felt pressured or skipped steps.
- The policy **expires after 2 years** unless the partners review and re-approve it. The prohibited uses in Section 8 never expire.

## 7. What Happens When a Problem Is Found

| Problem | Response |
|---|---|
| A missing log entry or step | Fix it and remind the team |
| A file delivered without its disclosure | Treat it as an incident (Section 11) |
| The same mistake happening repeatedly | Retraining, plus extra review of that team's work |
| A prohibited use, or a disclosure removed on purpose | Serious misconduct (Section 12) |

## 8. Limits

- The audit only sees work done on company accounts.
- It can confirm that a checklist was signed, not that the person checked carefully.
- The harms I care most about (a voice sounding too certain, and consent that was not truly free) are the hardest to measure.

The audit cannot guarantee the policy is followed, but it makes skipped steps visible so the firm finds problems before a client does.
