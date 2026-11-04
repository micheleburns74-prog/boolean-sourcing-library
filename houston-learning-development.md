# Worked example: Training & Development Manager, Houston (oil and gas)

A complete LinkedIn Recruiter search build for a hard-to-source corporate L&D role, showing which filter gets which part of the search.

## Which box gets what

In LinkedIn Recruiter's left filter panel there are two separate cards, and the whole search depends on using the right one.

| Filter card | Where it sits | How it works |
| --- | --- | --- |
| Job titles | Near the top, Current/Past toggle | Typeahead. Type and pick from LinkedIn's list, one title at a time. No pasting. |
| Keywords | Further down, below Skills | Accepts a pasted boolean string. Matches anywhere on the profile. |

A title list pasted into Keywords matches those words anywhere on a profile, so a project manager who once supported a training program comes back as a hit. That is the single most common cause of junk results.

**Test before layering anything.** Put only the Job titles string in the Job titles filter. No keywords, no location, no industry. Check the first ten results. Every one should carry a training or L&D title. If any is a project manager, the string is in the wrong box.

## Role snapshot

| Field | Target |
| --- | --- |
| Title | Training & Development Manager |
| Location | Houston metro |
| Industry | Energy / oil and gas |
| Years of experience sweet spot | 3 to 6 years |
| Platforms | LinkedIn Recruiter, Sales Navigator, LinkedIn basic |

Keywords here come from the title and industry. With a job description in hand, tune the strings to its stated must-haves.

## Company quality: set these first

Titles alone cannot separate a corporate L&D manager from a tanning salon or restaurant training manager. Both hold the title. Two filters do the work no string can.

**Company headcount: 501+.** Select 501-1,000, 1,001-5,000, 5,001-10,000 and 10,001+. Franchise units and single-location businesses are small employers, so this removes most of the noise on its own.

**Industry filter: include only these**

```
Oil, Gas and Mining
Chemical Manufacturing
Utilities
Electric Power Generation
Industrial Machinery Manufacturing
Engineering Services
Construction
Airlines and Aviation
Aviation and Aerospace Component Manufacturing
Pharmaceutical Manufacturing
Medical Equipment Manufacturing
Transportation, Logistics, Supply Chain and Storage
Motor Vehicle Manufacturing
Business Consulting and Services
Hospitals and Health Care
```

Leave out Restaurants, Food and Beverage Services, Retail, Wellness and Fitness Services, Consumer Services and Hospitality. The industry filter reads the company's industry rather than words on the profile, which is a distinction keywords cannot make.

## Search 1: in-industry (oil and gas)

Job Titles filter set to **Current**. Keywords box gets industry terms only. Location = Greater Houston, 50 mi. Years of experience = 3 to 6.

**Job titles filter (Current).** Enter these one at a time, picking LinkedIn's match. If nothing appears, that title is not in LinkedIn's taxonomy, so skip it.

| # | Title | Priority |
| --- | --- | --- |
| 1 | Training and Development Manager | Core |
| 2 | Training Manager | Core |
| 3 | Learning and Development Manager | Core |
| 4 | Talent Development Manager | Core |
| 5 | Organizational Development Manager | Core |
| 6 | Learning Manager | Core |
| 7 | Senior Training Specialist | 3 to 6 yr range |
| 8 | Training and Development Specialist | 3 to 6 yr range |
| 9 | Learning and Development Specialist | 3 to 6 yr range |
| 10 | Training Specialist | 3 to 6 yr range |
| 11 | Learning and Development Business Partner | 3 to 6 yr range |
| 12 | Learning and Development Consultant | 3 to 6 yr range |
| 13 | Corporate Trainer | 3 to 6 yr range |

Skip Training Coordinator, Training Supervisor and Training Lead. Restaurant and retail groups use those for shift leads who onboard crew. If Recruiter offers a "similar titles" expansion toggle, turn it off. That is another route by which project managers get in.

**Keywords box**

```
("oil and gas" OR "oil & gas" OR oilfield OR upstream OR midstream OR downstream OR refinery OR refining OR petrochemical OR LNG OR drilling OR completions OR offshore OR "E&P" OR pipeline OR terminals OR "competency assurance" OR "process safety") NOT ("project manager" OR "program manager" OR recruiter OR "talent acquisition" OR restaurant OR franchise OR salon OR spa OR tanning OR gym OR cosmetology OR esthetician)
```

## Search 2: outside industry

