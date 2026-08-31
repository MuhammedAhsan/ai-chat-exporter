# Getting help

This repository is the support desk for the **AI Chat Exporter** browser
extension. Everything goes through one of four routes.

| What you have | Where it goes |
| --- | --- |
| Something is broken | **[Report a bug](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=bug_report.yml)** |
| An idea for the extension | **[Suggest a feature](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=feature_request.yml)** |
| A question, or you are not sure it is a bug | **[Start a discussion](https://github.com/MuhammedAhsan/ai-chat-exporter/discussions)** |
| A security or privacy vulnerability | **[Report it privately](https://github.com/MuhammedAhsan/ai-chat-exporter/security/advisories/new)** — see [SECURITY.md](SECURITY.md) |

There is no support email. Every route is here, in the open, except security
reports — which are private by design.

---

## Before you report a bug

Two minutes here saves a round-trip.

**Check [Known limitations](README.md#known-limitations) first.** Some of the most
reported behaviour is deliberate and documented: equations print on one line,
emoji are dropped from PDFs (only PDFs), code line numbers are off by default,
and Claude conversations are scrolled before being read.

**Check you are on the latest version.** Open `chrome://extensions`, find AI Chat
Exporter, and compare the version against the top of [CHANGELOG.md](CHANGELOG.md).

**Try one other format.** If a PDF export is wrong but the Markdown is fine, the
problem is in the PDF writer. If every format is wrong, the problem is in reading
the page. Knowing which halves the search.

---

## 🔒 Never paste a real conversation

This extension exists because your conversations are private. A GitHub issue is
public, permanent, and indexed by search engines within hours.

**Describe the structure instead of pasting the content.** "A table with three
columns where the middle cell holds a code span" is more useful than the table
itself — it tells me exactly what to build a test case from, without publishing
anything of yours. If you need to show markup, replace the text with invented
content first.

The same applies to screenshots. Crop them, or blur the text.

---

## What I can and cannot help with

**I can help with:** exports that are wrong or incomplete, the editor
misbehaving, a site that stopped working after a redesign, redaction missing
something, the popup failing to detect a conversation.

**I cannot help with:** the chat sites themselves, recovering a conversation you
have already deleted, or exporting from a site that is not one of the five
supported ones. Support for a new site is a
[feature request](https://github.com/MuhammedAhsan/ai-chat-exporter/issues/new?template=feature_request.yml),
not a bug.

---

## About contributions

**The extension is closed source and its code is not in this repository.** Pull
requests cannot be accepted, so please do not spend time on one — there is
nothing here to patch.

That is not a reason to stay quiet. Bug reports and feature requests genuinely
shape what gets built next, and a well-described report is worth more to this
project than a patch would be. Both live in [Issues](https://github.com/MuhammedAhsan/ai-chat-exporter/issues).

---

## Response times

This is a free extension maintained by one person alongside other work. Issues
are read, and most get a reply within a week. A report that reproduces cleanly
gets fixed a great deal faster than one that needs three messages to understand —
which is what the issue forms are for.
