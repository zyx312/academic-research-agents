# Conference Paper Writing

## Purpose

This skill provides a comprehensive guide to writing, formatting, and submitting conference papers. It covers strategy for different page limits, structuring preliminary results, navigating the conference submission process, camera-ready preparation, and converting conference work into journal publications.

## Related
- [research-paper.md](research-paper.md) - General paper writing
- [cover-letter.md](cover-letter.md) - Submission letters
- [rebuttal.md](rebuttal.md) - Respond to reviews
- [revision.md](revision.md) - Post-review revision

---

## Conference vs. Journal Papers: Strategic Differences

| Aspect | Conference Paper | Journal Paper |
|--------|-----------------|---------------|
| **Timeline** | Fixed deadline, fast turnaround | Rolling submission, slower review |
| **Length** | 4-12 pages (strict limits) | 15-30+ pages (flexible) |
| **Review rounds** | Usually one round | Multiple revision rounds |
| **Scope** | Focused contribution, preliminary OK | Comprehensive, thoroughly validated |
| **Novelty** | Ideas can be early-stage | Expected to be mature and complete |
| **Presentation** | Paper + talk/poster required | Paper only |
| **Visibility** | Immediate community exposure | Indexed, long-term reference |
| **Acceptance rate** | Top venues: 15-25% | Varies widely |

### When to Target a Conference
- You have a novel idea with promising preliminary results
- You want fast feedback from the community
- The conference is the premier venue in your sub-field
- You need a publication for a deadline (graduation, tenure, grant)
- You want networking opportunities at the event

### When to Go Directly to a Journal
- You have comprehensive results with thorough evaluation
- The work does not fit standard conference page limits
- Your field values journal publications more (varies by discipline)
- You need detailed methods/proofs that require space

---

## Understanding Page Limits

### Common Conference Formats

| Format | Typical Venues | Strategy |
|--------|---------------|----------|
| **4-page short paper** | Workshop papers, IEEE ITSC short | One focused contribution, 1-2 experiments |
| **6-page paper** | IEEE conferences (IV, ITSC) | Core contribution + key evaluation |
| **8-page paper** | ACM conferences, AAAI | Full methodology + solid evaluation |
| **10-page paper** | NeurIPS, ICML, ICLR | Detailed method + comprehensive experiments |
| **12-14 page paper** | CVPR, ECCV, some IEEE | Full paper with supplementary material |

### Page Budget Allocation

#### 6-Page Paper (IEEE format, double-column)

| Section | Pages | Content Priority |
|---------|-------|-----------------|
| Abstract | 0.15 | Problem, method, key result, impact |
| Introduction | 0.85 | Motivation, contribution list, paper structure |
| Related Work | 0.75 | Position your work, not a full survey |
| Methodology | 1.5-2.0 | Core contribution -- this gets the most space |
| Experiments | 1.5-2.0 | Setup, results, analysis, ablation |
| Conclusion | 0.25 | Summary, limitations, future work |
| References | 0.5 | ~20-30 references for a 6-page paper |

#### 4-Page Short Paper

| Section | Pages | Content Priority |
|---------|-------|-----------------|
| Abstract | 0.15 | Ultra-concise: problem + result |
| Introduction | 0.6 | Motivation + contributions (combined) |
| Related Work | 0.25 | Brief positioning only (or merge into intro) |
| Methodology | 1.0-1.25 | Focused on the novel element |
| Experiments | 1.0-1.25 | Most important results only |
| Conclusion | 0.15 | 3-4 sentences |
| References | 0.5 | ~15-20 references |

#### 8-10 Page Paper (Single-column, NeurIPS-style)

| Section | Pages | Content Priority |
|---------|-------|-----------------|
| Abstract | 0.25 | Comprehensive summary |
| Introduction | 1.0-1.5 | Full motivation, clear gap, contributions |
| Related Work | 1.0-1.5 | Thorough positioning |
| Methodology | 2.5-3.0 | Complete technical description |
| Experiments | 2.5-3.0 | Comprehensive evaluation + ablations |
| Conclusion | 0.5 | Summary, limitations, future directions |
| References | 1.0+ | ~30-50 references |

