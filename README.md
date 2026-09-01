# Guitar Scale & Chord Trainer

## Project Status

Current prototype: **v0.2**

v0.2 is a progression-first redesign. It replaces the information-dense v0.1 scale map with a focused tool for seeing chord-specific pentatonic pathways and moving between them.

## Purpose

The app helps a guitarist use Pickup Music's diagonal pentatonic approach over chord changes:

- major chord → major-pentatonic 3-2 pathway;
- minor chord → minor-pentatonic 2-3 pathway.

The practical goal is to see where a pathway emerges from any usable root, identify notes that survive a chord change, and locate strong chord-tone landing notes without rebuilding everything by counting from a root.

## Default Example

The app opens with:

`C × 3 bars → Em × 1 bar → G × 1 bar`

For this progression it reveals:

- C major pentatonic: C–D–E–G–A
- E minor pentatonic: E–G–A–B–D
- G major pentatonic: G–A–B–D–E
- Notes across all three: D–E–G–A
- Chord tone across all three chords: G
- C to Em shared chord tones: E and G
- Em to G shared chord tones: G and B

## Main Views

### Current Pattern

- Shows one chord-specific 3-2 or 2-3 route.
- Connects the route with a line so the diagonal grouping is visually obvious.
- Distinguishes chord tones from the remaining pentatonic notes.
- Shows all roots in the selected neck area.
- Lets the user tap any root to align the route to that practical entry point.

### Transition

- Overlays the selected current and next pathways.
- Shows positions available in both routes.
- Separates positions leaving the current route from positions entering the next.
- Rings shared chord tones as strong landing-note candidates.
- States which pitch names work in both pentatonic scales even when the chosen physical pathways do not place every one at the same fret.

## Progression and Range Editing

- Three editable chord slots
- Root, major/minor quality, and 1–8 bars per slot
- Fret-range presets from open position through fret 22
- Custom ranges of up to 10 consecutive positions
- Complete selected range visible without horizontal scrolling

## Files

- `index.html` — complete dependency-free GitHub Pages application
- `README.md` — project purpose, behavior, and workflow
- `REQUIREMENTS.md` — agreed v0.2 scope and deferred features

## Deployment

1. Replace the repository-root `index.html`, `README.md`, and `REQUIREMENTS.md` with the v0.2 files.
2. Commit the changes to `main`.
3. GitHub Pages republishes automatically when it is already configured for the `main` branch and repository root.
4. Confirm that the bottom of the live page reads **Prototype v0.2**.

No build step or external dependency is required.

## Development Workflow

1. Discuss meaningful learning and interaction decisions before implementation.
2. Preserve working behavior unless an approved change requires altering it.
3. Generate complete replacement files for deployment.
4. Test the published version on an iPhone.
5. Keep GitHub as the authoritative source for the published app.
6. Tag confirmed versions as known-good checkpoints.

## Music-Theory Model

Chord-specific pentatonic notes are calculated from the chord root and quality. Major pentatonic uses degrees 1–2–3–5–6; minor pentatonic uses 1–flat-3–4–5–flat-7. Chord tones use 1–3–5 for major and 1–flat-3–5 for minor.

The pathway is calculated from the selected physical root anchor using absolute guitar pitches. This preserves the diagonal route across the B-string tuning change and prevents the route from wrapping incorrectly to a lower octave inside the displayed range.

Root anchors on strings with the same route parity reproduce the same underlying position. The interface presents every root as an entry point because that is more useful in practice than making Position 1 and Position 2 the primary choice.

## Relationship to v0.1

The full seven-note scale map, diatonic chord palette, and multi-layer chord overlay remain valid later possibilities, but they are intentionally removed from the primary v0.2 experience. The current app should first prove that it makes chord-specific 3-2/2-3 navigation and transitions easier.
