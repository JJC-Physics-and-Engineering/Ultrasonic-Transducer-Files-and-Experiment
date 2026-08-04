# Ultrasonic Transducers for the Introductory Physics Laboratory

Open design files, build instructions, and lab activities for a set of low-cost
ultrasonic transmitter/receiver probes used to teach acoustics in introductory
physics laboratory courses.

Each probe is a piezoelectric ultrasonic transducer mounted in a 3D-printed
stand with banana-jack terminals, so it can be driven from an ordinary function
generator and read on an ordinary oscilloscope. The stands clamp to a rail or
meter stick, which makes it straightforward to run quantitative experiments on
the speed of sound, diffraction, and interference with equipment already
present in most teaching labs.

Two frequencies are supported: **25 kHz** and **40 kHz**. Transmitters and
receivers are matched sets — a 25 kHz transmitter must be paired with a 25 kHz
receiver, and likewise for 40 kHz. Color- or shape-coded shrouds make the pairs
easy to tell apart at a glance.

---

## What's in this repository

| Folder | Contents |
| --- | --- |
| [`Part Files And Blueprints/`](Part%20Files%20And%20Blueprints) | CAD source and exports for every printed and cut part: Autodesk Inventor (`.ipt`), STEP (`.stp`), STL, 3MF, and dimensioned PDF blueprints. Also contains the laser-cut slit plates (`.dwg`/`.dxf`). |
| [`3D Print Settings/`](3D%20Print%20Settings) | Recommended slicer settings and plate-orientation screenshots for each printed part. |
| [`Assembly Instructions/`](Assembly%20Instructions) | Parts list with supplier links, required tools and skills, and a photo-illustrated step-by-step build guide. |
| [`Lab activities/`](Lab%20activities) | Student-facing lab handouts — the original experiments plus revised versions written for these transducers, and equipment instructions for the function generator and oscilloscopes. |

---

## Parts to print, cut, and buy

### 3D-printed parts

| Part | Purpose |
| --- | --- |
| Transmitter + Receiver Stand | Holds the transducer and the banana jacks; mounts to a rail or ruler |
| Shrouds (25 kHz T/R, 40 kHz T/R) | Cover the wiring and identify the frequency and role of each probe |
| Ruler square | Reference square for positioning probes along a ruler/rail |
| Slit holder | Holds the laser-cut slit plates upright for diffraction experiments |

All prints were developed on a **Bambu Lab A1** using otherwise standard
profiles. Per-part settings live in `3D Print Settings/<part>/`. In brief:

- Stands, ruler square, and slit holder: 4 wall loops, 30 % cubic infill.
- Shrouds: 2 wall loops, 15 % cubic infill.
- Supports are **on** only for the transmitter/receiver stand; orientation for
  that print matters — see the included example-plate screenshot.
- Several of these prints lift off the plate. A glue stick on the build plate
  is strongly recommended.

Anywhere a part has a **4 mm hole**, it is sized for an M3 heat insert and
thumb screw so the part can be clamped to a rail or ruler.

### Laser-cut parts

Single-slit (λ/4, λ/2, 1λ, 2λ) and double-slit plates are provided for both
25 kHz and 40 kHz, as `.dwg` and `.dxf`. Cut from **20″ × 12″ × 1/8″ plywood**;
choose a plywood with as little resin as possible, since resin-heavy stock cuts
poorly and smokes badly. Laser cutters use proprietary software, so no machine
settings are included — import the DXF into whatever your cutter uses. See
[`Part Files And Blueprints/Slit experiments/READ ME.txt`](Part%20Files%20And%20Blueprints/Slit%20experiments/READ%20ME.txt).

### Purchased parts

Full parts list with supplier links: [`Assembly Instructions/Part List.docx`](Assembly%20Instructions/Part%20List.docx).

**Essential:** ultrasonic transducers (25 kHz and/or 40 kHz transmitter and
receiver pairs), banana jacks with nuts, 18 AWG wire, PLA or PETG filament.
**Optional:** M3 heat inserts, a heat-insert soldering tip, and M3 × 18 mm
thumb screws for rail mounting.

