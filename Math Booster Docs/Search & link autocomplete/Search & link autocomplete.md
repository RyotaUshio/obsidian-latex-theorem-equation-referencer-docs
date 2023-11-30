# Search & link autocomplete

Math Booster provides three different tools for quickly search or insert links to your theorems and equations:

- [[Enhancing Obsidian's built-in link autocomplete]]
- [[Custom link autocomplete]]
- [[Search modal]]

## Overview

Math Booster [[Enhancing Obsidian's built-in link autocomplete|enhances Obsidian's built-in link autocomplete]] (the one that is triggered when you type `[[` in the editor) by displaying formatted theorem titles and rendered equations.

This built-in autocomplete works in a *top-down* manner: you select a note first, and then choose a theorem or an equation contained in it.
This is useful when you know exactly which note the theorem/equation that you want to reference lives in.

However, it might be also the case you're not very sure where the target theorem/equation is. In that case, you can use either of the following features Math Booster offers:

- [[Custom link autocomplete]]
	- Similar to the built-in autocomplete, but you can search theorems and equations ***across*** the vault, recently opened notes, or the currently active note.
- [[Search modal]]
	- Essentially the same as [[Custom link autocomplete]], but available in as a modal similar to Quick Switcher or Command Palette.
	- Also, it adds Dataview query support to the editor completion, which means you can search theorems or equations based on folders, tags, properties, and more!

Both of them work in a *bottom-up* manner as opposed to the built-in completion. Now you have different tools that you can use for different situations.
