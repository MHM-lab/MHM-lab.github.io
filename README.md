# Mental Health Mapping – website

Live at **https://mhm-lab.github.io**. GitHub Pages rebuilds the site automatically about a minute after every change.

## What is where

| To change…                         | Edit this file                 |
|------------------------------------|--------------------------------|
| Team members (name, role, bio)     | `_data/people.yml` + photo in `images/` |
| Alumni                             | `_data/alumni.yml`             |
| Selected publications (Research page) | `_data/publications.yml` |
| Research themes (homepage + Research page) | `_data/research.yml`   |
| Homepage text                      | `index.html`                   |
| Highlights (homepage, 8 newest from the last 6 months) | `_data/news.yml` (newest first) |
| Menu, footer links, site title     | `_config.yml`                  |
| Any other page                     | the `.md` file with its name (e.g. `teaching.md`, `join_us.md`) |
| Colours, fonts, spacing            | `assets/style.css`             |
| Page frame (header/footer)         | `_layouts/default.html`        |
| German version of a page          | the same file name in `de/` (e.g. `de/teaching.md`) |
| Search engine / AI summary         | `llms.txt`, `robots.txt` (structured data in `_includes/structured-data.html` updates itself) |

You can edit everything directly on github.com: open the file, click the pencil icon, change it, then "Commit changes".

## English and German

English is the default. Every page also exists in German under `/de/` with the same address (e.g. `/people/` and `/de/people/`); the EN/DE button in the header switches between them.

- **Text pages**: the German text is in `de/` with the same file name. When you change an English page, update its German twin too.
- **Data files**: German text sits next to the English one in fields ending in `_de` (`bio_de` in `people.yml`, `title_de`/`short_de`/`text_de`/`name_de` in `research.yml`, `summary_de` in `publications.yml`, `group_de` in `alumni.yml`). If a `_de` field is missing, the German page shows the English text.
- **Menu**: `title_de` in `_config.yml`.
- Names, roles (e.g. PostDoc), paper titles, and course titles stay in English on the German pages.

## Common tasks

**Add a team member**
1. Upload a photo to `images/`: square, 400 × 400 px, `.jpg`, on the shared light sage background (RGB 232, 237, 230), face roughly centered.
2. In `_data/people.yml`, copy an existing block and fill it in (keep alphabetical order):

```yaml
- first: Jane
  last: Doe
  role: PhD Candidate
  photo: jane.jpg
  bio: >-
    One paragraph in the first person. Markdown links work: [lab](https://example.org).
  bio_de: >-
    Derselbe Text auf Deutsch.
```

Role wording used so far: Principal Investigator, PostDoc, PostDoc & Humboldt Fellow, PostDoc & Boehringer Ingelheim Fellow, PhD Candidate, Data Scientist & IT Infrastructure, MSc Student & HiWi, MSc Student, BSc Student, HiWi & Research Assistant.

**Someone leaves** – delete their block in `people.yml` and add a line to the right group in `alumni.yml`:

```yaml
  - name: Jane Doe
    years: 2024–2027
    next: Postdoc, University of X
```

**Add a publication** – add a block at the top of `_data/publications.yml` (newest first; years are grouped automatically):

```yaml
- year: 2027
  title: Title of the paper
  venue: Nature Neuroscience
  link: https://doi.org/...
  link_text: Paper        # or Preprint
  summary: >-
    Two or three sentences on why it matters.
  summary_de: >-
    Zwei oder drei Sätze auf Deutsch.
  date: "2027-01"          # optional: month accepted/published -> appears in the homepage Highlights for 6 months
  highlight: >-            # optional: the highlight sentence (the journal is shown on the card; otherwise the title is used)
    Accepted: Jane Doe's paper on ...
  highlight_de: >-
    Angenommen: die Arbeit von Jane Doe zu ...
```

**Add a new page** – create `my_page.md` with this at the top, then add it to `nav` in `_config.yml` if it belongs in the menu:

```markdown
---
title: My Page
permalink: /my_page/
---

Text in markdown…
```

## Writing style (keep it consistent)
- American English: *modeling, organize, behavior, aging*.
- Serial comma in lists: *machine learning, neuroscience, and psychiatry*.
- Section headings in sentence case (*Open positions*); names of courses, papers and themes keep their capitals.
- Bios in the first person (*I am…*, *My research…*), no contractions, refer to the lab as *the MHM Lab*.
- Use *and* rather than *&* in running text; en dash for ranges (*2024–2026*, *12:15–13:45*).
- Role labels: Principal Investigator, PostDoc, PhD Candidate, MSc Student, BSc Student, HiWi (combine with *&*, e.g. *MSc Student & HiWi*).

## Tips
- YAML is picky about indentation: use spaces (not tabs) and keep the same indentation as the block you copied.
- If a change breaks the build, GitHub emails you; the previous version stays online until it is fixed.
- To preview locally (optional): `gem install jekyll` then `jekyll serve` in this folder, and open http://localhost:4000.
