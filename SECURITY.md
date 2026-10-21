# Security at YouGame

YouGame runs games, emulators and mods that anyone can make on players' computers and phones. The
code that keeps players safe from a malicious game is public on purpose, so anyone can check it:
the [desktop sandbox](https://github.com/yougame-co/yougame-sandbox) and
[YG Dolphin](https://github.com/yougame-co/orca-netplay), our fork of the Dolphin emulator. Please try to break them.

## Report a vulnerability

- **On GitHub, privately (preferred):** use **Report a vulnerability** on the Security tab of the
  repo the problem is in, or
  [this form](https://github.com/yougame-co/.github/security/advisories/new) for yougame.co, the
  desktop app or anything else. Only we see it.
- **By email:** security@yougame.co, for anything.

**Bugs in Dolphin's own code.** YG Dolphin is a fork of the Dolphin emulator, so a bug you find in YG Dolphin
may also be in Dolphin and in everything built on it. We fix it in YG Dolphin, report it privately to the
Dolphin team at the same time, and time the release of our public source with them, so our fix
doesn't reveal the bug before Dolphin's users are protected. Please don't report it publicly
anywhere in the meantime.

Please don't open a public issue for a vulnerability. We aim to reply within 5 business days and to
tell you what we decided within 15, and we credit you when the fix ships unless you'd rather we
didn't.

## What we most want to hear about

1. **Getting out of the sandbox:** a game running in the desktop app's sandbox that reads the
   player's files, starts a program, survives a restart, or reaches the network or another process
   beyond what [the sandbox design](https://github.com/yougame-co/yougame-sandbox/blob/main/docs/DESKTOP_SANDBOX.md)
   allows.
2. **Getting out of the emulator:** a mod or game whose guest code runs its own code in YG Dolphin's
   process ([the mod threat model](https://github.com/yougame-co/yougame-sandbox/blob/main/docs/ORCA_MODS.md)).
3. **The YouGame plugin and MCP server:** running code, leaking a key, or acting on a creator's
   account without them.
4. **yougame.co:** getting into another person's account, data or coins.

Out of scope: the known gaps listed in the sandbox design, and bugs in GPU drivers, the OS kernel or
third-party services (please report those to their vendors). An online native build capturing and
sending the player's screen is a documented, accepted risk, not a bounty finding.

## Rules for testing

- Use your own accounts and your own games. Never access, change or delete other people's data. If
  you reach some by accident, stop and tell us.
- Never test against other players or their computers. Build your own setup.
- If you upload a test game, keep it private (testers only), never list it, and delete it when
  you're done.
- Don't buy coins, tip or request payouts to test. If a test needs coins, ask us and we'll set you
  up.
- No denial of service, spam, social engineering or physical attacks.
- You must be 18 or older, and you can't be in a country under US sanctions.
- Give us 90 days to fix before you publish, or less once the fix has shipped.

## Safe harbor

YouGame is run by Fluo Inc. If you follow these rules in good faith, we consider your research of
YouGame's own software and services authorized, and research that follows this policy doesn't
break our Terms of Service. We won't initiate or recommend legal action against you for it,
including under anti-hacking or anti-circumvention laws, and if someone else does, we'll make
clear that you acted with our authorization.

We can only authorize research on what is ours. That leaves out the games and protections of other
companies (Nintendo's discs and keys, for example) and the services YouGame runs on: Cloudflare,
Supabase, Stripe, GitHub and Google.

## Rewards

We pay **$200** for each report that qualifies under "What we most want to hear about", to the
first person to report each underlying problem. YouGame is small; we'll raise this as it grows. To
be paid you have to be able to receive it legally: we can't pay people in sanctioned countries, and
we may need a tax form.
