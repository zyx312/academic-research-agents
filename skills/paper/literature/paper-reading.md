# Paper Reading and Critical Analysis

## Purpose

This skill provides structured methods for reading academic papers efficiently and critically. It covers the three-pass method (Keshav), critical evaluation frameworks, note-taking templates, and strategies adapted for different paper types. The goal is to maximize comprehension while minimizing time spent on irrelevant material.

## Related
- [literature-search.md](literature-search.md) - Find papers to read
- [literature-review.md](literature-review.md) - Synthesize multiple papers
- [reference-management.md](reference-management.md) - Organize what you read

---

## The Three-Pass Method (S. Keshav)

Based on S. Keshav's widely adopted method from "How to Read a Paper" (ACM SIGCOMM, 2007), this approach prevents drowning in details before understanding the big picture.

### Pass 1: Survey (5-10 minutes)

**Goal**: Determine whether the paper deserves a deeper read.

**What to read**:
1. Title, abstract, and keywords
2. Introduction (first and last paragraphs)
3. Section headings (scan all of them)
4. Conclusion
5. References (scan for papers you recognize)

**What to capture after Pass 1**:
- [ ] Category: What type of paper is this? (empirical, theoretical, survey, system design, benchmark)
- [ ] Context: What problem does it address? What field?
- [ ] Contribution claims: What do the authors say is novel?
- [ ] Clarity: Is the paper well-written enough to justify reading further?
- [ ] Relevance: How relevant is this to my current research? (1-5 scale)

**Decision point**: Stop here if the paper is not relevant, or if it is a known area and you only need the contribution summary.

### Pass 2: Comprehension (30-60 minutes)

**Goal**: Understand the paper's content without deep verification.

**How to read**:
1. Read the entire paper, but skip proofs and heavy mathematical derivations
2. Study all figures, diagrams, and tables carefully -- they often contain the core message
3. Mark key references you have not read (for later follow-up)
4. Write brief marginal notes or highlights
5. Pay attention to methodology choices and justifications

**What to capture after Pass 2**:
- [ ] Research question stated precisely
- [ ] Methodology summary (approach, tools, datasets)
- [ ] Key results (quantitative where possible)
- [ ] Main figures/tables and what they show
- [ ] Strengths identified
- [ ] Weaknesses or limitations noted
- [ ] Connections to your own work
- [ ] Unread references to follow up on

**Decision point**: This is sufficient for most papers. Proceed to Pass 3 only for papers critical to your research.

### Pass 3: Reconstruction (3-5 hours)

**Goal**: Deeply understand the paper by virtually recreating it.

**How to read**:
1. Attempt to mentally re-derive key results
2. Challenge every assumption -- ask "what if this assumption is wrong?"
3. Verify the experimental setup: Are controls adequate? Is the evaluation fair?
4. Compare claimed results against the actual data presented
5. Think about how YOU would have solved the same problem differently
6. Identify implicit assumptions the authors may not have stated

**What to capture after Pass 3**:
- [ ] Detailed methodology critique
- [ ] Validity of experimental design
- [ ] Reproducibility assessment (is enough detail provided?)
- [ ] Alternative approaches the authors could have taken
- [ ] Ideas this paper inspires for your own research
- [ ] Specific gaps or follow-up studies needed

---

## Critical Reading Framework

### Evaluating Research Quality

Apply these questions systematically to any empirical paper:

#### 1. Problem and Motivation
- Is the problem clearly defined and significant?
- Is the motivation well-argued?
- Are the research questions/hypotheses stated explicitly?
- Is the scope appropriate (not too narrow, not too broad)?

#### 2. Related Work
- Is the literature review comprehensive and current?
- Do the authors position their work clearly relative to prior work?
- Are important competing approaches discussed fairly?
- Is the gap in knowledge clearly articulated?

#### 3. Methodology
- Is the method appropriate for the research question?
- Are there alternative methods that might be superior?
- Is the sample size / dataset adequate?
- Are variables operationalized clearly?
- Is the experimental design sound (controls, randomization, blinding)?
- Could there be confounding variables?

