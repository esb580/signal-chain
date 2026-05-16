# IR-200 Blues Rig — Patch Building Workflow

## Overview

This guide covers the core workflow for building and saving a blues patch on the BOSS IR-200 using a virtual amp sim combined with a custom loaded cabinet IR. This is the foundational skill for getting the most out of the IR-200 rig.

---

## The Rig

```
Guitar
  ↓
RC-1 Loop Station
  ↓
IR-200 (Amp Sim + Cabinet IR)
  │   Amp Sim:   Fender Twin Reverb (built-in)
  │   Cabinet:   Princeton P10R (USER IR — loaded via IR Loader)
  │   Send/Return: Tube Screamer (pre-cabinet)
  │   Ambience:  OFF
  ↓ (Stereo TRS — Output A and B)
Boss RV-6 Reverb (Stereo In / Stereo Out — Plate mode)
  ↓
Master Volume Controller
  ↓
Left Speaker (A) + Right Speaker (B)
```

---

## Key Concept — Amp Sim vs Cabinet IR

The IR-200 separates amp and cabinet into two independent stages:

| Stage | What it does | Source |
|-------|-------------|--------|
| **Amp Sim** | Preamp character, EQ, gain staging | IR-200 built-in models |
| **Cabinet IR** | Speaker + mic coloring | Built-in cabs OR loaded USER IRs |

You can mix and match any amp model with any cabinet IR. A USER IR file captures the cabinet and microphone only — no amp character. This means you can pair a Twin Reverb amp sim with a Princeton P10R 10" speaker IR for a unique hybrid tone not possible with a real rig.

---

## Loading Princeton P10R IRs (Pre-requisite)

Done once via the BOSS IR Loader app on macOS.

### Which files to use from the IR pack

| Decision | Choice | Reason |
|----------|--------|--------|
| Sample rate | **48k** | IR-200 runs at 48kHz natively |
| Length | **200ms** | Sufficient for speaker cab IRs — 500ms is overkill |
| Mic | Start with **121** (ribbon) or **121+57** (dual) | Best for creamy sparkly single coil blues tone |

### IR Loader steps

1. Connect IR-200 to Mac via USB and power on
2. Open BOSS IR Loader — select **IR-200** (not DAW CTRL) and click OK
3. Drag WAV files into USER IR slots 1–10
4. Recommended loading order:

| Slot | File | Character |
|------|------|-----------|
| USER IR 1 | WT PrinceVerb P10R 121.wav | Warm ribbon — dark and creamy |
| USER IR 2 | WT PrinceVerb P10R SR25.wav | Ribbon variant |
| USER IR 3 | WT PrinceVerb P10R 57.wav | Bright and present |
| USER IR 4 | WT PrinceVerb P10R 160.wav | Alternative placement |
| USER IR 5 | WT PrinceVerb P10R 7B.wav | Mid-forward, punchy |
| USER IR 6 | WT PrinceVerb P10R 121+57.wav | Dual: warm + sparkle |
| USER IR 7 | WT PrinceVerb P10R 121+SR25.wav | Dual: ribbon blend |
| USER IR 8 | WT PrinceVerb P10R 160+57.wav | Dual: presence blend |
| USER IR 9 | WT PrinceVerb P10R 160+SR25.wav | Dual: ribbon presence |
| USER IR 10 | WT PrinceVerb P10R 160+7B.wav | Dual: punchy blend |

"Not used in memory" is expected — slots are loaded but not yet assigned to a patch.

---

## Saved Patch — Memory 120

| Parameter | Value | Notes |
|-----------|-------|-------|
| **Memory slot** | 120 | |
| **Name** | RTS-CLN-1 ~ | ~ = voiced for Strat |
| **Amp** | Twin Reverb | |
| **Cabinet** | USER IR 6 | Princeton P10R — 121+57 dual mic (ribbon + SM57) |
| **Gain** | 50 | Clean headroom with some push |
| **Level** | 25 | |
| **Bass** | 50 | |
| **Mid** | 50 | |
| **Treble** | 60 | Slight top end lift for Strat single coils |
| **Ambience** | OFF | All reverb from RV-6 |
| **Send/Return** | ON — Before Cabinet | Tube Screamer in loop |

---

## Building the Patch from Scratch

### Step 1 — Connect the rig
```
Guitar → RC-1 → IR-200 → RV-6 → Master Volume → Speakers
```

### Step 2 — Start from any existing patch
You will set all parameters manually. The current patch in memory 120 doesn't matter — you're overwriting everything.

### Step 3 — Set the Amp Sim to Twin Reverb

