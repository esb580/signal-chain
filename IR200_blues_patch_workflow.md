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

### Patch B — PAF Gibson / 70s Vox Crunch (Memory TBD)
**Guitar:** Gibson / PAF humbuckers
**Target tone:** Warm, mid-forward 70s Brian May-style crunchy blues — thick harmonic sustain with treble punch

**Inspiration:** Brian May's Queen tone: Vox AC30 driven by a treble booster (Rangemaster), producing distinctive throaty midrange, harmonic richness, and controlled overdrive through amp input drive rather than pedal distortion. Paired with Gibson PAF humbuckers for thick, warm tone.

#### IR-200
| Parameter | Value | Notes |
|-----------|-------|-------|
| Amp | VOX AC30 | Captures the classic 70s crunch — natural breakup at moderate gain. AC30 pairs beautifully with humbucker thickness. |
| **OUT MODE** | **STEREO** | **Key: Use CABINET A and B in stereo spread across left/right speakers.** This creates width and depth, avoiding a centered, mono-ish tone. |
| **CABINET A** (LEFT) | 212 DIAMOND D57+R121-S | VOX AC30 cabinet (Celestion G12M Greenbacks) with dual mics: Shure SM57 + Royer R-121. Warm, balanced. Goes to your left speaker. |
| **CABINET B** (RIGHT) | 212 DIAMOND CND87-S | **Different mic: Neumann U87 condenser** — brighter, more presence. Creates stereo image width: warm on left, bright on right. The stereo pair creates a 3D soundstage. |
| Gain | 65 | Higher than Twin Reverb patch — AC30 gains authority through amp input drive, not pedal grit. This pushes the preamp into natural compression and mild saturation (the Brian May secret). |
| Level | 35 | Raised vs. clean patch — compensates for higher gain and maintains tape-like presence without digital harshness |
| Bass | 55 | Slight boost — humbuckers are naturally dark, and AC30s are warm. Just above center to keep low-mid body without boom. |
| Mid | 65 | Key setting. AC30s shine in midrange — this lifts the "throat" that makes the tone sing. Humbuckers + AC30 mids = Brian May spank. |
| Treble | 55 | Moderate — AC30 doesn't need the treble lift a Fender does. The STEREO pair already provides sparkle and presence. This slight peak avoids harshness. |
| Ambience | OFF / STEREO | All reverb from RV-6, BUT set AMBIENCE MODE to STEREO for spatial width through the reverb. |
| Send/Return | ON — Before Cabinet | Treble Booster in loop (simulating Rangemaster placement) |

#### Critical Setup: Stereo Output Configuration

To maximize this patch, **you MUST configure the IR-200 for stereo output:**

1. **IR-200 OUTPUT connections:**
   - OUTPUT A/MONO → LEFT SPEAKER (Master Volume Controller, L input)
   - OUTPUT B → RIGHT SPEAKER (Master Volume Controller, R input)

2. **IR-200 Menu Settings (per memory — these must be saved to patch):**
   - Press **[MENU]**, navigate to **CABINET**
   - Set **OUT MODE → STEREO** (not MONO MIX)
   - This sends CABINET A to OUTPUT A (left), CABINET B to OUTPUT B (right)
   - Navigate to **AMBIENCE**
   - Set **MODE → STEREO** (not MONO)
   - This makes the reverb spread across both channels

3. **Why this matters:**
   - MONO MIX would sum both cabinets together — you'd lose the stereo image and all the depth
   - STEREO MODE preserves the left/right separation, creating width and a 3D soundstage
   - The RV-6 then receives both L/R channels and applies reverb across the stereo field

Without stereo output configured, you'll have one amazing blended tone — but you'll be throwing away half the IR-200's potential.


This replicates the Rangemaster treble booster's role: drive the AC30's input to push it into saturation without adding distortion itself.

| Knob | Setting | Notes |
|------|---------|-------|
| Drive | 6–7 / 10 | Higher than the SRV patch. The booster's job is to push the AC30 input hard — this creates the natural overdrive and sustain. |
| Tone | 8 / 10 | Bright. Treble boosters always add presence. The AC30's natural warmth + humbucker thickness + bright boost = balanced. Treble cuts through without harshness. |
| Level | 8–9 / 10 | Very high. This is the "secret" of the Brian May tone — the booster output level drives the amp's preamp stage into compression and harmonic bloom. Set it just slightly lower than full to preserve headroom and tone definition. |

**Why these settings — The STEREO Cabinet Pairing Strategy:**

The IR-200 can run two separate cabinets simultaneously: CABINET A to OUTPUT A (left speaker), CABINET B to OUTPUT B (right speaker). This is far more powerful than a single centered cabinet.

- **LEFT (CABINET A): 212 DIAMOND D57+R121-S** — Royer ribbon + SM57 dual mic. Warm, balanced, full-bodied. Sets the foundation of tone.
- **RIGHT (CABINET B): 212 DIAMOND CND87-S** — Neumann U87 condenser mic. Bright, detailed, airy. Adds sparkle, presence, and width.

**Why this works for Gibson PAF + AC30:**
The ribbon mic (left) gives the PAF's natural warmth a home. The condenser (right) provides the cutting detail and presence that keeps a warm tone from sounding dull. Together: warm + bright = 3D, articulate, alive tone with stereo width. This is how Queen and 70s studios actually recorded — one warm mic, one bright mic, blended.

**Physical setup requirement:** Your OUTPUT A goes to LEFT SPEAKER, OUTPUT B goes to RIGHT SPEAKER. The RV-6 then receives both L/R in stereo, adding spatial reverb on top. This creates a theatrical, three-dimensional tone that a mono cabinet simply cannot match.

The Tube Screamer's bright tone curve mimics a Rangemaster treble booster when the drive and level are stacked high. The AC30 model's natural sag and compression at high input levels recreates the "push" behavior of the real amp.

#### RV-6 Reverb
| Parameter | Setting | Notes |
|-----------|---------|-------|
| Mode | Plate | Classic studio reverb — adds space without muddying the thick midrange tone |
| Time | 6 | Slightly longer than Patch A — humbuckers' sustain benefits from extended plate verb |
| Tone | 6 | Slightly brighter plate character — the dual mic cabinet (SM57+R121) already has good balance, so subtle brightening adds air without thinness |
| Effect Level | 4 | More subtle than clean patch — overdrive tone doesn't need as much reverb for definition |

#### Performance Notes
- **Guitar volume sweet spot:** Turn guitar volume back to 6–7/10 for cleaner, jangly lows (like Brian May's arpeggios). Push to 9–10 for thick, overdriven solos.
- **Booster interaction:** This patch shines with the Tube Screamer booster engaged. If you need a second "cleaner" variation, duplicate this patch and turn the Send/Return OFF for a pure AC30 tone without booster.
- **Comparison to Patch A:** Patch A (Twin Reverb + Strat) is cool and clean. Patch B (AC30 + PAF) is warm and crunchy — think "Bohemian Rhapsody" rhythm section energy vs. "Layla" fingerpicking.


