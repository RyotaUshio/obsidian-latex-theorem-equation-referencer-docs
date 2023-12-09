# Theorem callouts

This plugin offers **theorem callouts**, a special version of Obsidian's built-in [callouts](https://help.obsidian.md/Editing+and+formatting/Callouts). They are designed for creating theorem environments (theorem, definition, lemma, ...) in Obsidian as $\LaTeX$-like as possible.

## Basics

The syntax is:

```
> [!theorem] Title
> Content

> [!corollary]
> Content
```

^1d7868

It will be rendered as below.^[Appearance of theorem callouts depends on how you style them. See [[Styling]] for details.] As you can see, theorem callouts are **automatically numbered** by default. The numbering style can be configured in the settings.

> [!theorem] Title
> Content

^f58c13

> [!corollary]
> Content

^477885

One more important thing about theorem callouts is that they can be referenced as if using the `cleveref` package for $\LaTeX$. See [[Clever referencing]] for the details.

### Using aliases

Alternatively, you can use a shorer alias `thm` instead of `theorem`. It will be rendered the exactly same as above.

```
> [!thm] Title
> Content

> [!cor]
> Content
```

> [!thm] Title
> Content

^c61e2d

> [!cor]
> Content


Here's the complete list of available envionments and aliases.

| Environment name | Alias |
| ---------------- | ----- |
| axiom            | axm   |
| definition       | def   |
| lemma            | lem   |
| proposition      | prp  |
| theorem          | thm   |
| corollary        | cor   |
| claim            | clm   |
| assumption       | asm   |
| example[^1]          | exm   |
| exercise         | exr   |
| conjecture       | cnj   |
| hypothesis       | hyp   |
| remark           | rmk   |

