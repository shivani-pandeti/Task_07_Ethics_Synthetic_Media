# Task_07_Ethics_Synthetic_Media

> **Note:** This repository contains **no synthetic media**. It includes written analysis and a written policy only. No new synthetic artifacts were created, and no real or identifiable person's voice or likeness was used.

## 1. Task Description

Research Task 7, *The Ethics of Synthetic Representation*, follows Task 6, where I built a synthetic audio artifact. This task has two phases:

- **Phase A: Ethical analysis.** I return to my Task 6 artifact and reason outward from it using invented thought experiments along four axes (truth, consent, context, scale) plus one of my own (register). I then survey the main mitigations (disclosure, provenance, detection, law, platform policy, professional norms) and where each one breaks.
- **Phase B: Governance policy.** I write a policy that a specific organization could adopt for using, or refusing to use, synthetic voice and likeness, followed by an honest limitations section.

## 2. Link to Task 6

Phase A builds directly on my Task 6 work, which is linked here, not re-uploaded:

**Task 6 repository:** https://github.com/shivani-pandeti/Task_06_Deep_Fake

In Task 6, I turned an advisory script based on my Task 5 box-office analysis into three synthetic narrations using ElevenLabs stock voices (William and Brielle). I then tested a 30-second excerpt with Hive's AI detector, which returned a 99.2% AI-generated score.

## 3. Organizational Context and Why I Chose It

The policy is written for **Ledgerline Analytics**, a fictional 18-person data-analytics consultancy that produces client briefings and, more and more, recorded audio narrations of its findings.

**Why this context:**
- It is the closest real setting to what I built in Task 6: an advisory data narrative delivered in a synthetic voice.
- At a consultancy, the content is usually true and verified. That forces the policy to deal with harms that remain even when the content is true:
  - **Authority:** a confident voice making the analysis sound more certain than it is
  - **Context:** excerpts traveling without their label
  - **Consent:** clients asking for their executives' voices
- Data analytics has almost no professional norms specific to synthetic media, so the policy could not simply copy an existing code.

## 4. Repository Map

| File | What it contains |
|---|---|
| `README.md` | This overview |
| [`phase_a_analysis.md`](phase_a_analysis.md) | **Phase A:** a return to my Task 6 artifact (including a new provenance check), reasoning across the axes, the mitigation survey, and responses to research questions |
| [`phase_b_policy.md`](phase_b_policy.md) | **Phase B:** Part 1, the organization; Part 2, the full policy; Part 3, **limitations** (where the policy fails and what risk remains) |

## 5. What Surprised Me

I did not check provenance in Task 6. When I went back to my files for this task, I found that ElevenLabs had embedded a **C2PA manifest** in each of my three original MP3s, labeling them as AI-generated. The **30-second excerpt** I cut for Hive's upload limit had **no manifest at all**. Simply cutting the clip removed it.

Without meaning to, I had stripped the provenance from my own honest artifact in the first edited file I made, and my process log never noticed. Yet the Hive detector still identified that stripped clip as AI-generated. I had expected provenance to be the reliable safeguard and detection to be the weak one. In my own workflow, it went the other way.

This finding shaped the policy. Because metadata disappears so easily, the policy requires the disclosure to be **spoken in the audio itself**, not only stored in the file's metadata.
