# Content verification checklist

Status as of the initial Quarto build (1 November 2026). Sources: `CV_Thammarat_Yawisit.pdf`, KMITL Order No. 1151/2569, KMITL memorandum of 22 October 2026, arXiv abstract pages (checked 1 Nov 2026), public GitHub repositories.

## Titles and roles

- [x] Official title shown as **Engineer, Academic Support Division, Office of the Dean, School of Engineering, KMITL** (Order No. 1151/2569, effective 1 Oct 2026).
- [x] "Research engineer" is used only as a functional description, never as the official title. No faculty, professor or PI wording anywhere.
- [ ] **Owner to confirm:** the CV lists the current role as "Research Engineer, School of Engineering"; the appointment order says "Engineer", Academic Support Division. The site uses the order.
- [ ] **Owner to confirm:** "Office of the Dean" is part of the unit name (given in the project brief; not stated in the English appointment order).
- [ ] **Owner to confirm:** the CV calls Pittaya Pannil both "Prof." and "Assoc. Prof."; the site uses "Assoc. Prof." throughout.
- [x] Teaching shown as laboratory teaching-assistant and student-mentoring roles, explicitly not a faculty teaching appointment.

## Publications

- [x] No item labelled published or peer reviewed. CHEP 2026 proceedings: *under review*. IEEE SAS 2027: *submitted, decision pending*. arXiv:2512.20678: *preprint*.
- [x] arXiv identifiers and author lists checked against arXiv for 2601.18114, 2601.17043, 2610.24003 and 2512.20678.
- [x] **Owner confirmed (1 Nov 2026):** use the CV titles. The CHEP 2026 contribution titles (from the CV) differ from the arXiv titles of 2601.18114 and 2601.17043. The site shows the CV titles and notes the arXiv titles.
- [ ] Zenodo DOIs (18614095, 23020724, 23021859, 19332410) could not be opened from the build environment; click each once after deployment.
- [ ] Abstracts are empty. Paste each verbatim from arXiv/Zenodo into `data/publications.yml`.
- [x] No citation counts, quartiles or impact metrics.

## Recognition

- [x] Each item personally received per the CV; registration waiver and registration support described as such.
- [x] Government Science and Technology Scholarship nomination (memo of 22 Oct 2026) is shown, labelled "Nominated · decision pending": it is a nomination, not an award.
- [x] Planned M.Sc. at KIT (WS 2027/28) is shown, labelled "Planned".
- [x] **Owner decided (1 Nov 2026, later the same day):** show both publicly.

## Privacy

- [x] Home address, phone number and referee contacts are not shown on any page.
- [x] **Owner approved (1 Nov 2026)** publishing the current CV PDF, which includes your home address, phone number and referees' e-mail addresses. Consider uploading a public version without them.
- [x] E-mail displayed in obfuscated form; only the personal Gmail address is shown (the IceCube address may not be current). Add a KMITL address in `_variables.yml` once confirmed.

## Profiles and links

- [x] GitHub profile verified (repository owner).
- [x] ORCID, Google Scholar and LinkedIn URLs supplied by the owner (1 Nov 2026) and linked in the navbar, Home and CV.
- [x] Internal links: automated check found no broken links in the build.
- [ ] Locations for Siam Physics Congress 2026 and the Thai-IceCube MoA-signing visit are not in the CV and are left blank.

## Text written for the site (needs owner approval)

- [ ] Home mission statement and the "Who / What problems / What you can verify" panel (`index.qmd`).
- [ ] Short and academic biography, research statement, technical-expertise table (`about/index.qmd`).
- [ ] Project narratives (`research/*/index.qmd`, `engineering/*/index.qmd`): based on the CV, arXiv abstracts and repository READMEs.
- [ ] Launch note (`notes/posts/2026-11-01-website-launch/`).

## Technical QA

- [x] `quarto render` completes with no errors or warnings.
- [x] Pages checked at 1366 px and 390 px widths; no horizontal scrolling; no console errors.
- [x] Sitemap, RSS feed, 404 page, Open Graph and description metadata generated.
- [ ] After deployment: open the live site, test search, filters, CV download and the 404 page.

## Update of 1 November 2026 (chronology dossier and news)

- [x] CV PDF: references section removed ("Available on request"); referee e-mail addresses are no longer in the file. Home address and phone remain, at the owner's choice.
- [x] Added from the owner's chronological dossier: AFAPS and secondary-school education, WIPAC LOM-16 details, ThaiBev scope of work, Panasonic selection detail, KMITL academic distinction, student leadership, competitions, skills, society memberships and the ISA-95 course.
- [x] Not added: percentage impact claims for the ThaiBev internship, manuscripts "in preparation", and the dossier's speculative month-by-month narrative.
- [ ] Date conflicts between the dossier and the current CV were resolved in favour of the CV: WIPAC May–Aug 2025 (dossier and Thai PBS: research stay Jun–Jul 2025), ThaiBev May–Jul 2024 (dossier: Jun–Jul), Viriyah Mar–May 2022 (dossier: Mar–Apr).
- [x] News: Thai PBS (13 Oct 2026) and KMITL Engineering news (27 May 2025) were read and summarised.
- [ ] News: the KMITL Engineering Facebook post could not be opened (Facebook blocks automated access). Its summary is based on the headline only, and the date "Oct 2026" is approximate.
