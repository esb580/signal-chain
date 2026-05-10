# Rig Settings Reference

Hardware configuration, patch settings, and pedal values for the blues rig.

---

## IR-200 Key Settings

| Parameter | Setting | Notes |
|-----------|---------|-------|
| Amp type | Twin Reverb | Classic clean Fender platform for blues |
| Ambience | 0 / OFF | Using RV-6 for reverb instead |
| Bass | Nearly off | IR sim is very boomy — cut aggressively |
| Send/Return | ON | Blues Driver + Echo live here |
| Send/Return Position | Before Cabinet | Most natural sounding placement |
| Output | Stereo A + B | TRS cables to RV-6 stereo in |

---

## Blues Driver BD-2 — SRV-style Settings

| Knob | Setting | Notes |
|------|---------|-------|
| Drive (Overdrive) | 3–4 / 10 | Low — just kissing dirt |
| Tone | 6–7 / 10 | Brighter than you'd think — cuts through |
| Level | 7–8 / 10 | High — pushes the amp input stage hard |

The high output level is what makes it sing into a clean Twin sim. The pedal acts more as a clean boost with grit than a heavy overdrive — pushing the amp's input stage rather than adding distortion itself.

---

## Saving a Patch — Memory Slot 120

Use slot 120+ for personal patches, leaving lower factory presets untouched.

1. Dial in your sound
2. Press **[MENU] + [EXIT]** simultaneously → WRITE UTILITY screen
3. Push knob under **"WRITE"**
4. Turn **[AMP]** knob to select slot 120
5. Push **[MEMORY]** knob to confirm
6. Name it (suggested: `TWIN BLS` / `SRV RIG` / `BLUES 1`)
   - `[AMP]` knob = changes letter
   - `[CABINET]` knob = moves cursor
   - `[AMBIENCE]` knob = switches ABC / abc / 123
7. Push **[MEMORY]** knob to save

> **Note:** IR-200 will NOT auto-save. Send/Return must be saved per patch.

---

## Enabling Send/Return

1. Press **[MENU]**
2. Push knob under **"MEMORY"**
3. Navigate to **SEND/RETURN**
4. Set ON/OFF → **ON**
5. Set POSITION → **Before Cabinet**
6. Save the patch

---

## RV-6 Settings

| Parameter | Setting |
|-----------|---------|
| Mode | Plate |
| Connection | Stereo in / Stereo out |
| Position in chain | After IR-200, before master volume |

---

## AB/Y Notes — Tomsline ALR-3 Liner

- True bypass passive splitter
- LED indicators: Red = Path A, Green = Path B, Yellow = both
- **Watch for ground loop hum** when running DSL20 and IR-200 simultaneously — a passive inline ground lift adapter on one cable will fix it if it occurs
- Requires 9V DC (tip negative) for LED operation only

---

## General Notes

- IR-200 ambience/reverb is OFF — all reverb from the RV-6
- Bass on the Twin Reverb sim runs very boomy — cut it aggressively
- RC-1 captures clean dry signal; overdrive is looped via IR-200 send/return so it can be engaged on top of a clean loop
- FS-6 connects to RC-1 UNDO/STOP jack (stereo TRS) — controls Stop and Undo/Redo functions
