# Changelog

All notable changes to **AI Chat Exporter** are recorded here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and
this project uses [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

> **Note on the history below.** Versions before 2.7.0 were never published to any
> extension store — they were development builds, loaded unpacked. They are
> recorded for completeness, not as releases anyone could have installed. **2.7.0
> is the first public release.**

---

## 2.7.0 — 2026-08-30

The release prepared for the Chrome Web Store.

### Added
- **Report a bug** and **Suggest a feature** links in the popup footer, pointing
  at this repository.
- `npm run package` — builds an uploadable `.zip` from an allowlist of the files
  that ship, so nothing unintended can be published.
- An end user licence agreement, a privacy policy, and terms of use.
- Busy states during redaction and other slow operations, so the popup no longer
  looks frozen while it works.

### Changed
- Store description shortened to fit Chrome's 132-character limit.
- Source maps are no longer included in the packaged extension.

### Removed
- **"Export all open tabs as .zip".** It was the weakest feature in the
  extension and one of the two reasons the `tabs` permission was needed. Exporting
  each conversation individually is more predictable, and the shorter permission
  list is better for everyone.

### Fixed
- Popup controls now disable correctly on tabs that are not supported chat sites,
  instead of some sections staying active.

---

## 2.6.0 — 2026-08-21

Editing, extended to every kind of content.

### Added
- **Edit equations** — rewrite the LaTeX anywhere it appears, in a paragraph,
  heading, list item or table cell, with the readable form updating as you type.
- **Edit tables** — cell contents, plus adding and removing rows and columns.
  Bold, links and inline code survive.
- **Edit code blocks** and their language label. Untouched lines keep the syntax
  colours lifted from the page.
- **Edit quotes**, paragraph by paragraph, keeping inline formatting.
- **Edit nested lists** to any depth, each bullet numbered by its position
  (`2.1.3`) and indented to match.
- **Edit images** — alt text, caption, alignment, and width as a share of the
  text column.
- Blank space and divider blocks, insertable and styleable.
- Tooltips on every control in the block editor, replacing paragraphs of inline
  explanation.
- A test suite covering the exporters, redaction, the document model, and all
  five site adapters against saved page markup.

### Fixed
- Diagram backgrounds no longer carry the chat page's dark colour into a light
  document; hues are kept and lightness flipped.
- Diagram labels are legible rather than washed out, in the editor and in every
  export.
- Settings toggles now do what their labels say. Each one names something to take
  out, and switching it on takes it out.
- Redaction wording corrected where it described the wrong behaviour.

---

## 2.5.0 — 2026-08-13

### Added
- New extension icon.

### Changed
- jsPDF updated to 4.2.1.

### Fixed
- Security fixes in URL handling.
- Links in message text are now clickable in exports.
- Toggle copy in the Settings tab rewritten to match behaviour.

---

## 2.4.0 — 2026-08-11

### Changed
- **Messages tab rewritten** to fit roughly nine turns on screen instead of
  three, with the search box moved into it.
- Extraction is now restricted to the five supported chat sites. Previously the
  extension attempted extraction anywhere, and its last-resort detection would
  report ordinary page furniture — a navigation bar, a search results page — as a
  conversation.

### Fixed
- Settings tab layout, and several UI bugs in the Export tab.

---

## 2.3.2 — 2026-08-07

### Added
- **Share** — hand the finished file to your system's share sheet. Available for
  every format except DOCX, which Chrome will not share.

---

## 2.2.0 — 2026-08-06

### Added
- Customisation options for the document page header.

---

## 2.1.0 — 2026-08-06

### Added
- Toggles for leaving out your own messages, the User/Assistant labels, and the
  cover page.

### Fixed
- Message rows that expanded but would never collapse.
- Message previews shortened in the Messages tab.

---

## 2.0.0 — 2026-07-26

### Added
- **Four more sites: Claude, Gemini, Perplexity and DeepSeek**, each with its own
  adapter.
- In-page conversation editor, with a document stylesheet shared across every
  export format.
- Per-block selection, and jumping from the popup to a message on the page.
- Redaction, with its own panel.

### Changed
- Printed output optimised across all supported sites.

---

## 1.0.0 — 2026-07-21

First version. ChatGPT only, exporting to PDF, DOCX, HTML, Markdown, TXT and
JSON.

---

*Versions are not linked to release tags: the pre-2.7.0 builds were never
released, and there is nothing to tag them against. Once 2.7.0 is published,
tagging each future release and linking its heading here is worth doing.*
