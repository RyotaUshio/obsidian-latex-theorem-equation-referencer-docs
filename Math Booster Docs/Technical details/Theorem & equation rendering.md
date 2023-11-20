# Theorem & equation rendering

## Reading view

This is the easiest one. `ctx.getSectioinInfo()` is pretty reliable in this case, so we can almost always use it to obtain positions in the document (i.e. line numbers).

### Reading view's variants that require special care

Line numbers obtained with `ctx.getSectionInfo()` is not always reliable because there can be some offsets in the case of embeds or hover popovers associated with headings or blocks.
#### Embeds

Use the `src` attribute to obtain a linktext.

#### Hover popover (page preview)

The `src` attribute is not available, but we can listen to the `app.workspace.on('hover-link', ...)` event.

## Live preview

### Post-processing decorations provided by the Obsidian core

For callout CM6 widgets rendered by `MarkdownRenderer`, `ctx.getSectionInfo()` always returns `null`.

## PDF export

`ctx.getSectionInfo()` always returns `null`.
