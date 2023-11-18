# Local settings

Many of Math Booster's settings can be applied specifically to a certain folder or file, and they are called **local settings**. 

In the plugin setting tab, you can set up the local settings for the vault root (which we usually call _global_).
They apply all the files in the vault unless overwritten by another local settings for a lower-level folder/file.

You can make use of this cascaded structure for customizing the settings specific to each textbook or paper, for example:

```
Folder structure                    Local settings
───────────────────────────────────────────────────────────────
vault root
├── Textbook written in Japanese    <--- Profile = "Japanese"
│   ├── Chapter 1
│   │   ├── 1-1.md                  <--- Number prefix = "1.1."
│   │   └── 1-2.md                  <--- Number prefix = "1.2."
│   ├── Chapter 2
│   │   ├── 2-1.md                  <--- Number prefix = "2.1."
│   │   └── 2-2.md                  <--- Number prefix = "2.2."
├── Paper written in English.md     <--- Profile = "English"
├── ...
```

## How to set up local settings

There are several ways to set up the local settings.

- File explorer: Right-click on a file/folder, and then click `Math Booster: Open local settings`.
- Plugin setting tab (`Global` for the vault root, `Local` for other files/folders)
- `Open local settings for the current note` command
- `Open local settings for the current note` button in theorem callout settings
