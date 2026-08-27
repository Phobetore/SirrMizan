# Frequently asked questions

**Is SirrMizan free?**
Yes. Every command, every language, no premium tier and no vote lock.

**How do I add a dice bot to my Discord server?**
[Click Add to Discord](https://discord.com/oauth2/authorize?client_id=1044351816307048508&permissions=19456&integration_type=0&scope=bot+applications.commands), pick your server, and confirm. You need the Manage Server permission. It works right away, nothing to configure.

**How do I roll with advantage in Discord?**
`!r 2d20kh1` rolls two twenty-sided dice and keeps the highest. For disadvantage, `!r 2d20kl1` keeps the lowest.

**Does it work for Pathfinder 2e or Call of Cthulhu?**
Yes. SirrMizan is system agnostic, it rolls dice rather than enforcing rules. Pathfinder checks are `1d20+X`, Call of Cthulhu runs on `1d100`.

**Can I roll several ability scores at once?**
`!r 6#4d6kh3` gives you all six, each one rolling four dice and dropping the lowest.

**Does the bot read my messages?**
It reads commands addressed to it and nothing else. No message content is stored.

**Can I change the prefix?**
`/setprefix` sets your own. The default is `!`.

**Does it work in direct messages?**
Yes, the roller works in DMs the same way it does in a server.

**Are the rolls actually random?**
Every roll uses `secrets.SystemRandom`, a cryptographically secure generator. No result can be predicted, by anyone, including us. Details in the [README](../README.md#fair-dice-provably).

**How does it compare to Avrae, Dice Maiden or Rollem?**
Honestly, and in a table: [comparison page](https://sirrmizan.threatchaos.org/en/compare/). Short version: they are excellent at things we deliberately do not do, and vice versa.
