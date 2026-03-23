# Patent Mining (专利点挖掘)

> Skill for Claude Code — assists researchers in identifying patentable innovations from research work

## When to Use

- Reviewing research results to identify patentable innovations
- Preparing for a patent mining workshop with a research team
- Analyzing a technology system to find multiple patent points
- Converting a research paper into one or more patent applications
- Building a patent portfolio strategy around a core technology
- Conducting prior art searches to assess novelty
- Helping students and researchers understand what constitutes a patentable invention

## Related Skills

- [disclosure.md](disclosure.md) — Writing invention disclosure documents
- [patent-drafting.md](patent-drafting.md) — Drafting patent applications
- [office-action.md](office-action.md) — Responding to patent office actions

---

## What Makes a Patentable Invention

Under Chinese patent law (and broadly consistent with international standards), a patentable invention must satisfy three criteria:

### 1. Novelty (新颖性)
The invention must not be publicly disclosed anywhere in the world before the filing date. Public disclosure includes:
- Published papers, conference presentations, or preprints
- Public demonstrations or product releases
- Prior patent applications (published or granted)
- Oral disclosures at non-confidential meetings
- Thesis defenses (if publicly accessible)

### 2. Inventiveness / Non-Obviousness (创造性)
The invention must represent a substantive, non-trivial improvement over existing technology. It should not be an obvious combination of known techniques to a person skilled in the art. Key question: would an expert in this field, knowing all prior art, arrive at this solution without creative effort?

### 3. Practical Applicability (实用性)
The invention must be capable of being manufactured or used in practice, and must produce a beneficial technical effect. Purely theoretical results without a concrete implementation path are generally not patentable.

### What Cannot Be Patented (in China)
- Scientific discoveries (科学发现)
- Rules and methods for mental activities (智力活动的规则和方法)
- Disease diagnosis and treatment methods (疾病诊断和治疗方法)
- Animal and plant varieties (动物和植物品种)
- Atomic energy-related inventions (用原子核变换方法获得的物质)
- Designs that are purely aesthetic (covered by design patents or copyright instead)

---

## Five Methods for Patent Mining

### Method 1: Technology Decomposition (技术分解法)

Break a complex system into its constituent modules, components, and interfaces. Analyze each element for potential innovation.

**Process:**
1. Draw a system architecture diagram with all major modules
2. For each module, list: inputs, outputs, internal processing, interfaces
3. Ask: is there anything novel in how this module works?
4. Ask: is there anything novel in how modules interact?
5. Ask: is the overall system architecture itself novel?

**Example (Autonomous Driving SOTIF):**
- Perception module: novel sensor fusion algorithm? new failure mode detection?
- Decision module: new safety-aware planning method? novel risk assessment?
- Control module: new fail-safe control strategy? novel degradation mechanism?
- System-level: new architecture for monitoring and responding to SOTIF hazards?

**Output:** A table of module-level innovation candidates with novelty assessment.

### Method 2: Process Analysis (流程分析法)

Walk through a method, algorithm, or manufacturing process step by step. Identify novel steps, novel orderings, or novel combinations of known steps.

**Process:**
1. Write out the complete process as a numbered sequence of steps
2. For each step, ask: is this step done differently from existing methods?
3. For transitions between steps, ask: is the ordering or connection novel?
4. For the overall process, ask: does the combination produce an unexpected benefit?
5. Compare with the closest known process — what are the differences?

**Template:**
```
Step 1: [Description] — Novel? [Y/N] — Why: [explanation]
Step 2: [Description] — Novel? [Y/N] — Why: [explanation]
...
Overall process novelty: [assessment]
Key differentiators from prior art: [list]
```

### Method 3: Problem-Solution Mapping (问题-方案映射法)

Start from technical problems encountered during research. Each problem that required a creative technical solution is a potential patent.

**Process:**
1. List all technical problems encountered during the research
2. For each problem, describe the solution you developed
3. Search prior art: has anyone else solved this problem this way?
4. If your solution is novel, it is a patent candidate
5. Bonus: if you solved one problem in multiple ways, each way may be a separate patent

