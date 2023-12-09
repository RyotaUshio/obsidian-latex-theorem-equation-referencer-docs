# Proof environment

> [!remark]
> - _This is still an experimental feature._
> - See also [this post](https://forum.obsidian.md/t/new-plugin-math-booster-take-mathematical-notes-just-as-in-latex/65089/3?u=ush) on the forum for more information.

This plugin supports $\LaTeX$-like proof environments.

```
`\begin{proof}`
Lorem ipsum dolor sit amet, consectetur adipiscing elit, ...
`\end{proof}`
```

`BEGINPROOF`
Lorem ipsum dolor sit amet, consectetur adipiscing elit, ...
`ENDPROOF`

- You can use any string you like, `PROOF`/`QED` for example, instead of `\begin{proof}`/`\end{proof}`. See [[#Settings & styling]].
- To quickly insert a proof, I recommend using a [[#Latex Suite snippet|Latex Suite snippet]] or [assigning a hotkey](https://help.obsidian.md/Customization/Custom+hotkeys) to the command `Insert proof`.
%%- Proofs can be folded (collapsed) in Live Preview.%%

### Custom texts

Use the following syntax to print custom text. 
Any inline markdown syntax can be used, but inline formulas will render with flickering in the live preview.

```
`\begin{proof}[Solution.]`
Lorem ipsum dolor sit amet, consectetur adipiscing elit, ...
`\end{proof}`
```

`BEGINPROOF[Solution.]`
Lorem ipsum dolor sit amet, consectetur adipiscing elit, ...
`ENDPROOF`

### Linked proofs

Suppose that you have a theorem like below and it has a [block ID](https://help.obsidian.md/Linking+notes+and+files/Internal+links#Link%20to%20a%20block%20in%20a%20note) `123456`.


> [!theorem] Title
> Content

^123456

The following will be printed as "*Proof of Theorem 2 (Title).*" by default.

```
`\begin{proof}`@[[#^123456]]
Lorem ipsum dolor sit amet, consectetur adipiscing elit, ...
`\end{proof}`
```

`BEGINPROOF`@[[Theorem callouts#^f58c13]]
Lorem ipsum dolor sit amet, consectetur adipiscing elit, ...
`ENDPROOF`

> [!remark]
> Alternatively, you can just write:
> ```
> \begin{proof}[Proof of [[#^123456]].]
> ```
> For now, I prefer this due to its potentially higher potability. 
> The strength of the `@` syntax is it's rendered dynamically depending on the current [[Profiles|profile]].

## Settings & styling

Don't like `\begin{proof}`? You can use any string you like instead. Go to the plugin setting tab, and modify the **Beginning of proof** and **Ending of proof** fields. Also take a look at the `Proofs` section in the [[Profiles]] editing menu.

Beginning/ending of proofs are given the following CSS classes.

- `.math-booster-begin-proof`/`.math-booster-end-proof`
- `.math-booster-begin-proof-{tag}`/`.math-booster-end-proof-{tag}`: `{tag}` is each tag associated with the profile applying to the note.

## Latex Suite snippet

Using the following [Latex Suite](https://github.com/artisticat1/obsidian-latex-suite) snippet, you can quickly insert a proof by just typing `proof`+`Tab`.

```js
    { trigger: "proof", replacement: "`\\begin{proof}`\n$0\n`\\end{proof}`", options: "t" }
```
