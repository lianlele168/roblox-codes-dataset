# Roblox Game Codes Dataset

A community dataset of **527 redeem codes across 19 Roblox games**, extracted from the [robloxwikihub.com](https://robloxwikihub.com) network of fan-made game wikis.

Every code table in this dataset went through a **multi-source verification pass in September 2026**: each code was cross-checked against at least two independent public code trackers, community wikis, or official sources. Rewards use the source wording — where no source documented a reward, the entry says so instead of guessing.

## Why

We run 19 game-wiki sites and discovered that **roughly 78% of AI-generated code tables across our network were fabricated** — invented strings, made-up rewards, or codes for games that have no code system at all. We rebuilt every table from scratch with verification. This dataset is the cleaned, openly licensed result, published so others don't have to repeat that work.

See the full post-mortem: *(link to the write-up — coming soon)*

## Games covered

| Game | Codes | Active | Expired | Live wiki |
|---|---|---|---|---|
| [99 Nights in the Forest](https://99nights.robloxwikihub.com) | 4 | 3 | 1 | [99nights.robloxwikihub.com](https://99nights.robloxwikihub.com) |
| [Create a Car](https://createacar.robloxwikihub.com) | 10 | 3 | 2 | [createacar.robloxwikihub.com](https://createacar.robloxwikihub.com) |
| [Win A World Championship](https://winaworldchampionship.robloxwikihub.com) | 15 | 6 | 4 | [winaworldchampionship.robloxwikihub.com](https://winaworldchampionship.robloxwikihub.com) |
| [Rivals](https://rivals.robloxwikihub.com) | 12 | 11 | 1 | [rivals.robloxwikihub.com](https://rivals.robloxwikihub.com) |
| [Jujutsu Infinite](https://jujutsuinfinite.robloxwikihub.com) | 24 | 4 | 20 | [jujutsuinfinite.robloxwikihub.com](https://jujutsuinfinite.robloxwikihub.com) |
| [Anime Vanguards](https://animevanguards.robloxwikihub.com) | 13 | 3 | 10 | [animevanguards.robloxwikihub.com](https://animevanguards.robloxwikihub.com) |
| [Anime Defenders](https://animedefenders.robloxwikihub.com) | 33 | 16 | 17 | [animedefenders.robloxwikihub.com](https://animedefenders.robloxwikihub.com) |
| [Pressure](https://pressure.robloxwikihub.com) | 17 | 6 | 11 | [pressure.robloxwikihub.com](https://pressure.robloxwikihub.com) |
| [Fisch](https://fisch.robloxwikihub.com) | 137 | 3 | 134 | [fisch.robloxwikihub.com](https://fisch.robloxwikihub.com) |
| [Fish It!](https://fishit.robloxwikihub.com) | 27 | 27 | 0 | [fishit.robloxwikihub.com](https://fishit.robloxwikihub.com) |
| [Dress to Impress](https://dti.robloxwikihub.com) | 39 | 35 | 4 | [dti.robloxwikihub.com](https://dti.robloxwikihub.com) |
| [Sol's RNG](https://solsrng.robloxwikihub.com) | 13 | 4 | 9 | [solsrng.robloxwikihub.com](https://solsrng.robloxwikihub.com) |
| [Steal a Brainrot](https://stealabrainrot.robloxwikihub.com) | 20 | 1 | 19 | [stealabrainrot.robloxwikihub.com](https://stealabrainrot.robloxwikihub.com) |
| [Blade Ball](https://bladeball.robloxwikihub.com) | 59 | 16 | 43 | [bladeball.robloxwikihub.com](https://bladeball.robloxwikihub.com) |
| [Type Soul](https://typesoul.robloxwikihub.com) | 66 | 22 | 44 | [typesoul.robloxwikihub.com](https://typesoul.robloxwikihub.com) |
| [Anime Dice](https://animedice.robloxwikihub.com) | 17 | 12 | 5 | [animedice.robloxwikihub.com](https://animedice.robloxwikihub.com) |
| [Last Stop](https://laststop.robloxwikihub.com) | 5 | 5 | 0 | [laststop.robloxwikihub.com](https://laststop.robloxwikihub.com) |
| [Anime Origins](https://animeorigins.robloxwikihub.com) | 6 | 3 | 3 | [animeorigins.robloxwikihub.com](https://animeorigins.robloxwikihub.com) |
| [Jujutsu Shenanigans](https://jujutsushenanigans.robloxwikihub.com) | 10 | 1 | 9 | [jujutsushenanigans.robloxwikihub.com](https://jujutsushenanigans.robloxwikihub.com) |

## Format

Each game is a JSON file in [`data/`](data/):

```json
{
  "game": "Blade Ball",
  "site": "https://bladeball.robloxwikihub.com",
  "updated": "2026-09-19",
  "codes": [
    { "code": "SERPENT", "reward": "...", "status": "active", "note": "", "source": "" }
  ]
}
```

Fields:

- `code` — the redeem string exactly as it must be entered (case and punctuation included; some games require trailing `!`).
- `reward` — publisher wording where documented. Entries reading `Expired — reward not documented by the publisher` were never publicly documented; we did not invent values.
- `status` — `active`, `expired`, or `needs-check` (single-source or conflicting reports; flagged for in-game testing).
- `note` / `source` — verification notes where available (e.g. joke codes that *deduct* currency in Pressure).

## Caveats

- Roblox game codes expire constantly — some games kill weekly codes within 24 hours (Fisch does this by design). `active` means *verified active as of 2026-09-19*, not guaranteed today.
- Unofficial, community-maintained. Not affiliated with Roblox Corporation or any game developer.

## License

[CC BY 4.0](LICENSE) — use it, fork it, build on it. Attribution appreciated.

Live wikis with interactive calculators for every game: [robloxwikihub.com](https://robloxwikihub.com)
