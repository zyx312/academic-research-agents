# Undergraduate Thesis Supervision Guide

## Purpose

This skill provides a comprehensive framework for supervising undergraduate thesis
projects (also called senior thesis, capstone, or graduation design / 本科毕业设计).
It covers the full lifecycle from topic selection through defense, with actionable
templates, meeting structures, and intervention strategies for common problems.

---

## 1. Full Timeline Overview

A standard undergraduate thesis spans 6-8 months. The timeline below assumes an
academic-year project with defense in late spring.

### Phase 1: Topic Selection and Literature Survey (Weeks 1-4)

| Week | Milestone | Advisor Action |
|------|-----------|----------------|
| 1 | Distribute topic list or brainstorm with student | Provide 3-5 candidate topics scoped to undergrad level |
| 2 | Student selects top 2 preferences | Discuss feasibility, data availability, equipment needs |
| 3 | Topic confirmed; initial literature search | Share 5-8 seed papers; teach database search techniques |
| 4 | Literature review draft (15-20 sources minimum) | Review for coverage gaps; ensure mix of seminal and recent work |

### Phase 2: Proposal and Research Design (Weeks 5-8)

| Week | Milestone | Advisor Action |
|------|-----------|----------------|
| 5 | Research question formulated | Validate specificity and testability of the question |
| 6 | Methodology outline drafted | Check feasibility: does student have skills, tools, data? |
| 7 | Proposal document completed | Provide written feedback within 3 working days |
| 8 | Proposal defense or committee review | Attend; help student prepare 10-minute presentation |

### Phase 3: Core Research and Implementation (Weeks 9-20)

| Week | Milestone | Advisor Action |
|------|-----------|----------------|
| 9-10 | Environment setup, data acquisition | Ensure lab/compute access; check IRB if human subjects |
| 11-14 | Primary experiments or development | Weekly check-ins; review intermediate results |
| 15-16 | Midterm check (formal or informal) | Compare progress against proposal timeline |
| 17-20 | Analysis, iteration, additional experiments | Push for completion; scope reduction if behind |

### Phase 4: Writing and Defense (Weeks 21-28)

| Week | Milestone | Advisor Action |
|------|-----------|----------------|
| 21-22 | First draft of thesis chapters | Provide structural feedback; do not line-edit yet |
| 23-24 | Revised draft with figures and tables | Detailed feedback on technical accuracy |
| 25-26 | Final draft; format compliance check | Verify university formatting requirements |
| 27 | Defense rehearsal | Mock Q&A with lab group |
| 28 | Thesis defense | Attend; provide post-defense revision list |

---

## 2. Topic Selection Strategies

### Scoping for Undergraduate Level

The most critical advising task is scope management. Undergraduate theses should:

- Address a single, well-defined research question
- Be completable with existing tools and data (no 6-month data collection)
- Have a clear "minimum viable thesis" that guarantees a passable outcome
- Include stretch goals for ambitious students

### Topic Sources

1. **Subset of advisor's funded project** -- carve out a self-contained sub-problem
2. **Replication studies** -- reproduce a published result with variation
3. **Tool or method comparison** -- benchmark existing approaches on new data
4. **Industry collaboration** -- partner company provides problem and data
5. **Student-initiated** -- requires extra feasibility vetting by advisor

### Red Flags in Topic Selection

- Topic requires mastering an entirely new field in one semester
- No available dataset or data collection would take more than 4 weeks
- Success depends on a single external collaborator's responsiveness
- The problem has no known baseline to compare against

---

## 3. Weekly Meeting Structure

### Recommended Format (30-45 minutes)

```
1. Progress update (5 min)
   - What was accomplished since last meeting?
   - Show concrete artifacts: code, data, figures, writing

2. Blockers and challenges (10 min)
   - Technical obstacles
   - Resource needs
   - Conceptual confusion

3. Discussion and problem-solving (15 min)
   - Advisor provides guidance, suggests approaches
   - Whiteboard or sketch solutions together

4. Next steps (5 min)
   - Define 2-3 specific deliverables for next week
   - Student writes these down during the meeting
```

