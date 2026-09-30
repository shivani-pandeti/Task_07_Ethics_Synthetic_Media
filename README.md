# Phase B: Synthetic Voice Policy for Ledgerline Analytics

---

## Part 1: The Organization

**Ledgerline Analytics** is a fictional, composite data-analytics consultancy. I based it on the kind of work I did in Tasks 5 and 6.

- **Who works there:** 18 people: 3 partners (one handles sales), 11 analysts, 2 data engineers, 1 designer, and 1 operations manager. There is no in-house lawyer.
- **What it produces:** Slide decks, dashboards, written briefs, and increasingly **recorded narrations**: 1–5 minute audio walkthroughs of findings that client executives listen to or forward to their boards.
- **Clients:** Regional retailers, two hospital systems, a minor-league sports team, a county economic-development agency, and independent film distributors.
- **Audience:** Client executives first. Because clients forward material, a narration made for one person often reaches many people Ledgerline never meets.
- **What it cares about:** Being the firm whose numbers can be trusted.
- **Where synthetic media tempts it:**
  - Using a stock AI voice for narrations (exactly what I did in Task 6), which saves analysts recording time
  - Cloning a partner's voice for weekly updates
  - Spanish-language versions for a hospital client
  - A client asking, "Can you use our CEO's voice? He's too busy to record."
- **Where synthetic media endangers it:**
  - A confident voice making an analysis sound more certain than it is
  - Excerpts traveling without their label
  - A cloned executive voice being used for statements to investors

**Why this context:** It is the setting closest to what I actually built, an advisory data narrative in a synthetic voice. At a consultancy the content is usually true and verified, so the policy has to deal with the harms that remain after the content is verified: authority, context, and consent.

---

## Part 2: The Policy

**LEDGERLINE ANALYTICS: POLICY ON SYNTHETIC VOICE AND LIKENESS**
Owner: Responsible Use Lead · Reviewed every 12 months, and after any serious incident

### 1. Scope

This policy covers any audio, video, or image in which a voice or person is generated or altered by AI. It applies to all staff, contractors, and interns, on any tool, including personal accounts used for work. AI transcription and captioning of real recordings are not covered.

**Core rule:** A synthetic voice may deliver Ledgerline's analysis. It may never speak *as a real person*, and it may never make the analysis sound more certain than it is.

### 2. Roles

- **Responsible Use Lead (RUL):** A senior analyst appointed for two years. The RUL must not be the sales partner. The RUL approves requests, keeps the consent records and the synthetic media log, and leads incident response.
- **Project Lead:** Responsible for following the policy on each deliverable.
- **Verifier:** A second analyst, not the author, who checks the script before it is voiced.

### 3. Permitted Uses (no approval needed)

A use is permitted without approval only if **all** of the following are true:

1. The voice is a **stock voice** from an approved vendor. It is not a clone and not designed to sound like a real person.
2. The script is **Ledgerline's own analysis** and has passed verification (Section 5).
3. The narration speaks as "Ledgerline" or in the third person, never as "I, your analyst."
4. The audience is only the client who ordered the work.

**Examples:**
- A narrated dashboard walkthrough for a retail client
- An audio version of a written brief, for accessibility
- A Spanish narration of a verified brief, checked by a fluent speaker before it is voiced
- Internal practice drafts that are never shared outside the firm

*Note: My own Task 6 artifact would not qualify as it is. The script uses "I," and there is no disclosure in the audio.*

### 4. Uses That Need RUL Approval First

- Any use of a **real person's voice or likeness**, including your own, even with consent (see Section 6)
- **Composite personas** (for example, a "typical customer" voice). These must be labeled as composites and never given a real person's name or photo.
- Any narration meant for an audience **outside the client**, such as public release, investor materials, or social media
- Any narration of a **forecast or recommendation** the analysis rates below high confidence
- Any **new tool or vendor**

The RUL answers within 3 business days. **No answer means no.**

### 5. Verification Before Voicing

