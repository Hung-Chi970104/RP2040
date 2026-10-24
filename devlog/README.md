# Build log: Pico Computer

A fully programmable mini computer that fits in your hand. It can run Python, compile C/C++ and
control your own gadgets. No pre-built modules allowed: it's built from scratch.

I posted these as devlogs on [Hack Club Flavortown](https://flavortown.hackclub.com/projects/355) while building the project: 35 entries and 50 h 23 min of logged work, 21 Dec 2025 to 21 Apr 2026. The text is lightly edited for spelling and clarity; dates are UTC.

| # | Date | Logged | Entry |
|---|---|---|---|
| 1 | 21 Dec 2025 | 1 h 2 min | [Starting the dev board](#1--starting-the-dev-board) |
| 2 | 21 Dec 2025 | 1 h 2 min | [Schematic complete](#2--schematic-complete) |
| 3 | 21 Dec 2025 | 1 h 5 min | [Onto the PCB](#3--onto-the-pcb) |
| 4 | 22 Dec 2025 | 1 h 42 min | [Placement techniques](#4--placement-techniques) |
| 5 | 22 Dec 2025 | 1 h 8 min | [Wiring the power supply](#5--wiring-the-power-supply) |
| 6 | 22 Dec 2025 | 1 h 1 min | [Left side wired](#6--left-side-wired) |
| 7 | 22 Dec 2025 | 1 h 1 min | [Right side wired](#7--right-side-wired) |
| 8 | 22 Dec 2025 | 2 h 4 min | [Vias and a ground pour](#8--vias-and-a-ground-pour) |
| 9 | 23 Dec 2025 | 1 h 14 min | [Stuck on errors](#9--stuck-on-errors) |
| 10 | 23 Dec 2025 | 1 h 31 min | [The errors were missing vias](#10--the-errors-were-missing-vias) |
| 11 | 23 Dec 2025 | 1 h 21 min | [PCB design complete](#11--pcb-design-complete) |
| 12 | 23 Dec 2025 | 18 min | [Final touches](#12--final-touches) |
| 13 | 27 Dec 2025 | 1 h 12 min | [Pre-order checks](#13--pre-order-checks) |
| 14 | 9 Jan 2026 | 1 h 52 min | [Silkscreen, assembly parts and the 3D check](#14--silkscreen-assembly-parts-and-the-3d-check) |
| 15 | 15 Jan 2026 | 2 h 9 min | [Learning to program the RP2040 on a XIAO](#15--learning-to-program-the-rp2040-on-a-xiao) |
| 16 | 28 Jan 2026 | 55 min | [Every pin works](#16--every-pin-works) |
| 17 | 28 Jan 2026 | 2 h 27 min | [Learning to render the PCB](#17--learning-to-render-the-pcb) |
| 18 | 13 Feb 2026 | 1 h 1 min | [README, and planning V2](#18--readme-and-planning-v2) |
| 19 | 21 Feb 2026 | 2 h 0 min | [V2 schematic complete](#19--v2-schematic-complete) |
| 20 | 21 Feb 2026 | 57 min | [Footprints and rough layout](#20--footprints-and-rough-layout) |
| 21 | 21 Feb 2026 | 1 h 36 min | [Power supply routed](#21--power-supply-routed) |
| 22 | 22 Feb 2026 | 1 h 47 min | [Flash and decoupling routed](#22--flash-and-decoupling-routed) |
| 23 | 22 Feb 2026 | 1 h 42 min | [Left side routed](#23--left-side-routed) |
| 24 | 22 Feb 2026 | 1 h 36 min | [RP2040 routed](#24--rp2040-routed) |
| 25 | 22 Feb 2026 | 1 h 40 min | [Problems spotted](#25--problems-spotted) |
| 26 | 23 Feb 2026 | 1 h 42 min | [Fully routed, DRC clean](#26--fully-routed-drc-clean) |
| 27 | 24 Feb 2026 | 1 h 25 min | [Wrapping up the routing](#27--wrapping-up-the-routing) |
| 28 | 24 Feb 2026 | 43 min | [Personal touches](#28--personal-touches) |
| 29 | 27 Feb 2026 | 50 min | [Fighting a copper island](#29--fighting-a-copper-island) |
| 30 | 17 Mar 2026 | 1 h 2 min | [Test pads, and the order](#30--test-pads-and-the-order) |
| 31 | 28 Mar 2026 | 1 h 40 min | [Fixing the regulator wiring](#31--fixing-the-regulator-wiring) |
| 32 | 29 Mar 2026 | 1 h 40 min | [Switching to the RT6150B](#32--switching-to-the-rt6150b) |
| 33 | 7 Apr 2026 | 1 h 57 min | [Optimising every detail](#33--optimising-every-detail) |
| 34 | 21 Apr 2026 | 2 h 26 min | [Reflow attempt 1](#34--reflow-attempt-1) |
| 35 | 21 Apr 2026 | 1 h 36 min | [Reflow attempt 2](#35--reflow-attempt-2) |

---

## 1 · Starting the dev board
<sub>21 Dec 2025 · 1 h 2 min logged</sub>

After almost an hour reading the RP2040 datasheet and working out the basics, I completed these
parts of my dev board:

1. Imported the RP2040 and duplicated the power-supply capacitors.
2. Added a USB port and an LDO to convert 5 V to 3.3 V.
3. Added a crystal oscillator, and learned what it's for.

<p>
<img src="media/557-1.png" width="49%">
<img src="media/557-2.png" width="49%">
</p>

---

## 2 · Schematic complete
<sub>21 Dec 2025 · 1 h 2 min logged</sub>

Completed the schematic, including:

- Flash (more complicated, because I first had to understand how it works)
- I/O headers (should have been easy, but I kept making mistakes)
- Organising the schematic into blocks

<p>
<img src="media/692-1.png" width="49%">
<img src="media/692-2.png" width="49%">
</p>

---

## 3 · Onto the PCB
<sub>21 Dec 2025 · 1 h 5 min logged</sub>

Finally, the most exciting part: putting everything together on the PCB. This is far more
complicated than my previous macropad, like jumping from the beginner village straight to the boss
fight. I'm a little scared of wiring it all later, because there are so many crossings (just look at
the blue lines).

<p>
<img src="media/710-1.png" width="49%">
<img src="media/710-2.png" width="49%">
</p>

---

## 4 · Placement techniques
<sub>22 Dec 2025 · 1 h 42 min logged</sub>

After an hour and a half of hard work, I learned how to organise components based on the schematic.
Some techniques:

- Group components by the blocks in the schematic: select them together on the schematic page and
  they're selected on the PCB page too.
- Connect the main components first. This matters, because you don't want to place the capacitors
  first and then find they're in the way.

<p>
<img src="media/882-1.png" width="49%">
<img src="media/882-2.png" width="49%">
</p>

---

## 5 · Wiring the power supply
<sub>22 Dec 2025 · 1 h 8 min logged</sub>

After an hour I had aligned most of the components and started wiring the power supply. Honestly,
this was the most interesting and also the most frustrating part. Tips I picked up:

- Wire the closest pins and components first; the long-distance connections can go through vias.
- Stay patient. Very, very patient.
- Be careful with 90-degree angles (I've heard they're bad, though I'm not sure why).

<p>
<img src="media/898-1.png" width="49%">
<img src="media/898-2.png" width="49%">
</p>

---

## 6 · Left side wired
<sub>22 Dec 2025 · 1 h 1 min logged</sub>

After another hour of struggle, I wired up all the pins on the left. A very painful process. Nothing
much to add: staying patient is the best advice.

<p>
<img src="media/1049-1.png" width="49%">
<img src="media/1049-2.png" width="49%">
</p>

---

## 7 · Right side wired
<sub>22 Dec 2025 · 1 h 1 min logged</sub>

More good progress: I finished wiring the right side, which was much easier than the left. I also
fixed some wiring on the left to reduce the vias under the RP2040, because I need that space to
connect 3V3.

<p>
<img src="media/1084-1.png" width="49%">
<img src="media/1084-2.png" width="49%">
</p>

---

## 8 · Vias and a ground pour
<sub>22 Dec 2025 · 2 h 4 min logged</sub>

Added lots of vias and rerouted many things. I also added a GND pour, but there's still plenty of
work left, and GND still isn't fully connected.

<p>
<img src="media/1334-1.png" width="49%">
<img src="media/1334-2.png" width="49%">
</p>

---

## 9 · Stuck on errors
<sub>23 Dec 2025 · 1 h 14 min logged</sub>

This is driving me nuts. Can anyone help me with all these errors? I'm still very inexperienced.

<p>
<img src="media/1497-1.png" width="49%">
<img src="media/1497-2.png" width="49%">
</p>

---

## 10 · The errors were missing vias
<sub>23 Dec 2025 · 1 h 31 min logged</sub>

After an hour and a half of debugging, I realised the errors came from a lack of vias. Why vias
matter:

- They connect the front and back GND pours.
- Make sure every component's GND pin has at least two spokes.

So if you hit the same problem, add enough vias and you'll be fine.

<p>
<img src="media/1741-1.png" width="32%">
<img src="media/1741-2.png" width="32%">
<img src="media/1741-3.png" width="32%">
<img src="media/1741-4.png" width="32%">
</p>

---

## 11 · PCB design complete
<sub>23 Dec 2025 · 1 h 21 min logged</sub>

Finally! After hours of struggle, I completed the PCB design and exported the Gerber files. All
that's left is to order it from JLCPCB.

<p>
<img src="media/1784-1.png" width="32%">
<img src="media/1784-2.png" width="32%">
<img src="media/1784-3.png" width="32%">
<img src="media/1784-4.png" width="32%">
</p>

---

## 12 · Final touches
<sub>23 Dec 2025 · 18 min logged</sub>

Cleaned everything up and added some final touches:

- Pushed everything to GitHub.
- Uploaded a 3D model to Printables.

<p>
<img src="media/1803-1.png" width="49%">
<img src="media/1803-2.png" width="49%">
</p>

---

## 13 · Pre-order checks
<sub>27 Dec 2025 · 1 h 12 min logged</sub>

Before ordering the PCB:

- Double-checked every route and cleaned up some traces.
- Changed all traces from 0.2 mm to 0.18 mm.
- Added LEDs on VBUS (5 V), 3V3 and GPIO2 (GPIO2 was a random pick).

<p>
<img src="media/3219-1.png" width="32%">
<img src="media/3219-2.png" width="32%">
<img src="media/3219-3.png" width="32%">
<img src="media/3219-4.png" width="32%">
</p>

---

## 14 · Silkscreen, assembly parts and the 3D check
<sub>9 Jan 2026 · 1 h 52 min logged</sub>

- Added a silkscreen design with my logo and name.
- Chose parts for JLCPCB assembly (a lot of time went into avoiding extended parts).
- Fixed the 3D model in the PCBA viewer, which turned out to matter a lot (compare images 2 and 3).
- Rerouted GPIO24, RUN and GPIO25.
- Swapped the positions of the 3V3 and 1V1 capacitors.

<p>
<img src="media/9131-1.png" width="32%">
<img src="media/9131-2.png" width="32%">
<img src="media/9131-3.png" width="32%">
</p>

---

## 15 · Learning to program the RP2040 on a XIAO
<sub>15 Jan 2026 · 2 h 9 min logged</sub>

Learned how to program the RP2040 using a XIAO RP2040, since my own board hadn't arrived yet.
Tutorial I followed:
https://www.youtube.com/watch?v=07vG-_CcDG0&list=PLWNDWPAClRVoo0Z-QtCkXuM15jdb2Q54N&t=820s

- Installed the Thonny IDE (originally I planned to use MicroPython).
- Switched to CircuitPython so I could use VS Code.
- Troubleshot the CircuitPython extension (it was bad, and I gave up).
- Eventually noticed I could just use the serial monitor in VS Code (see my Lapse).

Video: https://hc-cdn.hel1.your-objectstorage.com/s/v3/4d0905c78ba392b4_img_0659.mp4

<p>
<img src="media/12183-1.png" width="49%">
<img src="media/12183-2.png" width="49%">
</p>

---

## 16 · Every pin works
<sub>28 Jan 2026 · 55 min logged</sub>

I tested all the pins, and they all worked perfectly.

- Installed CircuitPython.
- Tested every pin.
- Used a multimeter to confirm everything worked.

<p>
<img src="media/17076-2.jpg" width="70%">
</p>

▶ [Video (7.8 MB)](media/17076-1.mp4)

---

## 17 · Learning to render the PCB
<sub>28 Jan 2026 · 2 h 27 min logged</sub>

For the past two hours I was learning to render my PCB. It might not sound important, but it looks
extremely cool.

- Installed pcb2blender.
- Watched tutorials.
- Imported new models for the USB port.

I didn't know how to use Blender at all, and learned it along the way.

<p>
<img src="media/17123-1.jpg" width="32%">
<img src="media/17123-2.png" width="32%">
<img src="media/17123-3.png" width="32%">
</p>

---

## 18 · README, and planning V2
<sub>13 Feb 2026 · 1 h 1 min logged</sub>

Spent almost an hour updating the README and planning V2. The improvements:

- Larger flash (preferably 16 MB)
- Two Schottky diodes to allow an external power supply
- Replace the original voltage regulator with an RT6154AGQW
- Add a reset button
- Larger LED resistors (the LEDs are hard on the eyes)

See the highlighted parts. I also decided to reroute everything.

<p>
<img src="media/21945-1.png" width="49%">
<img src="media/21945-2.png" width="49%">
</p>

---

## 19 · V2 schematic complete
<sub>21 Feb 2026 · 2 h 0 min logged</sub>

Completed the schematic. What changed:

- Replaced the W25Q16JVUXIQ (2 MB) with the W25Q64JVXGIQ (8 MB, a huge upgrade).
- Replaced the MCP1700x-330xxTT linear regulator with the RT6154AGQW buck converter, which is much
  more efficient.
- Added a Schottky diode to allow an external power supply.
- Added a RESET button.
- Changed the 33 pF crystal capacitors to 15 pF to match the crystal I ordered.

My custom dev board will be much more powerful and resilient.

<p>
<img src="media/24294-1.png" width="70%">
</p>

---

## 20 · Footprints and rough layout
<sub>21 Feb 2026 · 57 min logged</sub>

Assigned footprints (replacing many 0402 parts with 0603 and 0805) and roughly placed the layout.

<p>
<img src="media/24319-1.png" width="70%">
</p>

---

## 21 · Power supply routed
<sub>21 Feb 2026 · 1 h 36 min logged</sub>

Finished routing the power-supply section. It went much more smoothly than I expected, probably
thanks to the layout.

<p>
<img src="media/24589-1.png" width="70%">
</p>

---

## 22 · Flash and decoupling routed
<sub>22 Feb 2026 · 1 h 47 min logged</sub>

Completed routing the flash and the 1 µF capacitors.

- The two 1 µF capacitors need to sit very close to pins 44 and 45.
- This flash chip is much larger than the original (but it has four times the storage).
- Widened the data lines (I've heard that's better).

<p>
<img src="media/24615-1.png" width="70%">
</p>

---

## 23 · Left side routed
<sub>22 Feb 2026 · 1 h 42 min logged</sub>

Finished routing the left side, applying what I've learned over the past few weeks:

- The BOOT button can take a long trace, since it's very low-frequency.
- Gave 3V3 wide traces throughout (0.5 mm where possible, otherwise 0.3 mm).

Not much else to say; it's routing.

<p>
<img src="media/24663-1.png" width="70%">
</p>

---

## 24 · RP2040 routed
<sub>22 Feb 2026 · 1 h 36 min logged</sub>

Just finished routing the RP2040 and most of the rest. There isn't much to routing beyond trial and
error.

<p>
<img src="media/24852-1.png" width="70%">
</p>

---

## 25 · Problems spotted
<sub>22 Feb 2026 · 1 h 40 min logged</sub>

Things I noticed:

- An unwanted copper island on the back, directly under the flash.
- Unconnected GND because of the very tight layout.

I somewhat regret not switching to a 4-layer board (though it's also more expensive, so we'll see).

<p>
<img src="media/24952-1.png" width="70%">
</p>

---

## 26 · Fully routed, DRC clean
<sub>23 Feb 2026 · 1 h 42 min logged</sub>

Finally finished routing the entire board and cleaned up the DRC. I'll add a few more final touches
before ordering, like cleaning up the silkscreen.

<p>
<img src="media/25017-1.png" width="70%">
</p>

---

## 27 · Wrapping up the routing
<sub>24 Feb 2026 · 1 h 25 min logged</sub>

Time to wrap this up. I cleaned up all the routing; the changes:

- Moved the diode to the top-right corner instead of squeezing it in beside the power regulator.
- Moved as many traces to the front as possible to keep the back copper clean.
- Added thicker 0.5 mm traces.
- Removed two islands from the back copper (it's sacred).
- Cleaned up the DRC once again.

<p>
<img src="media/25306-1.png" width="70%">
</p>

---

## 28 · Personal touches
<sub>24 Feb 2026 · 43 min logged</sub>

- Added back silkscreen.
- Picked purple as the main colour.
- Started picking parts from LCSC.

I'm really trying to polish this as much as I can.

<p>
<img src="media/25534-1.png" width="49%">
<img src="media/25534-2.png" width="49%">
</p>

---

## 29 · Fighting a copper island
<sub>27 Feb 2026 · 50 min logged</sub>

Spent a lot of time fixing this island. I did my best, but still had to compromise on many traces
because of the large flash chip.

<p>
<img src="media/26236-1.png" width="70%">
</p>

---

## 30 · Test pads, and the order
<sub>17 Mar 2026 · 1 h 2 min logged</sub>

Spent an hour on the following:

- Added test pads (in case the RT6154AGQW fails again).
- Managed to prevent the copper island.
- Ordered the board after cleaning up the DRC.

<p>
<img src="media/32242-1.png" width="70%">
</p>

---

## 31 · Fixing the regulator wiring
<sub>28 Mar 2026 · 1 h 40 min logged</sub>

Another big update. I didn't actually reflow the board, because it wouldn't have worked anyway. I
spent some time fixing the RT6154A connection: I had connected VIN directly to VINA, which would
short-circuit the whole thing. I also changed the angle of the GPIO24 resistor so the 100 nF
capacitor could sit closer to 3V3. Let's hope it works perfectly this time.

<p>
<img src="media/35328-1.png" width="70%">
</p>

---

## 32 · Switching to the RT6150B
<sub>29 Mar 2026 · 1 h 40 min logged</sub>

I caught another crucial mistake: the Schottky diode I picked can only handle up to 1 A, so the
RT6154A is way overkill and not even necessary. I switched to the RT6150B. Hopefully it works; I was
already traumatised.

<p>
<img src="media/35910-1.png" width="70%">
</p>

---

## 33 · Optimising every detail
<sub>7 Apr 2026 · 1 h 57 min logged</sub>

Locked in for another two hours. What I did:

- Fixed the same power-supply route.
- Rerouted GPIO traces to make more room for the 0.1 µF capacitors.
- Moved GPIO traces from the back to the top so the back layer is cleaner.
- Replaced the 0603 LEDs with 0402.

Basically I was optimising everything, down to tiny details; I want this version to be the best
quality possible. Now I wait about ten days for the board. I also re-rendered it; it might not look
very different, but it is.

<p>
<img src="media/38544-1.png" width="70%">
</p>

---

## 34 · Reflow attempt 1
<sub>21 Apr 2026 · 2 h 26 min logged</sub>

I only spent an hour populating and reflowing the board, and to my surprise it worked perfectly. I
loaded the UF2 file, ran `print("Hello World")`, and it did its job. Then the 3V3 indicator went out
after I heard a little crack from the USB-C port, and everything stopped working; the board no
longer responded to my computer. Devastating.

How I tried to fix it:

- Went over the MCU, USB-C and flash again with the soldering iron, but nothing helped.
- Replaced the inductor, in case it was saturating and letting too much current through.
- Swapped the USB-C port, because not even the 5 V indicator was lighting up (I should have
  measured the resistance first).
- Replaced the RT6150B, since the regulator was honestly the biggest suspect.

Finally I removed the RP2040 and the flash to measure the resistance again. It was still normal
(over 100 kΩ), but 3V3 kept reading 0.04 V. It was already 2 a.m., so I had to sleep; I'll update
once the new board is done.

<p>
<img src="media/42796-1.jpg" width="70%">
</p>

---

## 35 · Reflow attempt 2
<sub>21 Apr 2026 · 1 h 36 min logged</sub>

After an hour of reflowing and repair, my board works flawlessly. To repeat: this board has four
times the flash of the previous one (8 MB) and supplies up to 800 mA, which is plenty for any
peripheral. A huge success, and the GPIOs all work. It's so clean and good-looking (just look at the
purple silkscreen).

<p>
<img src="media/42811-1.jpg" width="70%">
</p>
