# Research Paper Writing

> Skill for Claude Code — assists researchers in structuring, drafting, and polishing research papers for journals and conferences.

## When to Use

- Drafting a complete research paper from scratch given an outline, notes, or experimental results
- Restructuring a messy draft into a coherent narrative
- Writing or rewriting individual sections (abstract, introduction, methods, results, discussion)
- Polishing academic English for non-native speakers
- Checking logical flow, argument strength, and narrative consistency
- Preparing a paper for a specific venue (journal or conference) with formatting constraints

---

## Core Frameworks

### Framework 1: Simon Peyton Jones' Seven Principles

These principles, from his widely cited talk "How to Write a Great Research Paper," form the foundation of effective academic writing.

1. **Do not wait; write early.** Start writing before the research is complete. Writing clarifies thinking, reveals gaps in logic, and shapes the research direction. A rough draft written mid-project is more valuable than a perfect draft started after all experiments are done.

2. **Identify your key idea.** Every paper should convey exactly one clear, sharp idea. If you cannot state it in one sentence, the paper is not ready. Test: "The main contribution of this paper is ___."

3. **Tell a story.** Papers are narratives, not lab notebooks. Structure the paper as: "Here is a problem. It is interesting because ___. It is hard because ___. Here is my idea. Here is how it works. Here is how I evaluated it. Here is what I learned."

4. **Nail your contributions to the mast.** State contributions explicitly in the introduction as a bulleted list. Each bullet should be refutable and specific. Bad: "We improve performance." Good: "We reduce inference latency by 3.2x on the KITTI benchmark while maintaining mAP within 0.5% of the baseline."

5. **Related work is not the enemy.** Be generous to prior work. Acknowledge what others did well. Position your work as building on and extending theirs, not replacing it. Criticize approaches, never people.

6. **Put your readers first.** Use examples before formalisms. Provide intuition before proofs. Give the reader a reason to care before diving into technical details. Every section should answer: "Why should the reader keep reading?"

7. **Listen to your readers.** When a reader misunderstands, the fault lies with the writer. Do not argue; rewrite. Track which parts confuse early readers and revise until clarity is achieved.

### Framework 2: Jennifer Widom's Five-Point Introduction

A structured approach to writing introductions that ensures completeness and logical flow.

1. **What is the problem?** State the broad area and the specific problem you address. Be concrete. "Autonomous vehicles must detect pedestrians in real time, but current detectors fail in adverse weather conditions."

2. **Why is it interesting and important?** Explain the real-world impact or scientific significance. Connect to a community the reader cares about. "Pedestrian detection failures account for 40% of AV-related accidents in rain and fog."

3. **Why is it hard? (Why do naive approaches fail?)** Show that this is not trivially solved. Identify the key technical challenge. "Existing LiDAR-camera fusion methods assume clean sensor inputs, but rain droplets create ghost points that corrupt the 3D feature space."

4. **Why hasn't it been solved before? (What's missing?)** Distinguish your insight from prior work. "Previous denoising approaches operate in raw point-cloud space, losing geometric context. No prior work has addressed weather-induced noise in the fused feature representation."

5. **What are the key components of your approach and results?** Summarize your method and headline results. "We propose WeatherFusion, a noise-aware feature fusion module that operates in BEV space. On the WaymoRain benchmark, WeatherFusion achieves 78.3% mAP, a 12.1% improvement over the state of the art."

### Framework 3: IMRAD + Hourglass Model

The IMRAD structure (Introduction, Methods, Results, And Discussion) follows an hourglass shape:

```
    BROAD: General context, motivation         ← Introduction (wide)
      ↓    Narrow to your specific problem
    NARROW: Exact methods, specific setup      ← Methods (narrow)
    NARROW: Specific findings, data            ← Results (narrow)
      ↓    Broaden to implications
    BROAD: Interpretation, future directions   ← Discussion (wide)
```

The introduction funnels from broad context to your specific question. Methods and results are tightly focused. The discussion widens back out to implications, limitations, and future work.

### Framework 4: ABT Storytelling (And-But-Therefore)

Randy Olson's ABT framework transforms academic writing from a list of facts into a narrative:

- **And** — Establish the context. "Deep learning has revolutionized perception in autonomous driving, AND large-scale datasets have enabled rapid progress."
- **But** — Introduce the tension. "BUT these models are trained on fair-weather data and degrade catastrophically in adverse conditions."
- **Therefore** — Present your contribution. "THEREFORE, we propose a weather-robust training framework that synthesizes realistic adverse-condition data from clean-weather inputs."