- Press **[AMP] knob** to enter amp edit
- Turn **[AMP] knob** to select **Twin Reverb**
- Set parameters to match saved patch:

| Parameter | Value | Notes |
|-----------|-------|-------|
| Gain | 50 | Clean headroom with some push |
| Level | 25 | |
| Bass | 50 | |
| Middle | 50 | |
| Treble | 60 | Slight top end lift for Strat |

### Step 4 — Turn Ambience OFF

- Long-press **[AMBIENCE] knob** to toggle OFF
- All reverb comes from the RV-6 at the end of the chain

### Step 5 — Enable Send/Return for Tube Screamer

- Press **[MENU]**
- Push knob under **"MEMORY"**
- Navigate to **SEND/RETURN**
- Set **ON/OFF → ON**
- Set **POSITION → Before Cabinet**

This places the Tube Screamer between the amp sim and the cabinet IR — exactly where it sits in a real amp's effects loop.

### Step 6 — Select the Princeton Cabinet IR

- Press **[CABINET] knob** to enter cabinet edit
- Turn **[CABINET] knob** to scroll to **USER IR 6** (121+57 dual mic — the chosen cab for this patch)

**Mic character guide for auditioning alternatives:**

| IR | Mic | Character |
|----|-----|-----------|
| USER IR 1 | 121 (ribbon) | Warmest — most "creamy" |
| USER IR 3 | 57 | Brightest — most presence |
| USER IR 6 ✓ | 121+57 dual | Best of both — **saved patch uses this** |

### Step 7 — Dial in the Tube Screamer (SRV settings)

Once the cabinet is chosen, kick on the Tube Screamer:

| Knob | Setting | Notes |
|------|---------|-------|
| Drive | 3–4 / 10 | Low — just kissing dirt |
| Tone | 6–7 / 10 | Brighter than you'd think |
| Level | 7–8 / 10 | High — pushes the amp hard |

The high output level is the key. SRV used the Tube Screamer as a clean boost that pushed the amp's input stage rather than adding distortion itself.

### Step 8 — Set RV-6 Reverb

| Parameter | Setting |
|-----------|---------|
| Mode | Plate |
| Time | To taste — start subtle |

---

## Saving to Memory 120

Once everything sounds right:

1. Press **[MENU] + [EXIT]** simultaneously → WRITE UTILITY screen appears
2. Push knob under **"WRITE"**
3. Turn **[AMP] knob** to select destination slot **120**
4. Push **[MEMORY] knob** to confirm
5. Name the patch using the knobs:
   - **[AMP] knob** — changes letter
   - **[CABINET] knob** — moves cursor left/right
   - **[AMBIENCE] knob** — switches ABC / abc / 123
   - This patch saved as: **RTS-CLN-1 ~** (~ denotes Strat voicing)
6. Push **[MEMORY] knob** to save

---

## Recalling the Patch

1. Push **[MEMORY] knob** to move cursor to memory number
2. Turn **[MEMORY] knob** counter-clockwise to **120**
3. Full blues rig loads up ready to play

---

## Important Notes

- IR-200 does **not auto-save** — always write after any change you want to keep
- Unsaved data is lost on power off
- Send/Return ON/OFF is a **per-patch memory parameter** — must be saved for each patch separately
- USER IR slots are cabinet/mic only — amp character always comes from the IR-200's built-in amp sim
- "Not used in memory" in IR Loader = normal; means the slot is loaded but not yet referenced by a saved patch. Once you save a patch pointing to that slot it will show as used.

---

## Alternative: Real Amp Preamp → IR-200 Cabinet

Instead of the built-in Twin Reverb sim, you can run a real amp's preamp through the IR-200 cabinet IRs:

```
Guitar
  ↓
Real Amp (e.g. Marshall DSL20) — FX Loop SEND only
  ↓
IR-200 INPUT
  │  Amp Sim: OFF
  │  Cabinet: Any USER IR
  ↓
RV-6 → Master Volume → Speakers
```

- Turn the IR-200 **Amp Sim OFF** — you're feeding a preamp signal, not a guitar signal
- The real amp's power amp section is bypassed and sits idle
- This uses the real amp's preamp character with a high quality cabinet IR instead of the amp's physical speaker cab

---

## Appendix 1 — Patch Reference Sheets

Quick reference for all saved patches. Full build workflow above applies to each — only the values change.

---

### Patch A — RTS-CLN-1 ~ (Memory 120)
**Guitar:** Strat (single coil)
**Target tone:** Creamy sparkly edge-of-breakup clean blues

