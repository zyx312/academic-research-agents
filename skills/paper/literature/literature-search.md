# Systematic Literature Search Strategy

## Purpose

This skill provides a comprehensive framework for conducting systematic, reproducible, and exhaustive literature searches across academic databases. A well-executed search is the foundation of any research project, ensuring you build on existing knowledge and identify genuine gaps.

## Related
- [literature-review.md](literature-review.md) - Synthesize found literature
- [paper-reading.md](paper-reading.md) - Deep-read individual papers
- [reference-management.md](reference-management.md) - Organize references

---

## Core Principles

1. **Reproducibility**: Document every search so others (or future you) can replicate it exactly.
2. **Sensitivity vs. Specificity**: Balance broad recall (finding everything relevant) against precision (avoiding irrelevant noise).
3. **Triangulation**: Use multiple databases, methods, and search terms to minimize blind spots.
4. **Iteration**: Refine your search strategy as you learn the vocabulary and structure of the field.

---

## Step 1: Define Your Research Question

Use the PICO/PICo framework to decompose your question into searchable concepts:

| Element | Description | Example |
|---------|-------------|---------|
| **P** - Population/Problem | Who or what is being studied? | Autonomous vehicles |
| **I** - Intervention/Interest | What is the main focus? | Safety validation methods |
| **C** - Comparison | What is the alternative? | Traditional testing vs. simulation |
| **O** - Outcome | What are you measuring? | Fault detection rate |

For engineering/CS research, adapt to: **Context - Intervention - Mechanism - Outcome (CIMO)**.

### Action Checklist
- [ ] Write your research question in one sentence
- [ ] Identify 2-4 core concepts from the question
- [ ] List 3-5 synonyms, abbreviations, and related terms for each concept
- [ ] Identify relevant controlled vocabulary (MeSH, IEEE Thesaurus, ACM CCS)

---

## Step 2: Select Databases

### Primary Databases by Discipline

| Database | Best For | Syntax Notes |
|----------|----------|-------------|
| **Web of Science** | Multidisciplinary, citation analysis | TS= for topic, TI= for title, proximity: NEAR/x |
| **Scopus** | Broader coverage than WoS, engineering | TITLE-ABS-KEY(), W/n for proximity |
| **IEEE Xplore** | Electrical/computer engineering, AI | Controlled vocabulary via IEEE Thesaurus |
| **Google Scholar** | Broad discovery, grey literature | No Boolean NOT; use minus sign (-); limited advanced search |
| **PubMed/MEDLINE** | Biomedical, health sciences | MeSH terms, [tiab] for title/abstract |
| **CNKI** | Chinese-language scholarship | SU= for subject, TI= for title, supports Chinese Boolean |
| **ACM Digital Library** | Computer science | ACM CCS classification, full-text search |
| **Engineering Village** | Engineering (Compendex + Inspec) | Controlled vocabulary, command-line search |
| **arXiv** | Preprints in CS, physics, math | Full-text search, category filters |
| **DBLP** | CS publication metadata | Author/venue search, no abstracts |
| **Wanfang Data** | Chinese dissertations and journals | Supports subject/title/abstract fields |
| **Semantic Scholar** | AI-powered relevance ranking | API available, influence scores |

### Selection Heuristic
- **Minimum**: Search at least 2 major databases + Google Scholar
- **Systematic reviews**: Search at least 3-4 databases + grey literature sources
- **Interdisciplinary topics**: Add domain-specific databases for each discipline
- **Chinese research**: Always include CNKI + Wanfang for comprehensive coverage

---

## Step 3: Construct Search Strings

### Boolean Operators

| Operator | Function | Effect on Results |
|----------|----------|-------------------|
| **AND** | Combines different concepts | Narrows (intersection) |
| **OR** | Combines synonyms/alternatives | Broadens (union) |
| **NOT** | Excludes terms | Narrows (use sparingly -- may exclude relevant work) |

### Advanced Operators

| Technique | Syntax Example | Purpose |
|-----------|---------------|---------|
| **Phrase search** | "autonomous driving" | Exact phrase match |
| **Truncation** | autonom* | Captures autonomous, autonomy, automobile |
| **Wildcard** | wom?n | Captures woman, women |
| **Proximity** | safety NEAR/3 validation (WoS) | Terms within 3 words of each other |
| **Field limiting** | TI=("safety") | Search only in title field |
| **Nesting** | (autonomous OR self-driving) AND (safety OR security) | Group terms with parentheses |

