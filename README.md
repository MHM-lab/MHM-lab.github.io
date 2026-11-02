# Mental Health Mapping – website

Live at **https://mhm-lab.github.io**. GitHub Pages rebuilds the site automatically about a minute after every change.

## What is where

| To change…                         | Edit this file                 |
|------------------------------------|--------------------------------|
| Team members (name, role, bio)     | `_data/people.yml` + photo in `images/` |
| Alumni                             | `_data/alumni.yml`             |
| Selected publications              | `_data/publications.yml`       |
| Research themes (homepage + Research page) | `_data/research.yml`   |
| Homepage text                      | `index.html`                   |
| Menu, footer links, site title     | `_config.yml`                  |
| Any other page                     | the `.md` file with its name (e.g. `teaching.md`, `join_us.md`) |
| Colours, fonts, spacing            | `assets/style.css`             |
| Page frame (header/footer)         | `_layouts/default.html`        |

You can edit everything directly on github.com: open the file, click the pencil icon, change it, then "Commit changes".

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
```

Role wording used so far: PI, PostDoc, PhD Candidate, MSc Student, BSc Student, HiWi, MSc & HiWi.

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
- Role labels: PI, PostDoc, PhD Candidate, MSc Student, BSc Student, HiWi (combine with *&*, e.g. *MSc & HiWi*).

## Tips
- YAML is picky about indentation: use spaces (not tabs) and keep the same indentation as the block you copied.
- If a change breaks the build, GitHub emails you; the previous version stays online until it is fixed.
- To preview locally (optional): `gem install jekyll` then `jekyll serve` in this folder, and open http://localhost:4000.