---

## Writing Each Section

### Title
- Be specific and descriptive (readers scan titles to decide relevance)
- Include key method AND application/domain
- Avoid vague words: "novel," "efficient," "improved" (unless quantified)
- Keep under 15 words for most conferences
- Good: "LiDAR-Camera Fusion for Robust Pedestrian Detection in Adverse Weather"
- Weak: "A Novel Approach to Improve Object Detection"

### Abstract (150-250 words)
Follow this four-sentence structure:
1. **Context**: What is the problem and why does it matter?
2. **Gap**: What is missing in current approaches?
3. **Method**: What do you propose? (one sentence capturing the key idea)
4. **Results**: What did you achieve? (quantitative: "improves X by Y% on dataset Z")

### Introduction
Structure for maximum impact:
1. **Opening hook**: Broad significance of the problem (2-3 sentences)
2. **Narrow the focus**: Specific sub-problem you address (2-3 sentences)
3. **Gap statement**: What existing work fails to do (2-3 sentences)
4. **Your approach**: What you propose and why it works (3-4 sentences)
5. **Contributions**: Bulleted list (typically 3-4 items):
   - "We propose [method/framework] that [key advantage]"
   - "We demonstrate [result] on [dataset/benchmark]"
   - "We release [code/dataset] to enable reproducibility"
6. **Paper organization**: "The rest of this paper is organized as follows..." (optional for short papers)

### Related Work
- Organize by theme/approach, NOT chronologically
- Use topic sentences: "Simulation-based approaches include..." "Data-driven methods have..."
- Explicitly state how your work differs from the most similar papers
- Be fair to competitors -- reviewers may be the authors of those papers
- For short papers: merge into Introduction or keep to 0.5 pages

### Methodology
- Start with a system/method overview (often with an architecture figure)
- Use consistent notation throughout -- define every symbol
- Present the method logically (not in the order you developed it)
- Highlight what is novel vs. what is standard/borrowed
- Include enough detail for reproduction
- Use equations sparingly in short papers -- prioritize intuition

### Experiments
Structure:
1. **Experimental setup**: Datasets, metrics, baselines, implementation details
2. **Main results**: Compare against baselines in a table
3. **Analysis**: Discuss WHY your method works (not just that it does)
4. **Ablation study**: Show that each component contributes
5. **Qualitative examples**: Visualizations that demonstrate strengths (and honest failures)

Key principles:
- Use standard benchmarks and metrics for your field
- Compare against recent, competitive baselines (not just old/weak ones)
- Report statistical significance or variance when possible
- Include failure cases to show honest limitations
- Hardware/compute requirements for reproducibility

### Conclusion
- Summarize contributions (do not just repeat the abstract)
- State limitations honestly (reviewers respect this)
- Mention concrete future work directions
- Do NOT introduce new information or results

---

## Space-Saving Techniques

When you are over the page limit:

### Text Compression
- Eliminate redundancy between sections (intro/conclusion overlap is common)
- Use active voice ("We propose" not "A method is proposed by us")
- Combine short paragraphs that discuss related points
- Remove hedging language ("It is worth noting that" -> cut entirely)
- Use abbreviations after first definition

### Visual Optimization
- Combine multiple small figures into one composite figure
- Use subfigures instead of separate figures
- Reduce figure margins and padding
- Move large tables to a compact format (or to supplementary)
- Use `\vspace{-Xpt}` sparingly to reduce whitespace in LaTeX

### Structural Compression
- Merge Related Work into the Introduction
- Move implementation details to supplementary material
- Put additional experiments in supplementary material
- Reduce the number of baselines to the most relevant ones
- Use footnotes for minor clarifications instead of full sentences