### Search String Construction Template

```
Concept A: (term1 OR term2 OR term3 OR "phrase term")
Concept B: (term4 OR term5 OR term6*)
Concept C: (term7 OR term8)

Full search: (Concept A) AND (Concept B) AND (Concept C)
```

### Database-Specific Syntax Examples

**Web of Science:**
```
TS=("autonomous driving" OR "self-driving" OR "automated vehicle*")
AND TS=(safety OR "safety of the intended functionality" OR SOTIF)
AND TS=(valid* OR verif* OR test*)
```

**Scopus:**
```
TITLE-ABS-KEY("autonomous driving" OR "self-driving" OR "automated vehicle*")
AND TITLE-ABS-KEY(safety OR SOTIF)
AND TITLE-ABS-KEY(valid* OR verif* OR test*)
AND PUBYEAR > 2017
```

**PubMed:**
```
("autonomous vehicles"[MeSH] OR "self-driving"[tiab] OR "automated driving"[tiab])
AND ("safety"[MeSH] OR "safety"[tiab])
```

**IEEE Xplore:**
```
("autonomous driving" OR "self-driving") AND ("safety validation" OR "SOTIF")
Filter: Conferences + Journals, 2018-present
```

**CNKI (Chinese):**
```
SU=('自动驾驶' + '智能驾驶') * SU=('安全' + 'SOTIF' + '预期功能安全')
```

**Google Scholar:**
```
"autonomous driving" "safety validation" -patent
allintitle: autonomous driving safety
```

---

## Step 4: Execute and Filter

### Recommended Execution Order
1. Run search in each database separately
2. Export results to reference manager (Zotero recommended)
3. Remove duplicates (use DOI matching first, then title+author matching)
4. Apply inclusion/exclusion criteria in stages

### Inclusion/Exclusion Criteria Template

| Criterion | Include | Exclude |
|-----------|---------|---------|
| **Date range** | Define based on field maturity | Outside range |
| **Language** | English, Chinese (or your target) | Other languages |
| **Document type** | Journal articles, conference papers | Editorials, book reviews, news |
| **Peer review** | Peer-reviewed venues | Non-peer-reviewed (unless grey lit.) |
| **Topic relevance** | Directly addresses research question | Tangentially related |
| **Quality threshold** | Q1/Q2 journals, top conferences | Predatory journals |

### Screening Process
1. **Title screening**: Exclude clearly irrelevant papers (2-5 seconds per title)
2. **Abstract screening**: Read abstracts of remaining papers (30-60 seconds each)
3. **Full-text screening**: Read full papers for final inclusion (10-20 minutes each)
4. **Record reasons** for exclusion at each stage (required for PRISMA)
5. **Use dual screening** for systematic reviews: two reviewers screen independently, resolve conflicts

---

## Step 5: Citation Chaining

### Backward Citation Chaining (Reference Mining)
- Review the reference lists of your 5-10 most relevant papers
- Identify frequently cited foundational works
- Look for seminal papers that appear in multiple reference lists
- Check if you have missed any key methodological papers

### Forward Citation Chaining (Citation Tracking)
- Use "Cited by" features in Google Scholar, WoS, or Scopus
- Find recent papers that build on key works
- Identify emerging trends and new research directions
- Discover papers using alternative terminology you may have missed

### Snowball Method (Systematic)
1. Start with a set of 3-5 key seed papers
2. Apply backward chaining to all seed papers
3. Apply forward chaining to all seed papers
4. Screen new papers found; add relevant ones to your set
5. Repeat until no new relevant papers are found (saturation)
6. Document each iteration with dates and counts

---

## Step 6: Grey Literature and Supplementary Sources

### Sources to Check
- **Preprint servers**: arXiv, SSRN, TechRxiv, ChinaXiv
- **Dissertations**: ProQuest, CNKI dissertations, institutional repositories
- **Technical reports**: Government agencies (NHTSA, EU publications), standards bodies (ISO, SAE)
- **Conference proceedings not indexed**: Workshop papers, extended abstracts
- **Industry white papers**: From major companies in your field
- **Standards documents**: ISO, IEEE, SAE, GB/T standards

