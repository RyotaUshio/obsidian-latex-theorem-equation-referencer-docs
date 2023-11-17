# Editor auto-completion

Math Booster lets you insert links to theorems or equations with ease.

In the editor, type `\ref` (by default; you can change it as you like in the plugin settings). Then, live suggestions for all theorem callouts & equation blocks in the entire vault show up.

[![Suggestions show up](https://github.com/RyotaUshio/obsidian-math-booster/raw/master/docs/fig/suggest-ref.png)](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/fig/suggest-ref.png)

Press Enter to insert a link to the selected item.

[![Suggestion inserted](https://github.com/RyotaUshio/obsidian-math-booster/raw/master/docs/fig/suggest-insert.png)](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/fig/suggest-insert.png)

Or you can jump to the selected item by pressing Cmd + Enter on Mac / Ctrl + Enter on Windows.

[![Jump to suggestion](https://github.com/RyotaUshio/obsidian-math-booster/raw/master/docs/fig/suggest-jump.png)](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/fig/suggest-jump.png)

Use `\tref` or `\eqref` (by default) instead of `\ref` to suggest only theorems or only equations.

[![Suggest only theorems](https://github.com/RyotaUshio/obsidian-math-booster/raw/master/docs/fig/suggest-theorem.png)](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/fig/suggest-theorem.png)

[![Suggest only equations](https://github.com/RyotaUshio/obsidian-math-booster/raw/master/docs/fig/suggest-equation.png)](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/fig/suggest-equation.png)

## [](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/suggest.md#available-search-keys)Available search keys

### [](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/suggest.md#theorem-suggestion)Theorem suggestion

| Key | Example |
| --- | --- |
| Environment type | definition, theorem, ... |
| Formatted title | Definition 1.1 (Continuity) |
| Formatted label[^1] | def:continuity |
| Note path | folder/note.md |

[^1]: Requires the `Include theorem callout label for search target` option to be turned on.

[![Theorem suggestion example](https://github.com/RyotaUshio/obsidian-math-booster/raw/master/docs/fig/suggest-theorem-ex.png)](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/fig/suggest-theorem-ex.png)

### [](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/suggest.md#equation-suggestion)Equation suggestion

| Key | Example |
| --- | --- |
| Equation number (if any) | (1) |
| LaTeX source code | `\lim_{n \to \infty} \int f_n \, d\mu = \int f \, d\mu` |
| Note path | folder/note.md |

[![Equation suggestion example](https://github.com/RyotaUshio/obsidian-math-booster/raw/master/docs/fig/suggest-equation-ex.png)](https://github.com/RyotaUshio/obsidian-math-booster/blob/master/docs/fig/suggest-equation-ex.png)

## Remark

This feature inserts wikilinks (i.e. `[[]]`) even if you are turning off `Use \[\[Wikilinks\]\]` in the app settings because markdown links are not suitable for dynamically updating the displayed text.

## Search modal

### Query type

Choose among:
- search both theorems & equations
- search theorem callouts only
- search equations only
### Search range

Specify the range of files to be searched. Available options are:
- Vault: the entire vault
- Recent notes: recently opened notes
- Active note: the note currently edited
- Dataview query: filter notes by powerful Dataview queries. Only available if Dataview is enabled.

#### Dataview queries

Although most parts of Math Booster don't require [Dataview](https://blacksmithgu.github.io/obsidian-dataview/), I recommend installing it together with Math Booster because it brings a tremendous filtering capability to this theorem & equation searching functionality.

Note that only [LIST queries](https://blacksmithgu.github.io/obsidian-dataview/queries/query-types/#list) without [GROUP BY](https://blacksmithgu.github.io/obsidian-dataview/queries/data-commands/#group-by) are supported.

> [!example]
> - Filtering by a folder
>   ```
>   LIST FROM "Papers"
>   ```
> - Filtering by a tag
>   ```
>   LIST FROM #statistics
>   ```
> - Filtering by dates
>   ```
>   LIST WHERE file.cday >= date("2023-11-01")
>   ```

