[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&duration=3499&pause=649&color=019A47&center=true&vCenter=true&multiline=true&width=435&height=60&lines=Hi!;I'm+Miles+Howell)](https://git.io/typing-svg)

I replace the old internal system that everybody depends on and nobody wants to touch.

That's most of what I do now. Somebody's business runs on an undocumented ASP.NET app, a Microsoft Access database, or a spreadsheet that one person maintains, and it can't keep going — but it also can't break for a single day. I rebuild those in Django, carefully, and try to make the switchover boring.

Background's in math, physics, and systems engineering. I came up through computer vision and reinforcement learning, and I still keep a foot in it.

---

### How I work

Most of the difficulty in this kind of project isn't writing the new thing. It's proving you understood the old one.

So I port legacy queries close to verbatim before I improve anything, and when I find what looks like a bug in the original — a `CASE` that should say `AND` instead of `OR`, a join that quietly drops rows — I leave it, mark it `QUIRK`, and go ask someone. Production behavior may depend on that bug. "Obviously wrong" and "safe to change" aren't the same claim, and the second one needs evidence.

The other half is admitting what I don't know. Reverse-engineering a legacy app means most of your questions have no one left to answer them, so I keep the open ones written down as **blockers to resolve, not details to invent.** A confidently wrong guess about how a system works is much more expensive than an unanswered question.

### Working alongside agents

The models got good enough that this is now a real part of how I build, so I write for them deliberately. Every serious project gets an `AGENTS.md`: what the system is, which decisions are already settled and shouldn't be relitigated, which legacy quirks are load-bearing, and — most importantly — which open questions an agent must **stop and ask** about instead of filling in with something plausible.

That last part matters more the more sensitive the codebase is. On regulated data, the failure mode isn't an agent writing bad code; it's an agent writing *confident* code on top of an assumption nobody checked. Durable written context is the cheapest guardrail I've found.

---

### Things I've built

| Project | What it is |
| :--- | :--- |
| **[Vixxing](https://github.com/miles-howell/Vixxing)** | Stops help desk vishing. Attackers call IT, impersonate an employee, and talk an agent into resetting MFA — every "verification" question they're asked is a fact that leaks. This puts a TOTP possession check on the call itself: read me the six digits, or we're done. Django + PyOTP, with an honest write-up of its own threat model and limits. |
| **[Bridge-Crossing-RL-Sim](https://github.com/miles-howell/Bridge-Crossing-RL-Sim)** | Hierarchical RL you can watch learn in the browser. A manager agent picks sub-goals, a worker executes them, and the usual failure is that their Q-estimates drift apart and poison each other. I fixed it with a profit-sharing reward — the worker earns a cut of whatever the manager's command actually gains — plus Hindsight Experience Replay. |
| **[Window-Works](https://github.com/miles-howell/Window-Works)** | Interactive office floor plan. Find your desk, book a free one, and let admins redraw the map without going into the database. |
| **[employee-database](https://github.com/miles-howell/employee-database)** | Company directory sitting on top of a legacy Access `.accdb`, sorted by real reporting hierarchy, with birthdays and work anniversaries on the front page. |
| **[Dashboard-Viewer](https://github.com/miles-howell/Dashboard-Viewer)** | Desktop launcher for departmental dashboards. CustomTkinter, packaged to a single `.exe`, because "just open the file share" never actually works. |

Day job is healthcare claims systems — EDI X12, PHI, and the kind of compliance work that makes you careful about what ends up in a log line. Most of that lives in private repos.

<details>
<summary><b>Where I came from</b></summary>

<br>

**FIRST LEGO League** — Missouri state qualifier, 2013 and 2014.

**Hack4Good**, Springfield MO — 1st place 2017, 2nd place 2018. Community software, built against a clock.

**Republic High School** — ran the programming club, helped launch Missouri's first high school cybersecurity curriculum, and built tooling for 3D-printed prosthetics and device testing.

**University of Missouri–Columbia** — directed the ML/AI SIG, taught applied machine learning to undergrads, and worked on assistive AI with the campus robotics team. Teaching a thing is still the fastest way I know to find out whether I actually understand it.

</details>

---

Python, Django, PyTorch, SQL Server, C/C++, Linux. Enough security background to be appropriately nervous about what my apps are holding.

Happy to talk shop — especially about migrations off systems nobody documented.

<a href="https://github.com/miles-howell">
  <img src="https://github-readme-stats.vercel.app/api?username=miles-howell&show_icons=true&hide_border=true&theme=transparent#gh-light-mode-only" />
</a>
<a href="https://github.com/miles-howell">
  <img src="https://github-readme-stats.vercel.app/api?username=miles-howell&show_icons=true&hide_border=true&theme=dark&bg_color=00000000#gh-dark-mode-only" />
</a>
