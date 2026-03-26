# Research Direction Selection Guide

## Purpose

This skill provides systematic frameworks for identifying, evaluating, and
committing to a research direction. It covers gap identification, trend analysis,
feasibility assessment, and the decision process for both students choosing a
topic and advisors shaping their group's research portfolio.

---

## 1. Gap Identification Frameworks

### The Five Types of Research Gaps

Understanding what kind of gap you are targeting clarifies the contribution:

| Gap Type | Definition | Example |
|----------|-----------|---------|
| **Empirical gap** | Insufficient data or evidence on a topic | No large-scale study of X in population Y |
| **Methodological gap** | Existing methods inadequate for the problem | Current approaches cannot handle real-time constraints |
| **Theoretical gap** | Missing or incomplete theoretical framework | No formal model explaining relationship between A and B |
| **Population gap** | Under-represented group or context | Most studies focus on highways; urban intersections understudied |
| **Conflict gap** | Contradictory findings in existing literature | Study A shows positive effect, Study B shows negative |

### Systematic Gap Identification Process

```
Step 1: Survey the landscape
  - Read 3-5 recent survey papers in target area
  - Note the "future work" sections of each
  - Identify recurring open questions

Step 2: Map the existing work
  - Create a taxonomy of approaches (method vs domain matrix)
  - Identify empty cells in the matrix = potential gaps
  - Note which cells have only 1-2 papers = under-explored

Step 3: Check the "limitations" sections
  - Read limitations of top 20 cited papers
  - Group limitations by theme
  - Prioritize limitations that multiple papers share

Step 4: Consult with practitioners
  - Talk to industry contacts about unsolved problems
  - Attend industry workshops and panels
  - Read standards documents for unresolved technical issues

Step 5: Validate the gap
  - Search thoroughly to confirm no one has addressed it
  - Check preprints (arXiv, SSRN) and recent conference proceedings
  - Ask senior colleagues if they know of ongoing unpublished work
```

---

## 2. Trend Analysis Methods

### Bibliometric Analysis

Use quantitative tools to identify emerging topics and shifting research fronts.

**Tools and Platforms:**
- **Google Scholar Trends:** Track citation growth for key terms
- **Scopus / Web of Science:** Analyze publication volume over time
- **VOSviewer:** Visualize co-citation and keyword co-occurrence networks
- **Connected Papers:** Explore the citation graph around a seed paper
- **Semantic Scholar:** Use AI-powered paper recommendations
- **CiteSpace:** Detect emerging research fronts and knowledge clusters

**Key Metrics to Track:**
- Publication count per year for target keywords
- Citation acceleration (papers gaining citations faster than peers)
- New author entry rate (are new researchers entering this area?)
- Funding trends (which agencies are funding this topic?)
- Patent filings (indicator of commercial interest)

### Conference and Workshop Signals

- **New workshops** at top conferences indicate emerging sub-fields
- **Invited talk topics** reflect what the community considers important
- **Best paper awards** signal valued directions
- **Tutorial topics** indicate areas reaching enough maturity to teach
- **Industry sponsor interests** at conferences reveal applied demand

### Qualitative Trend Assessment

