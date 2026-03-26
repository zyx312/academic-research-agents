# Literature Review Writing

> Skill for Claude Code — assists researchers in conducting and writing systematic literature reviews
> for journal papers, thesis chapters, and grant proposals.

## When to Use

- Planning a literature search strategy for a new research topic
- Organizing collected references into a coherent narrative
- Writing the literature review section of a journal paper or thesis
- Identifying research gaps to justify a new study
- Conducting a standalone review paper (narrative, systematic, or scoping)
- Building a citation network map to find foundational and emerging works
- Preparing the Rationale section (立项依据) of an NSFC or other grant proposal

---

## Review Types

| Type | Purpose | Methodology | When to Use |
|------|---------|-------------|-------------|
| **Narrative Review** | Broad overview of a topic | Selective, expert-driven | Introduction sections, textbook chapters |
| **Systematic Review** | Comprehensive, reproducible synthesis | PRISMA protocol, predefined criteria | Standalone review papers, evidence-based research |
| **Scoping Review** | Map the extent of research in an area | PRISMA-ScR, broad inclusion | Emerging fields, identifying what has been studied |
| **Meta-Analysis** | Statistical synthesis of quantitative results | Effect sizes, heterogeneity tests | When 10+ comparable quantitative studies exist |
| **Bibliometric Analysis** | Quantitative analysis of publication patterns | VOSviewer, CiteSpace, keyword co-occurrence | Field mapping, trend identification, hot topic analysis |
| **Critical Review** | Evaluate and critique existing theories/methods | Analytical framework | Theory papers, methodology papers |

### Choosing the Right Type

- **For a journal paper introduction**: Narrative review (2-4 pages, thematic organization)
- **For an NSFC Rationale section**: Narrative review with gap identification (3-5 pages)
- **For a standalone review paper**: Systematic or scoping review with PRISMA
- **For identifying research trends**: Bibliometric analysis with visualization
- **For clinical/engineering evidence synthesis**: Systematic review + meta-analysis

---

## PRISMA 2020 Framework

PRISMA (Preferred Reporting Items for Systematic Reviews and Meta-Analyses) is the gold standard for systematic reviews. The 2020 update includes 27 checklist items.

### PRISMA Flow Diagram Structure

```
Records identified through          Additional records identified
database searching                  through other sources
(n = _____)                        (n = _____)
        |                                  |
        +----------------------------------+
        |
Records after duplicates removed
(n = _____)
        |
Records screened by title/abstract
(n = _____)  -----> Records excluded (n = _____)
        |
Full-text articles assessed
for eligibility
(n = _____)  -----> Full-text excluded, with reasons
        |           (n = _____):
        |             - Reason 1 (n = ___)
        |             - Reason 2 (n = ___)
        |             - Reason 3 (n = ___)
Studies included in
qualitative synthesis
(n = _____)
        |
Studies included in
quantitative synthesis (meta-analysis)
(n = _____)
```

### Key PRISMA Checklist Items

1. **Registration**: Register the protocol on PROSPERO or OSF before starting
2. **Eligibility criteria**: Define inclusion/exclusion criteria using PICO (Population, Intervention, Comparison, Outcome) or PCC (Population, Concept, Context) for scoping reviews
3. **Information sources**: List all databases searched with dates
4. **Search strategy**: Full search string for at least one database (reproducible)
5. **Selection process**: How many reviewers screened, how disagreements were resolved
6. **Data extraction**: What data items were collected from each study
7. **Quality assessment**: Risk of bias tool used (e.g., Cochrane RoB 2, Newcastle-Ottawa Scale)
8. **Synthesis methods**: How results were combined (narrative, vote counting, meta-analysis)

---

## Five-Stage Workflow

### Stage 1: Discover (Search Strategy)

**Goal**: Find all relevant literature through systematic, reproducible searching.

**Step-by-step procedure**:

