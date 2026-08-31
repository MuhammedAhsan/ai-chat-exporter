# AI Chat Exporter — Privacy Policy

*Last updated: 23 August 2026*
*Applies to: AI Chat Exporter browser extension, version 2.7.0 and later*

---

## Summary

The Extension does not collect your data, because it has nowhere to send it.
There is no account, no server, and no analytics. Your conversations are read
from the page already open in your browser, turned into a document on your own
machine, and saved where you tell the browser to put them.

The detail below is written so you can check it rather than take it on trust.

---

## 1. What the Extension reads

When you open the popup on a supported chat site, the Extension reads the
conversation currently displayed on that page — the messages, code blocks,
tables, equations, and images that are already on your screen.

This happens entirely inside your browser. The conversation is held in memory
only for as long as the popup is open, and is discarded when you close it. It is
never written to disk and never transmitted.

The Extension reads pages only on the five supported sites listed in section 6.
On every other site it does nothing: it does not read the page, and no code is
injected into it.

## 2. What is stored on your device

The Extension saves four settings, using your browser's own extension storage.
They stay on your device and are never transmitted.

| Setting | What it holds |
| --- | --- |
| `lastFormat` | The export format you used last, so that button is highlighted next time |
| `theme` | Whether you chose light, dark, or automatic |
| `activeTabPanel` | Which of the three popup tabs was open last |
| `exportPreferences` | Page size, margins, fonts, accent colour, and the five document switches |

That is the complete list. Nothing else is stored.

If your browser is signed in and syncing extension data, your browser may sync
these four settings between your own devices under its own privacy policy. They
contain no conversation content.

## 3. What is deliberately not stored

The following exist only while the popup is open and are gone when it closes:

- the conversation itself, and every message in it
- redaction terms you type, which are often sensitive by definition
- per-message notes
- anything you type into the search box

Search terms were previously saved and no longer are. What you search for inside
a private conversation is a fragment of that conversation, and it should not
outlive the window you typed it into.

## 4. Network connections

The Extension makes one kind of outbound request, and only one:

> Images already displayed in your conversation are fetched so they can be
> embedded in the exported file. The request goes to the site that is already
> serving that image to your screen. Nothing about you, your conversation, or
> your settings is included.

Your session cookies are sent with that request only when the image is hosted by
one of the five supported chat sites — which is what allows a picture from your
own conversation to load at all. For any other host, cookies are explicitly
omitted.

There are no other network connections. Specifically, there is no telemetry, no
analytics, no crash reporting, no advertising, no remote configuration, and no
update or licence check. The fonts used in PDF exports are bundled inside the
Extension and are not downloaded.

## 5. Files, clipboard, and sharing

| | |
| --- | --- |
| **Files** | An export is saved through your browser's own download mechanism, which asks you where to put it. The Extension does not choose the location and does not keep a copy. |
| **Clipboard** | Written only when you press "Copy as Markdown", and only with the conversation you are looking at. The Extension never reads your clipboard. |
| **Sharing** | The "Share" button hands the finished file to your operating system's share sheet, which offers whatever apps your machine already has. The Extension uploads nothing and does not see where you send it. |

## 6. Permissions, and why each is needed

| Permission | Why it is needed |
| --- | --- |
| `activeTab` | Read the conversation on the tab you are looking at, when you open the popup. |
| `scripting` | Inject the reader into the page, and the "Edit before export" overlay when you open it. Both are bundled in the Extension; no remote code is ever loaded or run. |
| `storage` | Save the four settings listed in section 2. |
| `downloads` | Save the exported file. |
| `tabs` | Read the current tab's address, to tell whether it is a supported chat site before doing anything at all. |
| `clipboardWrite` | Write to the clipboard when you press Copy. |
| `contextMenus` | Add the right-click export menu on supported sites. |

**Site access:** `chatgpt.com`, `chat.openai.com`, `gemini.google.com`,
`perplexity.ai`, `chat.deepseek.com`, `claude.ai`

Access is limited to these five services. The Extension cannot read any other
website.

## 7. Data we collect

**None.**

The Extension has no server. It sends no personal information, no usage
statistics, and no conversation content anywhere. Nothing is sold, shared,
rented, or disclosed to third parties, because nothing is collected in the first
place.

## 8. Your rights

Data protection law — including the GDPR, the UK GDPR, and the CCPA — gives you
rights over personal data a company holds about you, such as access, correction,
deletion, and portability.

No personal data about you is collected or held, so there is nothing to access,
correct, delete, or export. The four settings in section 2 live on your own
device and are under your control: removing the Extension removes them, and your
browser's extension settings can clear them at any time.

## 9. Children

The Extension is not directed at children and collects no information from
anyone, including children under 13.

## 10. Third-party services

The Extension works on sites operated by other companies — OpenAI, Anthropic,
Google, Perplexity, and DeepSeek. Your use of those services is governed by their
own privacy policies, not this one. The Extension is independent and is not
affiliated with or endorsed by any of them.

## 11. Changes to this policy

If this policy changes, the date at the top will change with it and the updated
policy will be published before the release it applies to. A change that affects
what is collected or transmitted will be stated plainly rather than buried.

## 12. Contact

Questions about this policy go through this repository:

- **General questions** —
  [open a discussion](https://github.com/MuhammedAhsan/ai-chat-exporter/discussions)
- **A privacy problem you have found** — report it privately through
  [GitHub's security advisories](https://github.com/MuhammedAhsan/ai-chat-exporter/security/advisories/new),
  not as a public issue. See [SECURITY.md](SECURITY.md).

There is no email address, deliberately: this Extension has no mailing list, no
account system, and nothing to send you.
