---
name: big-earl-eats-america-seedance-2-5-30s
description: "Seedance 2.5 video generation for the Facebook page BIG EARL EATS AMERICA. Hard-locked to one single 30-second 9:16 video per call, in a RAW REAL iPHONE VIDEO style (not cinematic, not 3D), with Big Earl locked to his reference images, his fixed voice, spoken dialogue and real street sound. Use for every Big Earl prompt (PROMPT 1 to PROMPT 200)."
---

# Big Earl Eats America — Seedance 2.5 30s Hard Lock (Real Phone Video Edition)

## Hard Lock (non-negotiable, overrides everything below)

- **Duration is locked at 30 seconds.** Always pass `duration: 30`.
- **Never deliver a 15-second result.** If the generated file is shorter than 29 seconds, it is not complete. Do not repeat the same route. Switch to the Seedance 2.5 30s composer route, or use `text_to_video` with the raw GitHub image URLs kept inside the prompt as references.
- **One single continuous video.** One tool call = one complete 30-second video.
- **Model is locked to Seedance 2.5.** Always pass `model_version: "seedance_2.5"`.
- **Ratio is locked to 9:16** (vertical reels).
- **Audio is ON.** Every video must include all spoken lines and the real background sounds exactly as written in the prompt. **No music.**
- **Style is locked to RAW REAL PHONE VIDEO.** Never cinematic, never 3D, never animation, never movie lighting.

### Anti-spreading rules — never do any of these:

- Never split into two 15-second clips or any multi-part sequence inside one request.
- Never propose, offer or mention a shorter or multi-clip delivery.
- Never claim Seedance 2.5 cannot do 30 seconds because one route returned 15 seconds. Switch route instead.
- Each "PROMPT 1, PROMPT 2 ..." is a separate, complete 30-second video and its own request. Make only the one prompt you were given.

### Maximum videos per reply: **1**

---

## Model Specification

- **Model:** Seedance 2.5 (`seedance_2.5`)
- **Duration:** 30 seconds, single continuous video
- **Ratio:** 9:16
- **Input:** prefer the visible/composer "Seedance 2.5 30s" route, or `text_to_video` with the raw GitHub image URLs inside the prompt. Use `image_to_video` only if it is verified to return 29-31 seconds in the current session.
- **Audio:** native — dialogue (lip-synced) and real ambient sound effects

---

## CHARACTER — BIG EARL (always the same)

### Reference image URLs

```
REFERENCE IMAGE URLS:
Big Earl FULL BODY = https://raw.githubusercontent.com/relnoorain2-droid/Big-Earl-Eats-America/main/Redheaded%20Cowboy%20in%20Studio.png
Big Earl FACE = https://raw.githubusercontent.com/relnoorain2-droid/Big-Earl-Eats-America/main/Rugged%20Ginger-Bearded%20Cowboy%20Portrait.png
```

Every prompt already contains these URLs and the CHARACTER LOCK. Use them as character references. Do not ask the user to upload images. If a prompt contains different Big Earl URLs, use the URLs in the prompt.

### CHARACTER LOCK (only add it if the prompt does not already contain it)

```
CHARACTER LOCK: Big Earl must look exactly like the reference images for the full 30 seconds. American man about 40, about 6'5" tall, heavy-set with a big round belly, fair sunburnt skin with freckles, long thick ginger-red beard reaching his chest, short ginger hair, small light-blue eyes, calm deadpan face. Same weathered brown leather cowboy hat, red-and-black buffalo-check flannel shirt with rolled sleeves, light-blue faded jeans, brown belt with a big oval silver buckle, worn brown cowboy boots. Never change his face, beard, hat, outfit, body size or age. Only one Big Earl in the video.
```

### VOICE LOCK

| Character | Voice |
|---|---|
| BIG EARL | deep, slow, calm American male voice with a light Texas drawl, about 40, few words, deadpan, never shouts |
| FRIEND (camera person, never seen) | casual young American male, laughing, short reactions |
| Everyone else | normal American voices that fit the person and the place |

---

## GLOBAL RULES (append to every prompt)

```
DURATION LOCK: Generate exactly one complete 30-second video. Use the full 0-30s timeline. Do not generate 5s, 10s or 15s.
STYLE: RAW REAL iPHONE VIDEO, vertical 9:16. Filmed by Earl's friend holding a phone (the friend is never seen). Handheld, natural small shake, casual framing, real autofocus and auto-exposure, slight phone noise, true-to-life colors, natural light. Looks like a real video uploaded to social media, not a movie. Real American places and real American people in the background who move and react naturally.
NOT ALLOWED: cinematic look, movie lighting, 3D animation, Unreal Engine, cartoon, slow motion, dramatic camera moves, drone shots, color grading, music, subtitles, text overlays, watermark, logo, more than one Big Earl, face morphing, beard or outfit changes, extra fingers, floating food, impossible physics. Normal shop signs that are part of the place are fine.
AUDIO: Speak every DIALOGUE line clearly with accurate lip-sync, in natural American English, in the given order, using the voice lock. Never skip a line. Dialogue is louder than background sound. Use only the real sounds of the place listed in SOUND. No music.
FOOD: Food looks real, steaming, messy and appetizing, at real-life size.
```

---

## Workflow

1. The user pastes ONE prompt (for example "PROMPT 37 — ..."). It is pre-approved. Generate immediately. Do not ask questions and do not ask for confirmation.
2. Keep the raw GitHub image URLs from the prompt as character references. Never use `github.com/.../blob/...` links or local file paths.
3. Final prompt order: `EXACT 30 SECOND OUTPUT REQUIRED. Use Seedance 2.5 30s route. Use the full 0-30s timeline.` + the user's prompt exactly as written + GLOBAL RULES.
4. Never shorten or drop a DIALOGUE line or the SOUND line. If the prompt is too long for the tool, shorten only the PLACE and visual description lines.
5. Check the output is 29-31 seconds. If it is about 15 seconds, regenerate with the 30s route and the same references.
6. Deliver the video via `NotifyHuman` with a renderable video asset. Do not add captions, hashtags or extra text.

## Tool Call Pattern (the only pattern)

```
text_to_video(
  model_version: "seedance_2.5",
  duration: 30,
  ratio: "9:16",
  prompt: "EXACT 30 SECOND OUTPUT REQUIRED. Use Seedance 2.5 30s route. Use the full 0-30s timeline. " + "<the user's PROMPT exactly as written>" + "<GLOBAL RULES>"
)
```

Only use `image_to_video` if that route is verified to produce 29-31 seconds in the current session.
