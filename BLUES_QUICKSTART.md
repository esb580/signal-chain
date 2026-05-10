# BLUES RECORDING QUICK-START
### GarageBand Template — IR-200 Blues Rig

---

## BEFORE YOU PLUG IN

- [ ] Tube Screamer connected to IR-200 Send/Return jacks
- [ ] RV-6 connected to IR-200 Output A + B (stereo TRS)
- [ ] Master volume controller connected to RV-6 stereo out
- [ ] IR-200 patch 120 loaded (TWIN BLS / SRV RIG)
- [ ] RV-6 set to Plate mode
- [ ] USB cable from IR-200 to Mac (for audio interface recording)

**Power-on order:** IR-200 → RV-6 → Master Volume → Speakers (guitar amp last)

---

## STEP 1 — GARAGEBAND PROJECT SETUP

**New project every session:**

1. Open GarageBand → New Project
2. Set **Tempo** before recording anything (you cannot easily change it later)
   - Blues shuffle standard: 60–90 BPM
   - Slow blues: 45–65 BPM
   - Try 72 BPM as a starting point
3. Set **Time Signature**: 4/4 (standard) or 12/8 (shuffle feel)
4. Set **Key**: E, A, or G for blues (affects Smart Instruments and MIDI)
5. Name and Save the project immediately — `File → Save As`

**Project naming convention:** `YYYY-MM-DD_Blues-Key-BPM` (e.g. `2025-05-10_Blues-E-72`)

---

## STEP 2 — DRUM TRACK FIRST (Critical)

The drum track is your foundation. Everything you record aligns to it.

**Option A — GarageBand Drummer Track (fastest):**
1. Track → New Track → Drummer
2. Choose a drummer style (Kyle = laid-back blues/rock, Ludwig = roots/country)
3. In the Drummer Editor, set:
   - Feel slider toward **Loose** (blues breathes)
   - Complexity slider toward the **left** (sparse = more authentic)
   - Check **Shuffle** if you want a swing feel
4. Drag the drummer region to fill your song length

**Option B — MIDI Drum Pattern (from me — see DRUM TRACKS section below)**

Either way: **Lock the drummer/drum track before recording anything else.**
Track → Lock Track (prevents accidental edits)

---

## STEP 3 — BASS OR CHORD FOUNDATION

Before recording guitar, lay down a basic chord/bass reference:

**If you have a bass guitar:** Record a simple 12-bar pattern
**If not:** Use GarageBand Smart Bass or a MIDI bass track (I can generate)

A simple 12-bar-blues in E:
```
| E7  | E7  | E7  | E7  |
| A7  | A7  | E7  | E7  |
| B7  | A7  | E7  | B7  |
```

This gives you harmonic context so your guitar solos land correctly.

---

## STEP 4 — AUDIO TRACK FOR GUITAR

**Setting up the track:**
1. Track → New Track → Audio
2. Set Input to **IR-200** (it appears as a USB audio interface)
   - Select Input 1 for mono, or Input 1+2 for stereo
3. Enable **Record Enable** (red circle button on track)
4. Check your **input level** — the level meter should peak around -12dB to -6dB
   - Too hot = distortion/clipping (bad)
   - Too quiet = poor signal-to-noise ratio (also bad)
