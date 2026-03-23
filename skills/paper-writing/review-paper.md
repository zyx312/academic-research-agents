# Review Paper Writing

## Purpose

This skill provides a comprehensive framework for planning, conducting, and writing review papers (also called survey papers). It covers the full spectrum from systematic reviews to narrative reviews, including PRISMA methodology, synthesis techniques, taxonomy design, and gap identification. A well-written review paper establishes the author as a field expert and provides lasting value to the research community.

## Related
- [research-paper.md](research-paper.md) - Original research papers
- [../literature/literature-review.md](../literature/literature-review.md) - Literature review skills
- [../literature/literature-search.md](../literature/literature-search.md) - Systematic search

---

## Types of Review Papers

| Type | Purpose | Search Required | Synthesis Method | Typical Length |
|------|---------|----------------|-----------------|---------------|
| **Systematic Review** | Comprehensive, reproducible evidence synthesis | Exhaustive, documented | Structured, may include meta-analysis | 8,000-15,000 words |
| **Scoping Review** | Map available evidence on a broad topic | Systematic but broader | Descriptive, charting | 6,000-12,000 words |
| **Narrative Review** | Discuss and interpret a topic with expert perspective | Selective, author-driven | Argumentative, interpretive | 5,000-10,000 words |
| **Umbrella Review** | Review of existing reviews | Systematic across reviews | Synthesis of syntheses | 6,000-10,000 words |
| **Bibliometric Review** | Quantitative analysis of publication patterns | Database-driven | Statistical, network analysis | 5,000-8,000 words |
| **Critical Review** | Evaluate and critique a body of work | Focused, selective | Analytical, evaluative | 4,000-8,000 words |
| **Meta-Analysis** | Statistical synthesis of quantitative results | Exhaustive | Statistical pooling | 6,000-12,000 words |

### Choosing the Right Type
- **New to a field?** Start with a scoping review to understand the landscape
- **Mature field with quantitative studies?** Consider a meta-analysis
- **Want to provide an authoritative perspective?** Write a narrative review
- **Need to inform policy or practice?** Conduct a systematic review
- **Want to analyze publication trends?** Use a bibliometric approach

---

## Phase 1: Planning

### Define the Review Scope

Answer these questions before you begin:

1. **What is the central question?** Write it as precisely as possible.
2. **What type of review will you conduct?** (See table above)
3. **What is the timeframe?** How far back will you search?
4. **What are the boundaries?** Geographic, methodological, application-specific?
5. **Who is the target audience?** Researchers, practitioners, policymakers?
6. **Which journal will you target?** Check if they publish reviews and word limits.

### Register Your Protocol (Systematic Reviews)

For systematic reviews, register your protocol before beginning:
- **PROSPERO**: For health-related reviews (crd.york.ac.uk/prospero)
- **OSF Registries**: For any discipline (osf.io/registries)
- **Protocol papers**: Some journals publish review protocols as standalone papers

### Form a Review Team

| Role | Responsibilities |
|------|-----------------|
| Lead author | Design protocol, coordinate team, write majority of paper |
| Co-screener | Independent screening of titles/abstracts/full texts |
| Domain expert | Validate taxonomy, check coverage completeness |
| Methodologist | Ensure PRISMA compliance, quality assessment |
| Statistician | For meta-analyses: pooling, heterogeneity analysis |

---

## Phase 2: Search Protocol

### Design Your Search Strategy

Refer to [literature-search.md](../literature/literature-search.md) for detailed search techniques.

Key steps specific to reviews:
1. Develop search strings with a librarian if possible
2. Test search in one database, refine, then expand to others
3. Document EVERYTHING (dates, databases, exact strings, filters)
4. Pilot the screening criteria on 50 records before full screening
5. Plan for forward/backward citation chaining

### Minimum Database Coverage by Discipline

| Discipline | Required Databases |
|-----------|-------------------|
| Engineering/CS | Scopus + Web of Science + IEEE Xplore (+ CNKI for Chinese lit.) |
| Medicine/Health | PubMed + Embase + Cochrane (+ CINAHL for nursing) |
| Social Sciences | WoS + Scopus + PsycINFO (+ ERIC for education) |
| Multidisciplinary | WoS + Scopus + domain-specific + Google Scholar |

---

## Phase 3: Screening and Selection

### Inclusion/Exclusion Criteria Template

```markdown
## Inclusion Criteria
- IC1: Published between [YEAR] and [YEAR]
- IC2: Written in [LANGUAGES]
- IC3: Peer-reviewed journal articles or conference papers
- IC4: Addresses [SPECIFIC TOPIC]
- IC5: Presents [TYPE OF EVIDENCE: empirical results / theoretical framework / ...]

## Exclusion Criteria
- EC1: Editorials, commentaries, letters, book reviews
- EC2: Duplicate publications (keep most complete version)
- EC3: Studies not directly addressing the research question
- EC4: Papers without accessible full text
- EC5: Grey literature (unless explicitly included in scope)
```

### Screening Process

