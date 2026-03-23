# NSFC Proposal Writing (国家自然科学基金申请书撰写)

> Skill for Claude Code — assists researchers in structuring, drafting, and refining NSFC proposals.
> This skill does NOT generate submission-ready text. NSFC explicitly prohibits AI-generated content.
> Use this skill for structural guidance, logic checking, gap analysis, and simulated peer review.

## When to Use

- Structuring a new NSFC proposal from scratch (确定框架和逻辑线)
- Reviewing and critiquing a draft proposal before submission
- Checking whether the research content aligns with the stated scientific questions
- Simulating an NSFC panel review to identify weaknesses
- Generating a literature review outline for the Rationale section (立项依据)
- Verifying budget allocation against NSFC guidelines
- Preparing responses to review feedback (非首次申请的修改)

## NSFC 2026 Reform: Key Changes

The 2026 reform (starting with the March 2025 call) introduced significant structural changes. All proposals must follow the new three-module format.

### Three-Module Structure (三大模块)

| Module | Content | Key Requirement |
|--------|---------|-----------------|
| Module 1: 立项依据 | Research significance, literature review, scientific questions | Must clearly state the specific scientific question(s) |
| Module 2: 研究内容 | Research plan, methods, technical approach, expected outcomes | NO preset outline. Write according to your own research logic |
| Module 3: 研究基础 | Team qualifications, prior work, facilities, budget | Must demonstrate capability to execute the proposed research |

### Critical Rule Changes

1. **No fixed outline for Module 2** — The old rigid structure (research objectives / research content / key problems / technical approach) is abolished. Write freely according to the internal logic of your research. This is both a freedom and a trap: poor organization will be more visible.
2. **30-page limit** — The total proposal body (excluding references) must not exceed 30 pages. This is strictly enforced.
3. **AI-generated content is prohibited** — NSFC explicitly bans submitting AI-generated text as proposal content. AI tools may be used for structural guidance, language polishing, and review simulation. The final text must be the researcher's own.
4. **Concise expression (精炼表达)** — The reform emphasizes substance over volume. Reviewers are instructed to penalize padding and repetition.
5. **References are now outside the page limit** — References no longer count toward the 30-page limit, but must be relevant and well-curated.

## Program Types and Requirements

| Type (类型) | Funding (资助额度) | Duration (研究期限) | Target Applicants (适用人群) | Success Rate |
|-------------|-------------------|--------------------|-----------------------------|-------------|
| 青年基金 (Young Scientists) | ~30万 | 3年 | Male <=35, Female <=40, no prior NSFC PI | ~20-25% |
| 面上项目 (General Program) | 50-80万 | 4年 | Established researchers with track record | ~16-20% |
| 重点项目 (Key Program) | 200-300万 | 5年 | Field leaders, often by invitation | ~25-30% |
| 优秀青年基金 (Excellent Young) | 200万 | 3年 | Male <=38, Female <=40, outstanding early career | ~10-15% |
| 杰出青年基金 (Distinguished Young) | 400万 | 5年 | Male <=45, Female <=48, top researchers | ~8-12% |

### Choosing the Right Program

- **First-time applicants**: Start with 青年基金. The bar for innovation is lower; reviewers focus on potential.
- **After 1-2 completed 青年/面上**: Apply for 面上项目. You need a clear publication track record in the proposed area.
- **Transitioning fields**: If your prior work is in a different area, you must explicitly bridge the gap in Module 3.
- **Professor Zhang's context (面上项目)**: Requires demonstrated research accumulation in autonomous driving safety/SOTIF, with publications in the specific subarea of the proposal.

## Section-by-Section Writing Guide

---

### 摘要 (Abstract)

**Constraint**: 400 Chinese characters maximum. Every character counts.

**Four-Sentence Template**:

```
[Sentence 1 — Background and Problem]
随着[领域]的快速发展，[具体问题]已成为制约[目标]的关键瓶颈。

[Sentence 2 — Your Approach]
本项目针对[科学问题]，提出[方法/理论/框架]的研究思路。

[Sentence 3 — Specific Content]
具体研究内容包括：(1)[子课题1]；(2)[子课题2]；(3)[子课题3]。

[Sentence 4 — Significance]
研究成果将为[理论贡献]提供新方法，并为[实际应用]提供技术支撑。
```

