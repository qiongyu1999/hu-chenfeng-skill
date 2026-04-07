# hu-chenfeng-skill

A Codex persona skill modeled after 户晨风, built from sampled livestream transcripts across 2023-2025.

This project does not try to copy surface catchphrases only. The core goal is to preserve the more stable parts of the persona:

- direct, high-pressure clarity
- fast reality-checking
- anti-delusion decision-making
- strong switching between reassurance, confrontation, and pragmatic advice

## What This Repository Contains

- [hu-chenfeng-skill/SKILL.md](./hu-chenfeng-skill/SKILL.md)
  The main Codex skill instructions.
- [hu-chenfeng-skill/references/persona-profile.md](./hu-chenfeng-skill/references/persona-profile.md)
  Distilled persona traits and reasoning patterns.
- [hu-chenfeng-skill/references/source-notes.md](./hu-chenfeng-skill/references/source-notes.md)
  Notes extracted from sampled source material.

## Design Principle

This skill is designed as a decision persona, not just a speaking-style persona.

The repository separates:

- `reasoning style`
- `interaction modes`
- `text-mode adaptation`

That means the skill aims to preserve how 户晨风 frames problems, pressure-tests plans, and distinguishes good-faith questions from bad-faith ones, while adapting the livestream tone into something more usable in Codex and chat.

## Current Abstraction

The current version is based on cross-year sampled transcripts rather than a full line-by-line pass of the entire archive.

Stable patterns captured so far:

- asks concrete questions quickly
- reduces emotional fog into one governing problem
- pushes people toward reality contact
- refuses to encourage unrealistic fantasies
- uses different intensity levels for sincere callers, challengers, and dreamers

## Sources

Primary public sources used for this version:

- [户晨风全集 archive](https://www.huchenfeng.live/)
- [2025-09-14](https://www.huchenfeng.live/2025-nian-09-yue/2025-09-14)
- [2025-03-31](https://www.huchenfeng.live/2025-nian-03-yue/2025-03-31)
- [2024-07-31](https://github.com/Olcmyk/HuChenFeng/blob/main/2024%E5%B9%B407%E6%9C%88/2024-07-31.md)
- [2023-03-10](https://github.com/Olcmyk/HuChenFeng/blob/main/2023%E5%B9%B403%E6%9C%88/2023-03-10.md)

## Notes

- This is a fan-made skill artifact, not an official project.
- The current version is a strong approximation, not a complete reconstruction.
- Livestream filler, donation rituals, and one-off performance moments are intentionally downweighted.
