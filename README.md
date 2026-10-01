# Receptes

## Adding or editing a recipe

Create `content/receptes/<slug>.md`:

```markdown
---
title: "Nom de la recepta"
categories: ["Peixos i mariscos"]
lang: "ca"
date: 2026-10-01
lastmod: 2026-10-01
---

- Ingredient 1
- Ingredient 2

Pas a pas de la preparació.
```

- `categories` must be one of the values listed in `categoryOrder` in
  `hugo.toml` (`Amanides i entrants`, `Sopes i cremes`, `Arrossos i
  pasta`, `Llegums i verdures`, `Carns`, `Peixos i mariscos`, `Ous i
  làctics`, `Postres i dolços`, `Salses`, `Begudes`, `Altres`) — categories
  are always in Catalan, even for recipes written in Spanish. Add a new
  one to `categoryOrder` too if needed, in the position you want it to
  appear.
- `lang` is `"ca"` or `"es"` and sets the page's `html lang` attribute —
  use whichever matches the language the recipe is actually written in.
- Write ingredients as a Markdown list (`- ` per line) so they render as
  a proper list rather than one `<br>`-separated paragraph.

## Local development

```sh
brew install hugo   # once
hugo server          # http://localhost:1313/receptes/
```