**Checklist**:
- [ ] Contains the core scientific question in one clear sentence
- [ ] Lists 3-4 specific research tasks (not vague goals)
- [ ] States both theoretical and practical significance
- [ ] No jargon that a non-specialist reviewer cannot understand
- [ ] Exactly 400 characters or fewer (count precisely)
- [ ] Keywords (3-5) are specific, not generic ("autonomous driving safety" not "safety")

---

### 立项依据 (Rationale) — Module 1

**Recommended length**: 3-5 pages. This is the most important section. Reviewers form their first impression here.

**Structural Framework: "Funnel" Logic**

```
Layer 1: Strategic Importance (为什么重要)
  ↓ National strategy, industry demand, scientific frontier
Layer 2: Current State of Research (国内外研究现状)
  ↓ Organized by theme, NOT by author
Layer 3: Existing Gaps (现有研究不足)
  ↓ Specific, evidence-based gaps — not "研究不够深入"
Layer 4: Your Scientific Question (本项目的科学问题)
  ↓ One clear, focused question that addresses the gap
```

**Layer 1 — Strategic Importance (1/2 page)**

Open with why this research direction matters NOW. Use specific policy documents, industry data, or recent incidents.

Good opening patterns:
- National policy anchor: "《新一代人工智能发展规划》明确提出..."
- Industry data: "据统计，2024年我国L2+级自动驾驶渗透率已达..."
- Incident-driven: "2023年某自动驾驶车辆因[具体场景]导致的事故表明..."

Avoid:
- Generic openings: "随着科技的发展..." or "近年来..."
- Overly broad scope: Don't start with the entire history of AI

**Layer 2 — Literature Review (2-3 pages)**

Organize by research theme, NOT chronologically or by research group.

```
Theme structure (for each theme):

## 2.1 [主题名称]

[定义和范围，1-2句]

[代表性工作概述：XXX等[1]提出了...，YYY团队[2]进一步将...
 多个研究组比较：在[方面]，存在两种主要思路：(1)...[3-5]；(2)...[6-8]]

[该主题的局限：然而，上述工作主要关注[A]，对[B]的考虑不足。]
```

**Citation strategy**:
- Cite 50-80 references for 面上项目 (fewer looks under-researched, more looks padded)
- Always cite potential reviewers' work — look up the NSFC review panel member list for your discipline code (学科代码)
- Balance Chinese and international references (roughly 40:60 for engineering fields)
- Include 3-5 of your own prior publications to show continuity
- Cite recent work (last 3-5 years) predominantly; avoid heavy reliance on papers older than 10 years

**Layer 3 — Research Gaps (1/2 page)**

This is where most proposals fail. Be SPECIFIC about what is missing.

Bad gap statements:
- "现有研究不够深入" (Too vague)
- "缺乏系统研究" (What does "systematic" mean?)
- "尚未有效解决" (Why? What specifically fails?)

Good gap statements:
- "现有方法在[具体场景]下的[具体指标]仅为X%，无法满足[具体要求]"
- "已有理论假设[具体条件]，但在[实际情况]中该假设不成立"
- "多数研究聚焦于[A方面]，而忽略了[B因素]对[C结果]的影响机制"

**Layer 4 — Scientific Question (1/4 page)**

State the question explicitly. Use the exact phrasing:

```
综上所述，本项目拟解决的关键科学问题为：
[一句话明确表述科学问题]
```

A good scientific question:
- Is falsifiable (can be answered with evidence)
- Is not too broad ("如何提高自动驾驶安全性") or too narrow ("如何调整某参数")
- Sits at the intersection of the identified gaps
- Can be decomposed into 3-4 sub-problems (which become your research content)

---

### 研究内容 (Research Content) — Module 2

**2026 Reform**: No fixed format. You have freedom, but you must demonstrate clear research logic.

**Recommended Structure** (adapt to your research):

