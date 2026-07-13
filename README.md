🇫🇷 [Version française](README_FR.md) · 🇬🇧 **English**

# MythDesk

**The Game Master's study** — a screen companion for tabletop role-playing, built for the physical
table and the local network. The GM runs one application; players join from their browser, on the
same WiFi. No online account, no cloud: **everything stays on your machine, and everything works
without Internet**.

![MythDesk home screen](docs/captures/accueil.png)

> MythDesk is not yet another 3D virtual tabletop: no dynamic lighting, no marketplace. It is a
> **table companion** — the tool you open next to the dice, so the GM can tell the story instead
> of digging through notes.

## Features

**Universe** (the compendium)
- D&D 5 (SRD 5.1) and D&D 5.5 (SRD 5.2 / 2024) **built in and complete**: spells, creatures, magic
  items, languages, places, rules — plus, for 2024: species, backgrounds, feats, weapon masteries
- Fully **bilingual French / English** (interface AND data, chosen per machine)
- **Importable custom compendiums** (`.mythkeeper-compendium.json`): play any system. A
  [conversion guide](docs/GUIDE-CONVERSION-IA.md) lets you turn a rulebook PDF into a compendium
  with the help of an AI, and a chronicle's Universe can be exported back as a compendium

**Campaign** (the game in progress)
- **Branching scenario**: scenes, read-aloud text, GM notes, choices and consequences, linked map
  and soundscape — a "▶ Play" button that sets the table in motion
- **Maps** with fog of war (opaque for players, semi-transparent for the GM), tokens, measuring
  ruler, ping
- Company (character sheets with D&D auto-calculation of saves and skills), NPCs, campaign bestiary
  and inventory, projectable artwork and videos, campaign chronicle
- Import/export: the whole campaign or a single scenario, as one file

**GM Tools**
- **Combat**: initiative, HP synced with character sheets, token highlighting on the map
- **Soundscape**: a library of ambiences and music (CC0), sound scenes, loops
- **Slate**: shared free-hand drawing, quick tokens, image exports
- **Table screen**: a chrome-less window to put on a TV or second screen facing the players — map,
  artwork, initiative in real time

**And around it all**
- `@` mentions everywhere (characters, creatures, items) with a hover card
- **GM data never leaves the server**: scenarios, notes and combat are filtered server-side, not
  merely hidden on screen
- 100% offline: fonts, rules, audio and libraries are all bundled

## Quick start

1. Run `MythDesk.exe` (portable, nothing to install) — this is the GM's machine; keep it open.
2. Create your storyteller account, then your first chronicle.
3. Players open the address shown on the home screen (`http://<gm-ip>:47832`) in their browser, on
   the same network, and join with the chronicle's **invite code**.

To play remotely (outside the same WiFi), see [docs/JEU-A-DISTANCE.md](docs/JEU-A-DISTANCE.md)
(Tailscale / Radmin VPN, no advanced network setup).


The architecture is deliberately simple: no client-side build step (`.jsx` files transpiled on the
fly by the server), an authoritative Express + Socket.io server, a JSON database on disk. The
compendium format is documented in [docs/FORMAT-COMPENDIUM.md](docs/FORMAT-COMPENDIUM.md).

## Licenses & attributions

- **Code**: © MythDesk — all rights reserved (distribution license to come).
- **Game content**: this work includes material taken from the *System Reference Document 5.1* and
  the *System Reference Document 5.2.1* by Wizards of the Coast LLC, licensed under
  [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode).
  Full attributions are in the application's **Credits & licenses** screen.
  MythDesk is an independent tool, neither affiliated with nor endorsed by Wizards of the Coast.
- **Fonts**: Cormorant Garamond, Inter, Space Mono and Spectral, bundled under the
  [SIL Open Font License](fonts/LICENCES.txt).
- **Audio**: ambience library under CC0.
