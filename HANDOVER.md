# SIGNAL CHAIN PROJECT — HANDOVER NOTES
### From: Blues Rig v1 Project · To: Next Phase

---

## What This Project Delivered

A complete, documented blues guitar rig built around the BOSS IR-200, covering:
- Full signal chain design and rationale
- Hardware settings reference (IR-200, BD-2, RV-6, RC-1, FS-6, AB/Y)
- macOS driver setup and GarageBand integration
- Per-session recording quick-start checklist
- Two-weekend GarageBand study plan
- Signal chain SVG diagram
- Manual source references

The GitHub repo at `esb580/signal-chain` is the living document for this work.

---

## VISION FOR THE NEXT PHASE

### From a Single Rig to a Rig Library

The blues rig documented here should be **demoted from a standalone project to one entry in a larger rig library**. The top-level concept is a personal catalog of complete music systems — each documented to the same standard — that can be referenced, compared, and maintained independently.

```
RIG LIBRARY (top level)
│
├── Blues Rig          ← this project (v1 complete)
│   └── IR-200 · BD-2 · RV-6 · RC-1 · FS-6 · Twin Reverb sim
│
├── [Future Rig 2]     ← different tools, same documentation standard
│   └── e.g. acoustic rig, amp-in-the-room rig, pedalboard-only rig
│
├── [Future Rig 3]     ← different genre or use case
│   └── e.g. fingerpicking / slide / jazz clean
│
└── [Future Rig N]
```

Each rig in the library would have:
- Its own signal chain diagram
- Hardware settings reference
- GarageBand (or DAW) setup notes
- Quick-start checklist tuned to that rig
- Its own patch/preset documentation

The **README at the library level** becomes an index — what rigs exist, what genre/purpose each serves, and what gear they use — rather than being the home of a single rig's details.

---

## TODOS FOR THE NEXT PROJECT

### 1. Restructure the Repo as a Rig Library

- [ ] Rename or reorganize the repo to reflect the top-level "rig library" concept (e.g. `home-studio` or `rig-library`)
- [ ] Move all current blues rig files into a `/blues-rig/` subdirectory
- [ ] Create a new top-level `README.md` that serves as the library index
- [ ] Define a standard folder/file template that each new rig will follow so documentation stays consistent across rigs

---

### 2. MIDI Drum Pattern Library

The study plan promises MIDI drum patterns but no actual content exists in the repo yet. This is high value — it's the foundation every recording session builds on.

- [ ] Create a `/midi/` folder (either at rig level or library level)
- [ ] Add at least one 12-bar blues drum pattern per feel:
  - Straight 4/4 (Chicago style)
  - Shuffle / swing feel
  - Slow blues (half-time)
  - Uptempo boogie
- [ ] Document patterns as Piano Roll note references (text format) so they can be entered in GarageBand without a MIDI file import
- [ ] Consider adding a 12-bar bass line reference in the same folder for each key (E, A, G)

---

### 3. Add the Two New Recording Documents to the Repo

Created at the end of the blues rig project but not yet committed:

- [ ] Add `BLUES_QUICKSTART.md` — per-session recording checklist
- [ ] Add `GARAGEBAND_STUDY_PLAN.md` — two-weekend learning roadmap
- [ ] Update the README table of documents to include both

---

### 4. Troubleshooting / Known Issues Document

Hard-won lessons are currently scattered across the rig settings and notes sections. Consolidate into a single reference.

- [ ] Create `TROUBLESHOOTING.md` at the blues rig level
- [ ] Capture known issues and fixes, including:
  - Ground loop hum when running DSL20 and IR-200 simultaneously (passive ground lift fix)
  - IR-200 Twin Reverb sim very boomy — cut bass aggressively
  - IR-200 does not auto-save — patch changes lost on power off
  - Send/Return must be saved per patch (not a global setting)
  - IR-200 auto-off setting — disable if mid-session power loss occurs
  - RV-6 double-reverb warning — do not add software reverb in GarageBand on top of hardware reverb
  - RC-1 loop data lost if power is cut while LOOP indicator is blinking

---

### 5. RC-1 Loop Strategy Notes

The RC-1 is central to the workflow but its operational approach is only described conversationally, not written up as a proper reference.

- [ ] Add an RC-1 section to the blues rig settings or quick-start covering:
  - How the loop fits into the GarageBand recording workflow (RC-1 loop as a live performance layer vs. recording the RC-1 output as a GarageBand track)
  - Overdubbing strategy — when to use it vs. recording separate GB tracks
  - Using the FS-6 for stop/undo during a session
  - Clean loop + Tube Screamer lead workflow explanation

---

### 6. Library-Level Template

Once the structure exists, define a standard template so future rigs document themselves consistently.

- [ ] Create `_RIG_TEMPLATE/` folder with blank versions of:
  - `SIGNAL_CHAIN.md`
  - `RIG_SETTINGS_REFERENCE.md`
  - `QUICKSTART.md`
  - `signal_chain.svg` (blank diagram)
- [ ] Define what goes in the library-level README index (rig name, genre, key gear, status)

---

## NOTES ON CONTINUITY

- The BOSS IR-200 manual PDFs attached to the original project are the reference source — keep them accessible or link to the BOSS manual pages documented in the blues rig README
- The signal chain SVG (`blues_rig_signal_chain_v7.svg`) is the visual anchor for the blues rig — preserve it as a versioned file as the rig evolves
- GarageBand is the current DAW — all recording docs assume macOS + GarageBand. If the DAW changes, the setup and quick-start docs will need a parallel version

---

*Handover prepared: May 2026 · Blues Rig v1 → Rig Library v1*
