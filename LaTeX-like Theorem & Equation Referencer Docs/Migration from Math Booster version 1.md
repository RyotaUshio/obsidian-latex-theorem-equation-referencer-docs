# Migration from Math Booster version 1

Among many improvements that LaTeX-like Theorem & Equation Referencer/Math Booster version 2 introduces is a [[Theorem callouts|new format for theorem callouts]], which is ***much cleaner, more intuitive, more keyboard-friendly, and less plugin-dependent*** than the old format used in version 1.

To fully enjoy version 2, run the command `Migrate from version 1` to convert the old format to the new one.

> [!WARNING]
> **MAKE SURE YOU HAVE A BACKUP OF YOUR VAULT BEFORE CONVERSION. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DAMAGES OR OTHER LIABILITY ARISING FROM THIS OPERATION.**

## What's new in version 2

- [[Theorem callouts|New format for theorem callouts]]:
	- much cleaner,
	- more intuitive,
	- more keyboard-friendly,
	- and less plugin-dependent than the previous format
- New indexing mechanism:
	- no longer blocks UI
	- no longer hard-codes theorem indices in notes directly
- [[Enhancing Obsidian's built-in link autocomplete]]: now equations are rendered in the built-in completion as well.
- [[Custom link autocomplete]] improvements: filter theorems & equations (entire vault/recent notes/active note/dataview queries)
- [[Search modal]]: more control & flexibility than editor autocomplete
- Adding metadata to [[Theorem callouts#Adding metadata with comments|theorems]] and [[Equations#Adding metadata with comments|equations]] with comments
	- e.g. display name of equations
- Theorem/equation numbers now can be displayed *almost everywhere*:
  ````col   
  ```col-md
  textAlign=center
  ===
  #### Version 1
  
  
  |                    | Theorem number | Equation number |
  | ------------------ | -------------- | --------------- |
  | Reading view       |       ✅         |         ✅        |
  | Live preview       |       ✅         |         ✅        |
  | Embeds             |        ✅       |                 |
  | Hover page preview |        ✅       |                 |
  | PDF export         |       ✅         |                 |
  ```
  
  ```col-md
  textAlign=center
  ===
  #### **Version 2 🎉**
  

  |                    | Theorem number | Equation number |
  | ------------------ | -------------- | --------------- |
  | Reading view       |       ✅         |         ✅        |
  | Live preview       |       ✅         |         ✅        |
  | Embeds             |        ✅       |           ✅      |
  | Hover page preview |        ✅        |        ✅         |
  | PDF export         |       ✅         |            ✅     |
  ```
  ````

## No longer supported

- ["Show backlinks" right-click menu](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer/blob/1.0.4/docs/backlinks.md)
	- Use [Strange New Worlds](https://github.com/TfTHacker/obsidian42-strange-new-worlds) instead.
- [Projects](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer/blob/1.0.4/docs/projects.md)
	- might be supported later with some improvement
