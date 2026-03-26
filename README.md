# Co4Pilot

> **4P Framework for Academic Research** — People · Project · Paper · Patent

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude-Code-blueviolet)](https://claude.ai)
[![Skills](https://img.shields.io/badge/Skills-43-green)](./skills/)

## What is Co4Pilot?

**Co4Pilot** is an AI-powered toolkit that covers the complete academic research lifecycle through four pillars:

| Pillar | What it covers | Skills |
|--------|---------------|--------|
| **👥 People** | Student mentoring, teaching, career development | 13 |
| **📋 Project** | Proposals, execution, data management | 12 |
| **📝 Paper** | Literature, writing, peer review, academic impact | 14 |
| **💡 Patent** | Mining, disclosure, drafting, office actions | 4 |

Built on [Claude Code](https://claude.ai), each skill contains actionable frameworks, templates, checklists, and prompt templates — sourced from MIT, Stanford, Harvard, CMU and other top universities' best practices.

## The 4P Architecture

```
Co4Pilot/
│
├── skills/
│   ├── people/                    👥 People (13 skills)
│   │   ├── mentoring/               Student supervision
│   │   │   ├── undergrad-thesis       28-week undergraduate thesis guide
│   │   │   ├── master-program         2-3 year master's roadmap
│   │   │   ├── phd-program            4-5 year PhD lifecycle (IDP, milestones)
│   │   │   ├── research-direction     Gap identification, feasibility matrix
│   │   │   └── progress-tracking      Milestone tables, early warning system
│   │   ├── teaching/                Course design & delivery
│   │   │   ├── course-design          Backward design (Wiggins & McTighe)
│   │   │   ├── syllabus               Learning-centered syllabus design
│   │   │   ├── exam-design            Bloom's taxonomy, rubric creation
│   │   │   └── teaching-reform        SoTL framework, teaching portfolio
│   │   └── career/                  Academic career development
│   │       ├── cv-maintenance         13-section academic CV structure
│   │       ├── citation-tracking      H-index, altmetrics, alert setup
│   │       └── talent-program         杰青/优青/长江 application prep
│   │
│   ├── project/                   📋 Project (12 skills)
│   │   ├── proposal/                Grant & project proposals
│   │   │   ├── proposal-writing       Universal framework for any funder
│   │   │   ├── provincial-fund        Provincial/local funding landscape
│   │   │   ├── industry-project       Industry contracts, IP negotiation
│   │   │   └── defense-prep           ACE framework, Q&A strategies
│   │   ├── execution/               Project management
│   │   │   ├── midterm-report         Risk assessment, progress tracking
│   │   │   ├── final-report           Impact assessment, sustainability
│   │   │   ├── budget-management      8 categories, compliance essentials
│   │   │   └── audit-prep             Documentation checklist, self-audit
│   │   └── data/                    Research data management
│   │       ├── data-collection-plan   FAIR principles, DMP template
│   │       ├── annotation-guide       IAA metrics, 8 annotation tools
│   │       ├── dataset-release        Datasheets framework, 8 licenses
│   │       └── data-agreement         DUA/DTA/MTA/NDA templates
│   │
│   ├── paper/                     📝 Paper (14 skills)
│   │   ├── literature/              Literature research
│   │   │   ├── literature-search      PICO, 12 databases, Boolean syntax
│   │   │   ├── literature-review      PRISMA 2020, 5-stage workflow
│   │   │   ├── paper-reading          Keshav three-pass method
│   │   │   └── reference-management   Zotero advanced + BibTeX
│   │   ├── writing/                 Paper composition
│   │   │   ├── research-paper         SPJ + Widom + IMRAD + ABT
│   │   │   ├── review-paper           7 review types, PRISMA methodology
│   │   │   ├── conference-paper       Page budget, CCF ranking, conversion
│   │   │   ├── cover-letter           Section-by-section template
│   │   │   ├── rebuttal               CALM method, diplomatic language
│   │   │   └── revision               Triage system, latexdiff guide
│   │   ├── review/                  Peer review
│   │   │   ├── review-writing         Structured review template
│   │   │   └── editor-communication   Email templates, appeal strategy
│   │   └── impact/                  Academic dissemination
│   │       ├── wechat-article         Content strategy, headline formulas
│   │       ├── linkedin-post          Algorithm, hook patterns
│   │       ├── invited-talk           Assertion-Evidence slides, Q&A
│   │       └── media-interview        Message triangle, bridging
│   │
│   └── patent/                    💡 Patent (4 skills)
│       ├── patent-mining              5 mining methods, portfolio strategy
│       ├── disclosure                 Timing rules, TTO process
│       ├── patent-drafting            Claims, specification, PCT strategy
│       └── office-action              US/CN/EP rejection responses
│
├── agents/                        11 composite agents
├── workflows/                     5 end-to-end workflows
├── install.sh                     Append-only installation
└── LICENSE                        MIT
```

## Quick Start

```bash
git clone https://github.com/zyx312/Co4Pilot.git
cd Co4Pilot
./install.sh
```

Your existing dev environment stays untouched — everything installs with an `academic-` prefix. Uninstall: `./install.sh --uninstall`

## Why "4P"?

Academic researchers juggle four distinct types of work every day. Most AI tools treat research as a monolith. Co4Pilot recognizes that **mentoring a PhD student** requires fundamentally different skills than **responding to reviewer comments** or **drafting a patent claim** or **writing a midterm project report**.

The 4P framework ensures nothing falls through the cracks:

- **People** — Who are you developing? (students, yourself, your team)
- **Project** — What are you delivering? (proposals, reports, data)
- **Paper** — What are you publishing? (papers, talks, articles)
- **Patent** — What are you protecting? (inventions, IP, disclosures)

## Content Quality

Every skill file contains 200-500 lines of substantive content:
- **Actionable frameworks** from MIT, Stanford, Harvard, CMU, Oxford
- **Step-by-step templates** you can use immediately
- **Claude prompt templates** for AI-assisted workflows
- **Quality checklists** to catch common mistakes
- **Tool recommendations** with specific setup guides

Total: **43 skill files, 18,900+ lines of content.**

## Roadmap

- [x] Phase 1: Core skills (paper writing, rebuttal, literature review, PhD mentoring, patent mining)
- [x] Phase 2: All 43 skills with deep content
- [x] Phase 3: GitHub open-source best practices integration (gpt_academic, awesome-phd-advice, etc.)
- [ ] Phase 4: 11 agent system prompts
- [ ] Phase 5: 5 end-to-end workflow automation
- [ ] Phase 6: Community contributions

## Inspired By

This project was inspired by [automotive-claude-code-agents](https://github.com/theja0473/automotive-claude-code-agents) by Thejeswarareddy R (Bosch), which demonstrated how domain-specific knowledge can be systematically integrated into AI coding assistants.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). PRs welcome — especially for:
- Discipline-specific skills (medical, legal, social science)
- Language-specific writing guides (German, Japanese, Korean academic conventions)
- Tool integration guides (Overleaf, Zotero, VOSviewer workflows)

## Author

**Yuxin Zhang** — Professor at Jilin University, School of Automotive Engineering. Research: autonomous driving safety, SOTIF, scenario-based testing.

## License

MIT — use freely in academic and commercial contexts.
