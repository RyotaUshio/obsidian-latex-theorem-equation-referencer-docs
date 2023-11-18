# Math Booster version 2

[Math Booster](https://github.com/RyotaUshio/obsidian-math-booster) is an [Obsidian](https://obsidian.md) plugin for mathematical note-takers.

> [!remark] Major version update
> Using Math Booster since version 1? See [[Migration from Version 1]].

## Features

- [[Theorem callouts|Theorem environments]]
- [[Equations|Automatic equation numbering]]
- [[Rendering equations inside callouts]]
- [[Multi-line equation support inside blockquotes]]
- [[Clever referencing]]
- [[Search modal]]
- [[Proof environment|Proof environment (experimental)]]

## Installation

Since version 2 is still in beta, it's not on the community plugin browser yet.

But you can install the latest beta release using [BRAT](obsidian://show-plugin?id=obsidian42-brat):

1.  Install BRAT and enable it.
2.  Go to `Options`. In the `Beta Plugin List` section, click on the `Add Beta plugin` button.
3.  Copy and paste `RyotaUshio/obsidian-math-booster` in the pop-up prompt and click on **Add Plugin**.
4.  _(Optional but highly recommended)_ Turn on `Auto-update plugins at startup` at the top of the page.
5.  Go to `Community plugins > Installed plugins`. You will find “Math Booster” in the list. Click on the toggle button to enable it.

## Dependencies

### Obsidian plugins

Math Booster requires [MathLinks](https://github.com/zhaoshenzhai/obsidian-mathlinks) version 0.5.1 or higher installed to work properly ([[Clever referencing]]).

In version 2, [Dataview](https://github.com/blacksmithgu/obsidian-dataview) is no longer required. But I strongly recommend installing it because it enhances Math Booster's [[Search modal#Dataview queries|search]] functionality significantly.

### Fonts

You have to install [CMU Serif](https://www.cufonfonts.com/font/cmu-serif) (which this documentation uses) to get some of the preset styles for [[Theorem callouts|theorem callouts]] displayed properly.

Additionally, [Noto Sans JP](https://fonts.google.com/noto/specimen/Noto+Sans+JP) is required for render the preset styles properly in Japanese.

## Contributing to this docs

This documentation is generated from an Obsidian vault located under the `Math Booster Docs` folder of [this GitHub repository](https://github.com/RyotaUshio/math-booster-docs). To contribute:

1. [Fork](https://docs.github.com/ja/get-started/quickstart/fork-a-repo) the repository and clone the fork.
   ```
    git clone https://github.com/<YOUR NAME>/math-booster-docs.git
    ```
2. Open the `Math Booster Docs` folder under the cloned repository as an Obsidian vault ([Obsidian Help](https://help.obsidian.md/Getting+started/Create+a+vault#Open+existing+folder)).
3. Make changes in Obsidian so that links are properly updated.
4. Commit & push your changes to the fork and [make a pull request](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) to the original repository.

> [!remark] Webpage HTML Export
> This documentation website is generated from the `Math Booster Docs` vault using the awesome [Webpage HTML Export](https://github.com/KosmosisDire/obsidian-webpage-export) plugin.


## Credits

Math Booster has been inspired a lot by the great Obsidian community; see [[Credits]].

## Say thank you

If you find this plugin useful, please consider supporting my work by buying me a coffee!

<a href="https://www.buymeacoffee.com/ryotaushio" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>