### LaTeX-Specific Tricks
```latex
% Reduce space around equations
\setlength{\abovedisplayskip}{4pt}
\setlength{\belowdisplayskip}{4pt}

% Reduce space between caption and figure
\setlength{\abovecaptionskip}{4pt}
\setlength{\belowcaptionskip}{-4pt}

% Reduce bibliography font size (check if allowed)
{\small \bibliographystyle{IEEEtran} \bibliography{refs}}

% Use \textsc or \small for table content
```

**Warning**: Do NOT violate formatting rules (font size, margins, line spacing). Reviewers and organizers will desk-reject papers that violate templates.

---

## Submission Strategy

### Pre-Submission Checklist

- [ ] Paper follows the official conference template exactly
- [ ] Page limit is met (including references unless unlimited)
- [ ] Author names and affiliations are correct (check anonymity requirements)
- [ ] Abstract is within word limit
- [ ] All figures are readable when printed in black and white (if required)
- [ ] All references are complete (no "?" in LaTeX output)
- [ ] Paper is spell-checked and proofread
- [ ] Supplementary material is prepared (if allowed)
- [ ] Code/data are anonymized (if double-blind)
- [ ] Conflict-of-interest declarations are accurate
- [ ] Paper has been reviewed by at least one co-author

### Double-Blind Submission Rules
- Remove author names and affiliations from the paper
- Do not include acknowledgments (or anonymize them)
- Use third-person when citing your own prior work: "Zhang et al. [15] showed..." not "In our prior work [15]..."
- Anonymize any shared code/dataset links
- Do not include institution logos or project names that identify you
- Remove metadata from PDF properties

### Submission Platform Tips
- Create your account and register the paper (title/abstract) early
- Upload a draft version well before the deadline
- Most platforms allow unlimited re-uploads until the deadline
- The server WILL be slow in the final hours -- do not wait
- Keep a local copy with timestamps in case of platform issues

---

## Camera-Ready Preparation

After acceptance, prepare the final version:

### Camera-Ready Checklist

- [ ] Address all reviewer comments (even for accepted papers)
- [ ] Add author names and affiliations back (if double-blind)
- [ ] Add acknowledgments (funding, computing resources)
- [ ] Complete the copyright form (IEEE, ACM, etc.)
- [ ] Verify page limit for camera-ready (may differ from submission)
- [ ] Ensure all fonts are embedded in the PDF
- [ ] Check that the PDF meets the conference's PDF specifications
- [ ] Register at least one author for the conference (required for publication)
- [ ] Upload by the camera-ready deadline (no extensions typically)

### IEEE PDF Express / ACM Rights
- For IEEE conferences: submit PDF to IEEE PDF eXpress for validation
- For ACM conferences: complete the ACM rights form and add the correct copyright notice
- Common PDF issues: missing fonts, wrong page size, metadata problems

---

## Converting Conference Paper to Journal Paper

### The 30% Rule
Most journals require that a journal version contains at least 30% new content beyond the conference paper. Some venues require 50% or more.

### What Counts as New Content
- Extended methodology with additional technical details
- New experiments, datasets, or evaluation metrics
- Extended ablation studies and analysis
- Additional baselines and comparisons
- Deeper theoretical analysis or proofs
- New application scenarios or case studies
- Extended related work and discussion

### What Does NOT Count
- Reformatting the same content to fill more pages
- Adding text without substance
- Simply expanding the writing style

### Conversion Strategy
1. Start with the conference paper as a skeleton
2. Add a comprehensive Related Work section
3. Expand methodology with full details, derivations, and intuitions
4. Add 2-3 new experiments or significantly extend existing ones
5. Include deeper analysis (error analysis, parameter sensitivity, runtime)
6. Expand Discussion with broader implications and limitations
7. Cite the conference paper explicitly: "This paper extends our preliminary work [X]"

### Disclosure Requirements
- Always disclose the conference paper in your journal cover letter
- Cite the conference paper in your journal paper
- Some journals require you to submit the conference paper alongside the journal manuscript
- Check journal policy: some do not accept extended conference papers

---

## Conference Deadline Tracking Tools

