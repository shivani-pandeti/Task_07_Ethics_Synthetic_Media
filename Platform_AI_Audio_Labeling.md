# Follow-up Research: How Platforms Label AI-Generated Audio

## Why I Looked Into This

In Task 7, I found that the C2PA label on my Task 6 audio disappeared when I cut a 30-second excerpt, and that platforms often rely on this kind of metadata to label AI content. That raised a question: **how do platforms label AI-generated audio?** My guess was that audio gets less labeling than images and video. This follow-up tests that guess by comparing five platforms' published policies.

While doing this, I found it important to separate three different things a platform can do:

1. **Require creators to disclose** AI-generated audio.
2. **Automatically detect and label** AI-generated audio.
3. **Require disclosure only when the audio imitates a real person** or could mislead viewers.

Having an automatic labeling system also does not mean a platform can reliably detect all AI audio.

## What Each Platform Does

| Platform | When must AI audio be disclosed? | Who adds the label? | Automatic labeling? |
|---|---|---|---|
| **YouTube** | When content is **realistic** and could be mistaken for a real person, place, or event, such as making a real person seem to say something they didn't. Cloning **your own** voice for voiceovers is listed as exempt. A generic stock AI narrator is **not** explicitly listed either way. | The creator, by ticking a box when uploading | Yes, in some cases. YouTube can automatically disclose certain content created using its AI tools or carrying supported C2PA Content Credentials. |
| **TikTok** | AI content with "realistic images, audio or video" must be labeled. | The creator, through an AI label, sticker, or caption | Yes, in some cases. TikTok can auto-label content carrying C2PA Content Credentials. When this launched in 2024 it covered images and videos, and audio-only content was promised "soon." I could not confirm whether audio-only auto-labeling is now in place. |
| **Meta (Facebook, Instagram)** | Users must disclose "realistic-sounding audio that was digitally created or altered." | The user, and Meta may penalize accounts that don't | Yes, in some cases. Since April 2024, Meta applies AI labels to video, audio, and images when it detects industry-standard signals or when users disclose AI use. Detection is not comprehensive. |
| **Spotify** | For **music**: AI involvement (vocals, instruments, production) can be shown in Song Credits through a voluntary industry standard. Separately, Spotify bans unauthorized vocal impersonation (voice clones) of artists. | For AI credits: the artist or distributor, voluntarily. The impersonation ban is a separate platform rule, not a label. | Not described. Spotify notes that "the absence of a credit doesn't mean AI wasn't used." The policy I examined covers music and does not address podcasts or spoken audio. |
| **Apple Podcasts** | Covers "synthetic voices, AI-generated hosts... or AI-synthesized replicas of real individuals." | The creator must disclose **in the content itself and in the metadata, for each episode and the show** | Not mentioned |

## What I Found

**1. My guess was only partly right.** YouTube, TikTok, and Meta all describe some automatic labeling, so automatic labeling of audio is not absent. But each of these systems depends on signals such as C2PA metadata or the platform's own tools. My Task 7 test showed that C2PA metadata can disappear after one simple edit. Creator disclosure therefore still plays a large role in whether AI audio gets labeled.

**2. My Task 6 artifact would be treated differently depending on the platform.** My narration used a stock AI voice, imitated no real person, and had true content.

- **Apple Podcasts:** disclosure is clearly required, both spoken in the content and written in the metadata.
- **TikTok and Meta:** both cover realistic AI audio, so disclosure would most likely be expected.
- **YouTube:** unclear. A stock AI narrator is not on the exempt list, but it also does not imitate a real person. It would need to be judged under YouTube's "realistic content" rules.
- **Spotify:** the AI credits policy I examined is for music, so it would not clearly apply to a spoken narration.

The format also matters. My C2PA label was on an MP3 file. If that audio were placed inside a video or edited first, the label could be lost before any platform saw it.

**3. Apple Podcasts matches the rule I wrote for Ledgerline.** In Task 7, after losing the C2PA label, I decided that disclosure must be spoken in the audio itself. Apple Podcasts is the only platform in my comparison that explicitly requires disclosure both within the content itself and in its metadata. It was encouraging to see a real platform reach the same conclusion.

**4. Platforms differ in what triggers disclosure.** TikTok, Meta, and Apple Podcasts cover realistic or synthetic AI audio generally, even when no real person is imitated. YouTube's examples focus more on real people and real events. None of the policies I read directly addresses the "register" harm I described in Task 7: a realistic voice making an analysis sound more certain than it is.

**5. My interpretation: AI audio transparency has real weak points.** Automatic labels depend on metadata that is easy to lose, and the rest depends on creators choosing to disclose. Based on written policies alone, I cannot say whether audio is less protected than images or video. That would require testing actual detection, enforcement, and how labels survive editing.

## Limits of This Research

- I compared **written policies**. I did not upload audio to test how the platforms actually behave.
- Having an automatic labeling system does not show how accurately it detects AI audio.
- Some official help pages could not be opened directly, so parts of the YouTube and TikTok details come from reliable reporting on those policies.
- Platform rules change often, so these findings reflect the policies as I found them.

## Sources

- Apple Podcasts content guidelines (Section 1.11): https://podcasters.apple.com/support/891-content-and-subscription-guidelines
- Spotify, "Spotify Strengthens AI Protections" (Sept 2025): https://newsroom.spotify.com/2025-09-25/spotify-strengthens-ai-protections/
- TikTok Newsroom, "New labels for disclosing AI-generated content": https://newsroom.tiktok.com/new-labels-for-disclosing-ai-generated-content?lang=en
- TikTok Newsroom, "Partnering with our industry to advance AI transparency and literacy" (May 2024): https://newsroom.tiktok.com/en-us/partnering-with-our-industry-to-advance-ai-transparency-and-literacy
- Meta, "Our Approach to Labeling AI-Generated Content and Manipulated Media" (Apr 2024): https://about.fb.com/news/2024/04/metas-approach-to-labeling-ai-generated-content-and-manipulated-media/
- TechCrunch, "Meta deepfake labels" (Apr 2024): https://techcrunch.com/2024/04/05/meta-deepfake-labels
- YouTube Help, "Disclosing use of altered or synthetic content": https://support.google.com/youtube/answer/14328491
- NBC News, "YouTube says it will require creators to label 'realistic' AI content" (Mar 2024): https://www.nbcnews.com/tech/tech-news/youtube-says-will-require-creators-label-ai-content-rcna143937
