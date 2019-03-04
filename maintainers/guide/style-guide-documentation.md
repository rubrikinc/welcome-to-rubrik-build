---
title: Documentation Style Guide
---

# Documentation Style Guide

This style guide is for content in the GitHub account for Rubrik Build (rubrikinc).

These are **guidelines**, not rules. Use your best judgement.

## Cheatsheet

**Contact information**
- Use official Rubrik contact information.

**Dates and times**
- Format dates as `month day, year`. (December 13, 2018)
- When conveying a date in numerical form, use [ISO 8601] Format: `yyyy-mm-dd`.
- Use the 24 hour clock when referencing time.
- Times for single events (example: meetup) should be expressed in an absolute
  time zone such as Pacific Standard Time (PST) or Coordinated Universal Time
  (UTC).
- Times for reoccurring events should be expressed in a time zone that follows
  Daylight Savings Time (DST) such as Pacific Time (PT) or Eastern Time (ET).
- Supply a link to a globally available time zone converter service.
  - `http://www.thetimezoneconverter.com/?t=<TIME REFERENCE>&tz=<TZ REFERENCE>`

**Diagrams, images and other assets**
- Images and other assets should be stored in the same directory as the document
  that is referencing it.
- Filenames should be lowercase and descriptive of what they are referencing.
- Avoid excessively large images or include a smaller one while linking to a
  higher resolution version of the same image.

**Document Layout**
- Documents should follow the general template of:
  - Document metadata (if appropriate).
  - Title in `H1` (a single `#`).
  - A brief description or summary of the document.
  - A table of contents.
  - The general body of document.
- Do not repeat content. Instead link back to the canonical source.
- Large content or topic shifts should be separated with a horizontal rule.

**Formatting text**
- API objects:
  - Follow the established [API naming convention] when referring to API Objects.
  - Do not split API object names into their components.
  - Use `code` style for API objects or object parameters.
- Use **bold text** for user interface elements.
- Use _italics_ to emphasize a new topic or subject for the first time.
- Use angle brackets (`<` and `>`) to enclose a placeholder reference.
- Apply `code` styling to:
  - Filenames, directories, and paths.
  - Command line examples and flags.
  - Object field names.

**Language, grammar and tone**
- Documentation should be written in English.
- Prefer an active voice and present tense when possible.
- Use simple and direct language.
- Use gender-neutral language.
- Avoid personal pronouns ("I," "we," "us," "our," and "ours").
- Address the reader as "you" instead of "we".
- Do not use Latin phrases.
- Avoid jargon and idioms.
- If using acronyms, ensure they are clearly defined in the same document.
- If using an abbreviation, spell it out the first time it is used in the document unless it is commonly known. (example: TCP/IP)

**Moving a document**
- Use `[git-mv]` to move documents.
- Commit moved documents separately from any other changes.
- When a document has moved, leave a tombstone file with a removal date in its place.
  
**Punctuation**
- Do not use punctuation in headings.
- End full sentences with a period.
  - **Exception:** When a sentence ends with a URL or if the text would be unclear if the period is a part of the previous object or word.
- Add a single space after a period when beginning a new sentence.
- Avoid usage of exclamation points unless they are a part of a code example.
- Use an [Oxford comma] when a list contains 3 or more elements.

**Quotation**
- Use double-quotation marks (`" "`) over single-quotation marks (`' '`).
  - **Exception:** In code snippets where quotation marks have specific meaning.
  - **Exception:** When nesting quotation marks inside another set of quotation
    marks.
- Punctuation should be outside of quotation marks following the international (British) standard.
