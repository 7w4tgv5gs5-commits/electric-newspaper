# The Electric Newspaper — Restored Archive

**Australia's first independent online daily newspaper**  
Adelaide, South Australia · February – July 1998  
`www.electric.on.net`

---

## Live Archive

**[7w4tgv5gs5-commits.github.io/electric-newspaper](https://7w4tgv5gs5-commits.github.io/electric-newspaper/)**

Clicking **Enter the Archive** opens the paper inside a simulated Netscape Navigator 4 browser window at 800×600 pixels — the browser and screen resolution most Australians used in 1998.

---

## What It Is

The Electric Newspaper was a daily online newspaper produced by web design studio [Virtual Artists Pty Ltd](http://www.va.com.au) on Rundle Street, Adelaide, and edited by veteran broadcast journalist **Hendrik Gout**. It published 711 articles across eleven sections — news, essays, arts, film reviews, books, sport, food, holidays, fringe, letters, and a regular column — written by working journalists, academics, politicians, and critics.

It operated for seven months before publishing its final edition on 31 July 1998, with the farewell note: *"No time to say hello, see ya!"*

The paper's coverage was almost entirely South Australian in focus. Its seven-month lifespan coincided with two major political stories: the Olsen Liberal government's surprise decision to privatise ETSA (breaking a specific election promise), and the parliamentary privileges scandal surrounding Deputy Premier Graham Ingerson. It also covered the 1998 Adelaide Festival and Fringe season, and chronicled the Adelaide Rams' final, ill-fated NRL season.

---

## Repository Contents

```
/
├── index.html          Entrance page — intro, Enter the Archive, section links
├── about.html          About the Electric Newspaper — what it was, origin & context
├── history.html        Origin & Content — timeline, the people, defining stories
├── restoration.html    About This Archive — how the 1998 server archive was recovered
├── articles.html       Searchable and sortable index of all 711 articles
├── netscape.html       Simulated Netscape Navigator 4 browser (800×600)
├── site.css            Shared styles for all site pages
├── wikipedia.md        Draft Wikipedia article on The Electric Newspaper
├── README.md           This file
└── archive/            The complete restored archive
    ├── index.htm       Original front page
    ├── NEWS/           314 news articles
    ├── ESSAYS/         114 essays and opinion pieces
    ├── SPORT/          96 sport articles
    ├── FILMS/          45 film reviews
    ├── BOOKS/          40 book reviews
    ├── ARTS/           38 arts reviews
    ├── FRINGE/         26 Adelaide Fringe reviews
    ├── FOOD/           19 food and drink articles
    ├── HOLIDAYS/       17 travel articles
    ├── LETTERS/        Letters to the editor
    ├── COLONEL/        The Colonel column
    ├── TEAM/           Staff and contributors page
    ├── BUTTONS/        Navigation button GIFs
    ├── HEADERS/        Section header GIFs
    ├── IMAGES/         Logo and masthead images
    ├── ILLUSTRA/       Editorial illustrations
    ├── ADS/            Advertisement graphics
    └── ...
```

---

## The Team

| Name | Role |
|---|---|
| **Hendrik Gout** | Editor and chief reporter |
| **Andy Petrucevics ("AndyPC")** | Design and visual identity |
| **Chris Joyner** | Web production |
| **Ben Moretti** | Web production |
| Garry Quill | Canberra correspondent |
| Krista Eleftheriou | Reporter |
| Legh Davis | Essays (19 articles) |
| Sandra Kanck MLC | Essays — SA Democrats (16 articles) |
| John Spoehr | Essays — economic policy |
| John Rau | Essays — SA Labor; legal counsel |
| Nick Xenophon MLC | Essays — No Pokies |
| David Bradley | Film critic (45 reviews) |
| Denise Wels | Books reviewer (40 reviews) |
| Dianne Gall | Arts reviewer |
| Elaine Moore | Fringe reviewer |
| Phil Owens / "Piston Stoned" | Sport — NRL and motorsport |
| George Aldridge | Cartoonist; travel writer |
| Adrienne Eccles | Food and drink |
| Ray Thomas | Arts; News Digest |
| Victoria White | Operations |
| Tatiania Liemareff | Editorial assistant |

---

## Restoration Notes

The archive was preserved on Internode's Unix server as a tar file after the paper closed in July 1998, and sat dormant until 2024.

**The problem:** The tar extraction had truncated all filenames to eight characters — a Unix filesystem artefact — breaking every image reference in all 711 HTML articles. Additionally, many images were referenced via absolute URLs pointing to the defunct `www.electric.on.net` domain.

**What was recovered:** Systematic analysis mapped all but 2 broken image references back to their original files. All 711 articles, story photographs, navigation button GIFs, section header GIFs, advertisement graphics, and contributor portrait photos are intact. Of 18,000+ image references in the archive, 14,653 resolve correctly, 144 are external dead-ad URLs, and just 2 files (`news/logosa4.jpg` and `news/newlogosmall1.gif`) are genuinely absent from the original tar archive.

**Changes made to the original HTML:**
- Image paths corrected throughout (broken → relative)
- 269 absolute `http://www.electric.on.net/ads/...` URLs rewritten as relative paths
- Navigation links fixed (wrong extensions, one dead domain reference)
- Netscape 3-era rollover button JavaScript disabled for browser compatibility — original source preserved verbatim in HTML comments with attribution to authors Dave Sag and Mark King, Virtual Artists Pty Ltd, 1997
- Section `index.htm` pages built (did not exist in original archive)
- Root `index.htm` rebuilt as an entrance page

The article text and body HTML is entirely original and unmodified.

---

## Technical Details

All pages were hand-coded in HTML 3.2 by Chris Joyner and Ben Moretti of Virtual Artists. The site used a two-column table layout (standard for 1998), with navigation handled by a rollover button system written in JavaScript by Dave Sag and Mark King of Virtual Artists in July 1997.

The paper was hosted at `electric.on.net` on a Unix server provided by [Internode](https://en.wikipedia.org/wiki/Internode_(ISP)), the Adelaide-based ISP founded in 1991 by Simon Hackett and Robyn Taylor. Internode and Cobweb Internet Services are acknowledged as sponsors on every page of the paper.

---

## Sponsors (1998)

- **[Internode](http://www.on.net)** — internet service provider, Adelaide
- **[Cobweb Internet Services](http://www.cobweb.com.au)** — internet service provider
- **[Virtual Artists Pty Ltd](http://www.va.com.au)** — web design and production

---

## Archive Submission

This archive is being prepared for submission to [PANDORA](https://pandora.nla.gov.au/) (National Library of Australia's web archive) and [Trove](https://trove.nla.gov.au/), the national discovery service for Australian cultural heritage materials.

---

## Copyright

© 1998 The Electric Newspaper. Original article content is subject to copyright. The restoration work (path fixes, index pages, entrance page, Wikipedia article) is released under [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
