---
"@biomejs/biome": patch
---

Fixed [#12703](https://github.com/biomejs/biome/issues/12703): The Markdown formatter no longer indents an empty `>` line that follows a list inside a block quote. Previously each run indented the line further, until a following paragraph moved out of the quote. The formatter also keeps the `>` of a block that follows such a list, such as a heading, which previously moved out of the quote. Lazy continuation lines of a list item inside a block quote now get the quote's `>` markers, or join the previous line when they were indented, instead of shifting on every run.

```diff
 > - item one
 >   continued.
-  >
+>
 > Paragraph line one
 > line two.
```