### Deadline Aggregators

| Tool | URL | Features |
|------|-----|----------|
| **ccfddl.github.io** | ccfddl.github.io | CCF-recommended conference deadlines. Filter by CCF rank (A/B/C), category (AI, networks, security, etc.). Supports calendar subscription (iCal). The de facto standard for Chinese CS researchers. |
| **aideadlin.es** | aideadlin.es | AI/ML conference deadlines with countdown timers. Color-coded by sub-field (CV, NLP, ML, robotics). Export to Google Calendar. |
| **WikiCFP** | wikicfp.com | Broader coverage including workshops and symposia. User-submitted, so verify dates independently. |
| **Conference Partner** | myhuiban.com | Chinese platform (会伴) with conference rankings, past acceptance rates, and reviewer experience sharing. |

### CCF Ranking System (中国计算机学会推荐)

The China Computer Federation (CCF) ranks conferences and journals into three tiers. Understanding CCF rankings is essential for Chinese academic evaluation.

| Rank | Meaning | Examples (AI/CV) | Examples (Systems) |
|------|---------|-----------------|-------------------|
| **CCF-A** | Top-tier, internationally leading | CVPR, NeurIPS, ICML, ICLR, AAAI, IJCAI, ACM MM | OSDI, SOSP, SIGCOMM, MOBICOM |
| **CCF-B** | High-quality, internationally well-known | ECCV, ICCV (note: ICCV is A since 2022 list), COLT, ECML | SenSys, Middleware, ICDCS |
| **CCF-C** | Recognized international conferences | ACCV, BMVC, WACV, AISTATS | HotOS, LCTES |

**Important notes**:
- The CCF list is updated periodically (latest update: check ccf.org.cn)
- Some universities and funding agencies have their own ranking lists that may differ
- For automotive/ITS researchers: IEEE IV is CCF-C; IEEE ITSC is not on the CCF list
- Always verify the current ranking at ccf.org.cn/Academic-Evaluation

### arxiv-latex-cleaner for Submission Preparation

Before submitting to arXiv or conference systems, clean your LaTeX source:

```bash
# Install
pip install arxiv-latex-cleaner

# Basic usage: creates a cleaned copy of your project
arxiv_latex_cleaner /path/to/your/paper/

# Common options
arxiv_latex_cleaner /path/to/paper/ \
  --remove_todo_comments \          # Strip TODO/FIXME comments
  --resize_images \                 # Compress images to reduce upload size
  --im_size 500 \                   # Max image dimension in pixels
  --compress_pdf \                  # Compress embedded PDFs
  --commands_to_delete '\todo'      # Remove specific custom commands
```

**What it does**:
- Removes all comments (including `%TODO`, `\todo{}`)
- Strips unused `.tex`, `.bib`, and image files
- Flattens `\input{}` and `\include{}` into a single file
- Optionally resizes images to reduce file size (arXiv has a 50MB limit)
- Removes auxiliary files (`.aux`, `.log`, `.synctex`)

### Additional LaTeX Space-Saving Tricks

```latex
% Reduce space between items in lists
\usepackage{enumitem}
\setlist{nosep}  % or \setlist{itemsep=1pt, parsep=0pt}

% Reduce space around section headings
\usepackage{titlesec}
\titlespacing*{\section}{0pt}{6pt}{3pt}
\titlespacing*{\subsection}{0pt}{4pt}{2pt}

% Compact bibliography (IEEEtran)
\bibliographystyle{IEEEtran}
{\footnotesize \bibliography{refs}}

% Reduce space between columns in two-column layout
\setlength{\columnsep}{0.2in}  % default is usually 0.25in

% Shrink table text without changing column structure
\begin{table}
\centering
\footnotesize  % or \scriptsize for more aggressive shrinking
\begin{tabular}{...}
...
\end{tabular}
\end{table}

% Use booktabs for professional tables with less vertical space
\usepackage{booktabs}
% \toprule, \midrule, \bottomrule instead of \hline

% Reduce vertical space around figures
\setlength{\textfloatsep}{6pt plus 2pt minus 2pt}
\setlength{\floatsep}{6pt plus 2pt minus 2pt}
\setlength{\intextsep}{6pt plus 2pt minus 2pt}

% Force figures to appear where you want them
\usepackage{float}
\begin{figure}[H]  % Exact placement
```

