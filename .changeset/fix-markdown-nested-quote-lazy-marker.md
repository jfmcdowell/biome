---
"@biomejs/biome": patch
---

Fixed parsing of a Markdown line that continues a paragraph in a nested block quote but has fewer `>` markers than the paragraph's quote. The markers it has are now parsed as quote markers instead of paragraph text, so the formatter writes the full prefix on that line, as it already did when the quote isn't in a list item.

```diff
 1.  item
     > q
     > > nested
-    > lazy continuation
+    > > lazy continuation
```

When such a line holds only `=` or `-` characters, the formatter now escapes the first one, so the full prefix doesn't turn the line into a setext heading underline.

```diff
 > > nested
-> ===
+> > \===
```