1. No script goes into a voice tool until the Verifier confirms that every number matches the source analysis and every caveat from the written report is in the script.
2. **Caveats must be spoken, not cut.** For example, if the mean and median are very different, the narration must explain what that means.
3. Expressive or "style" settings may not be used to make recommendations sound more confident. On those sentences, style settings stay at or below the vendor's default.
4. Any edit made after verification goes back through verification.

### 6. Consent for a Real Person's Voice

1. **Only the person themselves can consent.** A client's communications team cannot consent for its CEO, and a partner cannot consent for an analyst.
2. Consent must be written and must name the specific project, the audience, and an end date **no more than 12 months** away. Blanket consent ("any future use") is not valid.
3. The person approves **every script** in writing before it is voiced.
4. The RUL obtains consent directly from the person, after playing them a sample of the synthetic voice, and records it in the consent register.
5. **Saying no has no consequences.** Consent is never a condition of a job, a promotion, or a project. An employee's consent ends when they leave the firm.
6. **Revocation:** A person can withdraw consent at any time in writing. Within 5 business days, Ledgerline stops all use, deletes the voice model (and gets deletion confirmation from the vendor), withdraws copies it controls, and informs affected clients. Copies that others have already forwarded cannot be recalled, and the consent form says so.
7. **Even with consent**, a synthetic version of a real person's voice may not deliver financial results, forecasts, statements to investors or regulators, or personnel decisions. The real person must record these.

### 7. Disclosure and Provenance

In my Task 6 work, making a 30-second excerpt removed the C2PA metadata completely. So **the disclosure must be spoken in the audio itself.** Metadata is only a backup.

1. **Start:** Within the first 5 seconds, the narration says: *"This narration uses an AI-generated voice. The analysis was prepared and verified by Ledgerline Analytics."*
2. **Repeat:** For narrations longer than 90 seconds, a short version ("AI-generated voice, Ledgerline Analytics") is repeated at least every 60 seconds and at the end.
3. **Video:** An "AI voice" label stays on screen for the whole video, in addition to the spoken disclosure.
4. **Files:** Filenames end in `_AIvoice`, and any transcript or email sent with the audio says in its first line that the voice is AI-generated.
5. **Provenance:** Use only vendors that add C2PA Content Credentials and a watermark. Deliver the **original exported file**. Do not trim, convert, or re-export it with tools that remove the metadata.
6. **Archive:** Keep the original file, its SHA-256 hash, the final script, and the verification sign-off for 3 years. This is how Ledgerline can prove what it did and did not publish.
7. Deliberately removing a disclosure, metadata, or watermark is a violation of this policy.

### 8. Prohibited Uses (no exceptions)

Ledgerline will not create or share synthetic media that:

1. Uses a **real person's voice or likeness without consent** under Section 6. This includes public figures, client executives, competitors, and deceased people, including as parody or a joke.
2. Delivers **financial results, forecasts, or market-moving information** in *any* synthetic voice to anyone outside the firm.
3. Is presented as a **recording of a real event**, such as an interview, focus group, customer call, or meeting.
4. Creates **testimonials, reviews, or quotes** attributed to clients, customers, or experts.
5. Relates to any **election, candidate, or political campaign**.
6. Makes or answers **live phone calls or leaves voicemails** with a synthetic voice.
7. Depicts **minors**, or depicts anyone in a sexual, violent, or demeaning way.
8. Narrates analysis that has **not passed verification**.
9. **Leaves out or removes the disclosures** in Section 7, or is designed to make listeners believe a human is speaking.

No partner, client, or deadline can make an exception to this section.

### 9. How Requests Are Reviewed

The RUL asks three questions and records the answers:

1. **Stripped-clip test:** If any 30 seconds of this were shared without labels, would a listener be misled about who is speaking, whether it really happened, or how certain the finding is?
2. **Consent test:** Has every identifiable person agreed to *these exact words*?
3. **Necessity test:** What does the synthetic voice add that a human recording or plain text would not? Saving time is a good reason for a stock voice. It is not a good reason to clone a person.

The RUL can approve, approve with conditions, or refuse. Two partners can overrule a refusal in writing, but never for a use prohibited in Section 8.

### 10. When Ledgerline Says No, Even to Permitted Uses

Ledgerline will not produce synthetic media when:

