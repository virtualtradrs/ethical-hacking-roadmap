# Recommended practice order

The README tells you *what* to learn. This page tells you *in what order to practise it*, so you are
not jumping between unrelated rooms and platforms and wondering why nothing sticks.

Two rules come first:

1. **Never practise outside an authorized environment.** See
   [Your first authorized practice session](YOUR-FIRST-AUTHORIZED-LAB.md).
2. **Labs are not progress until you have written them up.** One lab, one short report. Reports are
   what you show people, and writing them is the skill you are actually being paid for.

## The first 12 weeks (part-time)

A week is roughly 6–10 hours. Adjust freely; the sequence matters more than the calendar.

| Week | Practice target | Deliverable |
|------|-----------------|-------------|
| 1 | [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) levels 0–15, no walkthroughs | `SCOPE.md` plus notes for 15 levels |
| 2 | Bandit 16–34; shell basics until `find`, `grep`, pipes and permissions are reflex | One writeup page on the three levels you found hardest |
| 3 | Write a 100-line Python script that parses a log or checks your own system config | Script published with a README |
| 4 | [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/), easy tier, using browser dev tools only | Three findings written in report shape |
| 5 | [PortSwigger Academy](https://portswigger.net/web-security/learning-paths) — first learning path (server-side) | 10 labs solved; running count started |
| 6 | Same path, finished; keep a per-lab note of the *technique*, not the answer | 20 labs; two full writeups |
| 7 | Client-side path; read [MDN on CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) and [CSP](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP) properly | Notes explaining what the browser allows and why |
| 8 | One [TryHackMe](https://tryhackme.com/) beginner path, plus a [VulnHub](https://www.vulnhub.com/) machine in a local VM | Full end-to-end writeup of the VM |
| 9 | [picoCTF](https://picoctf.org/) archived challenges across at least three categories | Scores across categories, gaps identified |
| 10 | Your weakest category from week 9, plus [Root-Me](https://www.root-me.org/) challenges in it | A written honest assessment of the gap |
| 11 | [CTFtime](https://ctftime.org/) — enter a live CTF with a team or solo; or a [Blue Team Labs](https://blueteamlabs.online/) investigation | One CTF/incident writeup published |
| 12 | Consolidate: portfolio page, five writeups, lab index | Public portfolio ready for [Stage 8](../README.md#stage-8--the-professional-path) |

If you finish a week's target early, **write up what you did before starting the next one.** Do not
trade the writeup for another lab; that trade is the most common way people stay beginners for years.

## Choose the next target by evidence, not mood

Keep a simple tracker so you can see your own gaps. A CSV or a Markdown table is enough:

| Lab / machine | Platform | Category | Date | Solved? | Time | Technique learned | Writeup? |
|---|---|---|---|---|---|---|---|
| Bandit L12 | OverTheWire | Linux | 2026-10-16 | yes | 40m | `strings`, file types | – |
| Juice Shop: admin section | OWASP | Authz | 2026-10-20 | yes | 90m | forced browsing | yes |

Then pick the next target from the *least* filled column:

- **Few categories touched** → run a broad CTF, then go deeper into the two you found hardest.
- **Many solved, few writeups** → stop solving and write; your reports are behind your skills.
- **Everything feels easy** → move up a difficulty tier or into a lane in
  [Stage 7](../README.md#stage-7--specialize-pick-a-lane); ideally on a live CTF with a clock.
- **Everything feels impossible** → you have moved up too fast; drop a tier and finish what you start.

## Cadence that actually holds up

- **Daily, 30–45 minutes:** one lab task, or the [SANS Internet Storm Center](https://isc.sans.edu/)
  diary and a note on what you learned.
- **Weekly, 2–4 hours:** one machine or lab path section, ending in a writeup.
- **Monthly:** a live CTF if you can, and a review of your tracker to pick the next target.
- **Every quarter:** re-read one stage of the README that you assumed you knew. Everyone finds a hole.

## When you are ready for the next stage

Move on when you can do the thing without the tutorial open:

- Stage 3 → 4: you can describe a request/response and a cookie's attributes without looking them up.
- Stage 4 → 5: you can write a scope and a recon plan for a target you own, and say what you will not touch.
- Stage 5 → 6: you have five lab writeups, one of them end-to-end on a VM.
- Stage 6 → 7: you have reported a vulnerability you found yourself, following a real disclosure process.
- Stage 7 → 8: you have a public portfolio and can defend every claim in it.

Back to the [main roadmap](../README.md).