Apply ABT at multiple scales: the abstract, each section opening, and even individual paragraphs. Every paragraph should have implicit tension and resolution.

---

## Section-by-Section Writing Guide

### Title

**Formula:** `[Method/Approach] for [Problem/Task]: [Key Result/Contribution]`

Examples:
- "WeatherFusion: Noise-Aware Feature Fusion for Robust 3D Detection in Adverse Weather"
- "Learning to Detect Under Rain: A Synthetic Data Approach for All-Weather Perception"

Rules:
- Keep under 15 words (12 is ideal for readability)
- Avoid acronyms unless universally known in the field (e.g., LiDAR, SLAM)
- Do not use "Novel" or "A New Method" — reviewers assume novelty; state what is new instead
- Front-load the most important concept
- Test: Can a researcher decide relevance from the title alone?

### Abstract (150-250 words)

Write the abstract LAST, after the entire paper is complete. It is a self-contained summary, not a teaser.

**Template:**

```
[CONTEXT: 1-2 sentences] Broad area and why it matters.
[PROBLEM: 1 sentence] The specific gap or challenge.
[METHOD: 1-2 sentences] What you did — your approach at a high level.
[RESULTS: 1-2 sentences] Key quantitative findings with numbers.
[IMPACT: 1 sentence] Why this matters; broader implications.
```

**Example:**

"Reliable 3D object detection is critical for safe autonomous driving. However, existing detectors suffer significant performance drops under adverse weather due to sensor noise. We propose WeatherFusion, a noise-aware multi-modal fusion module that learns to identify and suppress weather-induced artifacts in the shared BEV feature space. On the WaymoRain benchmark, WeatherFusion achieves 78.3% mAP under heavy rain, improving over the previous state of the art by 12.1 percentage points while adding only 2.3ms latency. Our approach demonstrates that feature-level denoising is both more effective and more efficient than raw-input denoising for weather-robust perception."

Rules:
- Include at least two concrete numbers (performance metrics, dataset scale, speedup)
- No citations in the abstract
- No undefined acronyms
- Every sentence must earn its place — remove filler ruthlessly

### Introduction (Using Widom's 5-Point Structure)

**Paragraph 1 — The Problem and Its Importance:**
Open with the broad context. State why this area matters. Use a concrete fact, statistic, or scenario to ground the reader.

Transition phrases: "A critical challenge in...", "Central to the success of... is...", "Recent advances in... have enabled..., yet..."

**Paragraph 2 — Why It Is Hard:**
Explain the technical challenge. Why do straightforward solutions fail? What makes this problem non-trivial?

Transition phrases: "However, achieving this is challenging because...", "A naive approach would..., but this fails when...", "The core difficulty lies in..."

**Paragraph 3 — What Others Have Done (Brief):**
Summarize the dominant approaches in 3-5 sentences. Identify their shared limitation. This is NOT the Related Work section — keep it high-level.

Transition phrases: "Prior work has addressed this through...", "Existing methods typically...", "While effective in..., these approaches share a common limitation:..."

**Paragraph 4 — Your Insight and Approach:**
State your key insight. Explain your method at a conceptual level. This paragraph should make the reader think: "That is a clever idea."

Transition phrases: "In this paper, we observe that...", "Our key insight is...", "We propose..., which differs from prior work in that..."

**Paragraph 5 — Contributions:**
List contributions as explicit, refutable bullet points. Typically 3-4 bullets.

Template:
```
The main contributions of this paper are:
- We propose [method name], [one-sentence description of what it does and why it is new].
- We demonstrate that [key finding], achieving [metric] on [benchmark].
- We release [dataset/code/model] to facilitate future research.
```

### Related Work

**Organization:** Thematic, NOT chronological. Group by approach type.

**Paragraph template:**
```
[Topic sentence stating the theme of this group.]
[Author] et al. [year] proposed [method], which [what it does].
[Author] et al. [year] extended this by [improvement].
However, these methods [shared limitation].
In contrast, our approach [how you differ].
```

Rules:
- Every paragraph must end by connecting back to YOUR work
- Be fair and accurate — reviewers may be the authors you cite
- Cite recent work (last 2-3 years) to show awareness of the field
- If a related work is very close to yours, address it explicitly and state the difference clearly
- Do not pad with tangentially related citations

### Methodology

**Structure:**
1. **Overview/Architecture:** Start with a figure showing the full pipeline. Give a 1-paragraph overview before diving into components.
2. **Problem Formulation:** Define notation, inputs, outputs, and the objective mathematically.
3. **Component Details:** Describe each module/step. For each: (a) what it does, (b) why it is designed this way, (c) how it connects to other components.
4. **Training/Optimization:** Loss functions, training procedure, hyperparameter choices with justification.
5. **Implementation Details:** Framework, hardware, training schedule — enough for reproducibility.

