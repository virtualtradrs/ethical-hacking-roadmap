# Your first authorized practice session

This walkthrough exists for one reason: most beginners' first "hacking" attempt is against something
they have no right to touch, and it ends badly. Here is the legal path, in order, with a concrete first
session at the end. It takes an afternoon.

## 1. Understand what "authorized" means

You are authorized when **the owner of the system has given you permission, in writing, for a defined
scope**. Three forms of it are available to a beginner, and nothing else is:

| Situation | Authorized? | Why |
|---|---|---|
| A machine you own, or a VM on your own computer | Yes | You own it; it is your hardware and your risk. |
| A practice platform's sandbox (TryHackMe room, HTB machine, PortSwigger lab, wargame level) | Yes | The platform's terms grant permission *inside its own environment*. |
| An intentionally vulnerable app you deploy locally (Juice Shop, DVWA) | Yes | Software published for exactly that purpose, running on your host. |
| A website of a company you do not work for, "just checking" | **No** | No permission, no scope. Curiosity is not a defence. |
| A friend's or family member's machine, even with a verbal "sure, go for it" | **No** | Get it in writing, with a scope, or don't. |
| Your school or employer's network, without a signed engagement | **No** | Ownership of the network is not yours to assume. |

Practice-platform permission stops at the platform's boundary. Scanning the platform's own production
infrastructure, or a third party you reached from inside a lab, is not authorized and will get your
account closed and possibly worse.

> **The accidental-finding rule.** If, while doing something legitimate, you stumble onto a system or
> data you were not meant to reach: stop, do not go further, do not download anything, keep your notes,
> and report it to the owner through their security contact. Every professional has this rule; the ones
> who ignore it are the ones in the news.

## 2. Write a scope sheet, even for your own lab

A scope sheet is one page. For a self-directed lab it takes five minutes and it builds the habit that
keeps you out of trouble later.

```
PROJECT:            First practice session
OWNER / PERMISSION: Me. I own the hardware and the VM.
IN SCOPE:           127.0.0.1:3000 (Juice Shop container, on my laptop)
                    the VM 'labvm' on my host-only network 192.168.56.0/24
OUT OF SCOPE:       Everything else. Home router, work VPN, any public host.
RULES:              No denial-of-service, no brute force with real wordlists,
                    no data exfiltration, no persistence outside the VM.
START / END:        Today, 14:00–18:00
EVIDENCE:           Notes in ~/labs/2026-10-16-juiceshop/, screenshots as needed
REPORT TO:          Myself (learning log)
```

Keep the file next to your notes. When you eventually work a real engagement, this is the document you
will be handed or asked to write.

## 3. Build a lab you can reset

Pick one of these; each is legal, free, and designed for practice.

- **Intentionally vulnerable web app (easiest start).** Juice Shop or DVWA, run locally in a container
  or on a throwaway VM, and reachable only from your own machine:
  [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) with the maintainers' own free
  [companion guide](https://pwning.owasp-juice.shop/), and
  [DVWA](https://github.com/digininja/DVWA) for the classic OWASP Top 10 exercises.
- **A VM you can snapshot and destroy.** Install [VirtualBox](https://www.virtualbox.org/) and a Linux
  guest of your choice ([Kali's documentation](https://www.kali.org/docs/) covers its own setup), then
  **snapshot it before you touch anything.** Half the value of a lab is being able to reset it.
- **A hosted sandbox (zero setup).** [PortSwigger Web Security Academy](https://portswigger.net/web-security)
  gives you a fresh instance per lab in the browser, and [OverTheWire](https://overthewire.org/wargames/)
  gives you an SSH shell to puzzle with — useful if your machine cannot run VMs.
- **Container tooling**, if you don't have Docker yet: [Docker Engine installation docs](https://docs.docker.com/engine/install/)
  (Docker Desktop is free for personal use; the CLI alone is enough here).

## 4. The first session, step by step

1. **Set up the scope sheet** above, and save it as `SCOPE.md` in a new folder for the session.
2. **Start the target and prove it is yours to touch.** Confirm the app is reachable at `localhost`
   only, and that the VM is on a host-only network.
3. **Capture a baseline.** With the app running, open your browser's developer tools, open the network
   tab, and log in with the demo account. Save the request and response for the login POST.
   This is your first real "evidence": raw traffic, not a screenshot of a UI.
4. **Write three hypotheses before testing anything**, e.g. "the login form may reveal whether a
   username exists", "the session cookie may not be scoped or flagged", "the reset flow may send a
   token in a URL". Untested hypotheses are what a report is built from.
5. **Test one hypothesis only, slowly**, and record the exact request, the exact response, and your
   conclusion — including "wrong, and here is why".
6. **Write your notes in the report shape** from the start: *Target, Scope, Method, Observation,
   Evidence, Impact, Fix, What I'd do differently.* The writeup is the deliverable, always.
7. **Reset the lab** (restore the snapshot, delete the container). Leaving a deliberately vulnerable app
   running on a laptop you take to a café is its own kind of finding.
8. **Publish the writeup** as a Markdown file in your own repository. That file is portfolio item #1
   from [Stage 8](../README.md#stage-8--the-professional-path).

## 5. What to do if you get stuck

Spending an hour stuck is normal and useful. After that: read the lab's own hint system, read the
official documentation of the technology involved, then search for the *concept* — not the lab name
plus "walkthrough". Copying a walkthrough is fine once you have already solved the level your own way;
doing it first turns practice into typing.

When you are comfortable with this routine, move on to
[Recommended practice order](PRACTICE-PLAN.md) and [Stage 5 of the README](../README.md#stage-5--hands-on-labs-and-ctfs).
