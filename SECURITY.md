# Security Policy

AI Chat Exporter reads private conversations. That is the whole job, and it is
also the reason a security report here deserves a route that is not a public
issue. If you have found something, thank you — please use the private channel
below rather than filing publicly.

## Supported versions

| Version | Supported |
| --- | --- |
| 2.7.x | ✅ Yes |
| < 2.7 | ❌ No — update from the store first |

Only the latest published version receives fixes. Browser extensions update
themselves, so an old version means auto-update is off or the extension was
sideloaded.

## Reporting a vulnerability

**Report it privately** through GitHub, here:

> **[Report a vulnerability →](https://github.com/MuhammedAhsan/ai-chat-exporter/security/advisories/new)**

That form is private between you and the maintainer. It is not visible to anyone
else, and it stays private until a fix is published.

**Please do not** open a public issue, post it in Discussions, or describe it in
a store review. A public report tells everyone about the hole at the same moment
it tells me, and this extension's users have private conversations sitting behind
it.

### What to include

The more of this you can give, the faster it gets fixed:

- What the problem is, and what an attacker could actually achieve with it
- The extension version, the browser and its version
- Which chat site it happens on, if it is site-specific
- Steps to reproduce it
- Any page markup or configuration needed to trigger it

**Please redact your own conversation content** before sending anything. A
minimal reproduction with invented text is more useful than a real chat, and
safer for you.

### What happens next

| Stage | Timeline |
| --- | --- |
| Acknowledgement that I have read it | Within 5 days |
| An assessment — confirmed, needs more information, or not a vulnerability | Within 14 days |
| A fix published to the stores, for confirmed issues | As quickly as the store review queue allows |

This is a free extension maintained by one person, so these are honest targets
rather than a contractual guarantee. If something is being actively exploited,
say so in the report and it goes to the front.

You will be credited in the advisory and the [changelog](CHANGELOG.md) unless you
would rather not be. There is no bug bounty — no money, just credit and a fix.

## In scope

- Conversation content leaking out of the extension: to a page, to another
  extension, or over the network
- **Redaction failing to redact** — a term you entered surviving into an export,
  anywhere: message text, code blocks, table cells, captions, notes, the title,
  or a URL
- The image-fetch path: cookies sent to a host that should not receive them, or
  requests reaching a host outside the declared permissions
- Privilege or permission escalation beyond what the manifest declares
- Code injection into the popup or the editor overlay, including anything a
  crafted conversation could cause
- Stored settings holding something the [privacy policy](PRIVACY-POLICY.md) says
  they do not

## Out of scope

- Vulnerabilities in ChatGPT, Claude, Gemini, Perplexity or DeepSeek themselves —
  report those to the site concerned
- Anything requiring an already-compromised browser, a malicious extension
  already installed, or physical access to an unlocked machine
- An export being wrong, incomplete, or badly formatted — that is a
  [bug report](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=bug_report.yml)
- Missing hardening that has no demonstrated impact
- Bugs in the third-party libraries listed in [LICENSE.md](LICENSE.md) §8 — report
  those upstream, though do tell me if the extension's use of one makes it
  exploitable here