Rules:
- Justify every design choice: "We use X because Y" not just "We use X"
- Use consistent notation throughout
- Provide enough detail for reproducibility
- Include a figure showing the overall architecture

### Experiments / Results

**Structure:**
1. **Experimental Setup:** Datasets, metrics, baselines, implementation details
2. **Main Results:** Comparison table with baselines. Bold the best result. State the improvement explicitly in text.
3. **Ablation Studies:** Remove or replace each component. Show each contributes.
4. **Analysis:** Qualitative examples, failure cases, visualization of learned representations.

Rules:
- Every claim in the introduction must have supporting evidence here
- Report standard deviations or confidence intervals where applicable
- Include failure cases — reviewers trust honest papers
- Use consistent decimal precision in tables
- Describe trends in text; do not just point at tables ("As shown in Table 2, our method outperforms X by 3.2% on metric Y because Z.")

### Discussion

**Template:**
```
[Paragraph 1: Summarize the key findings and what they mean]
[Paragraph 2: Explain WHY your method works — what is the underlying reason?]
[Paragraph 3: Limitations — be honest and specific]
[Paragraph 4: Broader implications and connections to other problems]
[Paragraph 5: Future work — concrete next steps, not vague promises]
```

Rules:
- Do not simply repeat results — interpret them
- Limitations should be genuine, not strawmen you can easily dismiss
- Future work should be specific enough that someone could act on it

### Conclusion

Keep it to 1-2 paragraphs. Restate the problem, your approach, key results, and the takeaway. Do NOT introduce new information. The conclusion should be readable independently of the rest of the paper.

**Template:**
```
We addressed the problem of [X] by proposing [Y].
Our approach is based on the insight that [key insight].
Experiments on [benchmarks] demonstrate that [headline result].
[One sentence on broader significance or future direction.]
```

---

## Quality Checklist

Before submission, verify every item:

### Narrative and Logic
- [ ] The paper tells a coherent story from start to finish
- [ ] Every section flows logically into the next
- [ ] The introduction promises are fulfilled by the experiments
- [ ] Contributions listed in the intro match what is actually delivered
- [ ] The abstract accurately reflects the final paper content

### Technical Rigor
- [ ] All claims are supported by evidence (data, proofs, citations)
- [ ] Notation is consistent throughout the paper
- [ ] Equations are numbered and referenced in text
- [ ] Experimental setup is described in enough detail for reproduction
- [ ] Baselines are fair and recent (not outdated strawmen)
- [ ] Ablation studies isolate the contribution of each component
- [ ] Statistical significance or variance is reported where applicable

### Writing Quality
- [ ] No undefined acronyms on first use
- [ ] No orphaned references ("as shown in Figure X" where X does not exist)
- [ ] Figures and tables are referenced in the text before they appear
- [ ] Captions are self-contained — a reader should understand the figure from its caption alone
- [ ] No grammatical errors (run a grammar checker as a final pass)
- [ ] Consistent tense: present for established facts, past for your experiments
- [ ] No excessive hedging ("might possibly potentially suggest")

### Formatting and Compliance
- [ ] Paper meets the page/word limit of the target venue
- [ ] References follow the required citation style
- [ ] All figures are high-resolution and legible when printed in grayscale
- [ ] Supplementary material is properly referenced
- [ ] Author information is anonymized (for double-blind review)
- [ ] No self-identifying citations in blind submissions ("In our prior work [Author, 2024]...")

---

## Common Mistakes to Avoid

1. **Starting with "In recent years..."** — This is the most overused opening in academic writing. Start with the problem or a concrete scenario instead.
2. **Burying the contribution.** State what you did and why it matters in the first page. Do not make the reader hunt for your point.
3. **Confusing novelty with complexity.** Simple, elegant solutions are preferable. Do not add complexity to appear sophisticated.
4. **Writing the related work as a laundry list.** Group thematically. Every paragraph must connect back to your work.
5. **Over-claiming.** "Our method achieves state-of-the-art" is only valid if you compare against all relevant recent baselines on standard benchmarks. Be precise about the scope of your claims.
6. **Under-discussing limitations.** Reviewers distrust papers that claim no limitations. Be honest — it builds credibility.
7. **Tables without analysis.** Do not just present numbers. Explain trends, surprises, and what the numbers mean.
8. **Inconsistent notation.** Define symbols once and use them consistently. Create a notation table if needed.
9. **Vague future work.** "In the future, we will explore other domains" tells the reader nothing. Be specific about what open questions remain.
10. **Ignoring the audience.** A robotics paper submitted to a vision venue needs different framing than one submitted to a robotics venue. Tailor the motivation and related work accordingly.
11. **Writing the abstract first.** The abstract should be written last, after the paper content is finalized. An early abstract often misrepresents the actual paper.
12. **Passive voice overuse.** "The experiments were conducted" is weaker than "We conducted experiments." Use active voice for clarity and directness.
13. **Missing the "so what?" test.** After every paragraph, ask: "Why does the reader care about this?" If you cannot answer, rewrite or remove the paragraph.