### Pre-Meeting Requirements

Students should submit a brief progress note (3-5 sentences or bullet points)
at least 24 hours before the meeting. This note should cover:

- Tasks completed
- Current blockers
- Questions for the advisor

### Meeting Documentation

Maintain a shared document (Google Doc, Notion page, or lab wiki) where both
advisor and student record meeting notes and action items. This creates an
audit trail that is valuable for midterm reviews and dispute resolution.

---

## 4. Common Struggles and Interventions

### Struggle 1: Literature Review Paralysis

**Symptoms:** Student reads papers endlessly without synthesizing or moving forward.

**Intervention:**
- Set a hard deadline for literature review completion
- Require a structured summary table (paper, method, result, limitation)
- Teach the "three-pass" reading method (skim, comprehend, critique)
- Cap the number of papers at 25-30 for an undergrad thesis

### Struggle 2: Scope Creep

**Symptoms:** Student keeps adding features, datasets, or research questions.

**Intervention:**
- Return to the original proposal and research question
- Apply the "minimum viable thesis" principle
- Create a priority matrix: must-have vs nice-to-have
- Remind student that a completed focused thesis beats an incomplete broad one

### Struggle 3: Technical Roadblocks

**Symptoms:** Student stuck on debugging, environment setup, or tool learning.

**Intervention:**
- Pair with a senior graduate student for 1-2 sessions
- Suggest alternative tools or simpler approaches
- Set a time-box: if not resolved in N days, pivot approach
- Provide working example code or starter templates

### Struggle 4: Writing Avoidance

**Symptoms:** Student delays writing until the last weeks; produces poor drafts.

**Intervention:**
- Require writing to begin in parallel with research (week 14 onward)
- Assign one chapter per two weeks during writing phase
- Provide a thesis template with section headings pre-filled
- Share exemplary past theses as models

### Struggle 5: Motivation Loss

**Symptoms:** Missed meetings, late submissions, disengagement.

**Intervention:**
- Have a candid conversation about the student's situation
- Break remaining work into very small, achievable tasks
- Celebrate small wins explicitly
- If personal issues, refer to university counseling services
- Adjust expectations while maintaining minimum standards

---

## 5. Thesis Writing Template

### Standard Chapter Structure

```
Chapter 1: Introduction (3-5 pages)
  1.1 Background and motivation
  1.2 Problem statement
  1.3 Research objectives
  1.4 Thesis organization

Chapter 2: Literature Review (8-12 pages)
  2.1 Theoretical foundations
  2.2 Related work (organized thematically, not paper-by-paper)
  2.3 Research gaps and positioning

Chapter 3: Methodology (8-12 pages)
  3.1 Overall approach / framework
  3.2 Data description and collection
  3.3 Methods / algorithms / models
  3.4 Evaluation metrics

Chapter 4: Results and Analysis (10-15 pages)
  4.1 Experimental setup
  4.2 Results presentation (tables, figures)
  4.3 Analysis and discussion
  4.4 Comparison with baselines

Chapter 5: Conclusion (3-5 pages)
  5.1 Summary of contributions
  5.2 Limitations
  5.3 Future work

References (20-40 entries typical for undergrad)
Appendices (code listings, supplementary data, IRB approval)
```

### Writing Quality Checklist

- [ ] Every figure has a descriptive caption and is referenced in text
- [ ] Every table has column headers with units
- [ ] All acronyms defined at first use
- [ ] Consistent tense (past for methods/results, present for established facts)
- [ ] No orphan citations (every reference discussed, not just listed)
- [ ] Page numbers, headers, and formatting match university template

---

## 6. Grading Rubric

