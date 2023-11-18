# Editor auto-completion

Math Booster lets you insert links to theorems or equations with ease.

In the editor, type `\ref` (by default; you can change it as you like in the plugin settings). Then, live suggestions for all theorem callouts & equation blocks in the entire vault show up.

- `Enter`: insert a link to the selected item.
- `Shift`+`Enter`: insert a link to the note containing the selected item.
- `Cmd`+`Enter` on Mac/`Ctrl`+`Enter` on Windows: jump to the selected item by pressing.

Use `\tref` or `\eqref` (by default) instead of `\ref` to suggest only theorems or only equations.

## Filter files to be searched

- `\rer`/`\trer`/`\eqrer` (by default): search only within recently opened notes
- `\rea`/`\trea`/`\eqrea` (by default): search only within active note

> [!remark]
> There are $3 \times 3 = 9$ variants of link auto-completion. It is recommended to turn off unnecessary auto-completions in the plugin setting to improve performance.

## Available search keys

### Theorem suggestion

| Key | Example |
| --- | --- |
| Environment type | definition, theorem, ... |
| Formatted title | Definition 1.1 (Continuity) |
| Formatted label[^1] | def:continuity |
| Note path | folder/note.md |

[^1]: Requires the `Include theorem callout label for search target` option to be turned on.

### Equation suggestion

| Key | Example |
| --- | --- |
| Equation number (if any) | (1) |
| LaTeX source code | `\lim_{n \to \infty} \int f_n \, d\mu = \int f \, d\mu` |
| Note path | folder/note.md |


> [!remark] Wikilinks v.s. markdown links
> This feature inserts wikilinks (i.e. `[[]]`) even if you are turning off `Use [[Wikilinks]]` in the app settings because markdown links are not suitable for dynamically updating the displayed text.