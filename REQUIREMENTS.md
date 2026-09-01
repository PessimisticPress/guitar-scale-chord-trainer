# Guitar Scale & Chord Trainer — Prototype Requirements

## Status

Prototype baseline: **v0.1**

These requirements describe the first testable version. Visual treatments are provisional and should be judged on an iPhone before they are treated as settled.

## Learning Goal

Help a self-taught guitarist see one continuous scale across the fretboard while recognizing how the most useful target notes change with the active chord.

The parent scale must remain visually stable during chord changes. Changing from G major to C major while remaining in the key of G, for example, changes the emphasized chord tones from G–B–D to C–E–G; it does not rebuild or transpose the G-major scale.

## Relationship to Guitar Fretboard Trainer

- This is a separate companion application.
- Guitar Fretboard Trainer v2.1 is a reference for visual language, TAB orientation, mobile behavior, collapsible settings, and local preference storage.
- The existing trainer files are not part of this application's codebase and must not be modified.
- The prototype remains a dependency-free, single-page application suitable for GitHub Pages.

## Prototype Scope

### Scale Map

- Standard six-string tuning: E–A–D–G–B–E.
- TAB orientation: low E at the bottom, high E at the top.
- Select a tonic and one of four scales:
  - Major
  - Natural minor
  - Major pentatonic
  - Minor pentatonic
- Default state: G major, frets 0–12, note-name display.
- Display modes:
  - Note names
  - Scale degrees relative to the parent scale
  - Dots only
- Scale-degree labels do not change when the active chord changes.
- Use correct diatonic note spelling for supported keys, including spellings such as F-sharp and E-sharp in F-sharp major.

### Fret Range

- Show the complete selected range at once with no horizontal fretboard scrolling.
- Support frets 0–22.
- Provide presets for 0–12, 5–17, and 10–22.
- Permit a custom contiguous range of no more than 13 fret positions.
- Include normal single and double fretboard position markers throughout the supported range.

### Chord-Tone Overlay

- Derive seven diatonic triads from the related parent major or natural-minor scale.
- Label every chord with both its name and Roman-numeral function.
- Display the active chord name, function, and three chord tones.
- Preserve the scale map when the active chord changes.
- Distinguish visually among:
  - ordinary scale tones;
  - the parent-scale root;
  - active chord tones;
  - the active chord root.
- Do not communicate these roles through color alone.
- When a pentatonic scale omits a tone from an active diatonic chord, display that chord tone as a hollow dashed marker and identify it as outside the selected scale.

### 3-2 / 2-3 Pathway

- Provide an optional diagonal pathway overlay based on Pickup Music's pentatonic system.
- Major-family scales use 3 notes followed by 2 notes on alternating strings.
- Minor-family scales use 2 notes followed by 3 notes on alternating strings.
- Support Position 1 beginning on the low E string and Position 2 beginning on the A string.
- On a full major or natural-minor map, the overlay identifies the related pentatonic subset.
- On a pentatonic map, the overlay identifies the playable diagonal pathway within that scale.
- Use a shape treatment in addition to color so the pathway remains identifiable without color perception.

### Interaction and Persistence

- Use large, iPhone-friendly controls.
- Keep key, scale, fret-range, and 3-2 settings in a collapsible panel.
- Keep chord switching and display-mode switching immediately available on the main screen.
- Save appropriate settings locally and restore them on the next launch.
- Settings should start collapsed even when saved values are restored.
- Include light and dark color-scheme support.

## Explicitly Deferred

- Timed progressions and Follow the Changes
- Quizzes, scoring, statistics, and adaptive practice
- Ear training
- Audio or backing-track playback
- User-authored chord progressions
- Progressive hiding of assistance
- Native iOS packaging

The prototype should be tested for musical usefulness and mobile readability before any deferred feature is added.