**Template:**
```
PROBLEM: [Technical problem description]
PRIOR ART SOLUTIONS: [How others have addressed this]
YOUR SOLUTION: [Your technical approach]
NOVELTY ASSESSMENT: [What is new about your solution]
TECHNICAL EFFECT: [What benefit does your solution provide]
PATENT POTENTIAL: [High / Medium / Low]
```

### Method 4: Competitive Landscape Gap Analysis (竞争空白分析法)

Search existing patents in your technology area, map the landscape, and identify uncovered territory where you can file strategically.

**Process:**
1. Define your technology area using IPC/CPC codes and keywords
2. Search CNIPA and international databases for existing patents
3. Classify found patents into clusters (by sub-technology or application)
4. Create a technology-application matrix
5. Identify empty cells — these are potential filing opportunities
6. Assess whether your research fills any of these gaps

**Technology-Application Matrix Example:**
| Technology \ Application | Highway | Urban | Parking | Special Conditions |
|--------------------------|---------|-------|---------|-------------------|
| Sensor fusion | [Crowded] | [Some] | [Few] | [Empty] |
| Risk assessment | [Some] | [Few] | [Empty] | [Empty] |
| Fail-safe control | [Some] | [Empty] | [Empty] | [Empty] |

Empty or sparse cells = strategic filing opportunities.

### Method 5: From Research Paper to Patent (论文转化法)

Published research papers often contain patentable innovations, but the paper and patent serve different purposes. A paper focuses on scientific contribution; a patent focuses on technical solution and protection scope.

**Process:**
1. Identify the core technical contribution of the paper
2. Separate the scientific insight (not patentable) from the technical implementation (potentially patentable)
3. Ask: what is the specific technical means (方法/装置/系统) that achieves the result?
4. Reframe the contribution as a problem-solution pair
5. Expand the claims: what variations or generalizations of the method also work?
6. Draft claim structure: independent claim (broadest protection) + dependent claims (specific embodiments)

**Critical Warning:** If the paper is already published, the invention has been publicly disclosed. You must file within 6 months of publication (under Chinese grace period provisions, which apply only in limited circumstances — conference presentations at recognized academic conferences or first publication). Best practice is always to file BEFORE publication.

---

## Patent Mining Workshop Template

Use this format for a 2-3 hour team workshop to systematically mine patents from a research project.

### Preparation (1 week before)
- Each team member prepares a 1-page summary of their work highlighting technical challenges and solutions
- Advisor prepares a list of the project's key innovations
- Conduct a baseline prior art search in the core technology area

### Workshop Agenda

| Time | Activity | Output |
|------|----------|--------|
| 0:00 - 0:15 | Introduction: what makes a patentable invention | Shared understanding |
| 0:15 - 0:45 | Each member presents their technical contribution (5 min each) | Innovation list |
| 0:45 - 1:30 | Group brainstorm using Methods 1-3 | Expanded innovation list |
| 1:30 - 1:45 | Break | |
| 1:45 - 2:15 | Novelty assessment and prior art discussion | Filtered list |
| 2:15 - 2:45 | Prioritization and assignment | Action plan |
| 2:45 - 3:00 | Wrap-up and deadlines | Timeline |

### Prioritization Matrix

| Innovation | Novelty (1-5) | Commercial Value (1-5) | Defensive Value (1-5) | Effort to File (1-5, inverted) | Priority Score |
|-----------|---------------|----------------------|---------------------|-------------------------------|---------------|
| [Innovation 1] | | | | | |
| [Innovation 2] | | | | | |

Priority Score = sum of all columns. File highest scores first.

---

## Prior Art Search Guide

### Chinese Patent Database
- **CNIPA Patent Search (中国专利公布公告):** https://pss-system.cponline.cnipa.gov.cn/
- Free, official, comprehensive for Chinese patents
- Search by keyword, applicant, inventor, IPC code, date range

