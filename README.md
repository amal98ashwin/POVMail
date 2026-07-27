# POVMail

**Draft it once. See it their way.**

POVMail is a single-file web app for previewing an email in the reading UI of the client the recipient will actually open it in — before you send it. Write the subject and message directly inside a live mockup of Gmail, Outlook, Apple Mail, BlueMail, Titan Email, or a generic phone/desktop inbox, then copy the result straight into your real mail draft.

No build step, no backend, no dependencies — it's one HTML file you can open locally or host anywhere that serves static files.

## Why

The way you compose an email is rarely how the other person reads it. Font, spacing, line length, and layout all change across clients and devices, which makes it easy to misjudge how a message will land. POVMail lets you reskin the same draft across several common reading environments so you can sanity-check tone, length, and formatting before it goes out.

## Features

- **Type directly in the reading pane** — the subject and body fields are editable right inside the mocked-up inbox, not in a separate editor.
- **Eight reading UIs**, switchable without losing your draft:
  | Client | Form factor |
  |---|---|
  | Gmail | Desktop |
  | Gmail | Mobile |
  | Outlook | Desktop |
  | Apple Mail | Desktop |
  | BlueMail | Mobile |
  | Titan Email | Webmail |
  | Generic mail app | Phone |
  | Generic webmail | Desktop |
- **Dark mode** — toggle applies to the backdrop and to each client mockup individually (not a blanket filter).
- **Basic rich text** — bold, italic, underline, and bullet lists via the formatting toolbar.
- **Copy subject / copy message** — copies formatted HTML (so bold/italic/lists survive a paste into a rich-text compose box) with an automatic plain-text fallback.
- **"Not an original email" mark** — every preview carries a small disclaimer under the timestamp so a screenshot of this tool can't be mistaken for a real, received message.
- **Zero dependencies** — vanilla HTML/CSS/JS, nothing to install or build.

## Getting started

Clone the repo and open the file in a browser:

```bash
git clone https://github.com/<amal98ashwin>/<POVMail>.git
cd <POVMail>
open povmail.html   
```

## Usage

1. Pick a reading UI from the pills at the top.
2. Edit the sender name/email, recipient name, subject, and message — they're all editable in place.
3. Use the formatting toolbar (B / I / U / bullet list) as needed.
4. Switch clients any time to check how the same draft reads elsewhere; your content carries over.
5. Click **Copy subject** and **Copy message**, then paste each into your real mail client's compose window.


## Notes & limitations

- Nothing is saved between page loads — refreshing or closing the tab clears your draft. There's no storage or backend by design.
- The client mockups approximate each product's layout, typography, and color palette for recognizability; they are not pixel-perfect reproductions and are not affiliated with or endorsed by Google, Microsoft, Apple, BlueMail, or Titan.
- Clipboard access (`navigator.clipboard`) requires a secure context (`https://` or `localhost`) in most browsers.

## Contributing

Issues and pull requests are welcome — additional client skins (e.g. Yahoo Mail, ProtonMail, Superhuman), accessibility fixes, and small UX improvements are all good candidates. Since everything lives in one file, most changes are a single-file diff.

## License

MIT — see [LICENSE](LICENSE) for details.