1. **Import and deduplicate**: Use Zotero/Covidence/Rayyan
2. **Title screening**: Apply criteria liberally (when in doubt, include)
3. **Abstract screening**: Apply criteria more strictly; record exclusion reasons
4. **Full-text screening**: Apply all criteria; record detailed exclusion reasons
5. **Data extraction**: From all included papers (see Phase 4)

### Quality Assessment Tools

| Tool | Best For | Key Features |
|------|----------|-------------|
| Newcastle-Ottawa Scale | Observational studies | Star-based scoring |
| Cochrane RoB 2 | Randomized trials | Domain-based bias assessment |
| CASP Checklists | Various study types | Question-based appraisal |
| QUADAS-2 | Diagnostic accuracy | Risk of bias + applicability |
| Custom rubric | Engineering/CS studies | Design your own criteria |

For engineering/CS reviews where standard tools do not fit, create a custom quality rubric:
```
- Methodological rigor (0-3): Are methods clearly described and appropriate?
- Reproducibility (0-3): Could another researcher replicate this?
- Evaluation quality (0-3): Are baselines fair? Are metrics standard?
- Result validity (0-3): Do results support claims convincingly?
```

---

## Phase 4: Data Extraction

### Data Extraction Form Template

Create a spreadsheet (or use Covidence/JBI SUMARI) with these columns:

```
| Paper ID | Authors | Year | Venue | Country |
| Research Question | Study Design | Sample/Dataset |
| Method/Approach | Key Technique | Tools/Framework |
| Evaluation Metrics | Main Results | Limitations Noted |
| Quality Score | Relevant Findings | Notes |
```

### Extraction Best Practices
- Pilot the extraction form on 5 papers before full extraction
- Have two reviewers extract independently for critical reviews
- Use coding schemes for categorical data (method type, study design)
- Record both quantitative results AND qualitative insights
- Note how each paper defines key terms (definitions vary across papers)

---

## Phase 5: Synthesis

### Thematic Synthesis
1. Read all extracted data and identify recurring themes
2. Group papers by theme
3. Within each theme, identify agreements, disagreements, and gaps
4. Present findings organized by theme, not by paper

### Framework Synthesis
1. Select or develop a conceptual framework
2. Map each included study onto the framework
3. Identify areas of the framework with rich evidence vs. sparse evidence
4. Use the framework to structure your Results section

### Taxonomy Design

A well-designed taxonomy is the hallmark of an excellent survey paper:

1. **Bottom-up**: Read all papers, inductively identify categories
2. **Top-down**: Start with a theoretical framework, map papers into it
3. **Hybrid**: Combine both approaches, iterate

```
Example Taxonomy Structure:
Level 1: [Broad Category]
  Level 2: [Sub-category]
    Level 3: [Specific approach]
      - Paper A (2022): [key contribution]
      - Paper B (2023): [key contribution]
```

### Comparison Tables

Every good review paper contains comparison tables. Include:

| Column | Purpose |
|--------|---------|
| Reference | Paper citation |
| Year | Publication year |
| Method category | From your taxonomy |
| Dataset/Application | Where it was tested |
| Key technique | What makes it distinctive |
| Main metric + result | Quantitative performance |
| Open source? | Code/data availability |
| Limitations | Self-reported or observed |

### Trend Analysis
- Plot publication counts per year to show growing/declining interest
- Create a timeline of key milestones and breakthroughs
- Identify paradigm shifts (e.g., from rule-based to learning-based methods)
- Map geographic distribution of research (which countries/institutions lead)

### Bibliometric Analysis (Optional Enhancement)
- Use VOSviewer or CiteSpace for keyword co-occurrence networks
- Analyze author collaboration networks
- Identify most-cited papers and emerging hot topics
- Generate keyword evolution over time

---

## Phase 6: Writing the Review Paper

### Standard Structure

```
1. Title
2. Abstract (structured: Background, Methods, Results, Conclusions)
3. Introduction
   - Context and importance of the topic
   - Brief history / evolution of the field
   - Scope and objectives of this review
   - How this review differs from existing reviews
4. Methods (for systematic/scoping reviews)
   - Search strategy (databases, dates, strings)
   - Inclusion/exclusion criteria
   - Screening process
   - Data extraction approach
   - Quality assessment method
   - PRISMA flow diagram
5. Results / Main Body
   - Overview of included studies (descriptive statistics)
   - Organized by taxonomy/themes (NOT one section per paper)
   - Comparison tables
   - Trend analysis
6. Discussion
   - Summary of key findings
   - Comparison with previous reviews
   - Identified research gaps
   - Implications for research and practice
   - Limitations of this review
7. Future Research Directions
   - Specific, actionable research questions
   - Recommended methodological improvements
   - Emerging topics deserving attention
8. Conclusion
9. References
```

### PRISMA 2020 Checklist (27 items)

The PRISMA 2020 statement includes items covering:
- **Title** (item 1): Identify as systematic review, meta-analysis, or both
- **Abstract** (item 2): Structured summary
- **Introduction** (items 3-4): Rationale and objectives
- **Methods** (items 5-16): Eligibility, info sources, search strategy, selection, data collection, study risk of bias, effect measures, synthesis methods, reporting bias, certainty assessment
- **Results** (items 17-23): Study selection, study characteristics, risk of bias, individual results, synthesis results, reporting biases, certainty
- **Discussion** (items 24-26): Interpretation, limitations, implications
- **Other** (item 27): Registration and protocol, support, competing interests, availability

