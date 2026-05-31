# skill-scanner

> Scans your agent environment at project start and recommends the right skills for the job.

**skill-scanner** detects your project type, inventories installed skills and plugins, and recommends up to 5 missing but relevant skills — so you never start a project with the wrong toolkit.

## What it does

1. **Detects project context** — reads `package.json`, `requirements.txt`, `Cargo.toml`, `go.mod`, dominant file extensions, and `CLAUDE.md`
2. **Inventories what's installed** — runs `npx skills list` and `claude plugin list`
3. **Finds relevant skills** — searches skills.sh for your project type
4. **Recommends up to 5 skills** — prioritized, not exhaustive
5. **Integrates with skill-guard** — never installs directly; presents commands for you to validate

## Example output

```
[skill-scanner] Environment Audit

Project detected  : frontend (React 18 + TypeScript + Vite + Tailwind)
Installed         : 20 skills, 9 plugins

Already well-equipped for:
  - frontend-design-direction  - visual direction and design system
  - verify                     - test that components work in the real browser
  - git-sync                   - version and sync the project to GitHub

Recommended skills (3/5):

1. react-storybook
   -> Develop and document dashboard components in isolation
   -> npx skills add react-storybook

2. accessibility-checker
   -> Automated WCAG audit for enterprise-grade dashboards
   -> npx skills add accessibility-checker

3. performance-budget
   -> Monitor Lighthouse / Core Web Vitals on every Vite build
   -> npx skills add performance-budget

Note: To install, use skill-guard — it will check the risk level before
      each installation.
```

## Installation

```bash
npx skills add https://github.com/baalyerob/skill-scanner
```

## Works best with skill-guard

skill-scanner recommends, skill-guard protects. Install both:

```bash
npx skills add https://github.com/baalyerob/skill-guard
npx skills add https://github.com/baalyerob/skill-scanner
```

## Supported project types

`frontend` · `api` · `scraping` · `data` · `cli` · `mobile` · `fullstack` · `skill-dev`

## Author

Created by [@baalyerob](https://github.com/baalyerob) with Claude Code.

## License

MIT
