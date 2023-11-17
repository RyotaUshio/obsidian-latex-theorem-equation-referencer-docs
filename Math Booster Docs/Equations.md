# Equations

With Math Booster, you can get your equations get automatically numbered and reference them by their equation numbers,[^1] just as in $\LaTeX$.

[^1]: It was one of Obsidian's [long-standing](https://forum.obsidian.md/t/automatic-equation-numbering-latex-math/1325) problems.

Note that only equations with backlinks (i.e. the ones that are referenced elsewhere) are numbered.

## Examples

Suppose you have these three equations:

`````col

````col-md

**Source:**

```
$$
f(x)
$$

$$
g(x) \tag{$\ast$}
$$

$$
h(x)
$$
```

````

````col-md

**Rendered:**

![[Equations-20231118084238497.webp]]
````
`````

Now, insert a link to the last equation $h(x)$. Then, you will see the equation number `(1)` is xautomatically added to the equation and the inserted link is displayed with the corresponding equation number. 

`````col

````col-md

**Source:**

```
$$
f(x)
$$

$$
g(x) \tag{$\ast$}
$$

$$
h(x)
$$

Link to $h(x)$: [[#^934f5c]]
```

````

````col-md

**Rendered:**

![[Equation numbers-20231117195856635.webp]]

````
`````

But we can do this without Math Booster, right? All we have to do is just adding a [display text](https://help.obsidian.md/Linking+notes+and+files/Internal+links#Change+the+link+display+text) manually, like so: `[[#^934f5c|(1)]]`.

The problem of this naive approach is that the display text `(1)` will be never updated. What if we add a link to the first equation $f(x)$?

...Well, Math Booster does it right!

`````col

````col-md

**Source:**

```
$$
f(x)
$$

^05ce41

$$
g(x) \tag{$\ast$}
$$

$$
h(x)
$$

^934f5c

Link to $h(x)$: [[#^934f5c]] 
Link to $f(x)$: [[#^05ce41]] 
```
````

````col-md
**Rendered:**

![[Equation numbers-20231117195938005.webp]]

````

`````

Note that linking to the second equation $g(x)$ doesn't affect the numbers of other equations, because it has manually specified `\tag{...}` and Math Booster respects it.

`````col

````col-md

**Source:**

```
$$
f(x)
$$

^05ce41

$$
g(x) \tag{$\ast$}
$$

^f16880

$$
h(x)
$$

^934f5c

Link to $h(x)$: [[#^934f5c]] 
Link to $f(x)$: [[#^05ce41]] 
Link to $g(x)$: [[#^f16880]]
```

````

````col-md

**Rendered:**

![[Equation numbers-20231117200012405.webp]]

````
`````

Also observe that deleting these links remove the equation numbers.

## Adding metadata with comments

Just like for [[Theorem callouts#Adding metadata with comments|theorem callouts]], you can attach some metadata to each equation via $\LaTeX$ comments (`% ...`) with a yaml-like key-value pair syntax (`key: value`).

The currently available keys are `label` and `display`. They are also available for theorems, and their functionalities are also the same as the theorem counterparts.

### `label`

Has no effect for now. It might be used when exporting to Pandoc markdown or $\LaTeX$ is supported in the future.

### `display`

When set, all links to this equation are displayed with this text instead of its equation number (see also: [[Clever referencing]]).

## Remarks

### About markdown links

If you are turning off `Use [[Wikilinks]]` in the app settings, you will have to the [live suggestion](suggest) feature provided by this plugin instead of Obsidian's built-in `[[` suggestion. This is because the built-in suggestion generates markdown links (i.e. `[]()`) in this case, but they are not suitable for dynamically updating the displayed text.

### Spacing

You must include at least one line break between `$$ ... $$` if you want the equation to be numbered.
Otherwise, Obsidian will not recognize it as a math block.

In other words: 
```latex
Good
$$
f(x)
$$

Good
$$f(x)
$$

Good
$$
f(x)$$

Bad
$$f(x)$$
```

Also, make sure there is an empty line under the block ID of the equation. Again, this is needed due to how Obsidian works. You can enforce this using the [Linter](obsidian://show-plugin?id=obsidian-linter) plugin's rule "[Empty Line Around Math Blocks](https://platers.github.io/obsidian-linter/settings/spacing-rules/#empty-line-around-math-blocks)."

### Equations in callouts/blocks

You cannot insert a link to equations in callouts or blockquotes. 
This is an inherent limitation of Obsidian rather than this plugin.

### Hover page preview

Equation numbers will not be displayed in the hover preview ([Page Preview](https://help.obsidian.md/Plugins/Page+preview)). This is because there is seemingly no means to reliably get the corresponding line number in a hover popover.

But the good news is that [Hover Editor](https://github.com/nothingislost/obsidian-hover-editor) lets you avoid this problem.

### PDF export

Currently, dynamic equation numbers are not rendered in exported PDFs.
As a quick fix, you can run the command `Convert equation numbers in the current note to static \tag{}` to explicitly insert the equation numbers as static LaTeX tags (`\tag{...}`) to avoid this issue.

Make sure you make a backup before this command and undo the tag insertion after exporting finishes.

> [!info]
> This issue is tracked [here](https://github.com/RyotaUshio/obsidian-math-booster/issues/170). Let me know if you have any idea to fix this issue in a cleaner way!

## The `align` Environment

You can choose whether multi-line equations in an `align` environment are numbered _collectively as a group_:

![Collectively](https://ryotaushio.github.io/obsidian-math-booster/fig/equation_number_align_0.png)

or _individually_.

![Individually](https://ryotaushio.github.io/obsidian-math-booster/fig/equation_number_align_1.png)

Go to the `Number line by line in align` section in the plugin preferences to change the current setting.

When `Number line by line in align` is turned on, you can exclude a line from numbering by inserting `\nonumber`, just like in $\LaTeX$.

![Collectively](https://ryotaushio.github.io/obsidian-math-booster/fig/equation_number_align_2.png)