---

## Common Pitfalls

1. **Submitting to the wrong venue**: Match your contribution to the conference scope
2. **Violating the template**: Desk rejection for wrong fonts, margins, or column format
3. **Missing the deadline**: The submission server closes at the exact deadline
4. **Overselling results**: Reviewers penalize overclaiming more than modest claims
5. **Ignoring reviewer suggestions post-acceptance**: Camera-ready should address feedback
6. **Forgetting to register**: Unregistered papers are dropped from proceedings
7. **Weak baselines**: Compare against the current state-of-the-art, not outdated methods
8. **No ablation study**: Reviewers need to see that each component matters
9. **Poor figures**: Low-resolution, hard-to-read, or non-informative figures hurt perception
10. **Identical submission to multiple venues**: Dual submission is a serious ethical violation

---

## Prompt Templates for Claude

### Draft Conference Paper Structure
```
I am writing a [LENGTH]-page paper for [CONFERENCE NAME] on [TOPIC].
My key contribution is: [DESCRIPTION]
My results show: [SUMMARY OF RESULTS]

Please help me:
1. Propose a page budget allocation for each section
2. Draft an outline with subsection headings
3. Write a contribution list (3-4 bullet points)
4. Suggest what to include vs. move to supplementary material
5. Recommend the most impactful way to present my results
```

### Compress Paper to Fit Page Limit
```
My paper is currently [X] pages and needs to fit in [Y] pages for [CONFERENCE].

Here is the current structure with approximate lengths:
[LIST SECTIONS WITH PAGE COUNTS]

Please suggest:
1. Which content can be cut without losing the core message
2. Which content should move to supplementary material
3. Specific text compression techniques for each section
4. Whether any sections can be merged
5. LaTeX formatting adjustments that save space (within rules)
```

### Write Abstract for Conference Paper
```
Title: [TITLE]
Conference: [NAME] (abstract limit: [WORD COUNT] words)
Problem: [WHAT PROBLEM DO YOU SOLVE]
Method: [WHAT IS YOUR APPROACH]
Key results: [QUANTITATIVE RESULTS]
Significance: [WHY IT MATTERS]

Please draft a concise abstract following the structure:
1. Context/Problem (1-2 sentences)
2. Gap/Challenge (1 sentence)
3. Proposed approach (1-2 sentences)
4. Key results with numbers (1-2 sentences)
5. Impact/significance (1 sentence)
```

### Prepare Rebuttal for Conference Reviews
```
I received the following reviews for my paper submitted to [CONFERENCE]:

Reviewer 1 (Score: [X]):
[KEY COMMENTS]

Reviewer 2 (Score: [X]):
[KEY COMMENTS]

Reviewer 3 (Score: [X]):
[KEY COMMENTS]

Please help me:
1. Categorize each comment (factual error, valid concern, suggestion, misunderstanding)
2. Prioritize which comments to address first
3. Draft point-by-point responses that are concise and professional
4. Identify any additional experiments I should run during the rebuttal period
5. Suggest how to frame responses to address reviewer misunderstandings diplomatically
```

### Plan Conference-to-Journal Extension
```
I have a [LENGTH]-page conference paper published at [CONFERENCE] on [TOPIC].
I want to extend it to a journal paper for [JOURNAL].

The conference paper covers:
[LIST MAIN SECTIONS AND CONTENT]

Please help me:
1. Identify what qualifies as the minimum 30% new content
2. Suggest specific new experiments or analyses to add
3. Propose an expanded paper structure for the journal version
4. Draft a disclosure paragraph for the journal cover letter
5. Recommend additional related work to include
```
