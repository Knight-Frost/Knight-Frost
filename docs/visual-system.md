# Visual system

The profile presents itself as a record, because the work is about records.

## Palette

| Token | Light | Dark | Note |
|---|---|---|---|
| Ink / paper | `#111417` | `#F4F1EA` on `#0F1214` | 16.4:1 and above |
| Muted label | `#6B655C` | `#9AA3A8` | above 6:1 |
| Rule | `#CFC7B7` | `#3A4247` | decorative, non-text |
| Preserved trace | `#B0A794` | `#586268` | decorative, non-text |
| Accent, slate teal | `#276671` | `#78C4CF` | the system accent |
| Correction, muted amber | `#B07D2B` | `#D8A14A` | one 8px mark, nothing else |

Two colours carry meaning and nothing else does. Teal marks the newest sealed entry. Amber marks the
one point of correction. Neither is used decoratively, and no third accent is introduced.

## Masthead

`assets/masthead-light.svg` and `assets/masthead-dark.svg` are the same 1000x340 composition with the
palette inverted, served through a `<picture>` element so GitHub selects by `prefers-color-scheme`.
The `img` element carries the light variant as its fallback plus alt text repeating the name and the
thesis, so the page still reads correctly with images disabled.

The name is set small, in letterspaced monospace, as a signature. The thesis is set large in a serif,
because the sentence is the point. Beneath both runs the trace: a line of checkpoints where, at one
place, the path lifts away to a correction and rejoins, and the original segment stays drawn
underneath it in a lighter tone. That is the invariant the work is built on, drawn rather than
described. The same trace closes each flagship visual.

No external fonts, no scripts, no remote references, no tracking. Type is set in widely available
system stacks with generic fallbacks.

## Project visuals

Composited at 1100px so that they render close to 1:1 at GitHub's content width, rather than at a
source resolution that shrinks the interface text past reading. Every pixel of interface is a real
screenshot of the application running locally against seeded synthetic data. Nothing is mocked,
redrawn, or recomposed. Each visual carries at most three moments, and its captions live outside the
image so the image itself stays large.

## Constraints

- No badges, statistics cards, streak widgets, trophies, contribution animations, typing effects,
  skill bars, or technology logo walls.
- No emoji, and no em dashes in prose.
- Every claim names the file that proves it.
- Numbers that go stale live in repository READMEs with a verification date, not on the profile.
- Limitations are stated once, in calm status language, and linked rather than repeated.
