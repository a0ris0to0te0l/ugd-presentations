# UGD official

Presentation template for Goce Delchev University (Економски факултет, УГД), in Macedonian, 16:9. White content slides with the logo top right, red title and closing slides, in the ef.ugd.edu.mk colours.

There are two starting points in one style:

| | General | Event |
|---|---|---|
| Use for | Lectures and talks | Events with speakers and people to present |
| PowerPoint | `ugd-official-template.pptx` | `ugd-official-event-template.pptx` |
| LaTeX | `template.tex` | `template-event.tex` |
| Sample | `ugd-official-sample.pdf` | `ugd-official-event-sample.pdf` |

## Without LaTeX (PowerPoint)

1. Copy the `.pptx` and rename the copy.
2. Replace the placeholder text on each slide. Delete the slides you don't need.
3. Change the footer once: View → Slide Master → the „Содржина“ layout.
4. For a new slide: Home → New Slide → „Содржина“ or „Црвен слајд“. The logo, footer and slide number are already there.
5. For a photo in the event template: right-click the red circle → Format Shape → Fill → Picture or texture fill → Insert, then delete the initials.

The speaker notes on the slides repeat these steps. The file uses Arial and Calibri.

## With LaTeX

Copy these into the deck's folder, rename the `.tex` and compile with xelatex twice:

- `ugd-official-beamer.sty`
- `ugd-official-logo.png`, `ugd-official-badge.png`, `ugd-official-building.png`
- `fonts/`
- `template.tex` or `template-event.tex`

On the title slide, `\author` is optional. The short forms `\title[...]` and `\date[...]` make up the footer.

Normal frames with `\frametitle`, `itemize` and `block` work as usual. For laid-out slides, use `\UgdFrame{title}{TikZ}` with coordinates in cm from the top left of the 16 x 9 cm slide.

| Command | Does |
|---|---|
| `\UgdFrame{title}{TikZ}` | Content slide with placed elements |
| `\UgdClosingFrame{title}{message}` | Red closing slide |
| `\UgdCard{x}{y}{width}{height}{colour}` | Rounded card |
| `\UgdAvatar{x}{y}{diameter}{file}{initials}` | Round photo, or initials on red if the file is missing |
| `\UgdDisc{x}{y}{diameter}{fill}{text colour}{label}` | Small numbered circle |
| `\UgdPersonCard{x}{width}{name size in pt}{file}{initials}{name}{role}` | Person card; the role may be empty |

Colours: `ugdred`, `ugddark`, `ugdgrey`, `ugdtint`, `ugdline`, `ugdorange`.

## Changing the style

The `.sty` and the `.pptx` files are separate, so a style change has to be made in each of them. Rebuild the sample PDFs after changing the `.sty`.

## Fonts

Carlito and Liberation Sans, bundled in `fonts/` under the SIL Open Font License. Their licence texts are in the same folder.
