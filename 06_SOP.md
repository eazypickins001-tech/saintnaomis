# 06 — SOP (standard operating procedure)

> Filled for Saint Naomis Foundation. The stages do not change. They are the
> template.

---

## 1. Toolchain

| Job | Tool | Notes |
|---|---|---|
| Video generation | Veo and Omni | Veo 8 s max, Omni 10 s max. This bank uses 6 × 8 s. |
| Stills and inserts | Flux / Midjourney / Ideogram | Edit a near-miss over regenerating |
| Editing, text, captions | CapCut | All text is built here, never generated |
| Intro and outro | CapCut | Built once from `_SHARED/intro-prompt` and `_SHARED/outro-prompt`; values in `02_BRAND_SKIN.md` §5b |
| Scores, deadlines, labels | CapCut / After Effects | Never AI-generate a number or a result |
| Voice | ElevenLabs, voice "The Teacher" | Locked settings, one voice only |
| Music | Licensed library bed | No trending audio |
| Real records | Programme report PDFs, real screenshots | Never AI |
| Storage | Project Drive folder | Mirror of git-tracked files only |
| Repo | GitHub | Source of truth for words and prompts |
| Live site | saintnaomis.org | CTA targets, programme names, real stories |

**Rule:** video, audio and footage never enter git. If a file is over ~5 MB it
does not belong in the repo.

---

## 2. Weekly rhythm

| Day | Work |
|---|---|
| Mon | Pick four files from the queue; check pillar and category rotation; write the four hooks |
| Tue | Write prompts; publish post 1 |
| Wed | Generate clips in one batch by character and technique |
| Thu | Edit, add captions and file labels; publish post 2 |
| Fri | Voice and assemble; publish post 3 |
| Sat | Publish post 4; reply, pin, collect comments |
| Sun | Log numbers; weekly review; check permissions and service claims |

Four posts per week. Keep **one generation day** (Wednesday) and **one review
day** (Sunday).

---

## 3. Per-post pipeline

```
1 PLAN      topic, pillar, category (differs from last post), hook
2 CAST      choose the continuity clause; paste it verbatim
3 SCRIPT    clip table, one irreversible action per clip
4 PROMPT    six parts + negatives, continuity clause, palette clause
5 FACT      every number, exam, service and name checked and sourced
6 VALIDATE  node tools/validate-posts.js 03_POST_BANK.md
7 GENERATE  AI clips first; real records only where a record is the point
8 EDIT      captions, file tag, underlined word, bird wipe, sound
9 ASSEMBLE  wrap with the intro and outro (built once, never re-made)
10 CAPTION   platform caption + hashtags + pinned comment + compliance line
11 PUBLISH  publish, pin immediately, reply
12 LOG      row in 05_PROOF_TRACKER.md at 24h / 7d / 30d
```

---

## 4. Quality gates (all must pass before render)

**Script gate**

- [ ] Hook is the interrupt, inside 1 second
- [ ] One idea only
- [ ] Payoff delivered before the CTA
- [ ] Category differs from the previous post
- [ ] Pillar differs from the previous post, unless the series sub-type differs
- [ ] Pillar respects the standing instruction

**Fact and service gate**

- [ ] Every exam name, deadline and programme detail is correct
- [ ] Every number is from the programme report or a named public source
- [ ] Every number has a source line in the caption
- [ ] Every service named in the CTA is confirmed live with the programme team
- [ ] Every CTA points to a page that exists on the live site today
- [ ] No test-prep or admissions service is advertised; those posts teach only
- [ ] No exam, admission or scholarship promise
- [ ] No diagnosis, clinical claim or legal claim
- [ ] Every named real person has confirmed permission
- [ ] Every composite is labelled as a composite

**Prompt gate**

- [ ] Six parts present, in order
- [ ] Effect stated as verb + direction
- [ ] Camera locked or motion explicitly resolved
- [ ] Negative prompt on every clip
- [ ] Continuity clause pasted verbatim on every returning character
- [ ] Negative prompt excludes non-African characters and identity drift
- [ ] No text requested from the model
- [ ] Clip within the model limit
- [ ] Palette clause present

**Integrity gate**

- [ ] A face is never presented as a real student
- [ ] `Illustrative image. Not a real student.` is in the caption if a face
      appears
- [ ] No AI-generated score, acceptance letter, certificate or result
- [ ] No identifiable real person in a negative context
- [ ] No image of a child crying, undressed, injured or in distress

**Packaging gate**

- [ ] Intro is 1.2 s and hard-cuts into Clip 1
- [ ] Outro is 2.4 s, one CTA, no seam from the last clip
- [ ] Intro and outro are the same files used on every other post
- [ ] The three birds lift on the same frame every time
- [ ] Content is 48 s, published runtime is 51.6 s
- [ ] File tag and captions read at 40 px and on mute
- [ ] The logo's birds survive the 40 px avatar test

**Publish gate**

- [ ] Caption's first line is the hook
- [ ] 8-12 hashtags across the three tiers
- [ ] Source line present if there is a number
- [ ] Composite, AI-face or not-medical-advice line present where needed
- [ ] Pinned comment ready
- [ ] Logged in the tracker

---

## 5. Batch production (the efficiency rule)

Batch by **character and technique**, not by post:

1. Generate every Amara clip in one session.
2. Generate every Ngozi clip in one session.
3. Generate every Tunde, Mama, Adaeze and Baba clip in one session.
4. Generate every object, room and paper clip in one session.
5. Then assemble per post.

This keeps faces, hair and wardrobe consistent across the catalogue and cuts
generation time roughly in half.

---

## 6. Failure handling

| Failure | Fix |
|---|---|
| Face or hairstyle changes between clips | Paste the continuity clause verbatim; use the saved character still as the first frame |
| A non-African face appears | Reject the clip; add the exclusion to the negative prompt |
| Camera drift | Add `locked camera, no zoom pan tilt or rotation`; move the effect to the subject |
| Text garbled in generation | Remove all text from the prompt; build it in the editor |
| A generated score or certificate appears | Reject the clip. Records are real or absent |
| Effect looks decorative | Re-read the selection matrix; the category must mean something |
| The post promises an outcome | Rewrite the payoff as a process, not a guarantee |
| Post underperforms | Check 3s hold first. Low hold = hook. High hold + low completion = payoff |

---

## 7. Repo hygiene

- Commit posts as they are written; the file number in the message.
- Never hand-edit generated files.
- Update the standing instruction in the same commit as the evidence.
- When a rule conflicts with a newer decision, update the manual in the same
  commit. Never leave the repo self-contradictory.
- Keep `_SHARED/` identical to the template repo. Project choices go in
  `02_BRAND_SKIN.md`, never in `_SHARED/`.
