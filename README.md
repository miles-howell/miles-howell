[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&duration=3499&pause=649&color=019A47&center=true&vCenter=true&multiline=true&width=435&height=60&lines=Hi!;I'm+Miles+Howell)](https://git.io/typing-svg)

I replace the old internal system that everybody depends on and nobody wants to touch.

That's most of the job now. Somebody's business runs on an ASP.NET app whose author left in 2014, or an Access database sitting on a share drive, or a spreadsheet that one person in accounting maintains and nobody else can read. It can't keep going, and it also can't be down on Monday. I rebuild those in Django and try to make the cutover boring.

Background's math, physics, and systems engineering. I came up through computer vision and RL, and I still poke at it.

---

### How I work

The hard part isn't building the new thing. It's proving I understood the old one.

So the legacy queries get ported almost verbatim first, ugly parts included. When I hit something that looks like a bug — a `CASE` with an `OR` where it obviously wants `AND`, a join quietly eating rows — I don't fix it. I tag it `QUIRK`, write down what it actually does, and go find someone who remembers. About half the time it turns out three reports downstream have been relying on it for years.

The rest is keeping a running list of what I don't know. Nobody's left to answer most questions about a twelve-year-old app, so the open ones go in a file and stay open until someone answers them. Guessing is how you ship something that looks correct for six weeks.

### Working with agents

I use them a lot, so every project gets an `AGENTS.md`: what the system does, what's already been decided and doesn't need re-arguing, which weird legacy behavior is load-bearing, and what to stop and ask about rather than fill in. It's mostly the same page I'd hand a new contractor on day one.

The stopping part is the part that earns its keep. On claims data I'm not that worried about a model writing bad code — bad code shows up fast. I'm worried about clean, plausible code sitting on an assumption nobody checked.

---

### Things I've built

| Project | What it is |
| :--- | :--- |
| **[Vixxing](https://github.com/miles-howell/Vixxing)** | Help desk vishing is the attack where someone calls IT, says they're locked out, and talks the agent into resetting their MFA. Every verification question the agent asks is a fact an attacker can go look up first. So instead: read me the six digits off your authenticator, or we're done. Django + PyOTP, with a README that's honest about what it doesn't cover. |
| **[Bridge-Crossing-RL-Sim](https://github.com/miles-howell/Bridge-Crossing-RL-Sim)** | Hierarchical RL you can watch learn in a browser tab. A manager picks sub-goals, a worker carries them out, and the usual outcome is that they poison each other's Q-estimates. Gave the worker a cut of whatever the manager's command actually earned, added Hindsight Experience Replay, and it stopped falling apart. |
| **[Window-Works](https://github.com/miles-howell/Window-Works)** | Interactive office floor plan. Find your desk, book an open one, and let admins redraw the map without anyone going into the database. |
| **[employee-database](https://github.com/miles-howell/employee-database)** | Company directory sitting on top of a legacy Access `.accdb`, sorted by who actually reports to whom. Birthdays and work anniversaries are on the front page, because that's what people open it for. |
| **[Dashboard-Viewer](https://github.com/miles-howell/Dashboard-Viewer)** | Desktop launcher for the department dashboards. CustomTkinter, packed into one `.exe`, because "it's on the share drive" has never once worked. |

Day job is healthcare claims — EDI X12, PHI, and enough compliance around it that I think about what's in a log line before I write it. Most of that lives in private repos.

<details>
<summary><b>Where I came from</b></summary>

<br>

**FIRST LEGO League** — Missouri state qualifier, 2013 and 2014.

**Hack4Good**, Springfield MO — 1st place 2017, 2nd place 2018. Community software, built against a clock.

**Republic High School** — ran the programming club, helped launch Missouri's first high school cybersecurity curriculum, and built tooling for 3D-printed prosthetics and device testing.

**University of Missouri–Columbia** — directed the ML/AI SIG, taught applied machine learning to undergrads, and worked on assistive AI with the campus robotics team. Nothing finds the parts you only half-understand like having to explain them to a room.

</details>

---

Python, Django, PyTorch, SQL Server, C/C++, Linux. Enough security background to be appropriately nervous about what my apps are holding.

Happy to talk shop, especially about getting off a system nobody documented.

<a href="https://github.com/miles-howell">
  <img src="https://github-readme-stats.vercel.app/api?username=miles-howell&show_icons=true&hide_border=true&theme=transparent#gh-light-mode-only" />
</a>
<a href="https://github.com/miles-howell">
  <img src="https://github-readme-stats.vercel.app/api?username=miles-howell&show_icons=true&hide_border=true&theme=dark&bg_color=00000000#gh-dark-mode-only" />
</a>
