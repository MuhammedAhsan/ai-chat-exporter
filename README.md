# AI Chat Exporter

**Save an AI chat conversation as a proper document — PDF, DOCX, HTML, Markdown,
TXT or JSON — in a couple of clicks.**

It reads the conversation straight off the page you are looking at. No account,
no API key, no sign-in, and nothing is uploaded anywhere. That also means it
works on conversations an API could never reach: temporary chats, guest sessions,
and threads you are not signed in to.

[Report a bug](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=bug_report.yml)
· [Suggest a feature](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=feature_request.yml)
· [Ask a question](https://github.com/MuhammedAhsan/ai-chat-exporter/discussions)
· [Changelog](CHANGELOG.md)

---

## Supported sites

| Site | Address |
| --- | --- |
| ChatGPT | `chatgpt.com`, `chat.openai.com` |
| Claude | `claude.ai` |
| Gemini | `gemini.google.com` |
| Perplexity | `perplexity.ai` |
| DeepSeek | `chat.deepseek.com` |

Each of these is tested against real saved conversations, exported end to end,
with the text read back out of the finished PDF and DOCX to confirm it survived.

**Only these sites.** On anything else the popup says so and does nothing — it
does not read the page, and nothing is injected into it. This is deliberate:
narrow access is the whole basis of the privacy claim below.

---

## Installing

> **Coming to the Chrome Web Store.** The extension is in review. This page will
> carry the install link as soon as it is live, and Microsoft Edge Add-ons will
> follow.
>
> [**Watch this repository**](https://github.com/MuhammedAhsan/ai-chat-exporter/subscription)
> to be notified when it ships.

---

## Using it

1. Open a conversation on any supported site.
2. Click the extension icon. It reads the page and shows how many messages and
   words it found.
3. Click a format — **PDF**, **DOCX**, **HTML**, **Markdown**, **TXT** or
   **JSON**. The file downloads.

That is the whole basic flow. Everything below is optional.

**Three tabs in the popup:**

- **Export** — the format buttons, sharing, and copy-to-clipboard.
- **Messages** — every turn in the conversation, each with a checkbox. Untick
  anything you do not want, shift-click to take a whole run at once, or use
  **Keep: All / Assistant / You** to drop one side of the conversation in a
  click. Search filters the list. Expand a turn for its preview, its notes and
  its individual blocks. Click any row to jump the page to it.
- **Settings** — page size, margins, fonts, colour, and what the document
  includes.

You can also **right-click any supported page** and export from the context menu
without opening the popup.

---

## What it can do

### It keeps the formatting

Headings, paragraphs, lists, tables, quotes, links and images all survive. So do
the things that usually break:

- **Code blocks** keep their syntax colours, their language label, and their
  indentation — including code you pasted into the chat yourself, which most
  exporters flatten into one run-on paragraph.
- **Equations** are converted to readable notation, e.g. `x = (−b ± √(b² − 4ac))/2a`.
- **Diagrams** such as Mermaid are captured as images, keeping the styling the
  chart carries with it. One drawn for a chat page in dark mode is repainted for
  the light page it is going onto — hues kept, lightness flipped — so it arrives
  as a readable diagram rather than a black rectangle.
- **Inline code** keeps the tinted background chat sites give it.
- **Images** are numbered in document order — *Image 01*, *Image 02* — and the
  name is what prints wherever the picture itself cannot be embedded, linked to
  the original so it stays one click away.
- Attachments, citations and timestamps are included where the site provides
  them.

PDF and DOCX also get a cover page, a table of contents, styled tables and
colour-coded speaker headings.

### You choose exactly what goes in

The Messages tab lists every turn on one line — who said it, how many blocks, how
many words — so a long conversation can be reviewed about nine turns at a time.

- **One side of the conversation** — **Keep: All / Assistant / You** drops the
  other in a single click. It sets the checkboxes rather than hiding rows, so you
  can still adjust it by hand afterwards.
- **A run of messages** — click one checkbox, then shift-click another, and
  everything between follows.
- **Individual blocks** — expand a turn for its parts, each labelled by type with
  a hint (a code block's language, a table's size, a paragraph's opening words).
- **Search** narrows the list, and the bulk buttons then say *Include all
  matching* / *Exclude all matching*. Filtering never changes what is already
  selected.
- **Four switches in Settings** — each names something to take out, and switching
  it on takes it out: *your own messages* (leaving only the answers), the
  *User/Assistant labels*, the *cover page*, or *dividers*. Chat models punctuate
  long answers with horizontal rules freely, which reads as clutter in a document
  whose headings already do that job.

### Edit before exporting

**Edit before export** opens the document over the chat page, laid out exactly as
it will print.

- Insert blank space, dividers and page breaks; delete, reorder or restyle
  individual blocks — text, size, colour, heading level.
- Edit **lists** to any depth. Every bullet gets a field, numbered by its position
  (`2.1.3`) and indented to match, so a three-level list is editable all the way
  down rather than only at the top.
- Edit **quotes** — each paragraph gets a field, and its bold, links and inline
  code survive.
- Edit **table** cells, and add or remove rows and columns.
- Edit **code blocks** and their language label. Lines you leave alone keep the
  syntax colours lifted from the page.
- Rewrite an **equation's LaTeX**, wherever it sits. The readable form printed
  beneath the field updates as you type, so you can see what the export will say
  without knowing how the source reads.
- Set a **blank space** to any height, and style a **divider** — solid, dashed,
  dotted or double, any thickness, any colour, with a live preview.
- Edit a **note** — its text, the word before the colon (`Note:`, `Warning:`,
  `TODO:`), and a colour that tints its rule, label and background together.
- Edit an **image** — alt text, caption, alignment, and width as a share of the
  text column, so it means the same on A4 and Letter.
- Click the gear on the cover to rename the document or switch off any part of it.
- **Undo and redo** (`Ctrl+Z` / `Ctrl+Shift+Z`) cover every change.

Blocks only move within their own message, so nothing is ever attributed to the
wrong speaker. Edits last for the browsing session — **Close** keeps them,
**Discard** throws them away.

### Redact before exporting

Enter terms — an email address, an API key, a name — and every occurrence is
replaced with `[REDACTED]` in the copy being exported: message text, code blocks,
table cells, image captions, notes and the document title. URLs count too — the
conversation's own address, link targets and image sources — since a term sitting
in a query string is just as exposed as one in the body.

**The terms are never saved to disk, and the original page is untouched.**

### Share it straight to another app

The **Share** button hands the finished file to your system's share sheet — Mail,
WhatsApp, Teams, whatever the machine offers. Nothing is uploaded by the
extension; you pick where it goes.

Chrome restricts which file types a website may share, so this is not uniform:

| Format | What happens |
| --- | --- |
| PDF, HTML, TXT | Shared as themselves |
| Markdown, JSON | Shared as `.txt` — identical content, and you are told |
| DOCX | Cannot be shared; export it and attach the saved file |

The button is hidden where the browser cannot share files at all (most desktop
Linux builds).

### Other useful things

- **Copy as Markdown** straight to the clipboard.
- **Add a note** to any message, carried into the export.
- **Light and dark theme**, following your system by default.

---

## Choosing a format

| Format | Keeps layout | Good for |
| --- | --- | --- |
| **PDF** | Full | Reading, printing, archiving, sending on |
| **DOCX** | Full | Editing in Word or Google Docs |
| **HTML** | Full | Viewing in a browser; prints the same as the PDF |
| **Markdown** | Structure | Notes apps, wikis, anything in git |
| **TXT** | Plain text | Searching, quoting, plain archives |
| **JSON** | Complete data | Scripting and re-processing |

Per-block sizes and colours set in the editor reach PDF, DOCX and HTML. Markdown,
TXT and JSON have no way to express them and drop them silently. JSON keeps every
field regardless of the Settings switches, being a data format rather than a
document.

---

## Privacy

- The conversation is read from the page already open in your browser, and
  processed there.
- **Nothing is sent to any server.** The only outbound requests are for images
  already displayed in the conversation, so they can be embedded in the file.
- No account, no API key, no analytics, no telemetry.
- Redaction terms and per-message notes exist only for the current session and
  are never written to disk.

Four settings are stored on your device — your last format, your theme, which tab
was open, and your document preferences. That is the complete list.

**[Read the full privacy policy →](PRIVACY-POLICY.md)**

### Permissions, and why each is needed

| Permission | Why |
| --- | --- |
| `activeTab` | Read the page you have open, once it is confirmed to be a supported site |
| `scripting` | Inject the reader, and the editor overlay when you press "Edit before export" |
| `tabs` | Read the current tab's address, to tell whether it is a supported chat site before doing anything at all |
| `storage` | Remember your format, theme and document preferences |
| `downloads` | Save the exported file |
| `clipboardWrite` | Copy as Markdown |
| `contextMenus` | The right-click export menu |

The five named sites also get host access, which is what allows zero-click
extraction and the context menu there. The popup checks the hostname before it
reads anything, so no other site is ever touched.

---

## Known limitations

Please read this before reporting a bug — most of what follows is deliberate and
documented.

**Formatting**

- **Equations are single-line.** A fraction reads `(a)/(b)` rather than being
  stacked over a bar. Chat sites typeset maths with KaTeX, which relies on its own
  fonts and positioned elements, none of which survives being lifted off the page.
  Markdown exports keep the original LaTeX so a Markdown renderer can typeset it
  properly.
- **Emoji are dropped from PDFs.** The embedded font has no emoji glyphs, and a
  missing glyph would print as an empty box. Ones with a typographic twin are
  substituted (✅ becomes ✔, ⭐ becomes ★); the rest are omitted. **Every other
  format keeps them.**
- **Code line numbers are off by default.** Everything in a PDF is selectable
  text, so a number gutter is dragged along whenever code is copied out. Turn them
  on in Settings when you want them for reference.
- **Syntax colours are sampled from the page**, because some sites use minified
  class names no fixed palette can match. Colours from a dark-mode page are
  darkened — keeping their hue — until they are legible on the light code panel
  used in exports.

**Reading the page**

- **Claude is scrolled before reading.** It keeps only the turns near the viewport
  and discards the rest, so the extension walks the thread first, capturing each
  turn as it passes, then restores your scroll position. Long threads take a few
  seconds. No other site is scrolled.
- **A site redesign can break extraction.** Each site's detection uses several
  fallbacks, but a large redesign may need updated selectors. If this happens,
  [report it](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=bug_report.yml) —
  it is the most likely reason something that worked yesterday does not today.
- **Attachment, citation and tool panels** use best-effort detection and fall back
  to plain text extraction when the markup is unfamiliar.
- **Jumping to a message can fail on Claude**, where the original element may no
  longer exist. The popup says so instead of scrolling somewhere misleading;
  refreshing restores the links.

**Scope**

- **Very large conversations take a noticeable moment**, since everything is
  processed in the browser.
- **Only the five sites listed above.** Support for another is a
  [feature request](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=feature_request.yml).

---

## Reporting a bug, or asking for something

| | |
| --- | --- |
| Something is broken | [**Report a bug**](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=bug_report.yml) |
| An idea for the extension | [**Suggest a feature**](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=feature_request.yml) |
| A question | [**Discussions**](https://github.com/MuhammedAhsan/ai-chat-exporter/discussions) |
| A security or privacy vulnerability | [**Report it privately**](https://github.com/MuhammedAhsan/ai-chat-exporter/security/advisories/new) |

> **🔒 Never paste a real conversation into an issue.** Issues are public,
> permanent and indexed. Describe the structure instead — "a table with a code
> span in the middle cell" tells me what to build a test case from, without
> publishing anything of yours.

Full guidance is in [SUPPORT.md](SUPPORT.md).

---

## Documents

| | |
| --- | --- |
| [Changelog](CHANGELOG.md) | What changed in each version |
| [Privacy Policy](PRIVACY-POLICY.md) | What the extension does with data |
| [Terms and Conditions](TERMS-AND-CONDITIONS.md) | Terms of use |
| [Licence](LICENSE.md) | End user licence agreement |
| [Security Policy](SECURITY.md) | Reporting a vulnerability |
| [Support](SUPPORT.md) | Getting help |
| [Code of Conduct](CODE_OF_CONDUCT.md) | Conduct in issues and discussions |

**This repository holds documentation only.** The extension is closed source and
its code is not published here, so pull requests cannot be accepted. Bug reports
and feature requests very much can.

---

## Trade marks

ChatGPT and OpenAI are trade marks of OpenAI. Claude is a trade mark of
Anthropic. Gemini and Google are trade marks of Google LLC. Perplexity is a trade
mark of Perplexity AI. DeepSeek is a trade mark of DeepSeek.

**AI Chat Exporter is an independent product.** It is not affiliated with,
endorsed by, or sponsored by any of them. Those names appear only to describe
which sites the extension works with.

---

Copyright © 2026 Muhammad Ahsan. All rights reserved.
