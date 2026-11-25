# InfoSec Infirmary — Security Toolkit

> A suite of plain-language cybersecurity tools for small businesses. The idea behind the brand is simple: security should feel like a checkup, not a crisis.

**Live at [infosecinfirmary.com](https://infosecinfirmary.com/)**

> **This is a documentation repository.** It gives a high-level overview of each tool: what problem it solves, how it is designed, and the security thinking behind it.

## The tools

Each tool is named after a step in a medical checkup, because that is how the suite is meant to feel: a clear reading of your health, not a wall of jargon.

| Tool | What it does | Overview |
|------|--------------|----------|
| **Intake** | Scores a business against the NIST Cybersecurity Framework and shows where it stands | [Read →](./intake) |
| **Imaging** | Scans a website's public security signals and checks for cloud exposure | [Read →](./imaging) |
| **Bloodwork** | Checks email and password exposure in known breaches, without handling the real secret | [Read →](./bloodwork) |
| **Vitals** | Monitors uptime, certificate expiry, domain expiry, and new breaches around the clock | [Read →](./vitals) |
| **Injection Probe** | Red-teams a business's AI assistant for prompt-injection weaknesses | [Read →](./injection-probe) |
| **AI Policy Builder** | Turns a short form into a tailored one-page AI use policy | [Read →](./ai-policy) |

## The design principles shared across the suite

- **Plain language first.** Every result is written so a business owner with no security background knows what to do next. A finding is useless if the person reading it cannot act on it.
- **Privacy by construction.** Where a tool handles something sensitive, the privacy is built into the design, not promised in a policy. Bloodwork is the clearest example: it proves whether a secret has leaked without ever handling the real secret.
- **Read-only and in-scope.** The scanning tools only ever read public information and only touch the target the user is authorized to check. They never write, claim, or exploit anything.
- **Right tool, right place.** Some tools run entirely in the browser because they need no secrets. Others run server-side because a browser is not allowed to do the work. Each choice is deliberate and explained in the tool's overview.

## How these are built

The suite shares a common technical foundation: component-based JavaScript front ends, serverless functions for the work a browser cannot do, scheduled jobs for monitoring, and public standards (NIST CSF, TLS, SPF/DKIM/DMARC, the OWASP Top 10 for LLM Applications) as the backbone. The emphasis throughout is on defensive engineering: strict content-security policies, safe rendering, input validation, and failing loudly rather than giving a false all-clear.

## Contact

Built and maintained by InfoSec Infirmary. Learn more at [infosecinfirmary.com](https://infosecinfirmary.com/).

