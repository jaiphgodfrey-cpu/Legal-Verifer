# Legal Verifier

Check a PDF against its extracted text, one sentence at a time. Works offline.

## Start

1. Select the **Source PDF**.
2. Select the **Text file** (.json). You can select more than one.
3. Press **Open**.

To continue earlier work: tap it under **Recent work**, or use **Open project file**.

## Verify

Left: the PDF. Right: the sentence to check.

| Button | Use when |
|---|---|
| **Correct** | The text matches the PDF |
| **Wrong** | The text does not match. Fix it, then press **Save** |
| **Undo** | Reverse the last action |

Only the top sentence is active. Verify it and the next one moves up.

## Keyboard

| Key | Action |
|---|---|
| `C` | Correct |
| `X` | Wrong |
| `Z` | Undo |
| `Enter` | Save the correction |
| `Shift+Enter` | New line in the correction |
| `Esc` | Leave the text box |
| `R` | Rotate the PDF page |
| `←` `→` | Previous / next page |

## Rotate

**Rotate** turns the PDF page 90° each tap. Pages start in portrait. The rotation is remembered for each page.

## Tables

A table row shows as a grid of cells. **Correct** accepts the whole row. **Wrong** opens one box per cell. `Enter` saves.

## Missing text

Use the **Missing text** box when the extracted text left something out.

Format:

```
paragraph: words before [missing text] words after
```

Examples:

```
3c: the fee shall be [not less than] 5,000 per piece
3c: [Every person] shall pay the fee
3c: shall pay the fee [within thirty days]
```

Rules:
- Missing part goes in `[ ]`.
- Use as many words around it as needed. One is enough if it is clear.
- One gap per line.
- The page is already known. Do not write it.

## Save

- Progress saves automatically in this browser.
- **Save** writes a project file with the PDF and all progress. Keep it as your backup, and use it to continue on another device or browser.
- **Export** gives the results as JSON: original text, corrections, status, and missing text for every page.