### Writing Principles for Reviews

1. **Synthesize, do not summarize**: Group by theme/finding, not paper-by-paper
2. **Be critical**: Do not just report what papers say -- evaluate quality and consistency
3. **Be comprehensive but focused**: Cover the field but stay within your defined scope
4. **Use visual aids**: Tables, figures, timelines, and taxonomy diagrams add enormous value
5. **Identify gaps explicitly**: This is the main contribution readers expect from a review
6. **Stay objective**: Present all perspectives, even those you disagree with
7. **Update before submission**: Search once more for papers published during your writing period

---

## Common Pitfalls

1. **Paper-by-paper summaries**: "Smith (2020) did X. Jones (2021) did Y." -- synthesize by theme instead
2. **Missing PRISMA elements**: Reviewers will reject systematic reviews that skip PRISMA items
3. **Incomplete search documentation**: Every database, every string, every filter must be recorded
4. **No quality assessment**: Treating all papers as equally valid is a major weakness
5. **Weak gap identification**: Vague statements like "more research is needed" -- be specific
6. **Stale references**: If your newest reference is 2+ years old, the review feels outdated
7. **Ignoring existing reviews**: Always explain how YOUR review differs from prior reviews
8. **Scope creep**: Define boundaries early and stick to them
9. **Missing comparison tables**: Reviewers expect structured comparisons
10. **No actionable future directions**: Propose specific studies, not generic wishes

---

## How to Identify Research Gaps

### Gap Identification Framework

| Gap Type | Description | Example |
|----------|-------------|---------|
| **Knowledge gap** | Something is not yet known | No studies on X in context Y |
| **Methodological gap** | Existing methods are insufficient | Studies use metric A but ignore metric B |
| **Population gap** | Underrepresented groups/contexts | Most studies focus on region X, ignoring Y |
| **Theoretical gap** | Lack of theoretical grounding | Results exist but no unifying framework |
| **Practical gap** | Research does not address real-world needs | Lab results do not translate to deployment |
| **Empirical gap** | Insufficient evidence | Claims based on simulations only, no real-world testing |

### Techniques for Finding Gaps
1. Create a matrix: rows = research questions, columns = methods/contexts. Empty cells = gaps.
2. List common limitations reported across papers -- recurring limitations signal gaps.
3. Compare what practitioners need (from industry papers) with what academia provides.
4. Look for contradictory findings -- these indicate under-explored areas.
5. Check what the newest papers cite as future work -- if it has not been done, it is a gap.

---

## Prompt Templates for Claude

### Design a Review Protocol
```
I want to write a [TYPE: systematic / scoping / narrative] review on [TOPIC].
My target journal is [JOURNAL NAME] with a word limit of [LIMIT].

Please help me:
1. Refine my review question using the appropriate framework (PICO, PCC, etc.)
2. Suggest which databases to search and why
3. Draft inclusion/exclusion criteria
4. Propose a quality assessment approach
5. Suggest a structure for the review paper
6. Identify existing reviews on this topic that I should differentiate from
```

### Build a Taxonomy
```
I am writing a survey paper on [TOPIC]. I have included [NUMBER] papers.
Here are the approaches/methods found in these papers:
[LIST OF APPROACHES WITH BRIEF DESCRIPTIONS]

Please help me:
1. Design a multi-level taxonomy that logically organizes these approaches
2. Identify the classification criteria at each level
3. Suggest how to handle papers that span multiple categories
4. Create a visual taxonomy diagram outline
5. Identify any categories that seem underrepresented
```

### Draft Comparison Table
```
I have these papers for my review on [TOPIC]:
[LIST: Author (Year), Method, Dataset, Key Metric, Result]

Please create a comprehensive comparison table that includes:
1. All papers organized by [TAXONOMY CATEGORY]
2. Columns for: method type, dataset, metrics, results, code availability
3. Highlight the best-performing approaches
4. Add a "Notes" column with distinguishing features
```

### Identify Research Gaps
```
Here is a summary of findings from my review of [NUMBER] papers on [TOPIC]:

Themes covered:
[LIST THEMES WITH PAPER COUNTS]

Common methods:
[LIST METHODS]

Common datasets:
[LIST DATASETS]

Common limitations reported:
[LIST LIMITATIONS]

Please help me identify:
1. Knowledge gaps (what is not yet known)
2. Methodological gaps (what approaches are missing)
3. Application gaps (what contexts are understudied)
4. Specific, actionable future research directions
5. How to frame these gaps persuasively in my Discussion section
```

### Write Future Directions Section
```
Based on my review of [TOPIC], the key gaps I identified are:
[LIST GAPS]

Please help me write a "Future Research Directions" section that:
1. Presents each direction as a concrete, researchable question
2. Explains WHY each direction is important
3. Suggests HOW each direction could be approached methodologically
4. Connects each direction back to the gaps found in my review
5. Is organized from near-term achievable to long-term visionary
```
