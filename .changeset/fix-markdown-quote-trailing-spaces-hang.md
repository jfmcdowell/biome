---
"@biomejs/biome": patch
---

Fixed parsing of Markdown block quote lines that have only spaces or tabs after the `>`. Biome now treats such a line as blank, like a bare `>` line. Before, it could hang on a file where a list item contains a block quote with a list, made the list inside the quote loose, and parsed the whitespace as a hard line break or as the start of an indented code block.
