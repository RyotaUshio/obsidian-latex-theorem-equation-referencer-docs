# Search modal

Run the `Search` command to open a search modal.

This is similar to [[Custom link autocomplete]], but available as a search modal like [Quick Switcher](https://help.obsidian.md/Plugins/Quick+switcher) along with further search control functionalities.

> [!tip] Search modal can be controled by keyboard alone without mouse
> Use the `Tab`/`Shift`+`Tab` to move back and forth between the search window and two drop-down menus (`Query type` & `Search range`).
> 
> Also, you can use `Shift`+`ArrowUp`/`Shift`+`ArrowDown` to move around in each dropdown menu.

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
- Dataview query: filter notes by powerful [Dataview](https://blacksmithgu.github.io/obsidian-dataview/) queries. Only available if Dataview is enabled.

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