### International Databases
- **Google Patents:** https://patents.google.com/ — best for broad keyword search across jurisdictions
- **Espacenet (EPO):** https://worldwide.espacenet.com/ — comprehensive international coverage
- **USPTO Full-Text:** https://patft.uspto.gov/ — US patents full text
- **WIPO PATENTSCOPE:** https://patentscope.wipo.int/ — PCT international applications

### Search Strategy

1. **Keyword search:** Start with 3-5 core technical terms in both Chinese and English
2. **IPC/CPC code search:** Identify relevant classification codes from initial results, then search by code for comprehensive coverage
3. **Cited/citing analysis:** Find key patents in your area, then trace their cited references and forward citations
4. **Inventor/applicant search:** Search for patents by leading research groups and companies in the field
5. **Combination search:** Use Boolean operators (AND, OR, NOT) to refine results

### Documenting Prior Art

For each relevant prior art reference found, record:
```
Patent Number: [e.g., CN112345678A]
Title: [Patent title]
Applicant: [Company/University]
Filing Date: [YYYY-MM-DD]
Key Claims: [Summary of independent claims]
Relevance to Our Work: [How does this relate to our innovation]
Differences from Our Work: [What our innovation does differently]
```

---

## From Innovation to Disclosure

Once a patentable innovation is identified, the next step is writing a technical disclosure document (技术交底书). This document is the foundation for the patent application.

### Technical Disclosure Document Template

```
1. 发明名称 (Title of Invention)
   [Concise, descriptive title — avoid vague terms like "a new method"]

2. 技术领域 (Technical Field)
   [The specific technical domain, e.g., "autonomous driving safety" / "vehicle perception systems"]

3. 背景技术 (Background Art / Prior Art)
   [Describe the current state of the art and its limitations]
   - Existing approach A: [description] — limitation: [what it cannot do]
   - Existing approach B: [description] — limitation: [what it cannot do]
   - The technical problem to be solved: [clear statement]

4. 发明内容 (Summary of the Invention)
   4.1 Technical problem to be solved (要解决的技术问题)
   4.2 Technical solution (技术方案) — this is the core of the disclosure
       [Describe the method/device/system in precise technical language]
       [Include all essential steps or components]
   4.3 Beneficial effects (有益效果)
       [Quantitative comparison with prior art if possible]
       [e.g., "improves detection accuracy by 15%" or "reduces computation time by 40%"]

5. 具体实施方式 (Detailed Description of Embodiments)
   [At least one detailed example of how the invention works]
   [Include specific parameters, configurations, or algorithms]
   [Describe variations and alternative embodiments]

6. 附图说明 (Description of Drawings)
   [List all figures: system diagrams, flowcharts, data plots]
   [Each figure should be referenced in the detailed description]

7. 附图 (Drawings)
   [System architecture diagram]
   [Method flowchart]
   [Key experimental results or simulation results]
   [Comparison charts with prior art]
```

### Quality Checklist for Disclosure Documents
- [ ] Technical problem is clearly stated
- [ ] Solution is described with enough detail for reproduction
- [ ] At least one specific embodiment with concrete parameters
- [ ] Beneficial effects are stated with evidence (quantitative preferred)
- [ ] Figures clearly illustrate the invention
- [ ] Prior art is accurately described (do not misrepresent competitor work)
- [ ] No unnecessary limitations in the description (keep protection scope broad)

---

## Patent Portfolio Strategy

### What Is a Patent Portfolio?
A patent portfolio is a coordinated set of patents that collectively protect a core technology from multiple angles. A single patent is easy to design around; a portfolio creates a defensive perimeter.

### Building a Portfolio Around a Core Technology

**Layer 1: Core Patent (核心专利)**
- The fundamental innovation — broadest possible claims
- File this first with the strongest prior art differentiation

**Layer 2: Implementation Patents (实施专利)**
- Specific embodiments, configurations, or parameter ranges
- Protect the most practical and commercially valuable implementations

**Layer 3: Improvement Patents (改进专利)**
- Incremental improvements, optimizations, or extensions
- Filed as the technology matures through continued research

