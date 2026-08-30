# Changelog

Every release of the deployed bot, newest first. This file is updated automatically when a release lands; the version badge in the README reads from [version.json](version.json), same source.

## v1.5.6 · 2026-08-30

Added, the weekly report measures engagement and retention

## v1.5.5 · 2026-08-29

Fixed, the public changelog stopped receiving releases

## v1.5.4 · 2026-08-28

The help was four stacked code blocks that scrolled sideways on a phone. It reads as a page now: real headings, examples that wrap, and the link to the site next to the section it belongs to, in your own accent colour. The message a server gets when the bot joins follows the same shape.

## v1.5.3 · 2026-08-28

Compact results put the total on a line of its own, so it can be found when scrolling back through a session. The expression and the breakdown move to the line beneath it.

## v1.5.2 · 2026-08-28

The die faces ship with the bot instead of being fetched from the website, so the picture beside a roll no longer depends on the site being reachable.

## v1.5.1 · 2026-08-28

Fixed the die face sitting on a grey square the first time it appeared on Android, which only cleared after restarting the app. The image travels with the message now, so there is nothing left for the client to resolve.

## v1.5.0 · 2026-08-27

Roll results rebuilt. The total is drawn as a die face, the dice and the modifiers are labelled apart, and the result reads across the message instead of stretching down the channel.

## v1.4.8 · 2026-08-08

Removed a DNS resolver workaround that had been shipped in v1.4.4. The underlying resolver issue was fixed at the infrastructure level, so the bot no longer needs to cap resolution timeouts itself.

## v1.4.7 · 2026-08-07

Reverted the version-in-presence experiment from v1.4.6. Discord shows a single activity per bot, and the "Playing /roll" hint matters more to new users than a version number.

## v1.4.6 · 2026-08-07

Showed the current version on the bot's profile. Withdrawn one release later, see v1.4.7.

## v1.4.5 · 2026-08-07

Dependency updates.

## v1.4.4 · 2026-08-06

Capped the DNS resolver timeout so slash commands stop failing when a resolver is slow. Discord gives a bot three seconds to answer; a five-second DNS timeout ate the whole budget.

## v1.4.3 · 2026-08-05

The bot posts its server count to discordbotlist.com.

## v1.4.2 · 2026-08-04

The bot posts its server count to top.gg.

## v1.4.1 · 2026-07-30

First steps of the welcome message shown when the bot joins a server.

## v1.4.0 · 2026-07-27

Reworked the help embed, added link buttons, cleaned up typography.

## v1.3.2 · 2026-06-25

Reused the HTTP session for status heartbeats and fixed the statistics aggregator.

## v1.3.1 · 2026-06-25

Accurate response-time reporting for the public status page.

## v1.3.0 · 2026-06-25

The privacy release: added `/forgetme`, stopped storing user IDs entirely, and started the Uptime Kuma heartbeat that feeds the public status page.

## v1.2.0 · 2026-06-14

Keep and drop dice (`kh`, `kl`, `dh`, `dl`), roll sets (`6#4d6kh3`), clearer help, and a presence hint that shows both the prefix and the slash command.

## v1.1.7 · 2026-06-09

The bot reports its real version instead of a placeholder, plus an internal refactor pass.

## v1.1.6 · 2026-06-08

Security hardening after an audit, and a signature gate on deployments.

## v1.1.5 · 2026-06-08

Dependency security fix (aiohttp CVE) and removal of a concurrency cap on `!roll`.

## v1.1.4 · 2026-05-23

`!roll` no longer deletes the message that invoked it.

## v1.1.3 · 2026-05-23

Release process codified: the version bump travels inside the release PR.

## v1.1.2 · 2026-05-18

New embed color, migration to a Proxmox LXC, and pull-based deployments.

## v1.1.1 · 2026-05-10

Health-check rollback and a tighter process watchdog.

## v1.1.0 · 2026-05-09

First tagged release of the current codebase.

---

Before tagged releases, the bot ran and evolved continuously. The Discord application itself dates back to November 2022.
