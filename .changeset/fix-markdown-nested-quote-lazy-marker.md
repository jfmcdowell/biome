---
"@biomejs/biome": patch
---

Fixed parsing of a Markdown line that continues a paragraph in a nested block quote inside a list item but has fewer `>` markers than the paragraph's quote. The markers it has are now parsed as quote markers instead of paragraph text, so the formatter writes the full prefix on that line, as it already does when the quote isn't in a list item.

```diff
 1.  item
     > q
     > > nested
-    > lazy continuation
+    > > lazy continuation
```
