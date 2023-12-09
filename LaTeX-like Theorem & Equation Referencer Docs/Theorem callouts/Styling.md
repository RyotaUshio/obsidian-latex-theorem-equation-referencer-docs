# Styling

You can customize the appearance of theorem callouts either by **your own custom [CSS snippets](https://help.obsidian.md/Extending+Obsidian/CSS+snippets)** or by **[[#Styles gallery|preset sample styles]]**.

In the plugin settings, set `Theorem callouts > Style` to be `Custom` if you want to use your custom CSS snippets. 
This plugin defines several [[#Custom classes defined by this plugin|custom CSS classes]], allowing you to change the styles depending on specific languages or environments (theorem/definition/...).

Otherwise, the selected preset style will be applied. You need to reopen the note to see the style change.
When `Don't override the app's font setting when using sample styles` is turned on, the preset style will not change the default font family defined in the app's `Settings > Appearance > Font > Text font`.

> [!remark|*]
> "Custom" is highly recommended, since it will give you the most control. 
> 
> The preset styles are only for a trial purpose, and they might not work well with some non-default themes. You can view the CSS snippets for all the preset styles in the documentation or at the [GitHub repository](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer/tree/master/styles), which you can use as a starting point.

## CSS classes

### Obsidian built-in classes

- `.callout`
  - `.callout > .callout-title`
    - `.callout > .callout-title > .callout-icon`
    - `.callout > .callout-title > .callout-title-inner`
  - `.callout > .callout-content`

### Custom classes defined by this plugin

- `.theorem-callout`: Assigned to all theorem callouts.
- `.theorem-callout-{type}`: Indicates the environment type. For example, a theorem callout whose type is "theorem" will be given the `.theorem-callout-theorem` class.
- `.theorem-callout-{tag}`: A [[Profiles|profile]] has tags, each of which is converted to this `.theorem-callout-{tag}` class. As for the default profiles "English" and "Japanese", the tags are "en" and "ja", respectively. They are used to generate CSS classes `.theorem-callout-en` and `.theorem-callout-ja` indicating the language used for the theorem callout, making it possible to use different styles depending on it. I recommend defining language tags for your custom profiles.
- `.theorem-callout-main-title`: Lives under `.callout-title-inner`. For example, the "Theorem 1.1" part for `Theorem 1.1 (Cauchy-Schwarz)`
- `.theorem-callout-subtitle`: Lives under `.callout-title-inner`. For example, the "(Cauchy-Schwarz)" part for `Theorem 1.1 (Cauchy-Schwarz)`

## Styles gallery

Here are the list of preset sample styles. You can also view the CSS snippet generating each style.

Example theorem cited from: [Tao, Terence, ed. An introduction to measure theory. Vol. 126. American Mathematical Soc., 2011.](https://terrytao.files.wordpress.com/2012/12/gsm-126-tao5-measure-book.pdf)

### Plain

![Plain light](plain.png)
![Plain dark](plain-dark.png)

[<button>View CSS snippet</button>](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer/blob/master/styles/plain.scss)

### Framed

![Framed](framed.png)
![Framed dark](framed-dark.png)

[<button>View CSS snippet</button>](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer/blob/master/styles/framed.scss)

### MathWiki style

This beautiful style is taken from [MathWiki](https://github.com/zhaoshenzhai/MathWiki). A big thank you to [Zhaoshen Zhai](https://github.com/zhaoshenzhai), the owner of MathWiki and the [MathLinks](obsidian://show-plugin?id=mathlinks) plugin, for readily consenting to including it in this documentation.


![MathWiki style](mathwiki.png)

[<button>View CSS snippet</button>](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer/blob/master/styles/mathwiki.scss)

### Vivid

![Vivid light](vivid-light.png)
![Vivid dark](vivid-dark.png)

[<button>View CSS snippet</button>](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer/blob/master/styles/vivid.scss)
