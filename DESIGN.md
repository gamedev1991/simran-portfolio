# Design

<!-- impeccable:design-schema 1 -->

## World

**Brand Tone-of-Voice Guide.** The site is built as the artifact Simran actually produces for clients — a brand voice / style guide — applied to herself. Every section is a numbered "Rule," most pairing a struck-through vague/generic phrase with the precise, provable claim that replaces it. This is a redesign that fully replaced the prior "tech bro" dark/cursor/marquee identity; nothing from that world was carried forward.

Direction was chosen through Impeccable's concept-seed roll (`node .claude/skills/impeccable/scripts/concept-seed.mjs --scope direction --mode persuade`, seed key `f786b7d6`). The dice assigned "Keynote / Stage Deck"; the user pinned this direction (the builder's own top-ranked grounded candidate) instead, which is a valid, always-available override.

## Color

- `--paper: #F3F1EC` — warm off-white ground (page background).
- `--paper-2: #EAE6DC` — slightly deeper paper, unused surface variant reserved for future hover/alt-row states.
- `--ink: #17181A` — primary text, headings, primary button fill.
- `--ink-soft: #4E4B45` — secondary body copy.
- `--ink-faint: #67635A` — tertiary/label text (kickers, meta lines, dates). Deliberately darker than a typical "muted" gray — verified ≥4.5:1 against `--paper` (measured ≈5.3:1) since small tertiary text is exactly where the previous round's contrast bug lived.
- `--rule: #D8D3C6` — hairline dividers.
- `--red: #B01E30` — the single editorial accent: strike-through marks, the rule-number "×" icon color, hover states, focus outline, link hover. Never used as small body-text color, only as line strokes, icon fills, and backgrounds paired with `--ink`/`--paper` text.
- `--green: #2F6B45` — semantic "kept/correct" mark (check icon color only, never body text).

Restrained strategy: neutrals plus one accent, appropriate for a document/guide register rather than a marketing-drenched one.

## Type

- **IBM Plex Serif** (headings, rule numbers, stat numerals, names) — self-hosted via Google Fonts. Chosen because IBM Plex was originally built as IBM's own corporate/brand typeface system: a genuine thematic fit for a "brand style guide" page, not a default reach.
- **IBM Plex Sans** (body copy, nav, labels, UI) — same family, same rationale.
- No monospace anywhere (explicit rejection from the prior "tech bro" round).

## Composition

- Cover: name as H1 (undisputed first read), tagline, a "Style Guide — Internal Reference" badge *below* the heading (not a kicker above it — the craft floor bans that pattern outright), then Rule 00 — an auto-playing (no click required) strike-through edit of a generic bio line into her real, specific positioning line.
- Rules 01–04: each pairs a struck vague claim (`.row-vague`, red strike-through line, ink-faint text) with the kept precise version (`.row-kept`, green check icon) — stats, case studies, client roster (now with the client's real logo, `assets/logos/*`), and capabilities-as-glossary.
- Colophon: book-jacket-style author note (small circular photo, `assets/simran.png`, plus a one-line bio) ahead of the closing CTA and real contact details.
- Rule-row reveals animate in via `IntersectionObserver` (ambient, scroll-triggered, no click needed); Rule 00's hero edit plays on load. Both fully honor `prefers-reduced-motion`.

## Signature interaction

The struck-vague → kept-precise edit mechanic, playing automatically as the visitor scrolls (and once, immediately, in the hero) — this is the site's one authored moment, not scattered effects, and it's the literal enactment of "editing brand language into something provable," which is Simran's actual professional craft.

## Known constraints

- Code-led build: no image generation was available in this environment, so there is no approved comp; TYPE/MATERIAL/GROUND were judged against this document instead.
- The detector runs in degraded regex-only mode here (HTML parser dependencies not installed for `impeccable`), so computed contrast was checked manually — see Color section above.
- Advisory-only em-dash density finding (10 in body text) is expected and not actioned further: most are inside Simran's real, verbatim case-study copy from `PRODUCT.md`, which this build does not rewrite.
