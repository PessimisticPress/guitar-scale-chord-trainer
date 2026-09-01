# Guitar Scale & Chord Trainer — v0.2 Requirements

## Status

Current prototype: **v0.2**

This version replaces the broad v0.1 scale-map interface with a progression-first 3-2/2-3 practice tool.

## Central Learning Goal

Help a guitarist answer three immediate questions while soloing over a chord progression:

1. Where is the chord-specific 3-2 or 2-3 pentatonic pathway in this part of the neck?
2. Which notes remain available when the chord changes?
3. Which chord tones provide strong, nearby transition targets?

The interface should reveal a usable route before presenting broader scale theory.

## Progression

- Provide three editable chord steps.
- Each step has:
  - root;
  - major or minor quality;
  - bar count from 1 through 8.
- Default progression: C major for 3 bars, E minor for 1 bar, G major for 1 bar.
- Major chords use major-pentatonic 3-2 pathways.
- Minor chords use minor-pentatonic 2-3 pathways.
- Tapping a progression step makes it the active chord.
- Previous and Next controls move among the three steps.
- The transition after the third step compares it with the first step as a loop.

## Current Pattern View

- Show only the active chord's chord-specific pentatonic pathway.
- Use TAB orientation with low E at the bottom.
- Connect pathway notes with a visible route line.
- Display chord tones differently from the other pentatonic notes.
- Show every root occurrence in the selected fret range as a tappable anchor.
- Tapping a root occurrence should trace the continuous pathway aligned to that root.
- Root occurrences on later strings may reproduce one of the system's two route families; they should still be available as practical entry points.
- The selected root anchor must be clearly distinguishable from the other available roots.

## Transition View

- Compare the selected pathway for the active chord with the selected pathway for the next chord.
- Distinguish:
  - positions shared by both selected pathways;
  - positions belonging only to the current pathway;
  - positions belonging only to the next pathway.
- Give an additional ring to visible notes that are chord tones shared by both chords.
- Summarize in plain language:
  - notes contained in both pentatonic scales;
  - shared chord tones that make strong landing notes;
  - notes leaving and entering the pentatonic collection.
- Keep transition information out of Current Pattern view.

## Across-All Summary

- Calculate the intersection of all three chord-specific pentatonic scales.
- Separately calculate chord tones shared by all three chords.
- Show the result compactly near the progression.
- Do not imply that a common scale note is necessarily a chord tone.

## Fret Range

- Default to frets 3–12.
- Provide presets for 0–9, 3–12, 5–14, 10–19, and 13–22.
- Allow a custom range of no more than 10 consecutive fret positions.
- Show the complete selected range at once without horizontal fretboard scrolling.

## Interaction and Persistence

- Mobile-first, with comfortable iPhone touch targets.
- Keep progression editing and neck-range settings collapsed until requested.
- Save the progression, active step, selected anchors, fret range, and selected view locally.
- Restore saved values on the next launch while keeping editors collapsed.
- Support light and dark system appearance.

## Explicitly Deferred

- Full parent-scale map
- Diatonic chord palette
- Arbitrary progression length
- Timed playback or automated bar changes
- Audio and backing tracks
- Quizzes, scoring, and statistics
- Progressive hiding of assistance
- Native iOS packaging

These features should not be added until the progression-path and transition views prove useful in real practice.
