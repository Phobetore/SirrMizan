# Commands

Everything SirrMizan can do. Every command works both with the prefix (`!` by default) and as a `/slash` command. Admin commands need the Manage Server permission. The prefix shown is the default; each server can change it with `/setprefix`.

## Rolling

| Command | Prefix form | What it does |
|---|---|---|
| `/roll [expression] [target]` | `!roll` · `!r` | Roll dice with an expression like `2d6+3`. You can append a target name and it shows on the result. |

The expression grammar is documented in [dice-syntax.md](dice-syntax.md).

## Personalization

| Command | Prefix form | What it does |
|---|---|---|
| `/setcolor <color>` | `!setcolor <color>` | Choose your preferred embed color. |
| `/getcolor` | `!getcolor` | Show your current preferred color. |
| `/setrollshort <on\|off>` | `!setrollshort [on\|off]` | Toggle short single-line roll output for yourself. |
| `/forgetme` | `!forgetme` | Delete the data the bot stores about you: your embed color and compact-output setting. |

## Server settings (admin)

| Command | Prefix form | What it does |
|---|---|---|
| `/defaultroll <expression>` | `!defaultRoll <expr>` | Set a server-wide default dice expression, used when someone types a bare `!r`. |
| `/setlang <lang>` | `!setlang <en\|fr\|de\|es>` | Set the bot's language for this server. Available: en, fr, de, es. |
| `/setprefix <prefix>` | `!setprefix <prefix>` | Set a custom command prefix for this server. |

## Help

| Command | Prefix form | What it does |
|---|---|---|
| `/help` | `!help` · `!h` | Show the full list of commands, in the server's language. |

## Notes

- Everything works in direct messages too, so you can roll privately before committing to that attack.
- The bot reads the commands addressed to it and nothing else. No message content is stored. See the [privacy policy](https://sirrmizan.threatchaos.org/en/privacy/).