```
1. 科学问题与研究思路 (1/2 page)
   - Restate the scientific question from Module 1
   - Describe your overall research approach/philosophy
   - Explain why this approach can address the question

2. 总体技术路线 (1 page)
   - Technical roadmap figure (MUST include)
   - Text explaining the logical flow between research tasks
   - Show how sub-tasks interconnect

3. 研究内容 (4-6 pages, 3-4 sub-topics)

   3.1 [子课题1]：[名称]
       - 研究目标
       - 研究方案和方法
       - 预期结果

   3.2 [子课题2]：[名称]
       ...

   3.3 [子课题3]：[名称]
       ...

4. 关键科学问题与技术难点 (1/2 page)
   - 2-3 specific challenges
   - For each: what makes it hard + your approach to overcome it

5. 预期成果 (1/2 page)
   - Quantitative targets: papers (SCI/EI, number, target journals), patents, software copyrights
   - Qualitative targets: theoretical frameworks, validated methods, prototype systems
   - Be realistic: for 面上项目, typically 6-10 SCI papers, 2-3 patents
```

**Technical Roadmap Figure Guidance**:
- Use a flowchart showing inputs, methods, and outputs for each sub-task
- Show dependencies and data flow between sub-tasks
- Include a timeline bar at the bottom (Year 1 / Year 2 / Year 3 / Year 4)
- Keep it on ONE page, readable when printed in black and white
- Label every box and arrow; do not assume the reviewer will infer connections

**Sub-task Design Principles**:
- Each sub-task should address one aspect of the scientific question
- Sub-tasks should be logically connected but independently publishable
- 3 sub-tasks is optimal for 面上项目; 4 is acceptable; 5+ signals scope creep
- Each sub-task should produce at least 1-2 expected publications

---

### 创新点 (Innovation Points)

**Recommended**: 2-3 points, each 80-120 Chinese characters.

**Structure for each innovation point**:

```
创新点[N]：[一句话标题]
与现有方法[X]相比，本项目提出的[Y]能够[具体改进]，
解决了[具体问题]，实现了[量化提升/新能力]。
```

**Avoid these empty phrases**:
- "率先提出" / "首次研究" / "填补空白" — Unless you can truly prove it, reviewers will be skeptical
- "创新性地将A与B结合" — Combination alone is not innovation; explain WHY combining them solves a problem that neither alone can
- "提出了新的框架/体系" — What specifically is new about it?

**Good innovation writing**:
- Names the specific technical contribution
- States how it differs from existing approaches
- Includes a measurable or verifiable improvement

---

### 研究基础 (Research Foundation) — Module 3

**Purpose**: Convince reviewers that you CAN do what you propose.

**Structure**:

```
1. 工作基础 (Prior Work, 1-2 pages)
   - Direct connection between prior publications and the proposed research
   - For each cited paper: what it demonstrated, how it relates to the proposal
   - Highlight: "已初步验证了[方法]的可行性" or "前期工作已建立了[基础]"

2. 代表性成果 (1/2 page)
   List 5-10 representative publications:
   - Author(s), Title, Journal/Conference, Year, IF, Citations
   - Mark your role: corresponding author (*), first author
   - Highlight papers directly related to the proposal topic

3. 团队成员 (1/2 page)
   - Each member: name, title, expertise, role in this project
   - Show complementary skills covering all sub-tasks

4. 实验条件 (1/4 page)
   - Equipment, computing resources, experimental platforms
   - Data access, industry partnerships, collaboration agreements
   - For autonomous driving: simulation platforms, test vehicles, datasets

5. 在研项目说明 (1/4 page)
   - If you have other active grants: explain NO overlap with this proposal
   - If you have no active grants: emphasize your completed projects
```

---

### 预算 (Budget)

**Typical allocation for 面上项目 (50-80万)**:

| Category (科目) | Typical % | Notes |
|----------------|-----------|-------|
| 设备费 (Equipment) | 0-15% | Only if specific equipment is essential; usually low |
| 材料费 (Materials/Computing) | 10-20% | Computing costs, cloud services, data acquisition |
| 测试化验加工费 | 5-10% | Testing, prototype fabrication |
| 差旅/会议费 | 10-15% | Conference attendance (2-3 international, 2-3 domestic per year) |
| 劳务费 (Personnel) | 20-30% | Graduate student stipends (this is often the largest item) |
| 专家咨询费 | 3-5% | Advisory board, external reviewers |
| 间接费用 (Overhead) | 30% of direct costs | Automatically calculated; goes to the university |

