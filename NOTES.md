# Context for continuing this project from anywhere

**What this is:** An Arabic (RTL, Khaleeji dialect) apology web page for my girlfriend, pet name **سمسمتي**.
**Live URL:** https://xabdullashaker.github.io/note/
**Repo:** xAbdullaShaker/note. The page is `index.html` (self-contained: images are inlined as base64 data URIs). `note.mp4` is a separate hosted video file. `template.html` is the local source (not always in the repo).
**Hosting:** GitHub Pages on `master`. Any commit auto-rebuilds the live page (~1 min).

## The situation (keep the tone right)
- I tried to gaslight her in an argument, then fell asleep and left her upset. The page owns that — no excuses.
- Long-distance: she's in Egypt, I'm in Bahrain. Tonight I'm out at the cinema with a friend; I don't want to leave while she's upset.
- Tone: SHORT, sincere, lightly funny — NOT cringe or wordy. Dark theme, rose/gold accents, Reem Kufi + Tajawal fonts, faded tiled-Shrek background.

## What's on the page now (in order)
1. Header: "سمسمتي" + "كلمة وحدة بس… آسف".
2. "الاعتراف" panel — 2 short lines owning the mistake.
3. A gold two-line Arabic verse I wrote myself — **leave it exactly as-is**.
4. Meme: sus Shrek face — "أنا أول ما عرفت إني غلطان".
5. Meme: staring donkey — "وهذا ضميري، قاعد يطالعني من الصبح".
6. Video panel: "تذكرين «نوح الحنون»؟" + an inline `<video>` playing `note.mp4` (this REPLACED a broken TikTok embed — do not go back to an embed/iframe).
7. Note panel — out at the cinema with a friend tonight; "صالحيني قبل لا أطلع؟".
8. Meme: grinning "please" donkey — "حتى الحمار يقول لك سامحيه".
9. Meme: Puss in Boots begging eyes — "سامحيني… بس شوفي عيوني".
10. "سامحتيني؟" — "سامحتك" button + a "لا" button that dodges the finger, then 🤍 confetti.

## ⭐ PENDING TASK — add my Gemini "pixel" video of us
I made an AI (Gemini/Veo) pixel-style video of the two of us. It should go on the page, ideally **near the top (right after the header) as the heartfelt centerpiece**, and keep the funny «نوح الحنون» clip lower down where it is.

To add it (edit `index.html` directly — no build step needed):
1. Commit the video file to the repo, e.g. `us.mp4` (and optionally a poster image).
2. Insert this block where you want it:
```html
<section class="panel reveal">
  <div class="clipwrap">
    <video class="clip" controls playsinline preload="metadata">
      <source src="us.mp4" type="video/mp4">
    </video>
  </div>
</section>
```
The `.clip` / `.clipwrap` styles already exist, so it will match. GitHub Pages serves mp4 with range support, so it plays inline.

## How to continue from my phone
Open Claude Code on the web (claude.ai/code), pick the `xAbdullaShaker/note` repo, say **"read NOTES.md"**, then give your change. It edits `index.html`, commits, and the live page updates automatically.
