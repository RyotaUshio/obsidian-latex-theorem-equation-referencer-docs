# Getting started

Hello Obsidian community! I've recently updated my plugin called [LaTeX-like Theorem & Equation Referencer](https://ryotaushio.github.io/obsidian-latex-theorem-equation-referencer/), so I'd like to introduce it to you.

Basically, it adds some features that are indispensable to doing math in a LaTeX-like way but are missing from Obsidian: automatic equation numbering, theorem environments, ...　and some more special gifts!

I believe it will be useful for everyone who does math in Obsidian.



## Automatic equation numbering & link completion enhancement

Suppose a note of yours has an equation like this:

```
$$
\lim_{n \to \infty} \int f_n \, d\mu = \int f \, d\mu
$$
```

Now you want to reference this equation. As usual, you type `[[^` to trigger the link completion. Then, it will show you *plain* LaTeX source like this:

![[Pasted image 20231124222059.png]]

With this plugin installed, you will see something much cooler instead: the equation is now *rendered*.

![[Pasted image 20231124222252.png]]


Now, type `Enter` to insert a link. Then this plugin automatically numbers the target equation, and moreover, the link `[[#^bdf1f4]] ` you just added is displayed with the corresponding equation number!

![[Pasted image 20231124222314.png]]

Additionally, this plugin provides new types of link completion as well. For example, type `\ref` instead of `[[^`. 

It will show you all equations (and theorems; explained later) from the entire vault. It supports fuzzy search for LaTeX source and note path, so you don't have to accurately remember what equation lives in what note.

![[Pasted image 20231124222405.png]]


## Theorem environments

This plugin also supports various theorem environments.

```
> [!theorem] Title
> Content

> [!thm] Title
> Content
```

> [!theorem] Title
> Content

> [!thm] Title
> Content