[^1]: `> [!example]` conflicts with [Obsidian's built-in callout type](https://help.obsidian.md/Editing+and+formatting/Callouts#Supported%20types). There is a setting called `Don't treat "> [!example]" as a theorem callout`, and if it's turned on, an "example" theorem callout can be inserted only with the alias syntax `> [!exm]`.

> [!NOTE]
> The aliases are based on [Bookdown](https://bookdown.org/yihui/rmarkdown/bookdown-markdown.html#theorems), but some of the environments are not supported by it.

### Unnumbered theorem callouts

Similarly to the $\LaTeX$ syntax (e.g. `\begin{theorem*}`), the following will create an unnumbered theorem callout.

```
> [!lemma|*] Title
> Content
```

> [!lemma|*] Title
> Content


### Manually numbered theorem callouts

It is also possible to explicitly specify the theorem number by yourself. It's useful, for example, when making a side note about a textbook or a paper.

```
> [!def|A.1] Title
> Content
```

> [!def|A.1] Title
> Content


### Latex Suite snippets

You can insert theorem callouts via the following [Latex Suite](https://github.com/artisticat1/obsidian-latex-suite) snippets.

For example, type `def`+`Tab` or `definition`+`Tab` to insert a definition callout with [tabstops](https://github.com/artisticat1/obsidian-latex-suite/blob/main/DOCS.md#tabstops).

```js
    { trigger: "axm", replacement: "> [!axiom] $0\n> $1", options: "t" },
    { trigger: "def", replacement: "> [!definition] $0\n> $1", options: "t" },
    { trigger: "lem", replacement: "> [!lemma] $0\n> $1", options: "t" },
    { trigger: "prp", replacement: "> [!proposition] $0\n> $1", options: "t" },
    { trigger: "thm", replacement: "> [!theorem] $0\n> $1", options: "t" },
    { trigger: "cor", replacement: "> [!corollary] $0\n> $1", options: "t" },
    { trigger: "clm", replacement: "> [!claim] $0\n> $1", options: "t" },
    { trigger: "asm", replacement: "> [!assumption] $0\n> $1", options: "t" },
    { trigger: "exm", replacement: "> [!example] $0\n> $1", options: "t" },
    { trigger: "exr", replacement: "> [!exercise] $0\n> $1", options: "t" },
    { trigger: "cnj", replacement: "> [!conjecture] $0\n> $1", options: "t" },
    { trigger: "hyp", replacement: "> [!hypothesis] $0\n> $1", options: "t" },
    { trigger: "rmk", replacement: "> [!remark] $0\n> $1", options: "t" },
    { trigger: "axiom", replacement: "> [!axiom] $0\n> $1", options: "t" },
    { trigger: "definition", replacement: "> [!definition] $0\n> $1", options: "t" },
    { trigger: "lemma", replacement: "> [!lemma] $0\n> $1", options: "t" },
    { trigger: "proposition", replacement: "> [!proposition] $0\n> $1", options: "t" },
    { trigger: "theorem", replacement: "> [!theorem] $0\n> $1", options: "t" },
    { trigger: "corollary", replacement: "> [!corollary] $0\n> $1", options: "t" },
    { trigger: "claim", replacement: "> [!claim] $0\n> $1", options: "t" },
    { trigger: "assumption", replacement: "> [!assumption] $0\n> $1", options: "t" },
    { trigger: "example", replacement: "> [!example] $0\n> $1", options: "t" },
    { trigger: "exercise", replacement: "> [!exercise] $0\n> $1", options: "t" },
    { trigger: "conjecture", replacement: "> [!conjecture] $0\n> $1", options: "t" },
    { trigger: "hypothesis", replacement: "> [!hypothesis] $0\n> $1", options: "t" },
    { trigger: "remark", replacement: "> [!remark] $0\n> $1", options: "t" },
```

### Insert a theorem callout via GUI

If you prefer, you can run the `Insert theorem callout` command to insert a theorem callout via a popout like this.

![[Theorem callouts-20231117082725480.webp|500]]

### Customizing the display names of theorem environments


See [[Profiles]] for the details.

## Adding metadata with comments

You can add some metadata or options with markdown comments (`%% ... %%`).

> [!NOTE]
> Equations also can be given metadata with $\LaTeX$ comments; see [[Equations#Adding metadata with comments|here]].

Currently, `label`, `display`, and `main` are available. The followings are all appropriate syntaxes.

```
> [!theorem]
> %% label: my-theorem %%
> %% display: My Awesome Theorem %%
> %% main %%

> [!theorem]
> %% label: my-theorem %% %% display: My Awesome Theorem %% %% main %%

> [!theorem]
> %% 
> label: my-theorem
> display: My Awesome Theorem
> main: true
> %%
```

They are provided as key-value pairs with a yaml-like `key: value` format. But as an exception, you can write `main` instead of `main: true`.

### `label`

Has no effect for now. It might be used when exporting to Pandoc markdown or $\LaTeX$ is supported in the future.

### `display`

When set, all links to this theorem callout are displayed with this text instead of the usual formatted theorem title (see also: [[Clever referencing]]).

### `main`

When set, this theorem is marked as the "main" one of the note containing it. This means all links to this note are displayed with a formatted title of this theorem instead of the note title (see also: [[Clever referencing]]).

## Styling theorem callouts

Although theorem callouts are styled by the preset style by default, you have the full control over their styling through [CSS snippets](https://help.obsidian.md/Extending+Obsidian/CSS+snippets).

See [[Styling|here]] for more details.

> [!note]
> I strongly recommend using your custom styling instead of the presets because the presets are only tested for the default theme and might not work well with other community themes.

To use your custom CSS snippets, go to `Settings > Community plugins > LaTeX-like Theorem & Equation Referencer > Global > Theorem callouts > Style` and set it to `Custom`.

As examples, the snippets used for the presets can be found on the [GitHub repository](https://github.com/RyotaUshio/obsidian-latex-theorem-equation-referencer/tree/master/styles) of this plugin.

## Remarks

Theorem callouts will not work perfectly if they are nested inside another callout. Always use them as top-level blocks of your note.
