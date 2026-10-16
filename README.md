# Ethical Hacking Roadmap — Learn It the Legal Way, Step by Step

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Links: hand-checked](https://img.shields.io/badge/links-hand--checked-brightgreen.svg)](#link-health)

A curated, step-by-step roadmap for learning ethical hacking the legit way — from zero to responsible
disclosure — with hand-checked free and low-cost resources, structured labs, and a clear legal/ethical
frame at every stage.

**What this is:** a learning path and a resource collection — eight stages, in order, with author-
verified links, deliberate practice targets, and a "done when" test for each stage.

**What this is not:** a toolkit. There are no exploits, no payloads, no cracked or repackaged
commercial tools, no target lists and no evasion recipes in this repository. Every hands-on resource
here points at a lab that is designed to be attacked, or at a system you own or have written
permission to test. If you came for a script that breaks into someone else's box, this is the wrong
repository, and that is deliberate.

---

## Contents

- [How to use this roadmap](#how-to-use-this-roadmap)
- [The one rule that matters](#the-one-rule-that-matters)
- [Roadmap at a glance](#roadmap-at-a-glance)
- [Stage 1 — Foundations (OS, networking, Linux)](#stage-1--foundations-os-networking-linux)
- [Stage 2 — Programming for security](#stage-2--programming-for-security)
- [Stage 3 — Web security fundamentals](#stage-3--web-security-fundamentals)
- [Stage 4 — Networking and recon](#stage-4--networking-and-recon)
- [Stage 5 — Hands-on labs and CTFs](#stage-5--hands-on-labs-and-ctfs)
- [Stage 6 — Vulnerability assessment and responsible disclosure](#stage-6--vulnerability-assessment-and-responsible-disclosure)
- [Stage 7 — Specialize (pick a lane)](#stage-7--specialize-pick-a-lane)
- [Stage 8 — The professional path](#stage-8--the-professional-path)
- [Link health](#link-health)
- [Contributing](#contributing)

## How to use this roadmap

Work the stages in order; each one assumes the previous one. Nothing here is a course you must finish
before touching the next stage — the point of Stage 1 and Stage 2 is that they stop you from
copy-pasting commands you cannot read.

- **Two tracks.** If you already write code and use a Unix shell daily, compress Stages 1–2 into
  whatever time it takes to pass their "done when" test, and start Stage 3 immediately.
- **Labs over videos.** Passive watching feels like progress and is not. Budget at least half your
  time for a keyboard in front of an authorized lab.
- **Write everything down.** Notes in Markdown, with commands, output and your reasoning. This becomes
  your portfolio in Stage 8 and your report format in Stage 6.
- **Expect ~6–12 months part-time** (roughly 6–10 hours a week) to reach the point of a junior
  security role or a first paid engagement. Anyone promising faster is selling something.

## The one rule that matters

> **Only test systems you own, or systems you have explicit written permission to test.**

Unauthorized access is a crime in most jurisdictions — in the US, the Computer Fraud and Abuse Act
(and comparable laws elsewhere) does not care that you were curious, learning, or "helping". Every
stage below repeats a shorter form of this line; it is not decoration. The legal frame is covered
properly in [Stage 8](#stage-8--the-professional-path), but you need to hold it from Stage 1:
a lab you spin up on your own machine or a designated practice platform is where every technique in
this roadmap belongs until you have a signed scope.

## Roadmap at a glance

Times are typical for someone studying part-time (6–10 h/week) with a laptop and no prior security
background. They are estimates from the shape of the material, not measured benchmarks.

| Stage | Focus | Typical time |
|-------|-------|--------------|
| [1. Foundations](#stage-1--foundations-os-networking-linux) | How operating systems, networks and Linux actually work; the shell as a tool | 4–6 weeks |
| [2. Programming for security](#stage-2--programming-for-security) | Python and Bash to the point of writing your own small tools; reading other people's code | 6–8 weeks |
| [3. Web security fundamentals](#stage-3--web-security-fundamentals) | HTTP, sessions, same-origin, browsers, and the OWASP Top 10 categories as concepts | 4–6 weeks |
| [4. Networking and recon](#stage-4--networking-and-recon) | DNS, ports and services, OSINT methodology, scope discipline | 3–5 weeks |
| [5. Hands-on labs and CTFs](#stage-5--hands-on-labs-and-ctfs) | Authorized practice environments, CTF platforms, a repeatable lab routine | 8–12 weeks (and ongoing) |
| [6. Vulnerability assessment](#stage-6--vulnerability-assessment-and-responsible-disclosure) | Finding, validating, rating and reporting weaknesses; responsible disclosure | 6–8 weeks |
| [7. Specialize](#stage-7--specialize-pick-a-lane) | Pick a lane: web app, network, cloud or mobile | 8–12 weeks per lane |
| [8. The professional path](#stage-8--the-professional-path) | Certifications landscape, portfolio, ethics, law and the disclosure process | ongoing |

---

## Stage 1 — Foundations (OS, networking, Linux)

*Authorized testing only: in this stage your targets are your own machine, a VM you created, or a
purpose-built wargame. Nothing else.*

**What you will learn**

- Navigate a Unix filesystem fluently: permissions, processes, users, packages, logs, systemd basics.
- Explain what happens between typing a URL and seeing a page: DNS, TCP/IP, TLS, HTTP.
- Use the terminal as a tool (pipes, redirection, grep, find, ssh, tmux) rather than a last resort.
- Read a man page and a manual instead of searching for a YouTube tutorial that half-answers it.

**Resources**

- [MIT — The Missing Semester of Your CS Education](https://missing.csail.mit.edu/) — shell, scripting,
  editors, version control and debugging; the fastest way to stop being afraid of the terminal.
- [The Linux Command Line (free full book, PDF)](https://linuxcommand.org/tlcl.php) — William Shotts'
  introduction to the shell, from `ls` to writing your own scripts.
- [Linux man pages (online)](https://man7.org/linux/man-pages/) — the reference you will use for the
  rest of your career; learn to read SYNOPSIS, OPTIONS and EXIT STATUS.
- [GNU Bash Reference Manual](https://www.gnu.org/software/bash/manual/bash.html) — authoritative for
  shell behaviour and quoting rules.
- [Arch Wiki](https://wiki.archlinux.org/title/Main_page) — not just for Arch users: the clearest
  practical explanations of Linux internals, networking and boot to be found anywhere, free.
- [Ubuntu Server documentation](https://ubuntu.com/server/docs) — how the server-side pieces
  (netplan, ssh, ufw, nginx basics) are actually configured.
- [Operating Systems: Three Easy Pieces (free textbook)](https://pages.cs.wisc.edu/~remzi/OSTEP/) —
  processes, memory, concurrency and files, explained with jokes; read the virtualization sections.
- [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) — 30+ levels of SSH shell puzzles;
  the single best free way to prove your Linux basics are real.
- [Wireshark User's Guide](https://www.wireshark.org/docs/wsug_html_chunked/) — capture and read your
  own traffic so packets stop being abstract.
- [Wikipedia — Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) — a clear, free
  overview of the naming system that everything else in this roadmap builds on.

**Done when:** you can explain to another person what happens on the wire when `curl https://example.com`
runs, and you have completed Bandit (or 20 levels of it) without copying a walkthrough for the last
third.

---

## Stage 2 — Programming for security

*Authorized testing only: the code you write in this stage runs against your own host, a local file or
a dataset you generated. No scanning of third-party systems.*

**What you will learn**

- Python well enough to parse a log, talk to an API, and script a repetitive task.
- Bash well enough to glue those scripts together and automate a lab your way.
- Read unfamiliar code without panicking — the core skill behind code review and source analysis.
- Use static analysis and linters to find your own bugs before someone else does.

**Resources**

- [The Python Tutorial (official)](https://docs.python.org/3/tutorial/) — the language from the source;
  sections 1–11 plus the standard library tour are the useful ones here.
- [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/) — free to read online;
  file handling, regex, web scraping, spreadsheets: exactly the chores security work is full of.
- [Python for Everybody](https://www.py4e.com/) — free course and book; gentler pace, good if
  programming is completely new.
- [Google's Python Class](https://developers.google.com/edu/python) — free text plus exercise videos,
  strong on string/file/dict work you will do constantly.
- [Exercism — Python track](https://exercism.org/tracks/python) — free exercises with human mentoring;
  the fastest fix for "I can read code but cannot write it".
- [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html) — how professional
  Python is judged; read it before you share your first script.
- [ShellCheck](https://www.shellcheck.net/) — paste a Bash script and get the bugs explained; free,
  open source, browser or local.
- [Pro Git (free book)](https://git-scm.com/book/en/v2) — chapters 1–3 cover what you need; every
  engagement, report and portfolio piece lives in Git.
- [Git documentation](https://git-scm.com/doc) — the reference for when the book is not specific
  enough.
- [Bandit (Python security linter)](https://bandit.readthedocs.io/en/latest/) — run it on your own
  code and learn to recognise insecure patterns by name.
- [Semgrep documentation](https://semgrep.dev/docs/) — free CLI and rules for finding bug patterns in
  source; learn rule syntax and you can read any scanner's findings.
- [CodeQL](https://codeql.github.com/) — query code like a database; free for public repositories and
  the standard language of real code-review research.

**Done when:** you have written a script longer than 100 lines that does something genuinely useful to
you (parses a log, checks your own system's config, summarises a dataset) and pushed it to a public
repo with a README that a stranger could follow.

---

## Stage 3 — Web security fundamentals

*Authorized testing only: all practice here belongs in the labs listed below (Juice Shop, PortSwigger's
labs) or on an application you built yourself.*

**What you will learn**

- The HTTP request/response cycle properly: methods, status codes, headers, cookies, redirects.
- How the browser enforces boundaries — same-origin policy, CORS, CSP — and why the gaps matter.
- The OWASP Top 10 categories as concepts you can explain, not a list to memorise.
- Why "it's just a parameter" is how most real vulnerabilities start.

**Resources**

- [OWASP Top 10](https://owasp.org/www-project-top-ten/) — the industry's reference list of web
  application risk categories, with the reasoning behind each entry.
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/) — the defensive counterpart: how each
  class of bug is prevented, per topic, maintained by practitioners.
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) — a modern, deliberately vulnerable
  application you can run locally (Docker or Node) and work through at your own pace.
- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — free, browser-based labs
  written by the makers of Burp Suite; the best free web-security training that exists.
- [PortSwigger — Learning paths](https://portswigger.net/web-security/learning-paths) — ordered
  sequences (e.g. server-side, client-side, authentication) so you are not guessing what to do next.
- [PortSwigger — All labs](https://portswigger.net/web-security/all-labs) — the full catalogue with
  difficulty labels; use it to keep a running count of solved labs for your portfolio.
- [MDN — HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP) — the clearest free reference for the
  protocol you are about to spend years reading.
- [MDN — HTTP response status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) — worth
  knowing cold; 401 vs 403 vs 404 tells you a lot about what a server is really doing.
- [MDN — HTTP cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies) — session handling,
  attributes and flags; the root of a huge share of authentication bugs.
- [MDN — Same-origin policy](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy)
  — the browser security model in one page, including why it is not airtight.
- [MDN — Cross-Origin Resource Sharing (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
  — the deliberate holes in that model, and the misconfigurations they lead to.
- [MDN — Content Security Policy (CSP)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP) — how
  sites try to contain injected script, and how CSP mistakes are found.

**Done when:** you can take an arbitrary feature ("password reset by email link") and talk through the
likely failure modes in HTTP terms — tokens in URLs, reuse, enumeration, missing expiry — without
looking anything up, and you have finished the first 20 PortSwigger Academy labs in one learning path.

---

## Stage 4 — Networking and recon

*Authorized testing only: port scanning, DNS enumeration and OSINT collection may only be pointed at
your own infrastructure, a lab target, or a scope you have in writing. Scanning third-party hosts is
not "passive research".*

**What you will learn**

- How DNS resolution, records, zones and subdomains work — and what "enumeration" means legally.
- Ports, services, banners and protocol behaviour, and how to read a scan result honestly.
- A recon methodology: define the scope, gather only what the scope allows, record provenance.
- What is legitimately public (register data, certificates, search engines) versus what is not.

**Resources**

- [Nmap Network Scanning (the official book, free online)](https://nmap.org/book/) — the definitive
  reference on host discovery, port scanning and service detection, including the legal notes.
- [Nmap reference guide](https://nmap.org/book/man.html) — the manual page in readable form; keep it
  open next to your terminal.
- [MITRE ATT&CK](https://attack.mitre.org/) — a free knowledge base of how adversaries actually operate,
  which is also the best map of what defenders are looking for.
- [Bellingcat's Online Investigation Toolkit](https://bellingcat.gitbook.io/toolkit) — a maintained,
  journalist-grade OSINT tool index, with notes on reliability and ethics.
- [Have I Been Pwned](https://haveibeenpwned.com/) — check whether an address or domain appears in known
  breaches; a legitimate, free source for exposure research.
- [Wikipedia — Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) — if you skipped it
  in Stage 1, read it before touching DNS records; recursors, authoritative servers and caching explain
  most enumeration surprises.
- [NIST SP 800-115 — Technical Guide to Information Security Testing and Assessment](https://csrc.nist.gov/pubs/sp/800/115/final)
  — free US government methodology for planning an assessment, including rules of engagement and
  scope documents. Read it before you scan anything with permission.

**Done when:** you can produce a one-page recon plan for a target you own: scope, sources, method,
what you will *not* touch, and how you will record evidence — and you can explain why each source in it
is publicly available and legal for you to use.

---

## Stage 5 — Hands-on labs and CTFs

*Authorized testing only: every platform below hosts machines that are explicitly built to be attacked
inside its own sandbox. That permission does not extend to anything outside the sandbox — including the
platform's own production infrastructure.*

**What you will learn**

- A repeatable lab routine: recognise → read → hypothesise → test → record → write up.
- Enough speed to work under time pressure without skipping your notes.
- Where your strengths actually are (web, Linux privilege, crypto, blue team) — measured by results,
  not vibes.

**Resources**

- [TryHackMe](https://tryhackme.com/) — guided, browser-based rooms with a generous free tier; the
  friendliest on-ramp if you have never used a hacking lab.
- [Hack The Box](https://www.hackthebox.com/) — free-tier vulnerable machines and challenges; steeper
  but closer to real assessment work.
- [Hack The Box Academy](https://academy.hackthebox.com/) — modular, hands-on modules with some free
  material; pairs well with the machines above.
- [OverTheWire wargames](https://overthewire.org/wargames/) — free, classic wargames (Bandit, Natas,
  Leviathan) covering shell, web and binary basics; no account needed.
- [picoCTF](https://picoctf.org/) — beginner-friendly CTF competition with free archived challenges and
  writeups from a university programme.
- [pwn.college](https://pwn.college/) — free, university-run systems-security dojo; the best structured
  route into binary exploitation and low-level fundamentals.
- [CTFtime](https://ctftime.org/) — the global CTF calendar and archive; how you find the next event
  and read past scoreboards and writeups.
- [Root-Me](https://www.root-me.org/) — hundreds of free, ranked challenges across web, network,
  crypto, forensics and reverse engineering.
- [VulnHub](https://www.vulnhub.com/) — free vulnerable virtual machines you download and run locally;
  the standard way to practise full end-to-end tests offline.
- [OWASP Vulnerable Web Applications Directory](https://owasp.org/www-project-vulnerable-web-applications-directory/)
  — the maintained index of intentionally vulnerable apps, licensed and legal to run yourself.
- [DVWA (Damn Vulnerable Web Application)](https://github.com/digininja/DVWA) — a PHP/MySQL app you
  deploy locally to practise the OWASP Top 10 with adjustable difficulty.
- [Blue Team Labs Online](https://blueteamlabs.online/) — defensive investigations and challenges; most
  security jobs are blue team, and this is free training for it.
- [CyberDefenders](https://cyberdefenders.org/) — free blue-team challenges built from realistic
  artefacts; a good counterweight if you only practise attacking.

**Done when:** you have written up five completed labs or machines as short reports (target, scope,
what you did, what you found, what you would do differently) and at least one CTF writeup — published
in your own repo, in your own words.

---

## Stage 6 — Vulnerability assessment and responsible disclosure

*Authorized testing only: assessment work happens against an agreed scope. Finding a bug by accident on
a system you are not authorised to test means you stop, do not access anything further, and follow a
disclosure process — never "just have a look around".*

**What you will learn**

- Run an assessment from planning to report: scope, method, evidence, findings, remediation.
- Validate a finding instead of trusting a scanner's output, and rate its severity sensibly.
- Use the standard vocabularies — CVE, CWE, CVSS — so your report speaks the industry's language.
- Report a vulnerability to someone who did not ask for the news, without becoming the problem.

**Resources**

- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/) — the
  free, exhaustive checklist of web test cases; the scaffold of any web assessment report.
- [NIST SP 800-115 — Technical Guide to Information Security Testing and Assessment](https://csrc.nist.gov/pubs/sp/800/115/final)
  — the assessment lifecycle from an authoritative, free source, including planning and reporting.
- [FIRST — CVSS](https://www.first.org/cvss/) — the severity scoring standard, maintained by the Forum
  of Incident Response and Security Teams; read the current specification, not a blog summary.
- [FIRST — CVSS v4.0 calculator](https://www.first.org/cvss/calculator/4.0) — score a real finding you
  reproduced yourself and be able to justify every metric.
- [CVE Program](https://www.cve.org/) — how vulnerabilities get identifiers, and who assigns them.
- [NIST National Vulnerability Database](https://nvd.nist.gov/) — the enriched public database of CVEs;
  the first place to check whether someone already found your finding.
- [MITRE CWE](https://cwe.mitre.org/) — the taxonomy of weakness types; using its names makes your
  reports searchable and comparable.
- [disclose.io](https://disclose.io/) — free, open-source templates and terminology for safe-harbour
  vulnerability disclosure policies.
- [security.txt](https://securitytxt.org/) — the standard that tells researchers where to report; every
  project you work on should have one.
- [OWASP — Vulnerability Disclosure Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Vulnerability_Disclosure_Cheat_Sheet.html)
  — practical guidance for both the reporter and the receiver.
- [Hacker101 (HackerOne)](https://www.hacker101.com/) — free video and CTF curriculum on bug bounty
  basics, including how to write a report that gets triaged instead of closed.
- [Google Bug Hunters](https://bughunters.google.com/) — a real, well-documented vulnerability reward
  programme; reading its rules teaches you what a usable scope looks like.
- [Bugcrowd Vulnerability Rating Taxonomy](https://www.bugcrowd.com/vulnerability-rating-taxonomy/) —
  free, and shows how real programmes convert a finding into a priority and a payout band.
- [OWASP ZAP](https://www.zaproxy.org/) and its [documentation](https://www.zaproxy.org/docs/) — a free,
  open-source web proxy/scanner; use it on your own apps to learn what automated scanning can and cannot
  prove.

**Done when:** you have reported a vulnerability you found in a lab — or, better, in an open-source
project through its own security policy — with reproduction steps, impact, a CVSS score, and a fix
recommendation; and you can describe the disclosure timeline you followed.

---

## Stage 7 — Specialize (pick a lane)

*Authorized testing only: specialisation means deeper access, which means tighter scope discipline. Each
lane below lists labs or documentation only — no exploit packs, no cracked commercial tooling.*

Pick **one** lane and go deep. Breadth is what Stages 1–6 gave you; depth is what makes you hireable.
Each lane below is a credible starting set, not a syllabus to finish.

### Lane A — Web application testing

- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — the deep end of web
  application testing, free, with hundreds of labs.
- [Burp Suite documentation](https://portswigger.net/burp/documentation) — learn the tool properly
  rather than by clicking around.
- [Burp Suite Community Edition](https://portswigger.net/burp/communitydownload) — the free edition is
  enough for the Academy and for real manual testing; the paid Pro edition is optional.
- [OWASP API Security Top 10](https://owasp.org/API-Security/editions/2023/en/0x11-t10/) — modern apps
  are APIs with a UI; this is the counterpart list for them.
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/) — keep
  the checklist beside you until it is internalised.

### Lane B — Network and infrastructure

- [Nmap Network Scanning (free online book)](https://nmap.org/book/) — the tool and the discipline of
  mapping a network properly.
- [Wireshark User's Guide](https://www.wireshark.org/docs/wsug_html_chunked/) — if you cannot read a
  capture, you cannot debug a network finding.
- [Professor Messer — Network+ training](https://www.professormesser.com/) — free, complete video
  course on networking fundamentals; useful even if you never sit the exam.
- [MITRE ATT&CK](https://attack.mitre.org/) — the adversary-behaviour map that infrastructure defenders
  and testers both work from.

### Lane C — Cloud security

- [AWS Well-Architected — Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
  — the design guidance you will be assessing against, straight from the provider.
- [Microsoft Azure security benchmark](https://learn.microsoft.com/en-us/security/benchmark/azure/) —
  control-by-control cloud security baseline.
- [Google Cloud security foundations guide](https://cloud.google.com/architecture/security-foundations)
  — a reference architecture for a deliberately secured landing zone.
- [Kubernetes — Security concepts](https://kubernetes.io/docs/concepts/security/) and the
  [OWASP Kubernetes Top 10](https://owasp.org/www-project-kubernetes-top-ten/) — container and cluster
  risk, in official and community form respectively.
- [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) — an intentionally vulnerable AWS
  environment you deploy in your own account to practise cloud attack paths lawfully.
- [Cloud Security Alliance](https://cloudsecurityalliance.org/) — free research and guidance bodies of
  work that shape how cloud controls are assessed.

### Lane D — Mobile application security

- [OWASP MASTG — Mobile Application Security Testing Guide](https://mas.owasp.org/MASTG/) — the free
  mobile testing methodology and test cases.
- [OWASP MASVS — Mobile Application Security Verification Standard](https://mas.owasp.org/MASVS/) — the
  requirements side; what "secure enough" is defined to mean.
- [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/) — the risk categories for mobile.
- [Android security documentation](https://source.android.com/docs/security) — platform security model,
  app sandboxing and permissions from the source.
- [Apple Platform Security guide](https://support.apple.com/guide/security/welcome/web) — the iOS
  counterpart; free and unusually detailed.
- [MobSF — Mobile Security Framework](https://github.com/MobSF/Mobile-Security-Framework-MobSF) — a free,
  open-source static/dynamic analysis tool for apps you are authorised to review.

**Done when:** you have a public writeup or portfolio entry in your chosen lane that shows a full
finding — not a screenshot of a tool — and you can explain the underlying technology well enough to
answer "why does that work?" three times without repeating yourself.

---

## Stage 8 — The professional path

*Authorized testing only: your professional reputation is built on scope discipline. Read the ethics and
law block below as part of the job, not as a formality.*

**What you will learn**

- How the certification landscape is actually structured, and which ones are worth their cost for your
  situation.
- What a portfolio looks like when it is evidence rather than a list of logos.
- The legal ground you stand on — and the lines you never cross, even when a client asks.
- How to keep learning once the roadmap ends.

### Certifications and how to read them

- [CompTIA Security+](https://www.comptia.org/certifications/security) — the common entry ticket for
  junior roles; exam is paid, objectives are published free.
- [CompTIA PenTest+](https://www.comptia.org/certifications/pentest) — a mid-level, hands-on-adjacent
  penetration-testing certification; exam is paid.
- [OffSec PEN-200 / OSCP](https://www.offsec.com/courses/pen-200/) — the best-known practical offensive
  certification; course and exam are expensive, and it is aimed at people who already have lab hours.
- [GIAC certifications](https://www.giac.org/certifications/) — highly regarded, employer-funded in most
  cases; course and exam are paid.
- [(ISC)² CISSP](https://www.isc2.org/certifications/cissp) — a management-level certification that
  needs several years of experience behind it; not a starting point.
- [Linux Foundation training](https://training.linuxfoundation.org/) — free and paid courses on Linux and
  cloud fundamentals; the free intros are a low-risk way to fill gaps.
- [NIST NICE Framework](https://www.nist.gov/itl/applied-cybersecurity/nice) — the free, official map of
  cybersecurity work roles and the tasks and knowledge each one needs; use it to see what a job title
  actually means before you buy a course for it.
- [CyberSeek](https://www.cyberseek.org/) — free US labour-market data on cybersecurity roles and skill
  demand; helps you target, and sanity-checks any "shortage" claim you read.

### Portfolio

- [GitHub Pages](https://docs.github.com/en/pages) — free hosting for your writeups and tool
  documentation; free for public repositories.
- Five lab reports from [Stage 5](#stage-5--hands-on-labs-and-ctfs) and one full assessment writeup,
  in your own words, with the command output that backs each claim.
- One or two small tools you wrote in [Stage 2](#stage-2--programming-for-security) — scanners,
  parsers, log analysers, report generators — alongside a README that explains the reasoning.

### Ethics and law

- [EFF — Coders' Rights Project](https://www.eff.org/issues/coders) — free, practical material on
  security research and the law, including vulnerability reporting and safe harbour.
- [Computer Fraud and Abuse Act (overview)](https://en.wikipedia.org/wiki/Computer_Fraud_and_Abuse_Act)
  — a readable starting point on the US statute most often cited against researchers; check your own
  jurisdiction, and get authorisation in writing.
- [(ISC)² Code of Ethics](https://www.isc2.org/ethics) — the professional code that most certification
  holders are bound by; short, and worth reading once properly.
- [NIST SP 800-115](https://csrc.nist.gov/pubs/sp/800/115/final) — revisit the rules-of-engagement and
  legal-considerations sections before your first professional engagement.
- [disclose.io](https://disclose.io/) and [security.txt](https://securitytxt.org/) — the standards that
  make good-faith reporting safe and expected; used in [Stage 6](#stage-6--vulnerability-assessment-and-responsible-disclosure).

### Community and staying current

- [SANS Internet Storm Center](https://isc.sans.edu/) — free daily diary of what is being exploited
  right now; ten minutes a day beats a hundred bookmarked threads.
- [The DFIR Report](https://thedfirreport.com/) — free, detailed real-incident writeups; the closest
  thing to reading over a responder's shoulder.
- [Krebs on Security](https://krebsonsecurity.com/) — investigative reporting on breaches and the
  criminal ecosystem; free.
- [Google Project Zero blog](https://googleprojectzero.blogspot.com/) — deep technical vulnerability
  research, free, and unusually honest about timelines and process.
- [DEF CON](https://defcon.org/) and [BSides](https://bsides.org/) — the conference scene; local BSides
  events are cheap or free and are where most people meet their first employer.

**Done when:** you have a public portfolio, you can explain the law and ethics of your work in a client
conversation, and you know which single certification is worth your money next — with a reason that is
not "it is popular".

---

## Link health

Every external link in this repository was checked with `curl` (following redirects, browser
user-agent) before publishing, on **2026-10-16**. Links that returned a hard failure were removed or
replaced rather than shipped; nothing here is a paywalled-only resource without being labelled as such
in its description, and there are no affiliate or referral links.

Re-check everything at any time:

```bash
grep -ohE 'https://[^)"< ]+' README.md docs/*.md | sort -u |
  xargs -P 12 -I{} sh -c 'c=$(curl -sIL -o /dev/null -w "%{http_code}" --max-time 25 \
  -A "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124 Safari/537.36" \
  "{}"); echo "$c {}"' | sort
```

Sites that answer automated checks with a bot challenge may need a manual look; that is noted in
[CONTRIBUTING.md](CONTRIBUTING.md) so contributors do not re-litigate it.

## Contributing

Corrections, better free resources and new verified links are welcome. Read
[CONTRIBUTING.md](CONTRIBUTING.md) first — it sets out the link-check requirement, the no-affiliate rule
and the ethics rule that every contribution is held to.

Licensed under the [MIT License](LICENSE).
