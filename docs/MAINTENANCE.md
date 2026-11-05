# Maintenance guide

Every academic record lives in **one** place. Edit the source, commit, and the site rebuilds itself.

| To change… | Edit | Appears on |
|---|---|---|
| Name, official title, unit, e-mail, profile URLs | `_variables.yml` (and the hero text in `index.qmd`) | Home, CV |
| Publications | `data/publications.yml` | Publications (all), Home (`featured: true`) |
| Talks | `data/talks.yml` | Activities, Home (4 most recent non-outreach) |
| Courses taught (per term) | `data/courses.yml` | Teaching, Home |
| Earlier teaching, mentoring | `data/teaching.yml` | Teaching, Activities |
| Peer review, committees | `data/service.yml` | Activities |
| Appointments, research positions, internships | `data/appointments.yml` | About, CV |
| Degrees and training | `data/education.yml` | About, CV |
| Scholarships, awards | `data/recognition.yml` | Recognition |
| News and media coverage | `data/news.yml` | News, Home (3 most recent) |
| Student leadership | `data/leadership.yml` | Activities |
| Competitions and programmes | `data/competitions.yml` | Activities |
| CV PDF | replace `assets/cv/CV_Thammarat_Yawisit.pdf` (keep the file name) and update `cv.updated` in `_variables.yml` | Home, CV |

## Adding a publication

Add a block at the top of `data/publications.yml`:

```yaml
- id: yawisit2027example          # unique; also the BibTeX key and the #anchor
  title: "Full title"
  authors: ["T. Yawisit", "A. Coauthor"]   # exact order; "T. Yawisit" is bolded
  year: 2027
  sortdate: "2027-03-01"          # optional, for ordering within a year
  type: journal                   # journal | proceedings | abstract | preprint | report | other
  type_label: "Journal article"
  status: published               # published | accepted | under-review | submitted | presented | preprint | report
  status_label: "Published"
  venue: "Journal name, vol(issue), pages"
  note: ""                        # optional clarification shown under the venue
  doi: "10.xxxx/xxxxx"
  arxiv: "2701.00001"             # optional
  pdf: ""                         # optional link to an open-access PDF
  code: ""                        # optional repository URL
  data: ""                        # optional dataset URL
  area: "Neutrino Telescope Instrumentation"   # one of the research domains
  project: "/research/<slug>/"    # optional project page
  featured: false
  abstract: ""                    # paste verbatim from the publisher/arXiv record
```

**Status rules.** Change `status` only when you have written confirmation: *submitted → under-review → accepted → published*. Never label a preprint or submitted manuscript as published or peer reviewed. Do not add citation counts or impact metrics.

BibTeX is generated automatically from these fields.

## Adding a talk, teaching role or service item

Copy an existing block in the relevant `data/*.yml` file. Use `kind: invited` only when the organisers formally invited the talk. Keep the role description exactly as on the programme or letter.

## Adding a research or engineering project

1. Copy `_templates/research/` to `research/<short-slug>/` (or `_templates/engineering/` to `engineering/<short-slug>/`).
2. Fill in the front matter (`status`, `evidence`, `period`, `categories`, `order`, `featured`).
3. Delete any section you cannot support with a source. State whether results are **measured, simulated, proposed or preliminary**.
4. Keep `draft: true` until it is verified; drafts are removed from the public build.
5. Add figures next to `index.qmd` with descriptive alt text.

Research domains (use these exact names in `categories`): Experimental Astroparticle Physics · Neutrino Telescope Instrumentation · Detector Characterization and Validation · High-Speed Data Acquisition · Measurement Algorithms and Signal Processing · Quantum Measurement and Control · Optics, Photonics, and Advanced Electronics · Scientific Software and Computational Methods.

## Writing a note

Copy `_templates/notes/` to `notes/posts/YYYY-MM-DD-slug/`, set the date and one of the note categories, write, and remove `draft: true`. Equations, cross-references, citations and code highlighting are enabled for notes. The RSS feed updates automatically.

## Changes of position or affiliation

1. Add a new record to `data/appointments.yml` with `phase: present`; set the previous one to `phase: past` with an `end` date.
2. Update `position.*` in `_variables.yml` and the short biography in `about/index.qmd`.
3. Planned positions or degrees stay `hidden: true` (or `phase: planned`) until they have started.

## Enabling optional features

- **Analytics:** uncomment `google-analytics` and `cookie-consent` in `_quarto.yml`.
- **Custom domain:** add a `CNAME` file with the domain, list it under `project.resources`, update `site-url`, and configure DNS.
- **ORCID / Google Scholar / LinkedIn:** add the verified URL in `_variables.yml` and a link in `index.qmd` (Contact) and `cv/index.qmd`.

## Local checks before pushing

```bash
quarto render                 # must finish without errors or warnings
quarto preview                # click through navigation on desktop and a narrow window
```