### Conference Search Strategy
- Check proceedings of the top 3-5 conferences in your field
- Look at workshop papers (often more innovative, less polished)
- Review tutorial/survey presentations for comprehensive overviews

---

## Step 7: When to Stop Searching

You have likely achieved search saturation when:
- [ ] Forward and backward citation chaining yields no new relevant papers
- [ ] Multiple databases return the same core set of papers
- [ ] Recent review papers in the field cite the same works you have found
- [ ] Domain experts you consult do not suggest papers you have missed
- [ ] New searches with alternative terms return only papers already in your collection
- [ ] You can clearly articulate what IS and IS NOT covered in the existing literature

---

## Step 8: Document Your Search

### Search Log Template

```markdown
## Search Documentation

### Database: [Name]
- **Date searched**: YYYY-MM-DD
- **Search string**: [exact string used]
- **Filters applied**: [date range, document type, language]
- **Results returned**: [number]
- **After deduplication**: [number]
- **After title/abstract screening**: [number]
- **After full-text screening**: [number]
- **Final included**: [number]
- **Notes**: [observations about coverage, gaps, unexpected findings]
```

### PRISMA Flow Diagram Numbers to Track
- Records identified from each database (with database names)
- Records from other sources (citation chaining, grey literature)
- Records removed before screening (duplicates)
- Records screened (title/abstract)
- Records excluded at screening (with count)
- Reports sought for retrieval
- Reports not retrieved (with reasons)
- Reports assessed for eligibility (full text)
- Reports excluded with reasons (categorized)
- Studies included in final review

---

## Common Pitfalls

1. **Searching only Google Scholar**: Broad but poor reproducibility and limited filtering
2. **Using too many AND operators**: Over-narrowing misses relevant papers
3. **Ignoring non-English literature**: For global topics, include CNKI, J-STAGE, KCI
4. **Not using controlled vocabulary**: MeSH/Thesaurus terms catch papers that keywords miss
5. **Stopping too early**: One round of database searching is rarely sufficient
6. **Not saving search strings**: Without documentation, you cannot reproduce or update
7. **Ignoring grey literature**: Theses, reports, and preprints contain valuable findings
8. **Forgetting to set alerts**: Set database alerts for ongoing awareness
9. **Relying on a single search iteration**: Always refine based on initial results
10. **Not consulting a librarian**: Research librarians are expert search strategists

---

## Paper Discovery Platforms

Beyond traditional databases, these specialized platforms help discover relevant papers through different mechanisms.

### Discovery Tools

| Tool | URL | Discovery Method | Best For |
|------|-----|-----------------|----------|
| **dblp** | dblp.org | Complete CS bibliography; author/venue browsing | Finding all papers by an author or at a venue. No abstracts, but exhaustive metadata for CS. |
| **Semantic Scholar** | semanticscholar.org | AI-powered relevance ranking, TLDR summaries, influence scores | Large-scale discovery with automated paper summaries. Free API for programmatic access. |
| **Papers With Code** | paperswithcode.com | Links papers to code repositories, benchmarks, and leaderboards | Finding implementations, comparing SOTA results on benchmarks. |
| **Paper Digest** | paper-digest.com | AI-generated paper digests and trend reports | Quick summaries of recent papers in specific areas. |
| **Cool Papers** | papers.cool | Curated daily paper recommendations with Chinese summaries | Staying current with trending AI/ML papers; popular in Chinese research community. |
| **Connected Papers** | connectedpapers.com | Visual citation graph from a seed paper | Mapping related work around a specific paper. Free for 5 graphs/month. |
| **ResearchRabbit** | researchrabbit.ai | Continuous recommendation based on your collection | Ongoing discovery; add papers and get recommendations automatically. Integrates with Zotero. |
| **Inciteful** | inciteful.xyz | Network analysis from seed papers | Finding important papers you missed; identifying bridge papers between fields. |
| **Google Scholar** | scholar.google.com | Broad full-text search, citation tracking | Initial exploration, citation chasing, alert setup. |
| **arXiv** | arxiv.org | Preprint repository with daily listings | Accessing cutting-edge work before peer review. |
| **ChinaXiv** | chinaxiv.org | Chinese preprint repository | Chinese-language preprints across disciplines. |