- The client won't accept the disclosures, or asks for them to be shortened or removed.
- The client plans to clip the content for social media or public channels without RUL approval.
- There isn't time to verify the script. A late deliverable is better than an unverified one.
- The analysis is preliminary or low-confidence.
- The deliverable only works if listeners believe a human is speaking.
- **Any employee declines.** Anyone may refuse to work on synthetic media, with no reason required and no penalty.

### 11. Incident Response

An **incident** is any Ledgerline synthetic media that is misused, misattributed, shared without its disclosure, sent to the wrong audience, or made in breach of this policy. It also includes fake content claiming to come from Ledgerline.

**Within 24 hours:**
1. Report it to the RUL. Reporting your own mistake is never punished; hiding one is.
2. Save the evidence: the file, where it was found, screenshots, and URLs.
3. Compare the file against the archive, using its hash and metadata, to establish whether it is our original, an altered copy, or not ours at all.
4. Tell the affected client and anyone whose likeness is involved.

**Within 72 hours:**
5. Ask the platforms to remove it.
6. If the content reached the public, publish a correction and offer the original file. **Never respond with new synthetic media.**
7. Pause synthetic production on that project until the RUL clears it.

**Within 10 business days:**
8. Write a no-blame review: what happened, which safeguard failed, and what will change.

### 12. Violations

Breaking Section 8, or deliberately removing disclosures, is serious misconduct and can lead to termination. Other mistakes are handled first with retraining. Clients who repeatedly ask staff to break this policy may be dropped.

---

## Part 3: Limitations: Where This Policy Fails

This policy helps honest people at Ledgerline act consistently and gives the firm a record when things go wrong. It cannot protect audiences from dishonest people.

### Where well-meaning staff could break it

- **The excerpt gap.** The disclosure repeats every 60 seconds, but the review test imagines a 30-second clip. A 30-second excerpt taken between two disclosures would carry no label. My own Task 6 excerpt was about 30 seconds. I chose 60 seconds because a disclosure every 30 seconds would make a three-minute narration hard to listen to, and staff would stop following the rule. This is a known gap I have not solved.
- **Small edits remove provenance.** An analyst who trims two seconds of silence from a file removes the C2PA metadata. I did the same thing in Task 6 without noticing. The rule against it only works if people remember it.
- **Tone is a judgment call.** "Sounds more confident than the evidence" cannot be measured, and two reviewers may disagree. This is the harm I care most about from Phase A, and it is the hardest to enforce.
- **Stock voices may not be consent-free.** A stock voice like "Brielle" was probably built from a real voice actor's recordings. The policy treats stock voices as safe, but Ledgerline cannot check what that actor agreed to.
- **Composite personas can be misread.** A labeled "typical patient" clip could still be forwarded as "what patients are saying."

### What a bad-faith person can do anyway

- An employee can voice a script on a personal account with no disclosure. The policy can punish this afterward but cannot prevent it.
- A client can strip and re-caption a compliant file after delivery.
- Anyone can make audio that *sounds like* a Ledgerline narration, using a tool that adds no watermark or metadata.

### Where it relies on good faith

The policy assumes the Verifier really checks, staff don't edit delivered files, the RUL refuses even when a big client pushes back, and employees feel free to say no to consent. **The last one worries me most.** In an 18-person firm, a junior analyst asked by a partner to lend her voice may say yes because saying no *feels* risky, whatever the policy says.

I do not think relying on good faith is fatal. Every workplace policy governs people who could break it. But the honest description of this policy is that it is a **coordination tool for good-faith staff and an evidence trail for when things go wrong**, not a guarantee.

### What can and cannot be measured

Log completeness, pre-delivery checks, incident counts, and how quickly revocations are handled can all be measured. Whether a narration sounded too certain, or whether consent was truly free, cannot. The harms the policy most wants to prevent are the hardest to audit.

### Remaining risk
Even if Ledgerline follows this policy perfectly, its narrations can still be excerpted without a label, can still lose their metadata on the first careless edit, may still carry a voice built from an unknown actor's recordings, and will still sound more authoritative than a written memo. The policy makes synthetic narration **accountable**, not **safe**, and I think that is the most a single organization's policy can honestly promise.