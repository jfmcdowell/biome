---
"@biomejs/biome": patch
---

Fixed [#12703](https://github.com/biomejs/biome/issues/12703): The Markdown formatter no longer indents an empty `>` line that follows a list inside a block quote. Previously each run indented the line further, until a following paragraph moved out of the quote. The formatter also keeps the `>` of a block that follows such a list, such as a heading, which previously moved out of the quote.

```diff
 > - item one
 >   continued.
-  >
+>
 > Paragraph line one
 > line two.
```
