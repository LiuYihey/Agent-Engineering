---
name: opening-motion-taste
description: >-
  A working aesthetic for openings, reveals, and choreographed motion: how the
  owner spots a false note (fake material, machine-precise movement, crowding,
  speed-up, invented gestures, visible seams) and how they resolve it (use the
  real renderer, compound existing tools, compose human imperfection, restore
  rhythm, cut ornament). Use when designing, reviewing, or tuning an intro
  sequence, product reveal, staged interface moment, or any motion that depicts
  a user at work.
---

# Opening Motion Taste

Not a theory of beauty — a working eye. It records what the owner notices, what
they compare it against, and what they change. The cases are evidence; the
principles are what transfers to the next opening.

## How to use this skill

1. **Build with real material first.** Do not polish a placeholder.
2. **Review in the owner's order** (below), not in the order you wrote code.
3. **When something feels off, find the matching case** and fix the cause, not
   the symptom.
4. **Prefer compounding tools** over hand-rolled pixels (see "Build stance").

## The owner's review order

This is the sequence in which false notes get caught. Self-review in the same
order before showing anything.

1. **Is it real?** Does this frame show the actual product, or an imitation?
2. **Is it human?** Would a skilled person move, wait, and correct like this?
3. **Is it crowded?** Does anything touch, crowd, or compete with the focus?
4. **Is it too fast or too simultaneous?** Does it feel like a machine volley?
5. **Does the gesture mean anything?** Is this an action the product actually
   owns?
6. **Is there a seam?** A flash, a blank frame, a jump, a crossfade apology?
7. **Are the last details right?** Caret, handle, selection, final frame.

Most bad openings fail at 1–3. Most "almost there" openings fail at 4–7.

## Six principles, each anchored in a real correction

### 1. Truth before beauty

**The tell:** a frame that looks plausible but is not the product.
**The fix:** replace the imitation with the real thing, even if it is harder to
stage.

The first pass hand-built a fake protein out of code. It was ugly, and worse,
it was obviously *not* the molecule the product renders. The fix was not to
draw a better fake — it was to mount the real 3D viewer and reveal it through a
mask hole. The last frame then matched the live page by construction.

- If you cannot show the real artifact, show less, not a stand-in.
- A matched font is never matched; a rebuilt layout breaks at another width.
- The last frame and the first real frame should be indistinguishable without a
  cut. A transition used to hide the difference *is* the bug.

**Test:** pause on any frame and ask, "would I be looking at a lie?"

### 2. Compound, don't reinvent

**The tell:** effort spent rebuilding what the ecosystem already does better.
**The fix:** search the stack, the dependencies, and proven libraries before
writing a single pixel of your own.

The fake protein is the canonical lesson: AI-generated visuals from zero have a
low ceiling. A real renderer (3Dmol / three.js / an existing component) raises
both the floor and the ceiling, and its output compounds — same camera, same
material, same data as the product.

- Prefer the product's own components, DOM, and measured geometry as animation
  material.
- Prefer an established library or framework for rendering, physics, easing,
  and 3D over hand-written approximations.
- Reuse what can be reused: real data, real layout, real colors.
- If you must invent a placeholder, isolate it and schedule its replacement.
- AI is good at orchestration and iteration; it is bad at inventing visual
  fidelity from nothing. Spend the intelligence on composition, not on
  re-implementing a renderer.

**Test:** "Is there a tool in this stack that already does this well?" If yes,
use it before writing your own.

### 3. Compose imperfection

**The tell:** movement that is exact, linear, or simultaneous.
**The fix:** one approach, one settle — and make the approach human.

- A person arrives *near*, travels a *curve*, and settles only when the work
  demands it — not the instant they are dispatched.
- Imperfection must be composed, not random: a different approach angle, a
  slight overshoot, a pause before commitment.
- **One approach, one settle.** Arriving, resting, then repositioning is two
  machine moves wearing a human costume.
- Simultaneous action reads as machinery. A cascade reads as collaboration.
- If it feels too fast, remove distance or stagger the beats. **Never raise
  velocity to compensate** — speed is not a fix for impatience.

**Test:** would a real person's hand produce this path, or only an interpolator?

### 4. Restraint is density control

**The tell:** labels, icons, or decoration added to make the composition
"clearer".
**The fix:** delete until the focus is undeniable.

- One focal point per frame; support should be quieter than it wants to be.
- No label restating the obvious, no icon decorating the meaningful, no caption
  narrating what the eye sees.
- Negative space is a material, not leftover room. Clearance around the focus
  is correctness, not luxury.
- Accent color is currency: spend it once, where it carries meaning.

**Test:** remove the element. If nothing is lost, it was never design.

### 5. Gestures must be native

**The tell:** an invented interaction used to explain an idea.
**The fix:** use an action the product already owns.

An underline drawn under a word was replaced by a marquee selection and a color
change — because selecting and recoloring is what a real user does, and an
underline is a diagram of an idea. The same rule produced drag handles, caret
tracking, and window strokes.

- Select, drag, type, toggle, commit — never invent a gesture for legibility.
- Every gesture needs a visible cause and a visible effect.
- If the viewer needs a legend, the gesture is wrong.

### 6. Detail and handoff are the proof

**The tell:** a flash, a jump, a caret one glyph early, a pointer a few pixels
off its handle.
**The fix:** treat the last five percent as the product.

- The handoff happens exactly where the eye already is: same pixel, same frame.
  No flash of the wrong content, no blank screen, no crossfade apology.
- Micro-details carry trust: the caret rests on the final glyph, the selection
  holds before it changes, the pointer matches its handle to the pixel.
- One mismatch retroactively cheapens everything around it.
- The ending is not an exit; it is the beginning of the real thing.

## Casebook: what the owner caught, and what changed

| Before | After | Transferable lesson |
| --- | --- | --- |
| Hand-coded fake protein | Real 3D viewer revealed through a mask hole | Never imitate the product; use the real renderer |
| Whole text blocks faded in | Every character typed in place | The action must match the claimed work |
| Cursor snapped to the exact work point | Off-target hover, curved approach, late settle | Precision is a machine tell |
| Six agents departed together | Staggered wave | Synchronization reads as machinery |
| Motion felt sped up | Restored original pace; spacing fixed | Never solve impatience with velocity |
| Cursor brushed the text | Offsets and clearance in empty space | Comfort is correctness |
| Underline under the accent word | Marquee selection, then recolor | Use native gestures, not diagrams |
| Logo flashed when starting | Invisible handoff | A visible transition is a defect |
| Supporting icon and caption on the wordmark | Large centered wordmark only | Restraint creates hierarchy |

## Build stance

- **Search first:** the codebase, the dependencies, the ecosystem. Most visual
  problems already have a better implementation than the one you are about to
  write.
- **Compose, don't recreate:** real components, real data, measured geometry.
- **Raise the floor with tools:** a rendering or animation library gives you a
  baseline quality that hand-rolled code rarely reaches.
- **Isolate invention:** if a placeholder is unavoidable, make it clearly
  temporary and replace it before review.
- **Verify in the real medium:** real viewport, real data, real frame. Stills
  can lie about timing; measure the motion itself.

## Iteration protocol

Fix problems in this order, because later passes cannot rescue an earlier lie:

1. **Fidelity** — real material, final-frame parity.
2. **Behavior** — human arrival, curves, one settle.
3. **Rhythm** — beats, cascades, holds, original pace.
4. **Comfort** — clearance and density around the focus.
5. **Semantics** — native gestures.
6. **Detail** — caret, handle, selection, handoff.