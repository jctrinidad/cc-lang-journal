# Kotonoha (言の葉)

A single-file Japanese language-learning journal. Type romaji on an ordinary
English keyboard and it converts live to kana — hiragana by default,
katakana when you keep Shift held down for a whole word — so you practice
reading/writing kana instead of relying on a Japanese IME's autocorrect and
prediction.

Open `index.html` directly in a browser to use it (entries save to
`localStorage`), or publish it as a Claude Artifact to get cross-device
syncing (`db` capability) and an "Ask Claude to review" button that checks
an entry's correctness and naturalness (`sample` capability).

## Features

- **Romaji → kana engine**: standard gojuon, dakuten/handakuten, youon,
  sokuon (doubled consonants), ん disambiguation, `-` for the long vowel
  mark (ー), and `x`/`l` prefixes for small kana — implemented from
  scratch in `index.html`, no dependencies.
- **Daily journal entries**: navigate by day (prev/next, a date picker, or
  jump to today), with a sidebar of past entries.
- **N5/N4 writing prompts**: a bank of ~48 prompts spanning everyday
  topics and a mix of tenses/grammar points, shown under the date and
  removable if you'd rather write about something else.
- **Autosave**: debounced saves with a visible status indicator.
- **Claude review** (when available): sends your entry to Claude for a
  gentle correctness check and more-natural phrasing suggestions.
