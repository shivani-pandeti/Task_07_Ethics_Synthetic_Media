# Phase A: The Ethics of What I Built

This analysis builds on my Task 6 work: [Task_06_Deep_Fake](https://github.com/shivani-pandeti/Task_06_Deep_Fake).


## 1. Returning to What I Built

In Task 6, I turned a short advisory script based on my Task 5 box-office analysis into three synthetic narrations using ElevenLabs and two of its stock voices:

- **Attempt 1:** William, default settings (1:28)
- **Attempt 2:** Brielle, faster speed, low stability, moderate style (1:19)
- **Attempt 3:** Brielle, speed and stability near the middle, style exaggeration 56% (1:26)

The script recommends that a studio focus on Action over Comedy. It compares average gross ($165.5M vs. $108.1M) and median gross ($48.0M vs. $22.1M), and uses *Top Gun: Maverick* as a blueprint. Hive rated a 30-second excerpt of Attempt 2 as 99.2% likely AI-generated.

Nothing in this artifact is harmful. The content was verified in Task 5, no real person's voice was used, and the repository labels everything as synthetic. Still, looking at it again, I notice several things my process log did not capture.

**1. It was fast.** My log shows about 4–6 minutes for Attempt 1 and about 3 minutes each for Attempts 2 and 3. Giving the analysis a voice took far less time than producing the analysis.

**2. The "I" in the script is no one.** The script begins, "If I were advising a movie studio…" When I wrote it, "I" meant me. When the synthetic voice says it, "I" is an advisor who does not exist and cannot be questioned. The tool did not just read my analysis; it gave it a speaker.

**3. I picked the "best" attempt by how human it sounded.** I preferred Attempt 2 because it was more conversational and less like a direct reading. That is a reasonable goal for narration, but it is also exactly what someone trying to deceive would optimize for.

**4. The voice made my caveat sound as certain as my conclusion.** The script says, "This does not mean every Action movie will be successful." The numbers also need care: the Action mean ($165.5M) is much higher than the median ($48.0M), which means a few blockbusters pull the average up. In text, a reader can stop and think about that. In a smooth, confident voice, the caveat passes at the same pace as the recommendation. The content was true, but the delivery sounded more certain than the evidence was.

**5. My disclosure was in the README, not in the audio.** If someone plays one of the MP3 files on its own, nothing in the audio says it is synthetic.

**6. I removed the provenance without noticing.** I did not check provenance in Task 6. While preparing this task, I went back and checked my Task 6 files for C2PA Content Credentials:

```bash
for f in *.mp3; do echo "$f: $(strings "$f" | grep -ci c2pa)"; done
```

| File | C2PA matches |
|---|---|
| synthetic_audio_attempt1.mp3 (from ElevenLabs) | 16 |
| synthetic_audio_attempt2.mp3 (from ElevenLabs) | 16 |
| synthetic_audio_attempt3.mp3 (from ElevenLabs) | 16 |
| attempt2_detection_30sec.mp3 (my excerpt) | **0** |

ElevenLabs had embedded a signed C2PA manifest in each original. The manifest identifies the file as AI-generated (`trainedAlgorithmicMedia`) and names Eleven Labs Inc. as the author. My 30-second excerpt, which I made only because Hive limits uploads to about 30 seconds, has no manifest. Cutting the clip removed the provenance. I did not intend it and my log does not mention it. The one derivative file I created had already lost its machine-readable label.

(This check only shows whether the manifest is present. It does not validate the signature, and it does not test ElevenLabs' separate inaudible watermark, which may still be in the excerpt.)

### Where the tool refused or warned me

My log records no refusals. The only warning was that style exaggeration above 50% "may lead to instability," which is a quality warning, not an ethical one. My project never came near the boundaries vendors guard, such as cloning a specific person's voice. What it does show is that narrating any text in a stock voice is treated as ordinary: nothing checked whether my numbers were true, and nothing would have checked if they were false. The voice library also sells its voices on naturalness ("Brielle – Podcast girl extremely natural").

### What I would do differently

I would build the same artifact again, but I would put a spoken disclosure in the audio, avoid first-person narration, and check what any editing step removes before sharing a derivative file. I also no longer treat a stock voice as neutral: it was presumably built from a real voice actor's recordings, under terms I have not read.

---

## 2. Reasoning Across the Axes

Each scenario below is invented. Each starts from my artifact and changes one thing.

### Truth axis: same delivery, false content

**Scenario.** Someone wants a studio's stock to drop before a summer release. They write a 200-word script in the same advisory style as mine, but with invented numbers: "Pre-sales are tracking 41% below comparable titles." They use a stock voice with settings like my Attempt 2 and post it as a "Weekend Box Office Brief." Listeners hear a calm, specific analyst. Some investors sell, and a couple of articles repeat the number as "tracking data" before the real opening figures come out.

**What changes.** The mechanism is exactly the same as mine. The only difference is whether someone verified the content before it went into the tool. The synthetic voice does not create the lie, but it gives the lie the sound of a credible, accountable speaker without anyone having to stand behind it. This is why my policy requires verification *before* synthesis, not just a label after.

**Where I am unsure.** I believe a voiced fake is more persuasive than a written one, but I have not measured this.

### Consent axis: someone else's voice

**Scenario.** The same person clones a studio CFO's voice from public earnings calls and posts a 40-second "hot mic" clip: "We're going to have to push the release to next year. Don't put that in the transcript." The studio denies it, but a denial of "leaked audio" sounds like what a company would say anyway.

**What changes.** My artifact borrowed generic credibility from sounding like an analyst. This borrows a specific, real person's reputation and responsibility without their agreement. The victim is now a real person. Their denial loses force, because a fake sounds just like the real thing. And once clones are common, even genuine recordings of that person can be dismissed as fake. This is where the tool becomes a weapon: not the synthesis itself, but using an identity people rely on to decide who is responsible. A label does not fix this, because "AI voice of the CFO" still puts words in the CFO's mouth.

### Context axis: the label is stripped

**Scenario.** Someone takes 30 seconds from the middle of my Attempt 2, the part about Action movies averaging $165.5 million, and posts it as "audio from the studio's internal greenlight meeting." Every word is true, but the caption makes a synthetic narrator into a real executive and a public dataset into insider strategy.

**What changes.** I do not need to imagine the mechanics, because I already did them:
- My excerpt has no C2PA manifest, so a platform that labels AI content from metadata would see nothing.
- There was no spoken disclosure in the audio to begin with.
- The detector still worked (99.2%), but only people who already doubt a clip run it through a detector.

True content is not the same as safe content. Meaning depends on the content, the framing and the assumed speaker together.

### Scale axis: one artifact vs. thousands

**Scenario.** A content farm runs 200 "movie analytics" podcast channels. A script pulls public box-office data, a language model writes a short advisory for every release, and a text-to-speech API voices each one. Around 1,500 episodes a week go out, mostly accurate, some with invented numbers, none checked. Human analysts who verify their numbers are drowned out in search results.

**What changes.** My three attempts took about ten minutes by hand. Through an API, each one costs almost nothing. At that scale, the harm is less about any single clip and more about listeners no longer being able to assume that a recorded voice means someone took responsibility. Checking becomes the bottleneck, because producing is cheap and verifying is not. Detection also becomes a numbers problem: a detector that misses a small share of clips still misses a large number of them.

### Added axis: register (tone of authority)

Even with true content, a real consenting voice, a label and a single artifact, a synthetic voice can mislead by *sounding* more confident or expert than the content supports. This is point 4 from Section 1, and it is the one harm my own honest artifact actually committed. It is why my policy regulates how caveats are delivered, not just whether audio is labeled.

---

## 3. The Mitigation Landscape

| Mitigation | What it promises | Where it breaks | From my own work |
|---|---|---|---|
| **Disclosure** (labels, spoken notices) | Tells the audience the media is synthetic | Only reaches people who see or hear the label; lost when content is excerpted or re-posted | My disclosure was only in the README, not in the audio |
| **Provenance** (C2PA) | A signed, machine-readable record of origin | Removed by ordinary editing; a missing manifest proves nothing; only cooperating vendors add it | Present on my originals, gone from my excerpt |
| **Watermarking** | An inaudible signal meant to survive editing | Vendor-specific (the ElevenLabs detector finds only ElevenLabs watermarks); open-source tools do not add one | Not tested; requires a signed-in account |
| **Detection** (e.g., Hive) | Identifies synthetic media after the fact | Gives a probability with no explanation; generators keep improving; only used by people already suspicious | 99.2% on my stripped excerpt, but that is one sample |
| **Law and regulation** | Consequences and transparency requirements | Patchwork, slow, and focused on the most extreme harms | — |
| **Platform policy** | Labels and removal where content spreads | Relies on self-disclosure and metadata that is often already stripped; enforcement is uneven | My excerpt would upload unlabeled |
| **Professional norms** | Industry self-restraint | Voluntary; data analytics has almost no norms specific to synthetic delivery | — |

**The legal terrain, in general terms:**
- **Disclosure rules:** The EU AI Act's Article 50 transparency obligations apply from 2 August 2026. They require providers to mark AI-generated content in a machine-readable way and require those who publish deepfakes to disclose that they are artificial. A proposal to delay the marking requirement to 2 December 2026 was pending.
- **Non-consensual intimate imagery:** In the US, the TAKE IT DOWN Act covers AI-generated intimate images and requires platforms to remove them within 48 hours of a valid request. FTC enforcement began on 19 May 2026.
- **Voice and likeness rights:** Tennessee's ELVIS Act (2024) protects a person's voice from unauthorized AI imitation. The federal NO FAKES Act has been introduced several times but has not been enacted.
- **Robocalls:** The FCC ruled in 2024 that AI-generated voices in robocalls are "artificial" voices under the TCPA and require prior consent.
- **Elections:** Many US states have disclosure rules or restrictions on deceptive synthetic media near elections.

The law is strongest for the most extreme harms (sexual imagery, elections, fraud calls) and thinnest in the middle, where synthetic narration of commercial or informational content like mine sits.

**On platforms and professional norms:** Platforms ask creators to disclose realistic synthetic content and automatically label content that carries C2PA metadata. Both depend on signals my own workflow lost. Journalism generally bars presenting synthetic media as real reporting, performers' unions have negotiated consent and pay for digital replicas, and political consultants' associations have condemned deceptive deepfakes. Data analytics has almost nothing comparable.

**What this adds up to:** the mitigations that would catch my artifact are not the ones that would catch a bad actor. My artifact is easy to catch because I kept the originals, labeled the repository, and would admit what it is. A bad actor strips the metadata (as I did by accident), discloses nothing, and posts where no one runs a detector. The real value of these mitigations is that they make casual misuse harder, create evidence after something goes wrong, and let honest producers prove what they actually published. They protect the credibility of honest actors more than they protect the public from dishonest ones.

---

## 4. Responses to Selected Research Questions

**What specifically becomes dangerous?** Not the technology alone, but the loss of the audience's default assumption that a voice belongs to a person who is answerable for what was said. My artifact shows fluent delivery and accountability coming apart; scale makes that a public problem.

**Where does my policy rely on good faith, and is that fatal?** It relies on people actually verifying numbers and keeping disclosures intact. I do not think that is fatal, because every workplace policy governs people who could break it. It does mean the policy is a tool for coordinating honest people, not a defense against dishonest ones.

**Where does the ethical burden fall?** Mainly on the producer, because only the producer knows whether the content is true and whether consent exists. Platforms and vendors carry structural responsibility, because only they can make labels survive at scale. My case shows a gap: a vendor that signs the file but adds no spoken label leaves honest users one editing step away from losing it.

**Would a different context produce a different policy?** Yes. A newsroom policy would center on never presenting synthetic media as a record of real events. A campaign policy would center on opponents' likenesses. My consultancy policy centers on synthetic delivery lending authority to analysis. Consent and incident response carry over between settings; what counts as harmful authority does not.

---

## Sources

- Task 6 repository: https://github.com/shivani-pandeti/Task_06_Deep_Fake
- European Commission, AI Act transparency guidelines: https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-transparency-obligations
- Greenberg Traurig on Article 50 (June 2026): https://www.gtlaw.com/en/insights/2026/6/deepfakes-chatbots-ai-generated-text-european-commission-details-transparency-obligations-under-the-ai-act
- FTC, TAKE IT DOWN Act enforcement (May 2026): https://www.ftc.gov/news-events/news/press-releases/2026/05/ftc-begins-enforcing-take-it-down-act
- ElevenLabs Audio Detector documentation: https://elevenlabs.io/docs/eleven-creative/audio-tools/audio-detector
- NO FAKES Act: https://en.wikipedia.org/wiki/No_Fakes_Act
- ELVIS Act: https://en.wikipedia.org/wiki/ELVIS_Act
- FCC, deepfake audio in robocalls: https://www.fcc.gov/consumers/guides/deep-fake-audio-and-video-links-make-robocalls-and-scam-texts-harder-spot