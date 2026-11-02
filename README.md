# Charles Abboang: My Life in Trieste & Maths

Personal website and bilingual (English/French) blog of **Charles De Gaule Abboang Aveved**, a mathematics student at ICTP, Trieste.

- **My Life in Trieste:** stories from an international student in Italy.
- **Maths:** university-level notes with statements and proofs (analysis, algebra, differential geometry).
- Also included: Journey, Research (publications) and Contact pages.

Live site: `https://charlesabboang.github.io/blog` (or your own domain, see below).

## Project structure

```
index.html      # the whole website (design, pages, language switch)
posts.js        # all blog posts (the only file you edit to publish)
README.md       # this file
```

There is no build step and no framework. The site is plain HTML, CSS and JavaScript.

## Publish a new post

1. Open `posts.js` (on GitHub: open the file, then click the pencil icon).
2. Copy an existing post block and change:
   - `id`: a unique short name, lowercase, no spaces (e.g. `compactness-rn`)
   - `cat`: `"life"` or `"maths"`
   - `date`: `"YYYY-MM-DD"`
   - the `title` and `body` texts
3. Click **Commit changes**. The site updates in about a minute.

### Post format

```js
{id:"my-post",cat:"maths",date:"2026-12-15",
  en:{title:"My title",body:[
    "H:A heading",
    "A paragraph with inline math $x^2+1$.",
    "EQ:$$\\int_0^1 x\\,dx=\\tfrac12$$"
  ]},
  fr:{title:"Mon titre",body:["..."]}   // optional
},
```

- Each string in `body` is one paragraph.
- `H:` at the start makes a heading. `EQ:` at the start makes a display equation.
- Maths uses [KaTeX](https://katex.org/): `$...$` inline and `$$...$$` for display. **Write each backslash twice** inside the strings (`\\int`, `\\frac`).
- A new line inside a paragraph is written `\n`.
- If a post has only `en` (or only `fr`), it is shown in both languages.
- Put a comma between posts, and keep the closing `];` at the end of the file.

## Preview locally

Open `index.html` in a browser. Maths formulas need an internet connection, because KaTeX loads from a CDN.

## Content and rights

All texts, stories and photos are by Charles Abboang. © 2026, all rights reserved. Please ask before reusing them.

---

## En bref (français)

Site personnel et blog bilingue. Pour publier : modifie uniquement `posts.js`, ajoute un bloc d’article, puis clique sur **Commit changes**. Le site se met à jour en environ une minute. Les formules de maths s’écrivent en LaTeX entre `$...$`, avec chaque barre oblique inverse doublée.
