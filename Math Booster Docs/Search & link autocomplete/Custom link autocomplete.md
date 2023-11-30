# Custom link autocomplete

In the editor, type `\ref` (by default). Then, live suggestions for all theorem callouts & equation blocks in the entire vault show up. 

- `Enter`: insert a link to the selected item.
- `Shift`+`Enter`: insert a link to the note containing the selected item.
- `Cmd`+`Enter` on Mac/`Ctrl`+`Enter` on Windows: jump to the selected item by pressing.

Use `\tref` or `\eqref` (by default) instead of `\ref` to suggest only theorems or only equations.

## Filter files to be searched

- `\rer`/`\trer`/`\eqrer` (by default): search only within recently opened notes
- `\rea`/`\trea`/`\eqrea` (by default): search only within active note

> [!remark]
> You can change the trigger strings (e.g. `\ref`) to whatever you like in the plugin settings.

> [!remark]
> There are $3 \times 3 = 9$ variants of custom autocomplete. It is recommended to turn off unnecessary ones in the plugin setting to improve performance.

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


> [!remark] Wikilinks vs. markdown links
> This feature inserts wikilinks (i.e. `[[]]`) even if you are turning off `Use [[Wikilinks]]` in the app settings because markdown links are not suitable for dynamically updating the displayed text.
