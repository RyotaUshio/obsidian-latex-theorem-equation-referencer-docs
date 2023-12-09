# Theorem & equation rendering

## Reading view

This is the easiest one. `ctx.getSectioinInfo()` is pretty reliable in this case, so we can almost always use it to obtain positions in the document (i.e. line numbers).

### Reading view's variants that require special care

Line numbers obtained with `ctx.getSectionInfo()` is not always reliable because there can be some offsets in the case of embeds or hover popovers associated with headings or blocks.
#### Embeds

Use the `src` attribute to obtain a linktext.

#### Hover popover (page preview)

The `src` attribute is not available, but we can patch the core Page Preview's `onLinkHover` method so that the lastest `linktext` used to trigger hover page preview can be saved in the plugin instance. This approach was inspired by [Hover Editor](https://github.com/nothingislost/obsidian-hover-editor).

## Live preview

### Post-processing decorations provided by the Obsidian core

For callout CM6 widgets rendered by `MarkdownRenderer`, `ctx.getSectionInfo()` always returns `null`.

## PDF export

`ctx.getSectionInfo()` always returns `null`.