---

## AI-Powered Polishing Prompts

### English Academic Polishing (from gpt_academic)

```
Below is a paragraph from an academic paper. Polish the writing to meet
the academic style, improve the spelling, grammar, clarity, concision
and overall readability. When necessary, rewrite the whole sentence.
Firstly, you should provide the polished paragraph. Secondly, you should
list all your modification and explain the reasons to do so in markdown table.

Paragraph:
[PASTE YOUR PARAGRAPH HERE]
```

### Chinese Academic Polishing (from gpt_academic)

```
作为一名中文学术论文写作改进助理，你的任务是改进所提供文本的拼写、语法、清晰、
简洁和整体可读性，同时分解长句，减少重复，并提供改进建议。请先提供文本的更正版本，
然后在markdown表格中列出修改的内容，并给出修改的理由。

文本：
[粘贴你的文本]
```

### Top-Conference Style Polishing (from ChatGPT-Academic-Prompt)

```
I will provide you with a text that requires refinement, and you will
augment it with more sophisticated language and sentence structures
appropriate for academic writing. Please maintain the original meaning
and keep the response concise. Please follow the writing style of top
AI conferences, such as CVPR, ICCV, ICML and NeurIPS.

Text:
[PASTE YOUR TEXT HERE]
```

### Nature-Style Rewrite (from ChatGPT-Academic-Prompt)

```
I want you to act as an academic journal editor. Please rephrase the
paragraph from an academic angle based on the writing style of the
Nature journal, and target the audience as expert in the related field.

Paragraph:
[PASTE YOUR PARAGRAPH HERE]
```

### Grammar Error Detection with Table Output

```
Below is a paragraph from an academic paper. Find all grammar errors
and list them in a two-column markdown table. The first column is the
original sentence with the error, and the second column is the corrected
version with a brief explanation.

Paragraph:
[PASTE YOUR PARAGRAPH HERE]
```

### Mind Map Generation with Mermaid

```
Based on the following paper abstract (or outline), generate a Mermaid
mind map diagram showing the key concepts and their relationships.
Use the Mermaid mindmap syntax.

Abstract:
[PASTE ABSTRACT OR OUTLINE]
```

---

## Writing Enhancement Tool Stack

### Language and Phrasing Tools

| Tool | URL | Purpose |
|------|-----|---------|
| **Academic Phrasebank** | phrasebank.manchester.ac.uk | Templates for academic phrases by section (intro, methods, results, discussion). University of Manchester resource. |
| **Linggle** | linggle.com | N-gram search engine for checking if a phrase is commonly used in English. Supports wildcard patterns like `v. the * of`. |
| **ESODA** | esoda.org | Tsinghua-developed tool for English academic expression search. Enter a Chinese phrase, get English academic equivalents. |
| **COCA** | corpus.byu.edu/coca | Corpus of Contemporary American English (1B+ words). Check word frequency, collocations, and genre distribution. |
| **BNC** | corpus.byu.edu/bnc | British National Corpus. Useful for British English conventions. |
| **Ludwig.guru** | ludwig.guru | Search engine for sentences from academic papers. See how a phrase is used in context. |
| **Grammarly** | grammarly.com | AI-powered grammar and style checker with academic tone detection. |

### Prose Linting Tools

| Tool | Purpose | Usage |
|------|---------|-------|
| **Vale** | Customizable prose linter with style rules (Microsoft, Google, academic) | `vale --config=.vale.ini paper.md` — define rules for hedging, passive voice, jargon |
| **LanguageTool** | Open-source grammar/style checker with LaTeX support | Available as CLI, browser extension, LibreOffice plugin. Supports 30+ languages including Chinese. |
| **textidote** | Grammar checker designed specifically for LaTeX documents | `java -jar textidote.jar --check en paper.tex` — respects LaTeX commands |
| **proselint** | Checks for common writing issues (cliches, jargon, redundancy) | `proselint paper.md` — lightweight, opinionated |
| **write-good** | Naive linter for English prose (passive voice, weasel words, cliches) | `write-good paper.md` — quick first-pass check |