Same structure with no industry block, so every vertical comes through. Job Titles set to **Current or past**. Years of experience = 3 to 8, because someone with 7 years in hospital or retail L&D can read like 4 to an energy hiring manager.

**Job titles filter (Current or past).** The same thirteen titles as Search 1, plus four design-side titles:

| # | Title |
| --- | --- |
| 14 | Instructional Designer |
| 15 | Senior Instructional Designer |
| 16 | Learning Experience Designer |
| 17 | Instructional Design Manager |

**Keywords box**

```
("adult learning" OR ADDIE OR "instructional design" OR "curriculum development" OR "training needs analysis" OR "train the trainer" OR LMS OR Kirkpatrick OR "blended learning" OR "technical training" OR "compliance training" OR "leadership development") NOT ("project manager" OR "program manager" OR recruiter OR "talent acquisition" OR restaurant OR franchise OR salon OR spa OR tanning OR gym OR cosmetology OR esthetician)
```

## About the exclusion block

The NOT block is already inside both keyword strings above. Paste them whole, with nothing to append.

It scans whole profiles, so it will also drop a solid manufacturing candidate who waited tables years ago. If a search comes back too thin, delete everything from `NOT (` to the closing bracket and rely on the Industry and headcount filters instead.

## Corporate L&D signal

One keyword set that separates a professional training function from a retail one. A tanning salon training manager does not write "conducted training needs analysis with SMEs" on a profile. A corporate L&D person does.

```
"needs analysis" OR competency OR ADDIE OR "learning management system" OR stakeholder OR "subject matter expert" OR SME OR "compliance training" OR "technical training"
```

## Google X-Ray

One box, and title-style syntax works here because Google honors it. Run this when Recruiter results look thin.

```
site:linkedin.com/in/ ("Training and Development Manager" OR "Learning and Development Manager" OR "L&D Manager" OR "Training Manager" OR "Talent Development Manager") (Houston OR Katy OR "Sugar Land" OR "The Woodlands" OR Pearland OR Baytown) ("oil and gas" OR oilfield OR refinery OR petrochemical OR LNG OR midstream OR upstream) -"Project Manager" -"Account Manager" -recruiter
```

## Sales Navigator

Sales Navigator has its own Title field that accepts boolean. Put the Job Titles list from Search 1 or Search 2 in that field and the matching Keywords list in Keywords, the same split as Recruiter.

## Filter panel settings

Add these one at a time and watch the count after each.

| Filter | Search 1 (in-industry) | Search 2 (outside) |
| --- | --- | --- |
| Company headcount | 501+ | 501+ |
| Industry | list above | list above |
| Location | Greater Houston, 50 mi | Greater Houston, 50 mi |
| Years of experience | 3 to 6 | 3 to 8 |
| Job Titles filter | Current only | Current or past |

Run order: Company headcount and Industry first, then Job Titles and Location. The count should be in the hundreds. Then add Years of experience, then the Keywords box, then the exclusion block only if needed. If the number collapses at any step, that step is the problem.

## Tuning notes

- LinkedIn Recruiter does not support the `title:` field operator in its keyword box. Pasted there, it is read as plain text and matched against the whole profile (headline, summary, and every job description), which is why an earlier version of these strings returned recruiters, project managers and program managers. Titles belong in the Job Titles filter. `title:` works in Sales Navigator's Title field and in Google X-Ray, not in Recruiter.
- "Training Program Manager" was removed from every title list. It contains the words "Program Manager," so it pulls program and project managers into the results.
- No remaining title contains project, program, recruiter or coordinator, so a project manager cannot match the title list.
- Company headcount and Industry are the filters that fix company quality. No boolean string can tell a corporate training manager from a franchise one, because both hold the title.
- Every multi-word title is a full quoted phrase, never a bare stem. "Training" or "Development" alone pulls in Business Development and Program Management profiles.
- Senior Specialist titles at 5 to 6 years often beat a Manager at 3. They are doing the work rather than owning the org chart.
- To target the Houston operator and oilfield services bench directly, use Recruiter's Current Company filter: Halliburton, SLB, Baker Hughes, Weatherford, NOV, TechnipFMC, ChampionX, Oceaneering, ConocoPhillips, Chevron, Shell, ExxonMobil, Occidental, Phillips 66, Marathon Petroleum, LyondellBasell, Enterprise Products, Kinder Morgan, Energy Transfer, Cheniere, Targa, EOG, KBR, Quanta Services.
