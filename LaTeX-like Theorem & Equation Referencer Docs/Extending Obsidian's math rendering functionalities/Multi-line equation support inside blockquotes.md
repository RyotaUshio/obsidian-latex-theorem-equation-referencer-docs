# Multi-line equation support inside blockquotes

> [!important]
> This feature is planned to be removed from this plugin, and instead, it will be available as a separate plugin [**Better Math in Callouts & Blockquotes**](https://github.com/RyotaUshio/obsidian-math-in-callout), featuring a bunch of improvements. Currently awaiting for approval by the Obsidian team.

Obsidian natively renders $\LaTeX$ inside blockquotes, but it breaks when you use line breaks inside a math like this:

```
> $$
> \begin{align}
> a &= b \\
>   &= c
> \end{align}
> $$
```

With this plugin, you will no longer have this nightmare!