5. Turn **Monitoring OFF** (you're hearing yourself through the speakers already)

**Before hitting record:**
- [ ] Metronome is ON (Command+K toggles it)
- [ ] Count-in is ON (1-2 bar count helps you start on time)
- [ ] You can hear the drum track clearly

---

## STEP 5 — RECORDING TAKES

**The RC-1 Loop Station strategy:**
- Use the RC-1 to build your backing loop LIVE before recording into GarageBand
- OR record the RC-1 output directly as a GarageBand audio track (clean dry signal)
- Don't overthink it — just record

**Good recording habits:**
- Record in **cycles/passes** — don't try to nail everything in one take
- Use **Command+R** to quickly toggle record
- GarageBand keeps all takes — you pick the best one (Take Folder feature)
- Record a little before the phrase starts — you can trim later
- If a take is 90% good, keep it — you can punch in on the bad bar

**Take naming tip:** After recording, double-click the region and name it
(e.g. "Rhythm - Pass 1", "Solo - Lead Break")

---

## STEP 6 — BASIC EDITING

**Trim the regions:**
- Hover over the left/right edge of a region → cursor changes → drag to trim
- Remove dead silence at start/end of takes

**Align to the grid:**
- Drag regions to snap to bar/beat boundaries
- View → Snap to Grid (make sure this is ON)

**Volume automation (critical for blues feel):**
- Select a track → Mix → Show Automation (or press A)
- Draw volume curves to make quieter verses, louder choruses
- Pull solos up, rhythm guitar down when both play together

**Trim and fade:**
- End of song: select all regions → Edit → Add Fade Out
- Or draw the automation curve down manually (more control)

---

## STEP 7 — VOLUME MATCHING BETWEEN TRACKS

This is one of the most important steps beginners skip.

**Target levels (rough guide):**
| Track | Peak Level |
|-------|-----------|
| Drums | -6 to -3 dB (loudest element) |
| Bass | -12 to -8 dB |
| Rhythm Guitar | -14 to -10 dB |
| Lead Guitar / Solo | -10 to -6 dB (sits above rhythm) |

**Method:**
1. Solo each track individually — listen for whether it sounds right in isolation
2. Mute all tracks → unmute one at a time from drums out
3. Use the **fader** (the vertical slider on each track) to set relative levels
4. Use the **Master Volume** at the bottom of the mixer for overall output

**Key blues mixing principle:** Leave space. If two guitars are playing,
one should be quieter. Lead always wins. Drums sit underneath everything.

---

## STEP 8 — STEREO PLACEMENT

Give each instrument its own space in the stereo field:

| Track | Pan Setting |
|-------|------------|
| Kick / Snare | Center (0) |
| Hi-hat | Slight right (+15 to +20) |
| Rhythm guitar | Left (-20 to -30) |
| Lead guitar | Center or slight right |
| Bass | Center (always) |
| Reverb returns | Wide left+right |

**Your RV-6 is already giving you stereo reverb** — your guitar output
is naturally wide. GarageBand will record it as a stereo track if you
use both inputs (1+2). This sounds great.

Pan is the knob on each track (the small dial, not the fader).

---

## STEP 9 — RHYTHM CHECK BEFORE FINAL MIX

Listen to the full track and ask:

- [ ] Does the guitar track start exactly on beat 1 of the bar?
- [ ] Do chord changes land on the right beats?
- [ ] Does the solo phrase feel early or late? (Nudge the region left/right)
- [ ] Are fills and turnarounds landing with the drummer?

**Fixing timing:** Select a region → Edit → Quantize (for MIDI)
For audio, you can nudge regions by holding Option and pressing left/right arrows.

---

## STEP 10 — EXPORT / BOUNCE

When the track is done:

1. **Set the cycle region** to cover exactly the song length (yellow bar at top)
2. Share → Export Song to Disk
3. Choose: **AIFF or WAV** at 24-bit 44.1kHz (highest quality for archiving)
4. Name it with the same convention as the project

**Keep the GarageBand project file** — you'll want to come back and remix.

---

## QUICK REFERENCE — KEYBOARD SHORTCUTS

| Action | Shortcut |
|--------|---------|
| Play / Stop | Space |
| Record | R |
| Toggle Metronome | Command+K |
| Undo | Command+Z |
| Show/Hide Mixer | Command+M |
| Show Automation | A |
| Loop Region | L |
| Split Region at Playhead | Command+T |
| Zoom In/Out | Command+Right/Left |
| Solo Track | S (click track) |
| Mute Track | M (click track) |

---

## NOTES ON THIS RIG

- The IR-200 appears as a USB audio interface in GarageBand
- Your reverb (RV-6) is happening in hardware — do NOT add reverb plugins in GarageBand on top of it (double reverb sounds bad)
- Your amp sim (Twin Reverb) is in the IR-200 — do NOT add amp sim plugins in GarageBand
- You can add **light compression** in GarageBand if desired (use the Channel EQ or Compressor plugin sparingly)
- The stereo output from your rig gives a naturally wide, professional sound — trust it

---

*See also: GARAGEBAND_STUDY_PLAN.md for the two-weekend skill-building roadmap*