#### 4. Results and Analysis
- Do the results actually answer the research questions?
- Is the statistical analysis appropriate?
- Are effect sizes reported (not just p-values)?
- Are confidence intervals or error bounds provided?
- Do the figures and tables support the claims?
- Are negative results reported honestly?

#### 5. Discussion and Claims
- Are conclusions supported by the evidence?
- Do authors acknowledge limitations?
- Is there overstatement of results?
- Are alternative explanations considered?
- Is the generalizability discussed realistically?

#### 6. Reproducibility
- Is enough methodological detail provided for replication?
- Is the code/data publicly available?
- Are the experimental conditions fully specified?

---

## Reading Different Paper Types

### Empirical Research Papers
- Focus on: Experimental design, dataset quality, evaluation metrics, statistical tests
- Watch for: Cherry-picked results, unfair baselines, insufficient ablation studies
- Key question: Would these results hold under different conditions?

### Theoretical/Mathematical Papers
- Focus on: Assumptions, theorem conditions, proof strategy, tightness of bounds
- Watch for: Unrealistic assumptions, gaps in proofs, missing edge cases
- Key question: Are the theoretical results practically meaningful?

### Survey / Review Papers
- Focus on: Taxonomy design, completeness of coverage, search methodology
- Watch for: Biased selection of papers, outdated references, missing perspectives
- Key question: Does this survey help me understand the landscape?

### Systems / Design Papers
- Focus on: Architecture decisions, scalability, real-world deployment
- Watch for: Evaluation on toy examples only, missing failure cases
- Key question: Would this system work in practice at scale?

### Benchmark / Dataset Papers
- Focus on: Data collection methodology, annotation quality, bias analysis
- Watch for: Label noise, sampling bias, limited diversity, license restrictions
- Key question: Is this benchmark representative and fair?

### Position / Vision Papers
- Focus on: Clarity of argument, supporting evidence, actionability
- Watch for: Unsupported claims, strawman arguments
- Key question: Is this vision well-argued and achievable?

---

## Speed Reading vs. Deep Reading Strategy

### When to Speed Read (Pass 1 only)
- Broad literature surveys to understand a new field
- Screening search results for relevance
- Staying current with new publications
- Deciding whether to cite a paper

### When to Deep Read (Pass 2+)
- Papers directly related to your research problem
- Papers whose methodology you want to adopt or compare against
- Key references that multiple other papers cite
- Papers you plan to cite extensively

### When to Reconstruct (Pass 3)
- Papers you are building directly upon
- Papers you are reviewing for a journal/conference
- Papers whose claims you want to challenge or extend
- Foundational papers in your specific sub-area

### Triage Strategy for a Set of Papers
1. Export all titles and abstracts from your search results
2. Do Pass 1 on ALL papers: sort into "relevant" / "maybe" / "skip"
3. Do Pass 2 on all "relevant" papers, plus spot-check "maybe" papers
4. Do Pass 3 on the 5-10 most critical papers for your work
5. Track which pass you completed for each paper in your reference manager (use tags)

---

## Note-Taking Templates

### Quick Note Template (Pass 1-2)

```markdown
## [Paper Title] ([Year])
**Authors**: [Names]
**Venue**: [Journal/Conference]
**DOI/URL**: [Link]

### One-Line Summary
[What this paper does in one sentence]

### Problem
[What problem does it solve?]

### Approach
[Key method or idea]

### Key Results
- [Result 1 with numbers]
- [Result 2 with numbers]

### Relevance to My Work
[How does this connect to my research?]

### Tags
#[topic] #[method] #[dataset]
```

### Deep Analysis Template (Pass 3)

