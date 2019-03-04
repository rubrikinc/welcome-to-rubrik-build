# Cheatsheet: Markdown

**[Code blocks:](#code-blocks)**
- When possible, reference the language at the beginning of a Code Block.
- When a code block is used to reference a shell, do not include the command
  prompt (`$`).
  - **Exception:** When a code block is used to display raw shell output.
- Separate commands from output.

**[Emphasis:](#emphasis)**
- Use two asterisks (`**`) for **Bold** text.
- Use an underscore (`_`) for _Italics_.
- Use two tildes (`~~`) for ~~Strikethrough~~.
 
**[Headings:](#headings)**
- Use a single `H1` (`#`) Heading per document.
  - **Exception:** `H1` may be used multiple times in the same document when
    there is a large content shift or "chapter" change.
- Follow the Header hierarchy of `H2` > `H3` > `H4` > `H5` > `H6`.
- Use sentence-style capitalization in titles (first word and proper nouns).
- Avoid using special characters.
- Leave exactly 1 new line after a heading.
- Avoid using links in headings.

**[Horizontal rules:](#horizontal-lines)**
- Use three dashes (`---`) to denote a horizontal rule.
- Use a horizontal rule (`---`) to logically separate large sections.

**[Line length:](#line-length)**
- Prefer an 80 character line limit.

**[Links:](#links)**
- Prefer using reference style links over inline style links.
- When linking within the same directory, use a relative link.
- When linking to a document outside of the current directory, use the absolute
  path from the root of the repository.

**[Lists:](#lists)**
- Capitalize the first character of each entry unless the item is explicitly
  case sensitive.
- End each entry with a period if it is a sentence or phrase.
- Use a colon (`:`) to separate a list item name from the explanatory text.
- Leave a blank line after each list.
- Use `-` for unordered lists.
- For ordered lists repeating `1.` may be used.
- When inserting a code block into an ordered list, indent (space) an additional
  two times.

**[Metadata:](metadata)**
- If the document is intended to be surfaced on the Contributor Site; include a
  yaml metadata header at the beginning of the document.
- Metadata must include the `title` attribute.

**[Tables:](#tables)**
- Use tables for structured information.
- Tables do not need to adhere to the suggested line length.
- Avoid long inline links.
- Do not use excessively wide tables.
