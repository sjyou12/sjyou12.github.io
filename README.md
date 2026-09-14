# sjyou12.github.io

Personal academic page for Seonju You — served at **https://sjyou12.github.io**

A single self-contained `index.html`. No build step, no dependencies, no framework.
Edit the file, commit, push; the live site updates in about a minute.

---

## Deploy

From the repository folder on your machine:

```bash
git clone https://github.com/sjyou12/sjyou12.github.io.git
cd sjyou12.github.io

# copy index.html, README.md and .nojekyll into this folder, then:
git add .
git commit -m "Add academic homepage"
git push origin main
```

If your default branch is `master` rather than `main`, use that name instead —
`git branch --show-current` tells you which one you are on.

Then check **Settings → Pages** on GitHub:

- Source: *Deploy from a branch*
- Branch: your default branch, folder `/ (root)`

For a `<username>.github.io` repository this is usually enabled automatically as
soon as there is content on the default branch. Give it a minute, then open
https://sjyou12.github.io in a private window (a normal window may show a cached
404 from before the first deploy).

`.nojekyll` tells GitHub to serve the files as-is instead of running them through
Jekyll. Nothing here needs Jekyll, and without the file any future filename
starting with `_` would be silently dropped.

---

## Before you print the QR code

The QR code on your business cards and poster encodes `https://sjyou12.github.io`
and **cannot be changed after printing**. So:

1. The site must answer at that address before the cards go to print.
2. `cv.pdf` must live at the repository root — the link in the page points at
   `cv.pdf`, and that filename must stay fixed forever. Replace the file when the
   CV changes; never rename it.
3. Scan the QR from an actual printed sheet at real size, on both iOS and Android,
   before approving the print order.

---

## What to edit

The file has seven marked spots. Search for `EDIT #`.

| # | What | Notes |
|---|------|-------|
| 1 | Social preview image | Optional. Add `og.png` (1200×630) and uncomment the tag. |
| 2 | Conference banner | Fill in the poster number. Delete the whole `<div class="banner">` block after the meeting. |
| 3 | The one-line tagline | Currently: *"I heat amorphous ice with a laser and watch what the liquid does before it freezes."* Make it yours — it is the sentence people will remember. |
| 4 | Availability line | Confirm "from March 2027" matches your actual plan before publishing. |
| 5 | A figure | Add `figure.png` and uncomment the `<figure>` block. One good figure is worth more than a paragraph. |
| 6 | Public repository link | If you have a repository worth showing, link it in the Software section. |
| 7 | `cv.pdf` | Put the PDF in the repository root. |

Everything else is drawn straight from the September 2026 CV: beamtime counts,
techniques, software, the six selected publications, education, awards, talks and
teaching.

---

## Design notes

Choices that are deliberate, in case you want to keep them while editing:

- **The beamtime board sits above research and publications.** For a beamline
  scientist reading this on a phone after scanning a QR code at a poster, "30+ XFEL
  beamtimes, including LCLS" is the fact that decides whether they keep reading.
  LCLS is listed first and the XFEL row is highlighted for the same reason.
- **The availability line is in the header, not the footer.** If it is not visible
  without scrolling, nobody asks.
- **Two email addresses.** The institutional address stops working after
  graduation; replies may arrive in 2027.
- **Nothing above the fold requires scrolling on a phone** — name, one line,
  availability, email. That is the whole job of the first screen.
- **No phone number.** This page is public; the number belongs on the card.
- **Dark mode and print styles are both handled.** `Ctrl/Cmd+P` produces a clean
  one-page summary, which is occasionally useful.

---

## Updating later

```bash
# edit index.html
git add index.html
git commit -m "Update publications"
git push
```

After the meeting: delete the banner block, add the poster to a presentations
list, and refresh `cv.pdf`.