```markdown
## [Paper Title] ([Year])
**Authors**: [Names]
**Venue**: [Journal/Conference]
**DOI/URL**: [Link]
**Date Read**: [YYYY-MM-DD]
**Pass Level**: [1/2/3]

### Research Question
[Precise statement of what the paper investigates]

### Motivation
[Why is this problem important? What gap does it address?]

### Methodology
- **Approach**: [Description]
- **Dataset/Setting**: [Details]
- **Baselines**: [What is compared against]
- **Metrics**: [How success is measured]
- **Implementation**: [Tools, frameworks, hardware]

### Key Results
| Metric | Proposed Method | Best Baseline | Improvement |
|--------|----------------|---------------|-------------|
| [M1]   | [value]        | [value]       | [delta]     |

### Strengths
1. [Strength 1]
2. [Strength 2]

### Weaknesses / Limitations
1. [Weakness 1]
2. [Weakness 2]

### Questions / Concerns
- [Question about methodology or results]
- [Assumption that seems questionable]

### Ideas for My Research
- [Idea 1 inspired by this paper]
- [Idea 2 or extension]

### Key References to Follow Up
- [Ref 1]: [reason to read]
- [Ref 2]: [reason to read]

### Notable Quotes
- "[Quote]" (p. X) -- [why it matters]
```

---

## Reading Workflow Integration

### Daily Reading Habit
- Allocate 30-60 minutes daily for paper reading
- Alternate between breadth (Pass 1 on many papers) and depth (Pass 2-3 on few)
- Keep a reading queue in your reference manager with priority tags

### Reading Group Preparation
- For a paper you are presenting: complete Pass 3
- For a paper others are presenting: complete Pass 2
- Prepare 2-3 discussion questions per paper

### Connecting Papers Across a Literature
- After reading 10+ papers, create a concept map linking them
- Identify clusters of papers that share methods, datasets, or assumptions
- Note contradictions between papers -- these often signal research opportunities
- Track chronological evolution of ideas across papers

---

## PDF Reading and Translation Tools

### Translation Tools for Non-English Papers

| Tool | Purpose | Features |
|------|---------|----------|
| **CopyTranslator** | Real-time PDF translation while reading | Copy text from PDF, automatically translates in a floating window. Handles line-break concatenation (removes spurious line breaks from PDF copy). Open-source, GitHub: CopyTranslator/CopyTranslator. |
| **Saladict (沙拉查词)** | Browser-based dictionary and translation popup | Multi-dictionary lookup (Cambridge, Longman, Oxford, Google, DeepL). Hover or double-click for instant translation. Chrome/Firefox extension. Excellent for reading papers in browser-based PDF viewers. |
| **Zotero PDF Translate** | In-Zotero translation for PDF annotations | Translate selected text directly in Zotero's built-in PDF reader. Supports DeepL, Google, Bing, Baidu, and Tencent translation APIs. Install from GitHub: windingwind/zotero-pdf-translate. |
| **DeepL** | High-quality academic translation | Superior to Google Translate for academic text. Desktop app supports drag-and-drop PDF translation. Free tier: 5000 chars/month. |
| **知云文献翻译** | Full-page PDF translation for Chinese researchers | Specifically designed for academic PDFs. Preserves formatting. Desktop app for Windows/Mac. zhiyunwenxian.cn. |

### AI-Powered Paper Reading (gpt_academic style)

Use these prompts for AI-assisted paper comprehension:

#### Paper Summary Prompt
```
Read the following paper abstract and introduction, then provide:
1. A one-paragraph summary of the paper's main contribution
2. The key problem being solved and why it matters
3. The proposed approach in 2-3 sentences
4. The headline quantitative result
5. Three questions I should investigate when reading the full paper

Title: [TITLE]
Abstract: [PASTE ABSTRACT]
Introduction: [PASTE INTRODUCTION]
```

#### Section-by-Section Analysis Prompt
```
I am reading a paper on [TOPIC]. I have just read the [SECTION NAME]
section. Here is the content:

[PASTE SECTION TEXT]

Please help me understand:
1. What is the main point of this section?
2. What are the key assumptions made?
3. Are there any logical gaps or unclear steps?
4. How does this connect to the previous section?
5. What should I pay attention to in the next section?
```