### Figure and Visualization Tools

| Tool | Purpose | URL/Install |
|------|---------|-------------|
| **Paper-Picture-Writing-Code** | Collection of matplotlib/LaTeX plot templates for academic papers | GitHub: MLNLP-World/Paper-Picture-Writing-Code |
| **PlotNeuralNet** | Generate publication-quality neural network architecture diagrams in LaTeX | GitHub: HarisIqbal88/PlotNeuralNet |
| **draw.io (diagrams.net)** | Free, browser-based diagram editor. Export to PDF/SVG for LaTeX. | app.diagrams.net |
| **Mermaid** | Text-based diagram generation (flowcharts, sequence, mind maps) | mermaid.js.org — integrates with Markdown |
| **Mathpix** | Screenshot-to-LaTeX converter for equations and tables | mathpix.com — also converts PDF tables to LaTeX |
| **Excel2LaTeX** | Convert Excel tables directly to LaTeX tabular code | CTAN: Excel2LaTeX |
| **TikZ** | Native LaTeX drawing package for publication-quality graphics | Built into LaTeX — steep learning curve but maximum control |
| **pgfplots** | LaTeX package for creating plots directly in documents | CTAN: pgfplots — consistent styling with document |

### Submission Preparation Tools

| Tool | Purpose | URL |
|------|---------|-----|
| **arxiv-latex-cleaner** | Clean LaTeX source for arXiv submission (remove comments, unused files, flatten) | GitHub: google-research/arxiv-latex-cleaner |
| **ccfddl.github.io** | CCF-recommended conference deadline tracker (Chinese CS community standard) | ccfddl.github.io |
| **aideadlin.es** | AI conference deadline countdown with calendar export | aideadlin.es |
| **Overleaf** | Collaborative LaTeX editor with templates for most venues | overleaf.com |
| **IEEE PDF eXpress** | Validate PDF formatting for IEEE conferences | ieee-pdf-express.org |
| **LaTeX-to-Word** | Pandoc-based conversion for journals requiring .docx | `pandoc paper.tex -o paper.docx` |

---

## Prompt Templates for Claude

### 1. Outline from Research Notes

```
I have the following research notes and results. Help me create a detailed paper outline following the IMRAD structure. For each section, suggest 2-3 key points to cover and identify which figures/tables I will need.

Research topic: [topic]
Key finding: [finding]
Method: [brief method description]
Results: [key numbers]
Target venue: [conference/journal name]
```

### 2. Introduction Drafting

```
Write the introduction for my paper using Jennifer Widom's 5-point structure. Here is the information:

1. Problem area: [area]
2. Why it matters: [importance]
3. Why it is hard: [challenge]
4. Gap in prior work: [what is missing]
5. Our approach and key result: [approach + result]

Target length: 1.5 pages. Use formal academic English. End with a numbered contribution list.
```

### 3. Abstract Compression

```
Here is my full paper draft. Write a 200-word abstract following this structure:
Context (1-2 sentences) -> Problem (1 sentence) -> Method (1-2 sentences) -> Results with numbers (1-2 sentences) -> Impact (1 sentence).

Paper draft:
[paste full paper or key sections]
```

### 4. Related Work Organization

```
I have collected the following papers for my related work section. Organize them into 3-4 thematic groups, write a paragraph for each group, and end each paragraph by connecting to my work.

My method: [brief description]
My key difference from prior work: [difference]
Papers: [list of papers with one-sentence summaries]
```

### 5. Clarity and Flow Review

```
Review the following section for clarity, logical flow, and academic writing quality. For each issue found, provide:
1. The problematic sentence or passage
2. Why it is problematic
3. A suggested revision

Focus on: argument flow, hedging language, unsupported claims, unclear transitions.

Section:
[paste section]
```

---

## References

- Simon Peyton Jones, "How to Write a Great Research Paper," Microsoft Research talk, 2016
- Jennifer Widom, "Tips for Writing Technical Papers," Stanford University
- Hengl & Gould, "Rules of Thumb for Writing Research Articles," 2002
- Randy Olson, "Houston, We Have a Narrative," University of Chicago Press, 2015
- Zobel, "Writing for Computer Science," Springer, 3rd Edition
- Whitesides, "Whitesides' Group: Writing a Paper," Advanced Materials, 2004

## Related Skills

- [conference-paper.md](conference-paper.md) — Conference-specific formatting and page limits
- [cover-letter.md](cover-letter.md) — Submission cover letters
- [revision.md](revision.md) — Handling revision requests
- [../literature/literature-review.md](../literature/literature-review.md) — Literature review sections
