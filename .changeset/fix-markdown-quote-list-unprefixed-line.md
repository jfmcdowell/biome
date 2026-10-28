---
"@biomejs/biome": patch
---

Fixed parsing of Markdown lines without a `>` marker after a list inside a block quote. Such a line no longer continues the list item inside the quote: it starts a new block after the quote, or continues the item's paragraph as plain text when it can't start a block.

```diff
 > - a
-  - b
+- b
```
