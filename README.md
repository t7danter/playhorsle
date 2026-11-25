# Horsle

A guide to **Horsle** — a five-letter word game where the answer is never a mystery: it is always **HORSE**.

> Play it here: **https://playhorsle.com/**

---

## What this is

Horsle keeps the Wordle format — five letters, six guesses, green/gold/gray feedback — and removes the guessing of the *word*. The answer is fixed and stated up front, so the game becomes about **the route you choose**: solve it in one row, or build a longer, more elaborate grid first.

- Five letters, six guesses, free, no account
- Runs in the browser, no download
- The board sits above the guide, so returning players can type immediately

Play is not about finding a hidden word. It is about deciding what kind of result you want to produce.

## Quick start

1. Open https://playhorsle.com/
2. Type any valid five-letter English word, press **Enter**
3. Read the feedback, then either submit **HORSE** and finish, or keep building
4. Use **Play again** after the round ends

No timer, no daily streak on the fixed-answer modes.

## How a round works

- Enter a five-letter word with the on-screen keyboard or a physical keyboard, then press Enter.
- A **valid** guess fills a row and reveals feedback for each letter.
- An **incomplete** entry (fewer than five letters) or a **word outside this version's dictionary** leaves the row editable and does **not** spend a guess. Typos are free.
- Submitting **HORSE** wins immediately — you do not have to use all six rows.
- Six valid guesses without HORSE ends the round as a loss and reveals the answer.
- Finished boards stop accepting letters. You can then check statistics, share the pattern, or start again.

## Reading the three clues

| Symbol | Color | Meaning |
| --- | --- | --- |
| ✓ | Green | Letter and position both match |
| ↔ | Gold | The letter exists in the answer, but somewhere else |
| − | Gray | No unused copy of that letter remains |

Every tile carries a symbol and a text label as well as a color, so the clue does not depend on color vision. Settings offers a higher-contrast palette.

The on-screen keyboard keeps the **strongest** clue found for each letter during the round — a later gray copy never erases a green clue you already earned.

## Repeated letters

Each letter in the answer can support only one match. HORSE has exactly one H, one O, one R, one S and one E. The game matches exact positions first, then spends the remaining copies on letters found elsewhere, scanning left to right.

**ROSES** against HORSE → `R↔ O✓ S↔ E↔ S−`

O is in the right place. R, the first S and E belong elsewhere. HORSE contains only one S, and that copy is already used, so the final S gets a minus.

**EERIE** against HORSE → `E− E− R✓ I− E✓`

The last E takes the only E in HORSE because its position is correct. The earlier E tiles receive nothing.

## Worked examples

| Guess | Result |
| --- | --- |
| HORSE | All five match — instant win |
| HOUSE | H, O correct; S, E correct; U absent |
| WORSE | O, R, S, E correct; W absent |
| CURSE | R, S, E correct; C, U absent |
| SHORE | E correct; S, H, O, R all belong elsewhere |
| STORE | E correct; S, O, R elsewhere; T absent |
| CHORE | E correct; H, O, R elsewhere; C absent |
| PLANT | No letters in HORSE — a full gray row, still a valid guess |
| QUICK | All absent — a real word need not share any letter |

Opening words worth trying: **STARE** (S and R elsewhere, E correct, T and A absent) and **CHORE** (familiar letters, different positions). There is no optimal opener — the answer is already known, so no starting word grants an advantage.

## Modes

| Mode | Behaviour |
| --- | --- |
| **Classic** | One ongoing board, saved in the browser. Leave mid-word and your input returns. "Play again" unlocks after a win or loss. |
| **Unlimited** | "New game" is available even mid-round. Abandoned boards are not losses. Separate stats from Classic. |
| **Horsedle** (daily) | A *hidden* answer for each UTC date, new puzzle at 00:00 UTC. HORSE is a fine opener here, not the answer. Finished boards lock until the next date and daily streaks apply. |

Classic and Unlimited share the same fixed answer and letter rules, but their saved progress and statistics are tracked separately. Only Horsedle has streaks — the fixed-answer modes are available any time, so a daily counter would imply a restriction that does not exist.

## Sharing and statistics

- **Copy result** puts an emoji grid built from your real feedback on the clipboard.
- **Share result** opens the device share sheet where supported, falling back to copying.
- **Download image** generates a PNG in the browser with the mode, score and tile pattern — it is created locally and never uploaded.
- If automatic copying is blocked, a selectable text box lets you copy manually.

The statistics panel shows completed games, win percentage and the distribution of successful guess counts. A one-guess win lands in the first bar. Losses count toward games played and win percentage but are not added to a successful-guess bar. Reopening a finished result does not count as another game.

## Mobile, keyboard and accessibility

- On phones the board and keyboard share one centered area — tap letters, use delete to correct, tap Enter to submit.
- Physical keyboard: letter keys, Backspace, Enter.
- `Tab` moves between controls; Enter or Space activates a focused button; Escape closes dialogs and returns focus to the opening control.
- Reduced-motion preferences are respected and letter feedback is exposed as text.

## Common input problems

- **Enter does nothing** — the row has fewer than five letters, or the word is not in the dictionary. Read the message under the board; the row stays editable.
- **Extra letters seem ignored** — five cells is the limit. Use Backspace or the on-screen delete key.
- **Spaces, punctuation, numbers** — not accepted, and not counted as guesses.
- **Typing after a finished round** — the keyboard is intentionally disabled. Use *Play again* (Classic) or *New game* (Unlimited); a finished daily board waits for the next UTC puzzle.
- **Progress disappears** — guesses and settings live in this browser only. Blocked storage, cleared site data or a different device loses the record. There is no account sync.

## Dictionary

This version uses a filtered five-letter subset of the **CMU Pronouncing Dictionary**. It accepts many everyday English words and some less common ones, but it is not a full English dictionary and not the official Wordle word list. A rejected word never costs a guess.

## Repository purpose

This repo explains how Horsle works — the scoring rules, repeated-letter edge cases, mode differences and sharing flow. It is a guide, not the game's source code.

Official site: **https://playhorsle.com/** · Daily puzzle: **https://playhorsle.com/horsedle/** · Unlimited: **https://playhorsle.com/unlimited/**