#### IR-200
| Parameter | Value |
|-----------|-------|
| Amp | Twin Reverb |
| Cabinet | USER IR 6 — Princeton P10R 121+57 dual mic |
| Gain | 50 |
| Level | 25 |
| Bass | 50 |
| Mid | 50 |
| Treble | 60 |
| Ambience | OFF |
| Send/Return | ON — Before Cabinet |

#### Send/Return — Ibanez Tube Screamer (SRV settings)
| Knob | Setting |
|------|---------|
| Level | 7–8 / 10 |
| Tone | 6–7 / 10 |
| Drive | 3–4 / 10 |

#### RV-6 Reverb
| Parameter | Setting |
|-----------|---------|
| Mode | Plate |
| Time | 5 |
| Tone | 5 |
| Effect Level | 5 |

---

### Patch B — VOX-CLN-1 H (Memory 121)
**Guitar:** Gibson / PAF humbuckers
**Target tone:** 70s–80s British crunch — controllable with Gibson volume knob, Vox AC30 character

#### Tone Research — Who This Is Based On
Brian May ran his AC30 on the Normal channel with volume at 10 and the cut control all the way off for maximum treble, using the guitar's volume control to dial in textures from sparkling clean to thick dirty distortion. The treble booster drove the amp's input stage into natural power tube saturation — not a preamp gain sound, but a pushed amp sound. The Celestion Blue — the AC30's native speaker — delivers dampened attack, warm lows, mellow upper-mids and brilliant bell-like top-end, developing beautiful musical compression when pushed. Jimmy Page's approach was similar — gain at 6, bass at 8, mids at 6, treble at 7 on his Marshall Plexi, with PAF humbuckers doing most of the heavy lifting. The common thread: moderate-high gain from a pushed amp, mid-forward EQ, and guitar volume as the primary tone sculptor.

#### Cabinet Choice — Why and What to Load Next
The Princeton P10R (USER IR 1–10) is a 10" speaker and works, but for authentic British crunch the correct speaker is a **12" Celestion Blue** (AC30 native) or **Celestion Greenback** (Marshall native). The Greenback is voiced with extra broad midrange attack and restrained high end that fosters punchy chords and searing leads without fizz.

**For now (using current USER IRs):** USER IR 1 (single 121 ribbon) — warmest and most compressed of the loaded IRs, closest approximation to Celestion Blue character.

**Recommended next IR purchase:** Celestion official IR pack — Blue or Greenback. Both available at celestionplus.com. Load into USER IR 11–12.

#### IR-200
| Parameter | Value | Notes |
|-----------|-------|-------|
| Amp | Vox AC30 (or closest Vox sim available) | Normal channel character — clean platform pushed hard |
| Cabinet | USER IR 1 — Princeton P10R 121 single ribbon | Warmest/most compressed available; swap for Celestion Blue IR when loaded |
| Gain | 75 | Simulating AC30 pushed by treble booster — higher than Strat patch |
| Level | 30 | Slightly hotter than Strat patch |
| Bass | 35 | Restrained — Vox/PAF combo gets muddy fast |
| Mid | 65 | Mid-forward — the heart of British crunch |
| Treble | 70 | High — Vox character lives in the top end; guitar volume tames it |
| Ambience | OFF | |
| Send/Return | ON — Before Cabinet | Blues Driver in loop |

**Critical playing note:** Set Gibson volume to 6–7 to start. Roll back for clean, push to 10 for full crunch. This is how May and Page actually played — the amp is set for crunch, the guitar volume does the work.

#### Send/Return — Boss Blues Driver
The BD-2 here acts like the treble booster in the original rig — pushing the amp input rather than adding heavy distortion itself.

| Knob | Setting | Notes |
|------|---------|-------|
| Level | 6 / 10 | Higher than Strat patch — pushing the Vox harder |
| Tone | 4 / 10 | Darker than Strat patch — PAF humbuckers already have presence |
| Drive | 4 / 10 | Moderate — let the amp sim do the crunch work |

#### RV-6 Reverb
Plate kept shorter and drier than the Strat patch — British rock crunch is a drier, more immediate sound. May used tape delay more than reverb; this gives a sense of space without washing out the crunch.

| Parameter | Setting | Notes |
|-----------|---------|-------|
| Mode | Plate | |
| Time | 3 | Shorter than Strat patch — tighter, more immediate |
| Tone | 6 | Slightly brighter — complements the darker Blues Driver tone setting |
| Effect Level | 3 | Drier than Strat patch — British crunch sits drier in the mix |

#### H Naming Convention
`~` = Strat (single coil voicing)
`H` = Gibson humbucker voicing
Suggested name: **VOX-CLN-1 H**