#### Critical Analysis Prompt for Deep Reading
```
I have finished reading this paper and want to critically evaluate it.
Here are my notes:

Title: [TITLE]
Main claim: [CLAIM]
Method: [METHOD SUMMARY]
Key result: [RESULT]
My initial impression: [YOUR THOUGHTS]

Please act as a critical reviewer and help me:
1. Identify 3 strengths that make this paper valuable
2. Identify 3 weaknesses or potential issues
3. List unstated assumptions that could affect validity
4. Suggest 2 experiments that would strengthen or challenge the claims
5. Rate the paper's reproducibility (what is missing for replication?)
6. Identify how this paper could inspire my own research on [YOUR TOPIC]
```

#### Paper Comparison Prompt
```
I have read these two papers that propose different solutions to [PROBLEM]:

Paper A: [TITLE, YEAR] - [ONE-LINE SUMMARY]
Paper B: [TITLE, YEAR] - [ONE-LINE SUMMARY]

Key differences I noticed:
[YOUR OBSERVATIONS]

Please help me create:
1. A structured comparison table (method, data, metrics, results, limitations)
2. Analysis of which approach is stronger and under what conditions
3. Whether the two approaches could be combined
4. What gap remains unaddressed by both papers
```

---

## Common Reading Mistakes

1. **Reading linearly from start to finish**: Always do Pass 1 first to decide priority
2. **Reading without purpose**: Know WHY you are reading each paper before starting
3. **Not taking notes**: You will forget what you read; always capture at least a one-line summary
4. **Accepting claims uncritically**: Every paper has limitations; your job is to find them
5. **Reading too many papers superficially**: Better to deeply understand 10 key papers than skim 100
6. **Ignoring figures and tables**: These often communicate results more efficiently than text
7. **Not tracking what you have read**: Use tags in your reference manager (read/unread/pass-level)
8. **Reading alone**: Discussing papers with colleagues deepens understanding

---

## Prompt Templates for Claude

### Summarize a Paper
```
I have read the following paper and want help organizing my notes.

Title: [TITLE]
Authors: [AUTHORS]
Venue: [VENUE], Year: [YEAR]
Abstract: [PASTE ABSTRACT]

Please help me create a structured summary covering:
1. Research question and motivation
2. Methodology (approach, dataset, metrics)
3. Key results (quantitative where possible)
4. Main contributions claimed by the authors
5. Potential limitations I should investigate further
```

### Critical Analysis
```
I am doing a deep critical reading of this paper:
[TITLE, AUTHORS, VENUE]

Here is my understanding of the methodology: [YOUR SUMMARY]
Here are the key claims: [LIST CLAIMS]

Please help me critically evaluate:
1. Are the methodology choices well-justified?
2. What assumptions are being made (stated and unstated)?
3. Are there alternative approaches the authors should have considered?
4. Do the results convincingly support the claims?
5. What are the main threats to validity?
6. What follow-up experiments would strengthen or challenge these findings?
```

### Compare Multiple Papers
```
I have read these papers on [TOPIC]:
1. [Paper 1: Title, Authors, Year] - [one-line summary]
2. [Paper 2: Title, Authors, Year] - [one-line summary]
3. [Paper 3: Title, Authors, Year] - [one-line summary]

Please help me create a comparison covering:
1. A table comparing their methods, datasets, and key results
2. Points of agreement across the papers
3. Contradictions or disagreements between them
4. Gaps that none of them address
5. How they build on each other chronologically
```

### Extract Research Gaps
```
Based on my reading of [NUMBER] papers on [TOPIC], here are the common themes:
[LIST THEMES]

And here are the common limitations reported:
[LIST LIMITATIONS]

Please help me identify:
1. Research gaps that multiple papers acknowledge
2. Methodological limitations that represent opportunities
3. Under-explored combinations of existing approaches
4. Practical problems that the literature has not addressed
```

### Prepare Reading Group Discussion
```
I am presenting this paper at our lab reading group:
Title: [TITLE]
Main contribution: [SUMMARY]
Key method: [METHOD]

Please help me prepare:
1. A 5-minute verbal summary of the paper
2. 3 strengths to highlight
3. 3 weaknesses or limitations to discuss
4. 5 discussion questions for the group (ranging from clarification to big-picture)
5. 2-3 related papers the group might want to read next
```
