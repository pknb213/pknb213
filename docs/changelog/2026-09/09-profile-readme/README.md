# GitHub profile refresh

## Goal and scope

Replace the aging profile README with a recruiter-readable introduction, selected engineering evidence, and representative public code. Only this profile repository is in scope; portfolio and source projects remain unchanged.

## Decisions

- Use native GitHub Markdown for light/dark colors and responsive layout. Remove third-party counters, badges, and statistics images to reduce external failure points. Keep existing image assets untouched.
- Link to the verified portfolio root and existing hash routes, not the old /github.io/ path.
- Separate professional case studies from public learning repositories. Copy no private source code.
- Date the existing July 2026 measurements and state environment limitations. Test function counts are not pass rates; indexed items are not production traffic.
- Select one public repository per primary server language. Explicitly label the LangChain course project; omit duplicate, forked, and skeleton projects.
- Use one functional commit for this cohesive profile refresh.

## Sources

- Previous profile README: public contact email.
- Portfolio src/data/portfolio.ts: case studies, measurements, and routes.
- Portfolio src/data/openSourceProjects.ts: public implementation summaries.
- GitHub API inventory checked 2026-09-09: public repository names and visibility.

## Verification and progress

- Target cloned cleanly from origin/main; existing profile and portfolio source reviewed.
- README rewritten and independently reviewed; quantitative claims match the dated portfolio sources. Two dependency attribution gaps were resolved against project pyproject.toml files (see review.md).
- GitHub Markdown API renders the document successfully. No external image requests are required by the README.
- Verified public repository names/visibility with GitHub API and portfolio root with HTTP 200. Hash links match portfolio routes.
- Previewed API-rendered HTML inside the actual GitHub profile's Markdown container at 1440px (light/dark) and 390px (dark). This was a local browser preview, not a published change. Mobile document width remained 390px.
- Mobile preview exposed horizontal scrolling in the repository table; switched to stacked summaries so technology labels remain visible without scrolling.
- git diff --check passes. No application code or build pipeline is changed, so compilation and runtime tests do not apply.
- Final rendered-list check passes: no tables or external images; at a 390px viewport the document width remains 390px. Ready for one profile-refresh commit and non-forced push to origin/main.

## Independent review brief

Review the new profile README against the two source files in sibling pknb213.github.io. Check all quantitative claims, public repository names, skill summaries, learning/work distinction, and unsupported assertions. Do not edit the README. Write concise findings to review.md in this directory; explicitly say if no blocking findings remain.
