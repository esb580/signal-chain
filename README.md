# Signal Chain — Blues Rig

> Last updated: May 2026  
> Core platform: BOSS IR-200 · Twin Reverb sim · Stereo out

---

## Signal Flow Diagram

<!-- SVG renders natively in GitHub, Obsidian, VS Code Preview, and most markdown renderers -->

<svg width="100%" viewBox="0 0 680 1380" role="img" xmlns="http://www.w3.org/2000/svg">
  <title>Blues rig signal chain</title>
  <desc>Guitar splits at Tomsline ALR-3 Liner ABY switch: Path A to Marshall DSL20, Path B to tuner then RC-1 looper and full IR-200 rig with send/return loop (Blues Driver, Echo), USB to laptop/GarageBand, stereo to RV-6 reverb, master volume with Bluetooth input, left and right speakers.</desc>
  <defs>
    <marker id="arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
    <style>
      text { font-family: ui-monospace, "Cascadia Code", "Source Code Pro", monospace; fill: #1a1a1a; }
      .th  { font-size: 14px; font-weight: 600; fill: #1a1a1a; }
      .ts  { font-size: 12px; font-weight: 400; fill: #555; }
      .arr { stroke: #555; stroke-width: 1.5; fill: none; }
      .c-gray   > rect, .c-gray   > ellipse { fill: #f0efea; stroke: #888; stroke-width: 0.5; }
      .c-gray   > text { fill: #3a3a38; }
      .c-teal   > rect { fill: #e1f5ee; stroke: #0f6e56; stroke-width: 0.5; }
      .c-teal   > text { fill: #085041; }
      .c-blue   > rect { fill: #e6f1fb; stroke: #185fa5; stroke-width: 0.5; }
      .c-blue   > text { fill: #0c447c; }
      .c-amber  > rect { fill: #faeeda; stroke: #854f0b; stroke-width: 0.5; }
      .c-amber  > text { fill: #633806; }
      .c-coral  > rect { fill: #faece7; stroke: #993c1d; stroke-width: 0.5; }
      .c-coral  > text { fill: #712b13; }
      .c-green  > rect { fill: #eaf3de; stroke: #3b6d11; stroke-width: 0.5; }
      .c-green  > text { fill: #27500a; }
      .c-purple > rect { fill: #eeedfe; stroke: #534ab7; stroke-width: 0.5; }
      .c-purple > text { fill: #3c3489; }
    </style>
  </defs>

  <!-- GUITAR -->
  <g class="c-gray">
    <rect x="230" y="30" width="220" height="48" rx="8"/>
    <text class="th" x="340" y="54" text-anchor="middle" dominant-baseline="central">Guitar</text>
  </g>

  <line x1="340" y1="78" x2="340" y2="118" class="arr" marker-end="url(#arrow)"/>

  <!-- TOMSLINE ALR-3 ABY -->
  <g class="c-gray">
    <rect x="196" y="118" width="288" height="56" rx="8"/>
    <text class="th" x="340" y="138" text-anchor="middle" dominant-baseline="central">Tomsline ALR-3 Liner</text>
    <text class="ts" x="340" y="158" text-anchor="middle" dominant-baseline="central">True bypass ABY — splits to two paths</text>
  </g>

  <!-- PATH A: left → Marshall -->
  <path d="M196 146 L130 146 L130 214" fill="none" stroke="#555" stroke-width="1" marker-end="url(#arrow)"/>
  <text class="ts" x="80" y="180" text-anchor="middle" dominant-baseline="central">Path A</text>

  <g class="c-coral">
    <rect x="44" y="214" width="172" height="56" rx="8"/>
    <text class="th" x="130" y="234" text-anchor="middle" dominant-baseline="central">Marshall DSL20</text>
    <text class="ts" x="130" y="252" text-anchor="middle" dominant-baseline="central">Tube amp — room / stage</text>
  </g>

  <!-- PATH B: right → Tuner -->
  <path d="M484 146 L530 146 L530 214" fill="none" stroke="#555" stroke-width="1" marker-end="url(#arrow)"/>
  <text class="ts" x="566" y="180" text-anchor="middle" dominant-baseline="central">Path B</text>

  <g class="c-gray">
    <rect x="434" y="214" width="192" height="56" rx="8"/>
    <text class="th" x="530" y="234" text-anchor="middle" dominant-baseline="central">Tuner</text>
    <text class="ts" x="530" y="252" text-anchor="middle" dominant-baseline="central">Mutes signal when active</text>
  </g>

  <!-- Tuner → RC-1 -->
  <path d="M530 270 L530 310 L340 310 L340 330" fill="none" stroke="#555" stroke-width="1" marker-end="url(#arrow)"/>

  <!-- RC-1 LOOP STATION -->
  <g class="c-teal">
    <rect x="185" y="330" width="310" height="56" rx="8"/>
    <text class="th" x="340" y="350" text-anchor="middle" dominant-baseline="central">RC-1 Loop Station</text>
    <text class="ts" x="340" y="370" text-anchor="middle" dominant-baseline="central">Captures pure dry signal before any effects</text>
  </g>

  <!-- FS-6 control branch (drawn here so it renders over IR-200) -->
  <path d="M495 358 L570 358 L570 428" fill="none" stroke="#aaa" stroke-width="1" stroke-dasharray="5 4" marker-end="url(#arrow)"/>
  <text class="ts" x="580" y="392" text-anchor="start" dominant-baseline="central">CTL</text>

  <g class="c-purple">
    <rect x="484" y="428" width="172" height="56" rx="8"/>
    <text class="th" x="570" y="448" text-anchor="middle" dominant-baseline="central">BOSS FS-6</text>
    <text class="ts" x="570" y="466" text-anchor="middle" dominant-baseline="central">Dual footswitch (Undo / Stop)</text>
  </g>

  <!-- RC-1 → IR-200 -->
  <line x1="340" y1="386" x2="340" y2="446" class="arr" marker-end="url(#arrow)"/>

  <!-- IR-200 CONTAINER -->
  <g class="c-blue">
    <rect x="100" y="446" width="460" height="262" rx="12"/>
    <text class="th" x="330" y="470" text-anchor="middle" dominant-baseline="central">BOSS IR-200 — Amp &amp; IR Cabinet Sim</text>
  </g>

  <!-- Amp sim -->
  <g class="c-blue">
    <rect x="124" y="486" width="412" height="50" rx="6"/>
    <text class="th" x="330" y="506" text-anchor="middle" dominant-baseline="central">Amp sim — Fender Twin Reverb</text>
    <text class="ts" x="330" y="524" text-anchor="middle" dominant-baseline="central">Ambience: OFF · Bass: cut aggressively</text>
  </g>

  <line x1="330" y1="536" x2="330" y2="560" class="arr" marker-end="url(#arrow)"/>

  <!-- Send/Return -->
  <g class="c-amber">
    <rect x="124" y="560" width="412" height="50" rx="6"/>
    <text class="th" x="330" y="580" text-anchor="middle" dominant-baseline="central">Send / Return loop</text>
    <text class="ts" x="330" y="598" text-anchor="middle" dominant-baseline="central">Position: before cabinet · Blues Driver → Echo inside</text>
  </g>

  <line x1="330" y1="610" x2="330" y2="636" class="arr" marker-end="url(#arrow)"/>

  <!-- Cabinet IR -->
  <g class="c-blue">
    <rect x="124" y="636" width="412" height="40" rx="6"/>
    <text class="th" x="330" y="656" text-anchor="middle" dominant-baseline="central">Cabinet IR</text>
  </g>

  <!-- LEFT SIDE: Send → BD-2 → Echo → Return -->
  <path d="M124 580 L76 580 L76 678" fill="none" stroke="#aaa" stroke-width="1" stroke-dasharray="5 4" marker-end="url(#arrow)"/>
  <text class="ts" x="62" y="570" text-anchor="middle" dominant-baseline="central">Send</text>

  <g class="c-amber">
    <rect x="14" y="678" width="164" height="56" rx="8"/>
    <text class="th" x="96" y="698" text-anchor="middle" dominant-baseline="central">Blues Driver BD-2</text>
    <text class="ts" x="96" y="716" text-anchor="middle" dominant-baseline="central">Overdrive / boost</text>
  </g>

  <line x1="96" y1="734" x2="96" y2="774" class="arr" marker-end="url(#arrow)"/>

  <g class="c-amber">
    <rect x="14" y="774" width="164" height="56" rx="8"/>
    <text class="th" x="96" y="794" text-anchor="middle" dominant-baseline="central">Echo pedal</text>
    <text class="ts" x="96" y="812" text-anchor="middle" dominant-baseline="central">Delay / echo effect</text>
  </g>

  <path d="M178 802 L200 802 L200 598 L124 598" fill="none" stroke="#aaa" stroke-width="1" stroke-dasharray="5 4" marker-end="url(#arrow)"/>
  <text class="ts" x="208" y="712" text-anchor="start" dominant-baseline="central">Return</text>

  <!-- USB RECORDING -->
  <path d="M560 602 L626 602 L626 712" fill="none" stroke="#aaa" stroke-width="1" stroke-dasharray="5 4" marker-end="url(#arrow)"/>
  <text class="ts" x="632" y="656" text-anchor="start" dominant-baseline="central">USB out</text>

  <g class="c-green">
    <rect x="492" y="712" width="172" height="56" rx="8"/>
    <text class="th" x="578" y="732" text-anchor="middle" dominant-baseline="central">Laptop + dongle</text>
    <text class="ts" x="578" y="750" text-anchor="middle" dominant-baseline="central">GarageBand — record &amp; edit</text>
  </g>

  <!-- IR-200 stereo → RV-6 -->
  <text class="ts" x="232" y="732" text-anchor="start" dominant-baseline="central">Stereo TRS (A + B)</text>
  <line x1="330" y1="708" x2="330" y2="768" class="arr" marker-end="url(#arrow)"/>

  <!-- RV-6 REVERB -->
  <g class="c-teal">
    <rect x="185" y="768" width="310" height="56" rx="8"/>
    <text class="th" x="340" y="788" text-anchor="middle" dominant-baseline="central">BOSS RV-6 Reverb</text>
    <text class="ts" x="340" y="806" text-anchor="middle" dominant-baseline="central">Mode: Plate · Stereo in / Stereo out</text>
  </g>

  <line x1="340" y1="824" x2="340" y2="878" class="arr" marker-end="url(#arrow)"/>
  <text class="ts" x="356" y="853" text-anchor="start" dominant-baseline="central">Stereo L + R</text>

  <!-- MASTER VOLUME -->
  <g class="c-gray">
    <rect x="150" y="878" width="380" height="68" rx="8"/>
    <text class="th" x="340" y="902" text-anchor="middle" dominant-baseline="central">Master Volume Controller</text>
    <text class="ts" x="340" y="922" text-anchor="middle" dominant-baseline="central">L + R guitar · Bluetooth aux in</text>
  </g>

  <!-- BLUETOOTH SOURCE -->
  <g class="c-purple">
    <rect x="496" y="888" width="168" height="48" rx="8"/>
    <text class="th" x="580" y="908" text-anchor="middle" dominant-baseline="central">Bluetooth source</text>
    <text class="ts" x="580" y="926" text-anchor="middle" dominant-baseline="central">Phone / tablet / laptop</text>
  </g>
  <path d="M496 912 L530 912" fill="none" stroke="#aaa" stroke-width="1" stroke-dasharray="5 4" marker-end="url(#arrow)"/>
  <text class="ts" x="498" y="902" text-anchor="start" dominant-baseline="central">BT</text>

  <!-- Master Volume → Speakers -->
  <line x1="340" y1="946" x2="340" y2="976" class="arr" marker-end="url(#arrow)"/>
  <line x1="196" y1="976" x2="494" y2="976" stroke="#555" stroke-width="1" fill="none"/>
  <line x1="196" y1="976" x2="196" y2="1026" class="arr" marker-end="url(#arrow)"/>
  <line x1="494" y1="976" x2="494" y2="1026" class="arr" marker-end="url(#arrow)"/>

  <!-- SPEAKERS -->
  <g class="c-gray">
    <rect x="90" y="1026" width="212" height="50" rx="8"/>
    <text class="th" x="196" y="1046" text-anchor="middle" dominant-baseline="central">Left Speaker</text>
    <text class="ts" x="196" y="1064" text-anchor="middle" dominant-baseline="central">Output A</text>
  </g>
  <g class="c-gray">
    <rect x="388" y="1026" width="212" height="50" rx="8"/>
    <text class="th" x="494" y="1046" text-anchor="middle" dominant-baseline="central">Right Speaker</text>
    <text class="ts" x="494" y="1064" text-anchor="middle" dominant-baseline="central">Output B</text>
  </g>

  <!-- LEGEND -->
  <line x1="44" y1="1122" x2="72" y2="1122" stroke="#aaa" stroke-width="1" stroke-dasharray="5 4"/>
  <text class="ts" x="78" y="1122" dominant-baseline="central">Control / sidechain / digital</text>
  <line x1="340" y1="1122" x2="368" y2="1122" stroke="#555" stroke-width="1.5" fill="none" marker-end="url(#arrow)"/>
  <text class="ts" x="374" y="1122" dominant-baseline="central">Audio signal path</text>
</svg>

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
