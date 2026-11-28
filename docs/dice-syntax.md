# Dice syntax

Two ways to roll: the prefix (`!r`, customizable per server) or the `/roll` slash command. Both accept exactly the same expressions, and the syntax is identical in all four languages.

## The full grammar

| Expression | Meaning |
|---|---|
| `!r 1d20` | One 20-sided die. Exactly the same as `/roll 1d20`. |
| `2d6` | Several dice at once: two six-sided dice. |
| `1d20+5` | Add or subtract a flat number. |
| `2d6+1d4` | Mix different dice and modifiers in one roll. |
| `4d6kh3` | Keep the 3 highest dice (`kh`). The usual way to roll up stats. |
| `2d20kh1` | Advantage: roll two d20 and keep the higher one. |
| `2d20kl1` | Disadvantage: keep the lower of the two (`kl`). |
| `1d20+5 adv` | Advantage in a word, after a roll of one die: here `2d20kh+5`. `dis` keeps the lower. Each language's word works too: avantage, Vorteil, ventaja. |
| `4d6dl1` | Drop the lowest die (`dl`). |
| `5d6dh1` | Drop the highest die (`dh`). |
| `3d6!` | Exploding dice: a die that lands on its maximum is rolled again and added to itself. |
| `6#4d6kh3` | Roll the whole expression several times. `6#` gives six stat lines in one message. |
| `1d20 Goblin` | Add a name after the roll and it shows up on the result. |
| `!r` | On its own, falls back to the server's default roll, if one was set with `/defaultroll`. |

## Reading a result

The bot shows every die it rolled, marks which ones were kept, then the modifiers, then the total. Nothing is hidden and nothing is interpreted: whether 17 beats the DC is between you and your game master.

Dropped dice stay visible with a strike, so an advantage roll always shows both d20s. That is deliberate: in several systems (Pathfinder 2e degrees of success, Call of Cthulhu criticals) the individual die matters as much as the total.

## Limits

Chosen so a typo cannot flood a channel:

- 100 dice per term
- 20 repeats per command (`20#...` is the ceiling)
- 100 characters per expression
- Keep and drop must leave at least one die
- A die explodes at most 10 times in a row

## What is deliberately absent

No success counting, no character sheet variables, no per-system rules. The core stays small so that one syntax serves every game and nothing surprises you mid-session. The reasoning is laid out in the [README's philosophy section](../README.md#philosophy-a-dice-bot-not-a-rules-engine).

## Per-game walkthroughs

The website carries full guides with worked examples, in four languages:

- [D&D 5e](https://sirrmizan.threatchaos.org/en/dnd-5e-dice-bot/): advantage, ability scores, death saves, spell damage, a copy-paste cheat sheet
- [Pathfinder 2e](https://sirrmizan.threatchaos.org/en/pathfinder-2e-dice-bot/): degrees of success, multiple attack penalty, flat checks
- [Call of Cthulhu](https://sirrmizan.threatchaos.org/en/call-of-cthulhu-dice-bot/): percentile rolls, bonus and penalty dice, Sanity

Or try any expression live in the [browser playground](https://sirrmizan.threatchaos.org/en/roll/), no Discord needed.