**Budget Red Flags**:
- Equipment > 30% of total (reviewers will question if this is a science project or equipment purchase)
- No conference travel (suggests the team is not active in the community)
- Unrealistically low personnel costs (who will actually do the research?)
- Round numbers everywhere (suggests the budget was not carefully planned)

---

## Common Rejection Reasons (常见被拒原因)

Ranked by frequency based on published NSFC review statistics:

1. **创新性不足 (Insufficient Innovation)** — The most common reason. The proposed work is incremental or follows existing methods too closely.
2. **科学问题不明确 (Unclear Scientific Question)** — The proposal describes a research area but never pinpoints a specific question.
3. **研究内容与科学问题脱节 (Research content disconnected from the scientific question)** — The sub-tasks don't logically address the stated question.
4. **技术路线不清晰 (Unclear technical approach)** — Reviewers cannot follow how you will actually do the research.
5. **研究团队与研究内容不匹配 (Team-content mismatch)** — The PI's prior publications are in a different area.
6. **工作量过大或过小 (Scope too large or too small)** — Either trying to solve everything in 4 years, or proposing trivially little.
7. **写作质量差 (Poor writing quality)** — Logical gaps, grammatical errors, inconsistent terminology, sloppy formatting.
8. **立项依据文献陈旧 (Outdated references)** — Relying on papers from 10+ years ago without covering recent developments.
9. **预期成果不合理 (Unrealistic expected outcomes)** — Promising 20 SCI papers or claiming to "establish a new theory."
10. **与在研项目重叠 (Overlap with active grants)** — Reviewers will check your NSFC record.

---

## Reviewer's Perspective: What Evaluators Focus On

NSFC reviewers score proposals on five dimensions:

| Dimension | Weight | What Reviewers Look For |
|-----------|--------|------------------------|
| 科学价值 (Scientific Value) | High | Is the question important? Will solving it advance the field? |
| 创新性 (Innovation) | High | What is genuinely new? Not combination, but conceptual advance. |
| 可行性 (Feasibility) | Medium | Can this team realistically do this in 4 years? |
| 研究基础 (Foundation) | Medium | Does prior work demonstrate capability? |
| 写作质量 (Writing Quality) | Low-Medium | Is it clear, logical, and well-organized? |

**Practical reviewer behavior**:
- Most reviewers spend 30-60 minutes per proposal
- They read the abstract and innovation points FIRST
- If the scientific question is not clear by page 2 of the Rationale, the review is likely negative
- Reviewers look for their own papers in the references (cite them if relevant)
- A clean, well-formatted proposal signals a serious researcher

---

## Timeline for Proposal Preparation

| Milestone | Timing (relative to deadline) | Key Tasks |
|-----------|-------------------------------|-----------|
| Direction & Literature | T-8 to T-6 months | Finalize research direction; deep literature survey; identify the gap |
| Framework & Outline | T-6 to T-5 months | Define scientific question; design sub-tasks; draw technical roadmap |
| First Draft | T-5 to T-3 months | Write all sections; prepare figures and tables |
| Internal Review | T-3 to T-2 months | Send to 2-3 colleagues in the same field for feedback |
| Major Revision | T-2 to T-6 weeks | Restructure based on feedback; strengthen weak sections |
| Language Polish | T-6 to T-3 weeks | Refine language; eliminate padding; ensure consistency |
| Budget & Forms | T-3 to T-2 weeks | Complete budget tables; fill online system (ISIS) |
| Final Check | T-1 week | Proofread; check page limit; verify all references; PDF preview |
| Submit | Deadline day | Submit through ISIS; confirm with department admin |

