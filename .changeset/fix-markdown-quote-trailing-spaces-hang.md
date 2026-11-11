---
"@biomejs/biome": patch
---

Fixed a hang when parsing Markdown files where a list item contains a block quote with a list, and a later line of that quote has only a `>` followed by two or more spaces. Biome no longer stops responding on such files, and such a line no longer makes the list inside the quote loose.
