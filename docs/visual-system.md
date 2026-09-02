# Visual system

The profile presents itself as a record, because the work is about records.

## Palette

| Token | Light | Dark | Contrast on its ground |
|---|---|---|---|
| Ink / paper | `#111417` | `#F4F1EA` | 16.38:1 |
| Body text | `#3A362F` | `#D8D3C8` | above 12:1 |
| Muted label | `#5C5750` | `#9AA3A8` | 6.34:1 / 7.20:1 |
| Accent | `#276671` | `#78C4CF` | 5.77:1 / 9.32:1 |
| Rule | `#C9C2B4` | `#3A4247` | decorative, non-text |

One accent only. A second decorative hue is not added unless it carries semantic or accessibility weight.

## Masthead

`assets/masthead-light.svg` and `assets/masthead-dark.svg` are the same 1000x260 composition with the
palette inverted. They are served through a `<picture>` element so GitHub selects by
`prefers-color-scheme`, and the `img` element carries the light variant as the fallback plus alt text
that repeats the name and thesis, so the page reads correctly with images disabled.

The rule beneath the thesis is a row of linked blocks with the final block filled in the accent. It is
a hash chain: each record references the one before it, which is the mechanism the work is built on.
It is structure, not ornament.

No external fonts, no scripts, no remote references, no tracking. Type is set in widely available
system stacks with generic fallbacks. At GitHub's content width the name renders near 52px and the
smallest label near 11px.

## Constraints

- No badges, statistics cards, streak widgets, trophies, contribution animations, typing effects,
  skill bars, or technology logo walls.
- No emoji, and no em dashes in prose.
- Every claim names the file that proves it.
- Numbers that go stale live in repository READMEs with a verification date, not on the profile.
