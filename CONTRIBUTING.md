# Contributing

Thanks for helping make this roadmap better. This repository is a curated learning path, and curation
means every link costs someone a click — so the bar for adding or changing one is deliberately high.

## The ethics rule (non-negotiable)

This project teaches security work inside the legal frame: **only test systems you own or have explicit
written permission to test.**

- No content that enables attacks on systems the reader is not authorised to test — no live exploit
  code aimed at third-party software and no payloads, no target lists, no credential dumps, no
  bypass or evasion recipes, no cracked or licence-dodging copies of commercial tools.
- Hands-on resources must point at a lab that is designed to be attacked (a practice platform, an
  intentionally vulnerable application, a wargame) or at the reader's own infrastructure.
- Disclosure-related material must follow a recognised, good-faith process (report to the owner, allow
  time to fix, do not publish before the fix). Resources such as [disclose.io](https://disclose.io/)
  and the [security.txt standard](https://securitytxt.org/) are the reference points.
- Anything that suggests curiosity, good intent or "white hat" status is itself permission will be
  declined.

## Link rules

1. **Verify the link with `curl` before opening the pull request.** A link that works in your browser
   and fails under `curl` is not verified:
   ```bash
   curl -sIL -o /dev/null -w '%{http_code}\n' --max-time 25 \
     -A 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124 Safari/537.36' \
     '<your-url>'
   ```
   `200` is what we ship. `403` usually means bot protection on a real page — if you keep it, say so in
   your pull request and confirm you opened it yourself. `404`, `410` and `451` links are dropped.
2. **No affiliate, referral or tracking links.** No `?ref=`, no coupon codes, no link shorteners.
3. **No paywalled-only resources** unless the entry itself says so, plainly ("paid", "exam fee
   required", "employer-funded in most cases"). Free tiers and free-to-read books are preferred.
4. **Prefer primary sources**: official documentation, standards bodies (NIST, OWASP, MITRE, FIRST) and
   maintained open-source projects over listicles and SEO content.
5. **One link, one reason.** Every entry carries a short description saying what the reader gets from
   it. "Great resource!" is not a description.

## Structure rules

- Keep the eight-stage structure and the per-stage blocks: *What you will learn*, *Resources*,
  *Done when*.
- Every stage keeps its "authorized testing only" line. If you add a stage, add the line too.
- Keep the roadmap table in `README.md` in sync with the stage headings, and keep the anchors working
  (GitHub lowercases headings, strips punctuation and turns spaces into hyphens).
- `docs/` is intentionally small. New pages need to add material that does not fit the README; folders
  of link dumps will be declined.
- Do not invent numbers. Time estimates are clearly labelled as rough part-time estimates, and no
  repository, user, star or outcome statistics are claimed anywhere.

## Sending a change

1. Describe the change and why it belongs in the roadmap.
2. Include your `curl` output (or the status code) for every link added or changed.
3. Open a pull request against `main`. Small, focused pull requests get reviewed faster.

## Reporting a broken link

Open an issue or a one-line pull request with the URL and the status code you saw. Broken links are
treated as bugs, not as trivia.

## License

By contributing, you agree that your contributions are licensed under the [MIT License](LICENSE).