1. Define your research question using a framework:
   - **PICO**: Population, Intervention, Comparison, Outcome (for empirical studies)
   - **PCC**: Population, Concept, Context (for scoping reviews)
   - **SPIDER**: Sample, Phenomenon of Interest, Design, Evaluation, Research type

2. Identify key concepts and synonyms:
   ```
   Example for autonomous driving safety:
   Concept 1: autonomous driving | self-driving | automated vehicle | AV
   Concept 2: safety | collision | accident | crash | risk
   Concept 3: SOTIF | safety of the intended functionality | ISO 21448
   ```

3. Construct Boolean search strings (see Search Strategy Template below)

4. Search multiple databases (minimum 3 for a systematic review)

5. Supplement with:
   - Backward citation chasing (references of included papers)
   - Forward citation chasing (papers that cite included papers)
   - Grey literature (theses, technical reports, preprints)
   - Expert consultation (ask senior researchers for missed papers)

### Stage 2: Organize (Reference Management)

**Goal**: Deduplicate, tag, and structure your references for efficient retrieval.

**Procedure**:

1. Import all results into Zotero (preferred) or EndNote
2. Remove duplicates (Zotero's duplicate detection + manual check)
3. Create a folder structure mirroring your review themes:
   ```
   /Review Project
     /Theme 1 - [Name]
     /Theme 2 - [Name]
     /Theme 3 - [Name]
     /Excluded - Full text
     /Excluded - Title/Abstract
     /To Screen
   ```
4. Tag papers with: methodology type, key findings, quality rating
5. Screen by title/abstract first, then full text (record exclusion reasons)

### Stage 3: Map (Citation Networks)

**Goal**: Understand the intellectual structure of the field.

**Actions**:
- Use **Connected Papers** to visualize citation clusters around seed papers
- Use **Semantic Scholar** API for large-scale citation data
- Use **VOSviewer** or **CiteSpace** for keyword co-occurrence and co-citation analysis
- Identify: foundational papers, turning-point papers, recent hot papers, isolated clusters

**What to look for**:
- Which papers are most cited? (These are the "canonical" references you must cite)
- Are there distinct research communities working on this topic?
- What methods dominate? What methods are emerging?
- Where are the citation gaps? (Topics cited by one cluster but not the other)

### Stage 4: Analyze (Critical Reading)

**Goal**: Extract structured information from each included paper.

**Data extraction template** (create a spreadsheet with these columns):

| Column | Description |
|--------|-------------|
| Citation | Author, Year, Journal |
| Research Question | What question did this paper address? |
| Method | What methodology was used? |
| Dataset/Context | What data, size, domain? |
| Key Findings | 2-3 sentence summary of main results |
| Limitations | What the authors acknowledge or you identify |
| Relevance to Your Work | How does this paper relate to YOUR research question? |
| Quality Rating | High / Medium / Low (based on your assessment tool) |
| Theme | Which theme of your review does it belong to? |

**Critical reading questions for each paper**:
- Is the research question clearly stated?
- Is the methodology appropriate for the question?
- Are the conclusions supported by the data?
- What assumptions were made? Are they valid in your context?
- Can the results be generalized beyond the study's specific conditions?
- What would happen if you changed the assumptions or context?

### Stage 5: Synthesize (Thematic Writing)

**Goal**: Transform individual paper summaries into a coherent narrative.

**The cardinal rule**: A literature review is NOT a list of paper summaries. It is an ARGUMENT that leads to YOUR research question.

**Synthesis strategies**:
- **Compare**: How do different papers approach the same problem differently?
- **Contrast**: Where do findings disagree? Why?
- **Connect**: How does one study build on or complement another?
- **Critique**: What are the collective limitations of the body of work?
- **Converge**: What do most studies agree on? This is the established knowledge.

---

## Search Strategy Template

### Boolean Operator Syntax by Database

| Database | AND | OR | NOT | Phrase | Wildcard | Truncation |
|----------|-----|-----|-----|--------|----------|------------|
| Web of Science | AND | OR | NOT | "..." | * | $ |
| Scopus | AND | OR | AND NOT | "..." | * | * |
| Google Scholar | AND (default) | OR | - | "..." | N/A | N/A |
| IEEE Xplore | AND | OR | NOT | "..." | * | * |
| CNKI (知网) | * (AND) | + (OR) | - (NOT) | "" | % | ? |

### Example Search String (Web of Science)

```
TS = (("autonomous driv*" OR "self-driving" OR "automated vehicle*")
  AND ("safety" OR "collision" OR "risk assessment" OR "hazard")
  AND ("SOTIF" OR "intended functionality" OR "ISO 21448"
       OR "performance limitation" OR "misuse"))

Refined by: Document Types = (Article OR Review OR Proceedings Paper)
Timespan: 2018-2026
```

### Google Scholar Tips
- Google Scholar does not support complex Boolean well; use short, focused queries
- Use the "Cited by" feature for forward citation chasing
- Check "Related articles" for lateral discovery
- Use `site:arxiv.org` to restrict to preprints when needed
- The first 2-3 pages of results are usually the most relevant; diminishing returns after that

---

## Recommended Tool Stack

| Tool | Purpose | Cost | Best For |
|------|---------|------|----------|
| **Zotero** | Reference management, PDF annotation | Free | Organizing papers, generating bibliographies |
| **Connected Papers** | Visual citation graph from a seed paper | Free (limited) | Finding related work quickly |
| **Semantic Scholar** | AI-powered paper search and recommendation | Free | Large-scale literature discovery |
| **ResearchRabbit** | Citation-based paper discovery | Free | Continuous discovery as you add papers |
| **Litmaps** | Interactive citation maps with timelines | Free (limited) | Visualizing how a field evolved |
| **VOSviewer** | Bibliometric network visualization | Free | Keyword co-occurrence, co-citation analysis |
| **CiteSpace** | Bibliometric analysis with burst detection | Free | Identifying emerging trends in Chinese research |
| **Elicit** | AI research assistant for data extraction | Free (limited) | Extracting structured data from papers |
| **Obsidian** | Knowledge management with linked notes | Free | Building a personal knowledge graph of papers |
| **Scite.ai** | Smart citation analysis (supporting/contradicting) | Paid | Understanding how papers are cited in context |

### Minimal Setup for a Research Group

1. **Zotero** with WebDAV sync (group library for lab members)
2. **Connected Papers** for initial exploration of a new topic
3. **A spreadsheet** (Google Sheets or Excel) for structured data extraction
4. **VOSviewer** for bibliometric analysis if writing a review paper

---

## Writing Structure

### Thematic Organization (Preferred for Most Reviews)

Organize by research theme or approach, NOT chronologically and NOT by individual paper.

**Template for each theme section**:

```markdown
## [Theme Title]

[1-2 sentences: Define this theme and explain its relevance to the overall topic]

[Body: Discuss key contributions. Group related works together.
 Compare approaches, highlight agreements and disagreements.
 Use "Author (Year)" citations woven into the narrative — never
 write "In [1], the authors did X. In [2], the authors did Y."]

[Closing: State the limitation or gap within this specific theme
 that motivates the next section or your own research]
```

**Good writing patterns**:
- "Several studies have addressed X through [approach A] (Author1, Year; Author2, Year), while others have adopted [approach B] (Author3, Year; Author4, Year). The key difference lies in..."
- "While these methods achieve [result] under [condition], their performance degrades significantly when [challenging scenario], as demonstrated by Author (Year)."
- "A common assumption across these studies is [assumption]. However, in the context of [your domain], this assumption may not hold because [reason]."

**Bad writing patterns (avoid)**:
- "Author1 (2020) proposed X. Author2 (2021) proposed Y. Author3 (2022) proposed Z." (This is a list, not a review.)
- "Many researchers have studied this topic." (Vague; name them and say what they found.)
- "The literature is extensive." (Empty statement; show the extent through your organization.)

### Chronological Organization (Use Sparingly)

Only appropriate when temporal development is itself the story — e.g., "how SOTIF standards evolved from ISO 26262 to ISO 21448."

### Methodological Organization

Group by research method (simulation-based / field-test-based / analytical / data-driven). Useful for methodology-focused review papers.

---

## Gap Identification Framework

Identifying gaps is the most important outcome of a literature review. The gap justifies your research.

### Three Dimensions of Gaps

| Dimension | Question to Ask | Example Gap |
|-----------|----------------|-------------|
| **Topical** | What has been studied vs. what hasn't? | "Most SOTIF research focuses on perception failures; decision-making failures under SOTIF are understudied." |
| **Methodological** | What methods have been used vs. what's missing? | "Existing approaches rely on scenario-based testing; formal verification methods for SOTIF remain unexplored." |
| **Contextual** | What contexts have been examined vs. what's underexplored? | "SOTIF has been studied primarily for highway driving; urban mixed-traffic scenarios are underrepresented." |

### Gap Statement Template

```
Although [existing work summary], [specific limitation].
This gap is significant because [consequence of the gap].
The present study addresses this by [your contribution].
```

### Verifying Your Gap is Real

Before claiming a gap, check:
- [ ] Have you searched thoroughly? (Not just one database)
- [ ] Is the gap genuinely unstudied, or just published in venues you haven't checked?
- [ ] Is there a good reason the gap exists? (Maybe it is trivial, infeasible, or already solved by an adjacent field)
- [ ] Is the gap narrow enough to be addressable in one study?
- [ ] Will filling this gap matter to the field?

---

## Quality Checklist

Use this checklist to evaluate your literature review before submission.

### Completeness
- [ ] Searched at least 3 databases (Web of Science, Scopus, + domain-specific)
- [ ] Included both English and Chinese sources where relevant
- [ ] Covered the last 5-10 years comprehensively; included foundational older work
- [ ] Performed forward and backward citation chasing on key papers
- [ ] Included at least 40 references (journal paper) or 60+ (review paper)

### Organization
- [ ] Organized by theme, not by individual paper
- [ ] Each section has a clear topic sentence and closing transition
- [ ] The overall structure follows a logical progression toward the research gap
- [ ] No section is merely a list of paper summaries

### Critical Analysis
- [ ] Compared and contrasted different approaches, not just described them
- [ ] Identified strengths AND limitations of existing work
- [ ] Noted where findings agree and where they conflict
- [ ] Evaluated the quality and relevance of cited studies

### Gap and Motivation
- [ ] Research gap is explicitly stated (not implied)
- [ ] Gap is specific and evidence-based (not "further research is needed")
- [ ] Gap logically leads to the research question of the current study
- [ ] The gap is genuinely unaddressed (verified through thorough search)

### Writing Quality
- [ ] No "laundry list" paragraphs (Author1 did X. Author2 did Y.)
- [ ] Citations are woven into sentences, not parenthetical dumps
- [ ] Consistent terminology throughout
- [ ] Transitions between paragraphs and sections are smooth
- [ ] The review tells a coherent story, not a collection of facts

### Formatting
- [ ] All cited works appear in the reference list (and vice versa)
- [ ] Citation format matches the target journal's requirements
- [ ] Figures and tables (if any) have captions and are referenced in text
- [ ] Page length is appropriate for the venue

---

## Prompt Templates for Claude

### Template 1: Search Strategy Design

```
I am conducting a literature review on [TOPIC] for a [journal paper / thesis / NSFC proposal].

My research question is: [QUESTION]

Please help me:
1. Identify 3-5 key concepts and their synonyms/related terms
2. Construct Boolean search strings for Web of Science and Scopus
3. Suggest inclusion/exclusion criteria
4. Recommend any domain-specific databases I should search
5. Suggest 3-5 seed papers I can use for citation chasing
```

### Template 2: Thematic Organization

```
I have collected [N] papers on [TOPIC]. Based on reading them, I have identified
the following preliminary themes:
- Theme A: [description]
- Theme B: [description]
- Theme C: [description]

Here are the papers with brief descriptions:
[LIST OF PAPERS WITH 1-SENTENCE SUMMARIES]

Please:
1. Evaluate whether my thematic grouping is logical
2. Suggest if any themes should be split, merged, or reordered
3. Identify any papers that seem miscategorized
4. Suggest a logical ordering of themes that builds toward [my research gap]
5. Propose transition sentences between themes
```

### Template 3: Gap Analysis

```
Below is a summary table of [N] papers I reviewed on [TOPIC]:

[PASTE TABLE WITH: Author, Year, Method, Context, Key Finding, Limitation]

Please analyze this body of work and identify:
1. What topics/questions have been well-studied?
2. What topics/questions are understudied or missing?
3. What methodological approaches dominate? What is underused?
4. What contexts/domains have been examined? What is missing?
5. Where do findings conflict, and why might this be?
6. What is the most significant and addressable research gap?
```

### Template 4: Paragraph-Level Review Critique

```
Below is a paragraph from my literature review. Please critique it:
1. Is it organized by theme or by individual paper? (Theme is preferred)
2. Does it compare/contrast or merely describe?
3. Is the writing concise or padded?
4. Does it end with a clear transition or gap statement?
5. Rewrite it to improve the synthesis quality while preserving accuracy.

Paragraph:
[PASTE PARAGRAPH]
```

### Template 5: Review Paper Outline Generation

```
I want to write a review paper on [TOPIC] for [TARGET JOURNAL].
The paper should cover approximately [N] papers from [YEAR RANGE].

My goals are:
- [Goal 1, e.g., "map the landscape of SOTIF research"]
- [Goal 2, e.g., "identify methodological trends"]
- [Goal 3, e.g., "propose future research directions"]

Please generate:
1. A detailed section-by-section outline (6-8 main sections)
2. Suggested subsections under each main section
3. Recommended number of papers to discuss in each section
4. A suggested title for the review paper
5. 3-5 potential figures/tables that would strengthen the paper
```

---

## Bibliometric Analysis Tools (Detailed Guide)

### VOSviewer Workflow for Review Papers

VOSviewer (Leiden University) is the most widely used free bibliometric visualization tool.

**Step-by-step workflow**:
1. **Export data**: From Web of Science, export as "Full Record and Cited References" in Tab-delimited format. From Scopus, export as CSV with all fields.
2. **Create a map**: Open VOSviewer > Create > Create a map based on bibliographic data
3. **Choose analysis type**:
   - **Keyword co-occurrence**: Shows which topics appear together (use Author Keywords or Keywords Plus)
   - **Co-citation analysis**: Reveals intellectual foundations (which references cluster together)
   - **Bibliographic coupling**: Connects papers sharing references (identifies current research fronts)
   - **Co-authorship**: Maps collaboration networks
4. **Set thresholds**: For keyword co-occurrence, require minimum 5 occurrences. For co-citation, minimum 10 citations.
5. **Interpret the visualization**: Clusters (colors) represent distinct research themes. Distance between nodes indicates relatedness. Node size reflects frequency/citations.
6. **Overlay visualization**: Switch to overlay mode to color nodes by publication year — reveals temporal evolution of topics.
7. **Export**: Save as PNG/SVG for publication. Export the network data as CSV for further analysis.

**Download**: vosviewer.com (free, cross-platform)

### CiteSpace for Burst Detection and Trend Analysis

CiteSpace excels at identifying emerging research fronts through citation burst detection.

**Key analyses for review papers**:
- **Citation burst detection**: Identifies references or keywords with sudden surges in frequency. A burst indicates an emerging hot topic.
- **Timeline visualization**: Shows how research clusters evolve year by year.
- **Betweenness centrality**: Finds "bridge" papers connecting different research communities — these are often the most important papers to cite.
- **Modularity analysis**: Measures how cleanly the field separates into distinct sub-communities.

**Data preparation**: Export from Web of Science in "Plain Text" format (not Tab-delimited). CiteSpace requires this specific format.

**Download**: citespace.podia.com (free for academic use)

### Bibliometrix R Package

For researchers needing programmatic control or advanced analysis:

```r
install.packages("bibliometrix")
library(bibliometrix)

# Import and analyze
D <- convert2df(file = "wos_export.txt", dbsource = "wos", format = "plaintext")
results <- biblioAnalysis(D, sep = ";")

# Key outputs for review papers:
# 1. Most cited papers and authors
summary(results, k = 20)

# 2. Thematic map (strategic diagram) — classifies themes into:
#    - Motor themes (high centrality, high density): well-developed and important
#    - Niche themes (low centrality, high density): specialized
#    - Emerging themes (low centrality, low density): new or declining
#    - Basic themes (high centrality, low density): foundational but undeveloped
Map <- thematicMap(D, field = "DE", n = 250, minfreq = 5)
plot(Map$map)

# 3. Interactive dashboard
biblioshiny()
```

### Google Scholar Integration Prompt for Related Work

Use this prompt to draft a Related Work section based on a set of papers discovered via Google Scholar (inspired by gpt_academic):

```
I am writing the Related Work section of a paper on [TOPIC].
I have collected the following papers from Google Scholar and other sources.
For each paper, I provide the title, authors, year, and a one-line summary.

Papers:
1. [Title] ([Authors], [Year]) — [One-line summary]
2. [Title] ([Authors], [Year]) — [One-line summary]
...

Please help me:
1. Group these papers into 3-5 thematic categories
2. For each category, write a synthesis paragraph that:
   - Opens with a topic sentence defining the theme
   - Discusses 3-5 key papers, comparing their approaches
   - Identifies the shared limitation of this group
   - Ends with a transition connecting to the next theme or to my work
3. End the entire section with a summary paragraph that:
   - States what the collective body of work has achieved
   - Identifies the specific gap my paper addresses
   - Explains how my approach differs from prior work

My paper's contribution: [BRIEF DESCRIPTION]
Target venue: [JOURNAL/CONFERENCE]
```

### Bibliometric Visualization Prompt

```
I have exported bibliometric data from [Web of Science / Scopus] for my
review paper on [TOPIC]. The dataset contains [N] papers from [YEAR RANGE].

Based on VOSviewer/CiteSpace analysis, I found the following:
- Top keyword clusters: [LIST CLUSTERS]
- Citation burst keywords: [LIST BURST KEYWORDS WITH YEARS]
- Most-cited papers: [LIST TOP 5]
- Main research communities: [DESCRIBE CLUSTERS]

Please help me:
1. Write an "Analysis of Research Landscape" subsection interpreting these results
2. Create a narrative explaining the evolution of the field over time
3. Identify which research fronts are growing vs. declining
4. Suggest which emerging themes deserve more attention
5. Draft figure captions for the VOSviewer/CiteSpace visualizations
```

---

## References and Further Reading

- Page, M.J., et al. (2021). The PRISMA 2020 statement: an updated guideline for reporting systematic reviews. BMJ, 372, n71.
- Xiao, Y., & Watson, M. (2019). Guidance on Conducting a Systematic Literature Review. Journal of Planning Education and Research, 39(1), 93-112.
- Snyder, H. (2019). Literature review as a research methodology: An overview and guidelines. Journal of Business Research, 104, 333-339.
- Pautasso, M. (2013). Ten simple rules for writing a literature review. PLoS Computational Biology, 9(7), e1003149.

---

## Related Skills

- [literature-search.md](literature-search.md) — Finding papers and building search strategies
- [paper-reading.md](paper-reading.md) — Detailed analysis of individual papers
- [../paper-writing/review-paper.md](../paper-writing/review-paper.md) — Full review paper writing
- [../proposal/nsfc.md](../proposal/nsfc.md) — NSFC proposal writing (uses literature review in Rationale section)