### Connected Papers: Citation Graph Exploration

Connected Papers builds a visual similarity graph around a seed paper. Papers are positioned based on co-citation and bibliographic coupling (not direct citation).

**How to use effectively**:
1. Start with your most relevant seed paper
2. The resulting graph shows papers similar in topic, even if they don't directly cite each other
3. Papers closer together are more similar; paper size indicates citation count
4. Use the "Prior works" tab to find foundational papers
5. Use the "Derivative works" tab to find recent follow-ups
6. Build multiple graphs from different seed papers to cover different angles

**Limitation**: Only indexes papers with DOIs in Semantic Scholar. May miss workshop papers, Chinese-language papers, or very recent preprints.

---

## Search Alert Setup

### Google Scholar Alerts
1. Run your search in Google Scholar
2. Click "Create alert" at the bottom of the results page
3. Enter your email; receive notifications for new matching papers

### Web of Science / Scopus Alerts
1. Run and save your search query
2. Set up email alerts for new results
3. Set frequency to weekly for active topics, monthly for stable fields

### Semantic Scholar Alerts
1. Create an account at semanticscholar.org
2. Set up a Research Feed based on your interests
3. Follow specific authors to get notified of new publications
4. Use the "Research Feed" feature for personalized daily recommendations
5. API access: `api.semanticscholar.org` for programmatic alerts and batch queries

### Papers With Code Alerts
1. Follow specific benchmarks/tasks (e.g., "Object Detection on KITTI")
2. Get notifications when new SOTA results are reported
3. Subscribe to specific topics or methods via the "Subscribe" button

### arXiv Alerts
1. Subscribe to specific categories (e.g., cs.CV, cs.RO, cs.AI)
2. Use arxiv-sanity-lite (arxiv-sanity-lite.com) for personalized arXiv filtering
3. Use daily email digests: set up at arxiv.org/help/subscribe
4. Third-party tools: Arxiv Daily (arxivdaily.com) provides Chinese summaries of trending papers

### RSS / Table of Contents
- Subscribe to TOC alerts for key journals via journal websites
- Use RSS readers (Feedly, Inoreader) to aggregate multiple journal feeds
- Set Google Scholar alerts for key authors in your field
- Use IFTTT or Zapier to route alerts to Slack/WeChat for team awareness

---

## Prompt Templates for Claude

### Generate Search Strategy
```
I am researching [TOPIC] for a [TYPE: systematic review / scoping review / research paper].
My research question is: [QUESTION]

Please help me:
1. Decompose my question into 3-4 searchable concepts
2. Generate synonyms, abbreviations, and related terms for each concept
3. Construct Boolean search strings for Web of Science, Scopus, and [DATABASE]
4. Suggest inclusion/exclusion criteria appropriate for this review type
5. Identify key journals and conferences where relevant work is published
6. Recommend grey literature sources to check
```

### Evaluate and Refine Search Results
```
I searched [DATABASE] with the following string: [SEARCH STRING]
I got [NUMBER] results. Here are the titles of the first 20:
[LIST TITLES]

Please help me:
1. Assess whether the results seem well-targeted for my topic: [TOPIC]
2. Identify terms or concepts I may have missed
3. Suggest refinements to improve precision or recall
4. Flag any results that seem off-topic and suggest exclusion terms
```

### Translate Search Across Databases
```
I have this search string for Web of Science:
[WOS SEARCH STRING]

Please translate this into equivalent searches for:
1. Scopus (using TITLE-ABS-KEY syntax)
2. PubMed (using MeSH terms and [tiab] field tags)
3. IEEE Xplore (using IEEE-compatible syntax)
4. CNKI (using Chinese subject terms)

Preserve the logical structure and adapt controlled vocabulary where possible.
```

### Write Search Methodology for Paper
```
I conducted literature searches across the following:
- Databases: [LIST WITH DATES]
- Search strings: [STRINGS PER DATABASE]
- Filters: [DATE RANGE, LANGUAGE, DOCUMENT TYPES]
- Supplementary methods: [CITATION CHAINING, EXPERT CONSULTATION]
- Results: [NUMBERS AT EACH STAGE]

Please draft a reproducible search methodology paragraph for the Methods section,
following PRISMA 2020 reporting guidelines. Include all details needed for replication.
```
