# Mawhoobeen — مرحلة ثالثة ورابعة

A separate curriculum track from level2/level3 ("مهرجان الطفل الموهوب للغة
القبطية والألحان" — a gifted-child festival for younger kids). `index.html`
is the entry point and opens directly on the vocab flashcards; `texts.html`
and `dialogue.html` are reached from the same 3-item bottom nav (كلمات /
نصوص / حوار). A small home icon in the header links back to the main
flashcards landing page (`../../index.html`).

Font is loaded via a relative path to the shared `NEWATH.ttf` two levels up
(`../../NEWATH.ttf`), matching how `level2/`/`level3/` already load it in
this repo.

## Source and confidence

Unlike text extracted from a real PDF text layer, this content was
transcribed from **photographed textbook pages** — there was no copyable
text to mechanically convert. The New Athanasius keycode mapping itself is
solid (cross-validated letter-by-letter against `coptic-texts`'s own
already-verified data — Lord's Prayer, vocab-level1.json, etc.), but the
*word identity* for entries not already confirmed elsewhere relies on
reading the photographed glyphs plus general Coptic vocabulary knowledge,
not a mechanical extraction. Two words visible in the photos (an unclear
"مُر" entry and a "كرازة" entry) were dropped entirely rather than guessed.

The two memorization texts (`data/sign-of-cross.json`,
`data/creed-intro.json`) differ sharply in confidence:
- **رشم الصليب** (Sign of the Cross) is the exact same line as the Lord's
  Prayer's opening ("بسم الآب والابن..."), reusing that already-verified
  keycode string verbatim — full confidence.
- **مقدمة قانون الإيمان (تين ثينو)** is a best-effort reconstruction of a
  well-known hymn from the photo plus memory, not mechanically checked.
- `data/dialogue.json` (daily-conversation phrases) is similarly best-effort.

Both of those carry `"needsReview": true`, which renders a small amber
"راجع مع المعلم" notice directly on the page — have a teacher check these
two specifically before they're used for memorization.
