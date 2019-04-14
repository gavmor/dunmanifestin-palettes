# Dunmanifestin Palettes

Swatch-lists for generating plausible phraseage using [Dunmanifestin](https://github.com/quavmo/Dunmanifestin), e.g.

---
From `that which [verb] [subject] [verb] [subject]`,

`$ dunmanifestin -g ./sophistry` gives us:
>That which overcomes tact cures enthusiasm.

---
From `[placeName], [settlementType.article] built on [geologicalFormation.article] in [region] and [settlementDetail]`,

`$ dunmanifestin -g ./fantasy` gives us:
> Shelrift, a tomb built on a bog in Hetcene and rumored to hide the treasure of Toni Grenec beneath its foundations: Otu, the copper sword which fights of its own accord

---
`$ dunmanifestin -g ./hypotheticals`:
> What would you do if you could carry a winter?

---
`$ dunmanifestin -g fantasy:post-apocalpytic`:

> Thetutown, a colliseum built on a mountain in Wilayah Persekutuan Kuala Lumpur and famous for being the target of an attack by Entata Felldon, an infuriatingly paranoid accountant

## Attributions

Thank yous a million for dropping these things on the internet where I could scramble 'em:

- [Ben Christel](https://github.com/benchristel)'s Nevven
- u/JR-9615's [Mundane Items](https://www.reddit.com/r/DnD/comments/3yvy58/commonmundane_item_list_d100/)
- [Johnn Four](https://www.roleplayingtips.com/)'s [Encounters](https://s3.amazonaws.com/RPT-eBooks/1372-fantasy-roadside-encounters.pdf)

## ToDo

- [ ] Respect word order:

| order | relating to      | examples                              |
|-------|------------------|---------------------------------------|
| 1     | opinion          | unusual, lovely, beautiful            |
| 2     | size             | big, small, tall                      |
| 3     | physical quality | thin, rough, untidy                   |
| 4     | shape            | round, square, rectangular            |
| 5     | age              | young, old, youthful                  |
| 6     | colour           | blue, red, pink                       |
| 7     | origin           | Dutch, Japanese, Turkish              |
| 8     | material         | metal, wood, plastic                  |
| 9     | type             | general-purpose, four-sided, U-shaped |
| 10    | purpose          | cleaning, hammering, cooking          |

## Tips
The following command displays swatches by frequency.
```
grep -roh -P "\[(.*?)[\.\]]" . | sort | uniq -c | sort -n
```
pipe to this script for a histogram:
```
perl -lane 'printf "%-30s%s\n", $F[1], "=" x $F[0]'
```
