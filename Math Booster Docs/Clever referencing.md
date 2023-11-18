# Clever referencing

When you insert a internal link to [[Theorem callouts|theorem callouts]] or equation blocks, 
the link will be displayed with the corresponding theorem's title or [[Equations|equation number]].

See also:
- [[Theorem callouts#`display`]]
- [[Theorem callouts#`main`]]
- [[Equations#`display`]]

> [!remark]
>  This feature only works for wikilinks (`[[]]`), and markdown links (`[]()`) are not supported. Even if you are turning off `Use [[Wikilinks]]` in the app settings, you can still insert wikilinks using this plugin's [[Search modal|auto-completion]] feature.

> [!rmk] MathLinks API
> This functionality is implemented using the [MathLinks](https://github.com/zhaoshenzhai/obsidian-mathlinks) API. I wrote a sample plugin to demonstrate its usage; it can be found [here](https://github.com/RyotaUshio/obsidian-mathlinks-api-sample-plugin).