**NSFC typical deadline**: March 20 (check the specific year's notice)

---

## Prompt Templates for Claude

### Template 1: Rationale Structure Review

```
I have an NSFC proposal draft for a 面上项目 in the area of [FIELD].
My scientific question is: [STATE THE QUESTION].

Please review the logic flow of my Rationale section (立项依据):
1. Does the opening paragraph establish clear strategic importance?
2. Is the literature review organized by theme (not by author)?
3. Are the identified research gaps specific and evidence-based?
4. Does the scientific question naturally follow from the gaps?
5. Are there any logical jumps or missing connections?

Here is the text of my Rationale section:
[PASTE TEXT]
```

### Template 2: Innovation Point Critique

```
Below are the innovation points from my NSFC proposal.
For each point, please evaluate:
- Is the claim specific and verifiable?
- Does it clearly differentiate from existing work?
- Would a reviewer find it convincing or empty?
Suggest concrete improvements.

Innovation points:
[PASTE INNOVATION POINTS]
```

### Template 3: Research Content Coherence Check

```
My NSFC proposal has the following structure:
- Scientific question: [QUESTION]
- Sub-task 1: [TITLE AND BRIEF DESCRIPTION]
- Sub-task 2: [TITLE AND BRIEF DESCRIPTION]
- Sub-task 3: [TITLE AND BRIEF DESCRIPTION]

Please check:
1. Does each sub-task directly contribute to answering the scientific question?
2. Are the sub-tasks logically connected to each other?
3. Is the scope appropriate for a 4-year, [AMOUNT]万 project with [N] graduate students?
4. Are there obvious gaps — aspects of the scientific question that no sub-task addresses?
```

### Template 4: Abstract Compression

```
I need to compress my NSFC proposal abstract to exactly 400 Chinese characters.
Current version: [PASTE ABSTRACT]

Requirements:
- Sentence 1: Background and problem (research context)
- Sentence 2: Proposed approach (what this project does differently)
- Sentence 3: Specific research content (3-4 concrete tasks)
- Sentence 4: Significance (theoretical + practical)
- Must include the core scientific question
- Remove all filler words and redundancy
```

---

## Simulated Review Prompt (模拟评审)

Use this prompt to have Claude simulate an NSFC panel review of your proposal.

```
You are an experienced NSFC reviewer (国家自然科学基金评审专家) in the field of
[FIELD, e.g., 交通运输工程/计算机科学/控制科学与工程].

You have reviewed 50+ proposals over the past decade. You are rigorous but fair.

Please review the following NSFC [面上项目/青年基金/重点项目] proposal and provide:

1. Overall Assessment (总体评价): A/B/C/D
   - A: Strongly recommend funding
   - B: Recommend funding
   - C: Borderline, does not recommend
   - D: Clearly should not be funded

2. Scientific Value and Innovation (科学价值与创新性, score 1-5):
   - Is the scientific question clearly stated?
   - Is it a genuine question, not a task description?
   - What is specifically new compared to existing work?

3. Feasibility (可行性, score 1-5):
   - Is the technical approach clearly described?
   - Can the proposed work be completed in [N] years?
   - Are the expected outcomes realistic?

4. Research Foundation (研究基础, score 1-5):
   - Does the PI have relevant prior work?
   - Is the team composition appropriate?
   - Are the experimental conditions adequate?

5. Writing Quality (写作质量, score 1-5):
   - Is the logic clear and the structure well-organized?
   - Are there redundancies, vague statements, or logical gaps?

6. Specific Weaknesses (具体不足):
   - List 3-5 specific problems with the proposal
   - For each problem, explain why it matters and suggest improvement

7. Verdict:
   - Would you recommend this proposal for funding? Why or why not?

Proposal text:
[PASTE FULL PROPOSAL OR RELEVANT SECTIONS]
```

---

## NSFC-Specific Terminology Reference

| English | Chinese | Usage Context |
|---------|---------|---------------|
| Scientific question | 科学问题 | The core question the proposal addresses |
| Rationale | 立项依据 | Module 1: why this research should be funded |
| Research content | 研究内容 | Module 2: what you will do |
| Research foundation | 研究基础 | Module 3: why you can do it |
| Technical approach | 技术路线 | How you will execute the research |
| Innovation points | 创新点 | What is new about your proposal |
| Expected outcomes | 预期成果 | Papers, patents, prototypes you will produce |
| Key scientific problem | 关键科学问题 | The hardest challenge in your research |
| Discipline code | 学科代码 | NSFC classification code for your research area |

---

## Related Skills

- [proposal-writing.md](proposal-writing.md) — General proposal writing principles
- [defense-prep.md](defense-prep.md) — Proposal defense preparation
- [provincial-fund.md](provincial-fund.md) — Provincial/ministry-level funding proposals
- [../literature/literature-review.md](../literature/literature-review.md) — Literature review writing (for the Rationale section)