1. **Regulatory drivers:** New regulations create research needs
   (e.g., EU AI Act driving explainability research; China's SOTIF standard)
2. **Technology enablers:** New hardware/software enabling previously
   impossible research (e.g., foundation models enabling new applications)
3. **Societal needs:** Pressing problems attracting funding
   (e.g., autonomous driving safety, climate-related engineering)
4. **Cross-disciplinary convergence:** When two fields start citing each
   other heavily, the intersection becomes a fertile area

---

## 3. Balancing Novelty with Feasibility

### The Novelty-Feasibility Matrix

```
                    High Novelty
                         |
        "Moonshot"       |       "Sweet Spot"
     (high risk,         |     (novel and doable,
      may not finish)    |      ideal for PhD)
                         |
   ----------------------+---------------------- High Feasibility
                         |
     "Avoid"             |       "Safe Bet"
   (neither new          |     (doable but may
    nor practical)       |      lack novelty)
                         |
                    Low Novelty
```

### Feasibility Checklist

Before committing to a direction, verify each item:

- [ ] **Data availability:** Can you obtain the necessary data within 3 months?
- [ ] **Computational resources:** Do you have access to required hardware (GPU, HPC)?
- [ ] **Skills match:** Does the team have (or can quickly learn) needed skills?
- [ ] **Tool maturity:** Are required software tools stable and documented?
- [ ] **Collaboration access:** If external partners needed, are they committed?
- [ ] **Ethical clearance:** Can IRB/ethics approval be obtained in time?
- [ ] **Time estimate:** Is completion realistic within the degree timeline?
- [ ] **Backup plan:** If the main approach fails, is there a viable Plan B?

### Novelty Assessment Questions

- Does this specific combination of method + domain + data exist in the literature?
- Would a knowledgeable reviewer say "this is interesting and I have not seen it"?
- Can you articulate the contribution in one sentence?
- Is there at least one venue where this would be considered a contribution?

---

## 4. Using Bibliometric Tools Effectively

### VOSviewer Workflow

```
1. Export search results from Scopus/WoS (include abstracts, keywords, references)
2. Import into VOSviewer
3. Generate co-occurrence map of author keywords
   - Clusters reveal research themes
   - Bridge nodes between clusters = interdisciplinary opportunities
4. Generate citation network
   - Identify the most influential works
   - Find recent papers not yet highly cited but in growing clusters
5. Analyze temporal overlay
   - Color nodes by publication year
   - Newer clusters = emerging topics
```

### Connected Papers Workflow

```
1. Start with a key paper in your area of interest
2. Examine "prior work" graph for foundational papers you may have missed
3. Examine "derivative work" graph for recent extensions
4. Look for clusters of recent papers diverging from the main trajectory
   - These represent new sub-directions
5. Repeat with 3-5 seed papers to get a comprehensive map
```

### Research Discovery and Trend Analysis Tools

Beyond traditional bibliometric software, several modern tools enable more
effective research direction discovery:

**Connected Papers (connectedpapers.com)**
- Builds a visual graph of papers related to a seed paper.
- Uses co-citation and bibliographic coupling (not just direct citations).
- Reveals the landscape of related work around any paper.
- Particularly useful for students entering a new sub-field: start with
  one key paper and explore the graph to find the foundational and frontier works.
- Free tier allows 5 graphs per month; sufficient for most research planning.

**Iris.ai**
- AI-powered research exploration tool.
- Input a paper abstract or research question and get a map of related papers.
- Uses semantic similarity rather than citation links, finding conceptually
  related work that might not cite each other.
- Useful for identifying cross-disciplinary connections and unexpected
  related work in adjacent fields.

**Papers With Code (paperswithcode.com)**
- Links papers to their code implementations and benchmark results.
- Essential for computational research: quickly assess which methods have
  reproducible implementations and how they compare on standard benchmarks.
- Trend analysis: track which methods are gaining traction by watching
  benchmark leaderboards over time.
- Identify research gaps: methods with high performance but no code, or
  benchmarks where performance has plateaued (indicating need for new approaches).

**VOSviewer (vosviewer.com)**
- Free software for constructing and visualizing bibliometric networks.
- Creates co-authorship, co-citation, and keyword co-occurrence maps.
- Workflow: Export data from Scopus/WoS, import into VOSviewer, generate
  network visualizations that reveal research clusters and bridges.
- Temporal overlay shows which topics are emerging vs. declining.
- Essential for literature review sections of proposals and dissertations.

**CiteSpace**
- Developed specifically for detecting emerging research trends.
- Identifies burst keywords (terms that suddenly increase in frequency),
  which signal emerging hot topics.
- Creates timeline visualizations showing how research fronts evolve.
- Particularly popular in Chinese academic circles for bibliometric analysis.
- Complements VOSviewer with different analytical perspectives.

**Semantic Scholar (semanticscholar.org)**
- AI-powered citation context analysis distinguishes influential citations
  from incidental ones.
- Citation velocity metric shows which papers are gaining citations fastest.
- TLDR feature provides one-sentence paper summaries for rapid screening.
- Free API access enables systematic bibliometric analysis (see example below).

### Semantic Scholar API for Systematic Analysis

```python
# Example: Track publication trends for a topic
import requests

def get_publication_count(query, year_start, year_end):
    """Count papers per year for a search query."""
    results = {}
    for year in range(year_start, year_end + 1):
        url = "https://api.semanticscholar.org/graph/v1/paper/search"
        params = {"query": query, "year": f"{year}-{year}", "limit": 1}
        response = requests.get(url, params=params)
        data = response.json()
        results[year] = data.get("total", 0)
    return results
```

---

## 5. Advisor-Student Alignment

### Aligning Student Interest with Advisor Expertise

The ideal research direction sits at the intersection of:

1. **Student passion:** What excites the student intellectually?
2. **Advisor expertise:** Where can the advisor provide deep guidance?
3. **Funding alignment:** What does the advisor's grant support?
4. **Career relevance:** Will this help the student's next career step?

### Negotiation Framework

When student and advisor interests diverge:

```
1. Map overlap explicitly
   - Student lists top 5 interests
   - Advisor lists top 5 fundable/publishable directions
   - Identify intersections

2. Evaluate compromise options
   - Can the student's interest be framed as a sub-problem of the advisor's project?
   - Can the advisor's project benefit from the student's unique perspective?

3. Consider co-advising
   - If no overlap exists, find a second advisor who bridges the gap
   - Define clear roles: who supervises what aspects

4. Set expectations clearly
   - Advisor may provide less technical guidance on unfamiliar topics
   - Student may need to be more self-directed
   - Both must agree on this arrangement before committing
```

---

## 6. Pivoting Research Direction

### When to Consider a Pivot

- **Data problems:** Required data is unavailable, too noisy, or too small
- **Method failure:** Core approach does not work after reasonable effort (3+ months)
- **Scooped:** Another group publishes very similar work
- **Loss of interest:** Student dreads working on the topic (sustained, not temporary)
- **External changes:** Regulations, technology shifts, or funding changes

### How to Pivot Gracefully

```
1. Assess salvage value
   - What parts of the current work can transfer to a new direction?
   - Literature review? Data collection? Tool development? Skills gained?

2. Define the new direction
   - Apply the same gap identification process (abbreviated version)
   - Must be more feasible than the original to justify the lost time

3. Reset the timeline
   - Estimate remaining time realistically
   - Scope the new direction to fit available time

4. Communicate with stakeholders
   - Inform committee, funding agency if applicable
   - Reframe as "refined focus" rather than "failure"

5. Document lessons learned
   - Write up why the original direction did not work
   - This can become a section in the thesis (negative results have value)
```

---

## 7. Validation Checklist Before Committing

Use this checklist before finalizing a research direction:

### Intellectual Validation
- [ ] The research question is clearly articulated in one sentence
- [ ] The gap has been confirmed through thorough literature search
- [ ] At least 2 senior researchers agree this is a worthwhile direction
- [ ] The expected contribution type is identified (empirical, methodological, theoretical)
- [ ] At least 2 target publication venues are identified

### Practical Validation
- [ ] Data or experimental subjects are accessible
- [ ] Required tools and infrastructure are available or obtainable
- [ ] The team has the necessary skills or a plan to acquire them
- [ ] Budget is sufficient for the planned work
- [ ] Timeline is realistic with buffer for setbacks

### Strategic Validation
- [ ] This direction aligns with funding and group goals
- [ ] The work will advance the student's career
- [ ] Results (positive or negative) will be publishable
- [ ] The direction has room for extension (follow-up work)
- [ ] The work is differentiated from close competitors

---

## 8. Building on Existing Strengths

### Skills Inventory Assessment

Before choosing a direction, map the research group's current capabilities:

```
Technical Skills:
  - Programming languages: ___
  - ML/AI frameworks: ___
  - Domain-specific tools: ___
  - Statistical analysis: ___
  - Hardware/lab equipment: ___

Domain Knowledge:
  - Primary domain expertise: ___
  - Secondary domains: ___
  - Industry connections: ___
  - Dataset access: ___

Research Infrastructure:
  - Computing resources (GPU cluster, cloud credits): ___
  - Lab facilities: ___
  - Collaboration networks: ___
  - Funding status and duration: ___
```

### Leverage Strategy

- **Extend:** Apply existing tools to new problems
- **Combine:** Merge two strengths to create a unique niche
- **Deepen:** Push existing work to a new level of rigor or scale
- **Transfer:** Apply domain knowledge to an adjacent field

The best research directions often emerge from combining two existing strengths
of the group in a way that no competitor can easily replicate.

---

## Claude Prompt Templates

### Research Gap Analysis

```
You are a research advisor helping identify gaps in a field.

Field: [FIELD, e.g., autonomous driving safety]
Sub-area: [SUB-AREA, e.g., safety of the intended functionality (SOTIF)]
Recent key papers: [LIST 5-10 RECENT PAPERS WITH TITLES]
Known challenges: [LIST KNOWN OPEN PROBLEMS]

Perform a systematic gap analysis:
1. Categorize each paper's contribution type (empirical, methodological, theoretical)
2. Identify what each paper's "future work" section suggests
3. Find common limitations across papers
4. Identify under-explored combinations of methods and domains
5. Suggest 5 specific research gaps ranked by novelty and feasibility
6. For each gap, explain why it matters and what a study addressing it would look like
```

### Trend Analysis Report

```
Generate a trend analysis for a research area.

Research area: [AREA]
Time period: Last [N] years
Target audience: [PhD student / faculty planning / grant proposal]

Cover:
1. Publication volume trends (growing, stable, declining)
2. Key emerging sub-topics (appeared in last 2-3 years)
3. Dominant methodological approaches and shifts
4. Major datasets and benchmarks driving the field
5. Funding landscape (which agencies, which countries)
6. Industry involvement (companies publishing, hiring, deploying)
7. Regulatory developments affecting research priorities
8. Prediction: what will be the top 3 topics in 2-3 years and why?
```

### Direction Comparison

```
Help me compare two potential research directions.

Direction A: [DESCRIPTION]
Direction B: [DESCRIPTION]

Student profile:
- Skills: [SKILLS]
- Career goal: [INDUSTRY / ACADEMIA]
- Time remaining: [MONTHS]
- Advisor expertise: [AREAS]

Compare on these dimensions:
1. Novelty (how differentiated from existing work?)
2. Feasibility (can it be completed in the available time?)
3. Publication potential (which venues, how competitive?)
4. Career value (how will it position the student?)
5. Advisor alignment (how much guidance can the advisor provide?)
6. Risk level (what could go wrong?)
7. Resource requirements (data, compute, collaborators)

Recommend one direction with a clear justification, or suggest a hybrid approach.
```

### Research Positioning Statement

```
Help me write a research positioning statement for a new project.

Research topic: [TOPIC]
Key related works: [LIST 5-8 PAPERS]
Proposed approach: [BRIEF DESCRIPTION]
Expected contribution: [WHAT IS NEW]

Draft a 300-word positioning statement that:
1. Opens with the broader problem and its importance
2. Summarizes what existing work has achieved
3. Identifies the specific gap this work addresses
4. States how the proposed approach differs from prior work
5. Articulates the expected contribution clearly
6. Ends with the potential impact of the work

This will be used in the thesis proposal or grant application introduction.
```
