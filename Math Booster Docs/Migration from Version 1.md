# Migration from Version 1

Among many improvements that Math Booster version 2 introduces is a [[Theorem callouts|new format for theorem callouts]], which is ***much cleaner, more intuitive, more keyboard-friendly, and less plugin-dependent*** than the old format used in version 1.

To fully enjoy version 2, run the command `Migrate from version 1` to convert the old format to the new one.

> [!WARNING]
> **MAKE SURE YOU HAVE A BACKUP OF YOUR VAULT BEFORE CONTINUING. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DAMAGES OR OTHER LIABILITY ARISING FROM THIS OPERATION.**

## What's new in version 2

- [[Theorem callouts|New format for theorem callouts]]
- New indexing mechanism:
	- no longer blocks UI
	- no longer hard-codes theorem indices in notes directly
- [[Editor auto-completion]] improvements: filter theorems & equations (entire vault/recent notes/active note/dataview queries)
- [[Search modal]]: more control & flexibility than editor auto-completion
- Adding metadata to [[Theorem callouts#Adding metadata with comments|theorems]] and [[Equations#Adding metadata with comments|equations]] with comments
	- e.g. display name of equations
- Equation numbers now can be displayed even inside embeds

## Known issues

- Since version 1:
	- [Equation numbers not displayed in PDF export](https://github.com/RyotaUshio/obsidian-math-booster/issues/170): see [[Equations#PDF export|here]] for a quick fix
- New in version 2:
	- [Live preview fails to auto-number theorems correctly when a note is long enough](https://github.com/RyotaUshio/obsidian-math-booster/issues/192)