---

## Building a probe

You will need basic soldering skill, basic familiarity with heat inserts, and
patience. Tools: soldering iron and solder, heat-insert tip, wire strippers,
adhesive (super glue, hot glue, or PLA glue), and — highly recommended —
curved needle-nose pliers.

The build is six steps, each with photos in
[`Assembly Instructions/INSTRUCTIONS/`](Assembly%20Instructions/INSTRUCTIONS):

1. **Remove supports** from the printed stand.
2. **Insert heat inserts** into the 4 mm holes.
3. **Insert the transducer.** These are polarized — the positive (black-based)
   prong goes on the right. Press fit or glue.
4. **Insert the banana jacks.** Getting the nuts on without bent needle-nose
   pliers is genuinely painful.
5. **Solder.** Work close to the transducer body and keep the iron moving —
   it is easy to melt the plastic around the jacks or the transducer. Trim the
   transducer prongs short enough that the shroud will seat.
6. **Fit the shroud**, matching it to the transducer's frequency and role.
   Hot glue keeps the probe serviceable; super glue or PLA glue is permanent.

`Assembly Instructions/INSTRUCTIONS/Additional Ideas/` shows how a school logo
can be embedded in the stand (much longer print) or printed separately and
glued on (faster, slightly less clean).

---

## Lab activities

The handouts in [`Lab activities/`](Lab%20activities) are Word documents intended
to be edited for your own course.

**`Original versions from NIU/`** — the source experiments these activities were
built from, along with rewrites tracking the changes made:

- *Experiment 3 — Sinusoidal Motion: The Oscilloscope*
- *Experiment 10 — Speed of Sound* (wavelength via Lissajous figures)
- *Experiment 47 — Acoustic Diffraction and Interference* (single-slit
  diffraction, two-slit interference, Lloyd's mirror, transducer radiation
  pattern)

**`Updated lab activities/`** — revised for these transducers and for modern
benchtop equipment:

- *New speed of sound* — pulse–echo timing. The transmitter is driven in burst
  mode, the reflection off a movable flat surface is timed on the scope, and a
  linear fit of position vs. Δt/2 recovers *c* ≈ 343 m/s.
- *OG Speed of Sound* — the classic wavelength-based version, for comparison.
- *Equipment Instructions* — step-by-step operation of the function generator
  and of both oscilloscope models used in the lab.

Additional activities are planned, including Lloyd's mirror, two-slit
interference, single-slit diffraction, shape detection, airflow between
transducers, and the Doppler effect.

---

## Getting started

1. Print one stand and one shroud per probe, using the settings in
   `3D Print Settings/`. Remember that probes are used in matched pairs.
2. Order the transducers, banana jacks, wire, and (optionally) heat inserts and
   thumb screws from the parts list.
3. Build each probe following `Assembly Instructions/`.
4. Laser-cut the slit plates and print the slit holder and ruler square if you
   plan to run the diffraction and interference activities.
5. Adapt the handouts in `Lab activities/` to your course, checking the
   resonant frequency of the transducers you actually bought.

---

## Repository notes

- CAD is provided as native Inventor `.ipt` alongside neutral STEP and STL, so
  parts can be modified in most CAD packages.
- `.bak`, `.dwl`, and `.dwl2` files in the slit folders are AutoCAD backup and
  lock artifacts; the `.dwg` and `.dxf` files are the ones you want.
- Some folder and file names use the spelling "Reciever". These are preserved
  as-is so paths continue to match the CAD assemblies and instructions.

## Authors and acknowledgments

<!-- TODO: add student and faculty contributors, institution, and any grant or
     program support. -->

The original lab experiments derive from the physics laboratory manual used at
Northern Illinois University and reference T. D. Rossing, *The Science of Sound*.

## License

<!-- TODO: choose a license. For a project like this, a split license is common:
     e.g. CERN-OHL-S or CC BY-SA 4.0 for the hardware and design files, and
     CC BY-NC-SA 4.0 or CC BY 4.0 for the lab handouts. -->
