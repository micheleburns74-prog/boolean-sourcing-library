# Worked example: Senior Backend Engineer, developer tools (remote US)

A LinkedIn Recruiter search build for an engineering role at a developer-first company, using the same structure as the [Houston L&D example](houston-learning-development.md): titles in the title filter, domain terms in keywords, company quality in filters, and a Google X-Ray backup.

## Role snapshot

| Field | Target |
| --- | --- |
| Title | Senior Backend Engineer, developer platform |
| Location | Remote, United States |
| Domain | Developer tools, APIs, CI/CD, source control, infrastructure |
| Languages | Go, Rust, Python or TypeScript |
| Years of experience sweet spot | 5 to 10 years |

With a job description in hand, tune the strings to its stated must-haves.

## Which box gets what

Same split as any Recruiter search. Job titles is a typeahead filter, one title at a time. Keywords accepts a pasted boolean string and matches anywhere on the profile.

**Test before layering anything.** Put only the titles in the Job titles filter and check the first ten results. Every one should be an engineer. If any is a recruiter, a sales engineer or a product manager, something is in the wrong box.

## Job titles filter (Current)

| # | Title | Priority |
| --- | --- | --- |
| 1 | Senior Software Engineer | Core |
| 2 | Senior Backend Engineer | Core |
| 3 | Staff Software Engineer | Core |
| 4 | Senior Platform Engineer | Core |
| 5 | Software Engineer | Wider net, 5+ yr only |
| 6 | Principal Engineer | Wider net |
| 7 | Senior Infrastructure Engineer | Wider net |
| 8 | Senior Site Reliability Engineer | Wider net |

Turn off any "similar titles" expansion. Skip Engineering Manager and Solutions Engineer unless the role is a lead seat. Sales engineers and managers share the vocabulary but not the work.

## Keywords box

```
(Go OR Golang OR Rust OR Python OR TypeScript) AND ("developer tools" OR "developer platform" OR "developer experience" OR API OR SDK OR CLI OR "CI/CD" OR "source control" OR git OR Kubernetes OR "distributed systems" OR "open source") NOT (recruiter OR "technical recruiter" OR "sales engineer" OR "solutions engineer" OR "customer success" OR "talent acquisition")
```

Two blocks joined with AND: one for the stack, one for the domain. Requiring both is what separates a backend engineer who builds tools for other engineers from one who builds a retail checkout service.

## Company quality filters

For developer-first product companies, headcount and industry still do work no string can.

**Company headcount:** 51 to 10,000. Include earlier-stage companies. The 501+ cutoff from the Houston example would remove most of the developer-tools market.

**Industry filter: include only these**

```
Software Development
Technology, Information and Internet
IT Services and IT Consulting
Computer and Network Security
Data Infrastructure and Analytics
```

Leave out Staffing and Recruiting, which returns agency engineers and recruiters, and Higher Education unless the role is research-heavy.

## Signal strings

Pick one to add when results look too broad. Each separates people who build for developers from people who only use the tools.

```
"open source" OR "pull request" OR maintainer OR "developer tools" OR "internal tooling" OR "platform team" OR "developer productivity" OR "developer experience"
```

```
GitHub OR GitLab OR Bitbucket OR Jenkins OR CircleCI OR Terraform OR Kubernetes OR Docker OR gRPC OR GraphQL
```

An open source maintainer line is the strongest signal in this set. It also carries a public GitHub profile you can check before you reach out.

## Google X-Ray

Title-style syntax works here because Google honors it.

```
site:linkedin.com/in/ ("Senior Software Engineer" OR "Staff Engineer" OR "Senior Backend Engineer" OR "Platform Engineer") ("developer tools" OR "developer platform" OR "CI/CD" OR "open source") (Go OR Golang OR Rust) "United States" -recruiter -"Sales Engineer"
```

## GitHub X-Ray

For engineering roles, GitHub itself is a sourcing surface. Public profiles list location, organizations and pinned repositories.

```
site:github.com ("Go" OR "Rust") "developer tools" "San Francisco" OR "Remote" -jobs -hiring
```

Use this to find people, then check their public work. Reach out about the role, not about their personal repositories, and only use contact details they have chosen to make public.

## Filter panel settings

Add these one at a time and watch the count after each.

| Filter | Setting |
| --- | --- |
| Industry | list above |
| Company headcount | 51 to 10,000 |
| Job titles | Current |
| Location | United States, remote noted in outreach |
| Years of experience | 5 to 10 |
| Keywords | string above |

Run order: Industry and headcount first, then Job titles and Location. The count should be in the thousands at that point. Add Years of experience, then Keywords. If the number collapses, the last step is the problem.

## Tuning notes

- Remote roles need a wide location filter. Search the whole country and let the outreach note remote.
- Do not put languages in the title filter. "Go Engineer" is not a standard title, and people list stack in the skills section and job descriptions instead.
- A short tenure at a strong developer-tools company usually beats a long one at a company with no engineering brand.
- For a target company list, use Recruiter's Past Company filter on the competitors that hire for the same stack, since engineers rarely stay put and the bench of people who just left is often the warmest.
