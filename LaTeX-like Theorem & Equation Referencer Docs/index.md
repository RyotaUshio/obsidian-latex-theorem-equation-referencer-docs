---
title: LaTeX-like Theorem & Equation Referencer Docs
---
# LaTeX-like Theorem & Equation Referencer

[LaTeX-like Theorem & Equation Referencer](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer) is an [Obsidian](https://obsidian.md) plugin that provides a powerful indexing & referencing system for theorems & equations in your vault, bringing $\LaTeX$-like workflow into Obsidian.

> [!remark] Math Booster
> This plugin had been called **Math Booster** until before 2.2.0, but has been renamed for better clarity and discoverability.

> [!remark] Major version update
> Using this plugin since Math Booster version 1? See [[Migration from Math Booster version 1]].

## Features

- [[Theorem callouts|Theorem environments]]
- [[Equations|Automatic equation numbering]]
- [[Clever referencing]]
- [[Search & link autocomplete]]
	- [[Enhancing Obsidian's built-in link autocomplete]]
	- [[Custom link autocomplete]]
	- [[Search modal]]
- [[Proof environment|Proof environment (experimental)]]

> [!important]
> For more modular and focused enhancements, some features are planned to be transitioned from this plugin to dedicated, specialized plugins in the near future. Below are the upcoming changes:
> 
> ##### Transitioning to [**Better Math in Callouts & Blockquotes**](https://github.com/RyotaUshio/obsidian-math-in-callout)
> 
> - Rendering equations inside callouts
> - Multi-line equation support inside blockquotes
> 
> ##### Transitioning to [**Rendered Block Link Suggestions**](https://github.com/RyotaUshio/obsidian-rendered-block-link-suggestions)
> 
> - [[Enhancing Obsidian's built-in link autocomplete|Render equations in Obsidian's built-in link suggestions]]

## Installation

You can install this plugin via Obsidian's community plugin browser (see [here](https://help.obsidian.md/Extending+Obsidian/Community+plugins#Install+a+community+plugin) for instructions).

Also, you can test the latest beta release using [BRAT](https://github.com/TfTHacker/obsidian42-brat):

1.  Install BRAT and enable it.
2.  Go to `Options`. In the `Beta Plugin List` section, click on the `Add Beta plugin` button.
3.  Copy and paste `RyotaUshio/obsidian-latex-theorem-equation-referencer` in the pop-up prompt and click on **Add Plugin**.
4.  _(Optional but highly recommended)_ Turn on `Auto-update plugins at startup` at the top of the page.
5.  Go to `Community plugins > Installed plugins`. You will find “LaTeX-like Theorem & Equation Referencer” in the list. Click on the toggle button to enable it.

## Dependencies

### Obsidian plugins

This plugin requires [MathLinks](https://github.com/zhaoshenzhai/obsidian-mathlinks) version 0.5.3 or higher installed to work properly ([[Clever referencing]]).

In version 2, [Dataview](https://github.com/blacksmithgu/obsidian-dataview) is no longer required. But I strongly recommend installing it because it enhances this plugin's [[Search modal#Dataview queries|search]] functionality significantly.

### Fonts

You have to install [CMU Serif](https://www.cufonfonts.com/font/cmu-serif) (which this documentation uses) to get some of the preset styles for [[Theorem callouts|theorem callouts]] displayed properly.

Additionally, [Noto Sans JP](https://fonts.google.com/noto/specimen/Noto+Sans+JP) is required for render the preset styles properly in Japanese.

## Contributing to this docs

This documentation is generated from an Obsidian vault located under the `LaTeX-like Theorem & Equation Referencer Docs` folder of [this GitHub repository](https://github.com/RyotaUshio/math-booster-docs). To contribute:

1. [Fork](https://docs.github.com/ja/get-started/quickstart/fork-a-repo) the repository and clone the fork.
   ```
    git clone https://github.com/<YOUR NAME>/obsidian-latex-theorem-equation-referencer-docs.git
    ```
2. Open the `LaTeX-like Theorem & Equation Referencer Docs` folder under the cloned repository as an Obsidian vault ([Obsidian Help](https://help.obsidian.md/Getting+started/Create+a+vault#Open+existing+folder)).
3. Make changes in Obsidian so that links are properly updated.
4. Commit & push your changes to the fork and [make a pull request](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) to the original repository.


> [!remark] Webpage HTML Export
> This documentation website is generated using the awesome [Webpage HTML Export](https://github.com/KosmosisDire/obsidian-webpage-export) plugin.

## Credits

This plugin has been inspired a lot by the great Obsidian community; see [[Credits]].

## Say thank you

If you find this plugin useful, please consider supporting my work by buying me a coffee!

<a href="https://www.buymeacoffee.com/ryotaushio" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>