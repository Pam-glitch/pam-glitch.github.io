# How to edit this site

Edit any file directly on GitHub.com: open the file, click the pencil icon
(top right), make your change, scroll down and click **Commit changes**.
The live site updates automatically within a minute.

## What each file is

- `index.html` — homepage
- `works.html` — catalog of works (the table)
- `next.html` — upcoming premieres and performances
- `map.html` — works grouped by instrument family (draggable graph on desktop, tap-list on mobile)
- `about.html` — bio, education, performance history
- `contact.html` — contact info
- `style.css` — controls colors, fonts, spacing for ALL pages at once
- `sitemap.xml`, `robots.txt` — help Google find the site, rarely need editing

## Common edits

**Add a new work to the catalog (works.html)**
Copy an existing row (everything from `<tr>` to `</tr>`) and paste it in as
a new row, then change the text inside each `<td>...</td>`:
```html
<tr>
  <td>Piece Title</td>
  <td>2026</td>
  <td>instrumentation</td>
  <td>venue / context</td>
</tr>
```

**Change your bio or add a new performance (about.html)**
Text between `<p>` and `</p>` tags is a paragraph — edit freely.
List items are between `<li>` and `</li>` — copy one to add a new line,
or delete one to remove a line.

**Change the contact email (contact.html)**
Find `adamapambianchi at proton.me` and replace it. Keep it written as
"at" rather than "@" if you want to keep it harder for spam bots to scrape.

**Change colors (style.css)**
Near the top of the file, under `:root {`, you'll see:
```css
--red: #ff1131;
--green: #00e676;
--blue: #1f51ff;
```
Change any hex code and it updates everywhere that color is used
(links, table rules, the divider dot) — no need to hunt through the rest
of the file.

**Change fonts (style.css)**
Search for `font-family` — there are three roles:
- `h1, h2` — headings
- `body` — regular text
- `.nav, .meta, th` — small print / typewriter-style text

Swap in any font name; if it's not a common system font, add safe
fallbacks after it (e.g. `"Georgia", "Times New Roman", serif`).

## Adding a new page

1. Copy an existing file (e.g. `about.html`) as a starting point.
2. Change the `<title>`, the `<h2>` heading, and the content in `<main>`.
3. Add a link to it in the `<nav>` block of every page (copy the pattern
   used for the other links).

## If something breaks

HTML is picky about matching tags — every `<tag>` needs a `</tag>` to
close it. If a page looks broken after an edit, check that you didn't
delete a closing tag by accident. GitHub keeps every past version: open
the file, click "History" to see old commits, and you can always revert.
