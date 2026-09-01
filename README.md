# Guitar Scale & Chord Trainer

## Project Status

Current interactive prototype: **v0.1.1**

This version is intended for evaluation, especially on an iPhone. Its visual hierarchy and marker treatments are deliberately provisional.

### v0.1.1 Correction

Corrected the SVG note-marker radius reference that prevented scale and chord-tone markers from rendering in v0.1. No intended behavior or music-theory rules changed.

## Purpose

Guitar Scale & Chord Trainer is a mobile-first companion to Guitar Fretboard Trainer. It helps a guitarist see a parent scale continuously across the fretboard while watching the useful target notes change as the active chord changes.

The central principle is simple: **the scale map stays in place; the chord-tone emphasis changes.**

For example, in G major:

- G major highlights G–B–D.
- C major highlights C–E–G.
- The underlying G-major scale remains G–A–B–C–D–E–F-sharp in both cases.

## Prototype Features

- Major, natural minor, major pentatonic, and minor pentatonic maps
- All 12 tonic pitch classes with musically correct contextual spelling
- Note-name, scale-degree, and dots-only views
- Seven diatonic triads labeled with chord names and Roman numerals
- Immediate chord-tone switching without moving the parent scale
- Clear identification of chord tones omitted by a selected pentatonic scale
- Optional major 3-2 and minor 2-3 diagonal pentatonic pathways
- Position 1 from the low E string and Position 2 from the A string
- Fret-range presets for 0–12, 5–17, and 10–22
- Custom ranges of up to 13 consecutive positions across frets 0–22
- TAB orientation with low E at the bottom
- Collapsible settings and locally saved preferences
- Responsive light and dark themes

## Files

- `index.html` — complete dependency-free application
- `REQUIREMENTS.md` — agreed prototype behavior and deferred scope
- `README.md` — project purpose, workflow, and current status

## Deployment

The application is designed for GitHub Pages:

1. Put `index.html`, `README.md`, and `REQUIREMENTS.md` in the repository root.
2. Commit them to the `main` branch.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.

No build step or external dependency is required.

## Development Workflow

1. Discuss and document meaningful learning or design changes before implementation.
2. Preserve working behavior unless an approved change requires altering it.
3. Generate complete replacement files for deployment.
4. Test the published version on an iPhone.
5. Treat GitHub as the authoritative source for the published application.
6. After a version is confirmed good, create a release/tag as a known-good checkpoint.

## Music-Theory Model

The application calculates scale membership from pitch classes but uses contextual note-name tables so displayed notes retain correct diatonic spelling. Triads are constructed by stacking alternating degrees of the related seven-note parent scale.

Major and major-pentatonic selections use the related major key's diatonic chords. Natural minor and minor-pentatonic selections use the related natural-minor key's diatonic chords.

When a pentatonic selection omits one of an active chord's tones, the omitted tone appears as a dashed hollow marker. This preserves an honest distinction between:

- notes in the selected scale;
- notes in the active chord; and
- notes that belong to both.

Scale-degree labels always describe the selected parent scale. They do not reset to `1` when a different chord becomes active.

## 3-2 System

The optional pathway connects the familiar pentatonic system to the larger scale map:

- Major-family maps show alternating groups of 3 and 2 notes.
- Minor-family maps show alternating groups of 2 and 3 notes.
- Position 1 begins on the low E string.
- Position 2 begins on the A string.

On a seven-note scale, the pathway highlights only the related pentatonic subset. This makes notes that exist in the parent scale but outside the familiar pentatonic pathway easy to recognize.

## Deferred Features

Follow the Changes, timed chord progressions, quizzes, progressive hiding, ear training, and audio are intentionally excluded until the Scale Map and Chord-Tone Overlay have been tested successfully.

## iOS Direction

The prototype keeps domain logic, rendering, state, and storage conceptually separate inside one file. That makes the current GitHub Pages workflow simple while reducing unnecessary coupling if the project is later rebuilt as a native iOS application.