**Layer 4: Application Patents (应用专利)**
- Same core technology applied to different domains or use cases
- e.g., a safety monitoring method applied to highway driving, urban driving, parking

**Layer 5: Peripheral Patents (外围专利)**
- Related tools, testing methods, data processing pipelines
- Supports the core technology even if not the core innovation itself

### Portfolio Metrics to Track
- Total granted patents vs. filed applications
- Technology coverage: which aspects of the system are protected?
- Geographic coverage: China, US, Europe, PCT?
- Expiration timeline: when do key patents expire?
- Licensing potential: which patents have commercial value?

---

## Timing Considerations

### The Cardinal Rule
**File BEFORE any public disclosure.** This means before:
- Publishing a journal paper or conference paper
- Presenting at a conference (including poster sessions)
- Thesis defense (if thesis is publicly accessible)
- Product demonstrations or press releases
- Online preprint postings (arXiv, SSRN, etc.)

### China's Grace Period (宽限期)
Chinese patent law provides a 6-month grace period, but ONLY in limited circumstances:
- First presentation at a Chinese government-approved academic conference
- First publication in a Chinese government-approved academic journal
- Disclosure by a third party without the inventor's consent

**Do not rely on the grace period.** It is narrow, difficult to prove, and does not apply to most international filings.

### Recommended Timeline for Research Groups
```
Research result obtained → Internal review (1-2 weeks)
                         → Prior art search (1-2 weeks)
                         → Technical disclosure drafted (2-3 weeks)
                         → Patent attorney review (1-2 weeks)
                         → Patent application filed (←— THIS before publication)
                         → Paper submitted to journal/conference (after filing)
```

### For PhD Students
- Build patent awareness into the research process from Year 1
- Every significant technical contribution should be evaluated for patentability
- Discuss patent potential at regular advisor meetings
- Target: 1-2 patent applications during the PhD (varies by lab and field)

---

## Prompt Templates for Claude

### Identify Patentable Innovations
```
I have completed research on [topic]. Here is a summary of my key technical contributions:
[paste summary of methods, algorithms, or systems developed]

For each contribution, assess:
1. Is it a novel technical solution (not just a scientific finding)?
2. What is the closest prior art you are aware of?
3. What specific technical effect or improvement does it achieve?
4. How would you frame the core claim in patent language?
5. What variations or generalizations could broaden the protection scope?
```

### Prior Art Analysis
```
I am considering filing a patent for the following invention:
[describe the invention in detail]

Based on your knowledge, identify:
1. The closest known prior art (patents, papers, products)
2. Key differences between my invention and the prior art
3. Potential novelty challenges an examiner might raise
4. Suggestions for strengthening the novelty argument
```

### Paper-to-Patent Conversion
```
I have published (or plan to publish) the following paper:
Title: [paper title]
Core contribution: [what the paper proposes]
Method: [technical approach]
Results: [key results]

Help me:
1. Identify patentable technical solutions within this paper
2. Separate the scientific contribution from the technical implementation
3. Draft a preliminary claim structure (independent + dependent claims)
4. Suggest additional embodiments to broaden the patent scope
5. Flag any timing issues (has this been publicly disclosed already?)
```

### Patent Portfolio Planning
```
Our research group works on [technology area]. We currently have the following patents:
[list existing patents with brief descriptions]

Our recent research has produced these new results:
[describe new innovations]

Help me:
1. Map the existing portfolio coverage
2. Identify gaps in our patent protection
3. Suggest which new innovations to file first
4. Recommend a filing strategy (domestic vs. PCT vs. direct foreign filing)
5. Identify potential defensive filing opportunities
```

### Technical Disclosure Review
```
Review this technical disclosure document for patent filing readiness:
[paste disclosure document]

Evaluate:
1. Is the technical problem clearly defined?
2. Is the solution described with sufficient detail for reproduction?
3. Are the beneficial effects supported by evidence?
4. Are there unnecessary limitations that narrow the protection scope?
5. What additional embodiments or examples should be added?
6. Is the prior art description accurate and complete?
```