| Criterion | Weight | Excellent (A) | Good (B) | Adequate (C) | Poor (D/F) |
|-----------|--------|---------------|----------|---------------|------------|
| Problem formulation | 15% | Clear, novel, well-motivated | Clear, adequately motivated | Vague or overly broad | Missing or incoherent |
| Literature review | 15% | Comprehensive, synthesized | Adequate coverage | Superficial or listing | Missing major works |
| Methodology | 20% | Rigorous, well-justified | Appropriate, minor gaps | Weak justification | Flawed or absent |
| Results and analysis | 25% | Thorough, insightful | Complete, basic analysis | Incomplete analysis | Incorrect or missing |
| Writing quality | 15% | Professional, clear, polished | Minor issues | Frequent errors | Unreadable |
| Defense performance | 10% | Confident, handles questions | Adequate responses | Struggles with questions | Cannot explain work |

---

## 7. Defense Preparation

### Two Weeks Before Defense

- Finalize slide deck (15-20 slides for a 20-minute presentation)
- Structure: motivation, background, method, results, conclusion
- Ensure every slide has a clear takeaway message
- Limit text; use figures, diagrams, and tables

### One Week Before Defense

- Conduct a rehearsal with lab group or peers
- Time the presentation strictly
- Prepare for common question categories:
  - "Why did you choose this method over X?"
  - "What are the limitations of your approach?"
  - "How would you extend this work?"
  - "Can you explain this result / figure?"
  - "What did you learn from this project?"

### Day of Defense

- Arrive 15 minutes early to test projector and equipment
- Bring backup copy of slides on USB drive
- Have thesis document available for reference
- Take notes on committee feedback for revisions

---

## 8. Post-Defense Actions

1. Compile revision list from committee feedback
2. Set a 2-week deadline for final revisions
3. Submit final version to department and library
4. Discuss potential for publication (conference paper or journal letter)
5. Write a letter of recommendation if student performed well

---

## Claude Prompt Templates

### Topic Brainstorming

```
You are an academic advisor helping an undergraduate student select a thesis topic.

Context:
- Student's major: [MAJOR]
- Student's technical skills: [SKILLS]
- Advisor's research area: [AREA]
- Available resources: [RESOURCES]
- Timeline: [N] months

Generate 5 thesis topic suggestions that are:
1. Scoped appropriately for an undergraduate (single research question)
2. Completable within the timeline with existing tools and data
3. Have clear minimum viable outcomes
4. Connected to the advisor's research for effective supervision

For each topic, provide:
- Title
- One-paragraph description
- Minimum viable outcome
- Stretch goal
- Required skills and tools
- Potential data sources
```

### Literature Review Feedback

```
Review the following undergraduate thesis literature review section.

Evaluate against these criteria:
1. Coverage: Are seminal works and recent advances both included?
2. Synthesis: Does the student organize thematically rather than paper-by-paper?
3. Critical analysis: Does the student identify strengths and limitations?
4. Research gap: Does the review clearly motivate the student's own work?
5. Citation quality: Mix of journals, conferences, and appropriate recency?

Provide specific, actionable feedback with examples of how to improve.
Mark sections that need expansion and those that can be trimmed.

Literature review text:
[PASTE TEXT]
```

### Defense Preparation Coach

```
You are helping an undergraduate student prepare for their thesis defense.

Thesis title: [TITLE]
Thesis abstract: [ABSTRACT]
Key results: [RESULTS SUMMARY]

Tasks:
1. Generate 10 likely questions the committee will ask, categorized as:
   - Methodological questions
   - Results interpretation questions
   - Broader context questions
   - Future work questions

2. For each question, provide:
   - A model answer (2-3 sentences)
   - A tip for delivering it confidently

3. Identify any weak points in the abstract/results that the committee
   is likely to probe.
```

### Progress Assessment

```
Evaluate this undergraduate thesis student's progress against the expected timeline.

Current week: [WEEK N of 28]
Expected milestones by this point: [LIST]
Actual completed work: [DESCRIPTION]
Remaining deliverables: [LIST]

Provide:
1. A progress rating (on track / slightly behind / significantly behind / at risk)
2. Specific recommendations to get back on track if behind
3. Scope adjustment suggestions if significantly behind
4. A revised mini-timeline for the remaining weeks
```
