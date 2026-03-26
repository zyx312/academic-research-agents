# Responding to Reviewer Comments

> Skill for Claude Code — assists researchers in crafting professional, effective responses to peer review feedback.

## When to Use

- You have received reviewer comments from a journal or conference and need to draft a point-by-point response
- You need to write a cover letter to the editor summarizing the revision
- You want to identify which reviewer concerns are critical vs. cosmetic
- You need diplomatic language for disagreeing with a reviewer
- You are preparing a rebuttal for a conference that allows author responses (e.g., NeurIPS, ICLR, CVPR)
- You want to organize and prioritize a large set of reviewer comments into an action plan

---

## The CALM Method

A structured approach for processing and responding to reviewer feedback, adapted from Elsevier's guidelines for authors.

### Step 1: **C — Collect and Categorize**

Read ALL reviewer comments before responding to any of them. Categorize each comment:

| Category | Description | Typical Action |
|----------|-------------|----------------|
| **Critical** | Fundamental concerns about correctness, novelty, or methodology | Must address with new experiments, proofs, or major revisions |
| **Substantive** | Requests for clarification, additional analysis, or missing content | Address with text revisions and possibly minor new experiments |
| **Minor** | Typos, formatting, citation suggestions, wording improvements | Quick fixes; acknowledge and apply |
| **Misunderstanding** | Reviewer misread or misunderstood something | Clarify diplomatically — the misunderstanding is likely a writing problem |

### Step 2: **A — Analyze and Prioritize**

After categorizing, determine:
- Which comments overlap across reviewers? Shared concerns signal genuine weaknesses.
- Which critical comments can be addressed within the revision window?
- Which comments require new experiments vs. text changes only?
- Are there comments where the reviewer is factually incorrect? (Handle with extreme care.)

Create a revision plan before writing a single response. Estimate effort for each comment.

### Step 3: **L — Layout the Response**

Structure the response document systematically (see Response Document Structure below). Ensure:
- Every single comment is addressed — do not skip any, even minor ones
- Responses are self-contained: the editor should not need to flip between documents
- Changes to the manuscript are explicitly referenced with section, page, or line numbers
- New text added to the manuscript is quoted in the response so reviewers can see it without re-reading the whole paper

### Step 4: **M — Manage Tone**

The tone of your response is as important as the content. Rules:
- Thank each reviewer sincerely, even for harsh reviews
- Never be defensive, sarcastic, or dismissive
- Treat every comment as an opportunity to improve the paper
- If you disagree, provide evidence, not opinions
- If a comment stems from unclear writing, acknowledge the writing issue before providing the clarification
- Use "we" consistently — present a unified author response

---

## Response Document Structure

The complete response package typically contains three parts, assembled into a single document or submitted as separate files depending on the venue.

### Part 1: Cover Letter to Editor

This is a half-page to one-page letter summarizing the revision at a high level. The editor uses this to decide whether to send the paper back to reviewers or make an editorial decision.

**Template:**

```
Dear Editor [or "Dear Professor [Name]" if known],

Thank you for the opportunity to revise our manuscript [ID: XXXX],
titled "[Paper Title]," for [Journal/Conference Name].

We sincerely thank the reviewers for their constructive feedback,
which has significantly strengthened the paper. We have carefully
addressed all comments and made the following major changes:

1. [Major change 1 — e.g., "Added experiments on the Waymo Open
   Dataset to address Reviewer 2's concern about generalizability
   (Section 4.3, Table 3)."]
2. [Major change 2 — e.g., "Revised the introduction and related
   work to better position our contribution relative to [Author]
   et al. (2024), as suggested by Reviewer 1."]
3. [Major change 3 — e.g., "Added a computational cost analysis
   comparing our method to baselines (Section 4.5, Table 5)."]

A detailed point-by-point response to each reviewer comment is
provided below. All changes in the revised manuscript are highlighted
in [blue/tracked changes] for convenience.

We believe the revised manuscript addresses all reviewer concerns
and is now suitable for publication. We look forward to your
decision.

Sincerely,
[Authors]
```

### Part 2: Point-by-Point Response

This is the core of the rebuttal. Every reviewer comment must receive an explicit response.

**Formatting conventions:**
- Reviewer comments: **bold** or in a shaded box
- Your response: regular text
- New/revised text from the manuscript: indented block quote or colored text
- References to the manuscript: include section number, page number, and line numbers where applicable

**Template for each comment:**

```
---

**Reviewer [1/2/3], Comment [N]:**
**"[Exact text of the reviewer's comment, quoted verbatim or
faithfully paraphrased.]"**

**Response:**
Thank you for this observation. [Your response here.]

We have revised [Section X.Y / Page P / Lines L1-L2] as follows:

> "[Exact new text added to the manuscript, quoted here so the
> reviewer can read it without searching the paper.]"

---
```

**Rules for Point-by-Point Responses:**
- Address comments in the order the reviewer wrote them — do not rearrange
- Never merge multiple comments into one response unless they are truly identical
- If a comment has multiple sub-parts, respond to each sub-part separately
- If the same concern appears from multiple reviewers, respond fully to the first occurrence and cross-reference in subsequent ones: "Please see our response to Reviewer 1, Comment 3, where we address this concern in detail."
- Quantify wherever possible: "We added 3 new experiments" is stronger than "We added experiments"

### Part 3: Summary of Changes

A concise list of all modifications made to the manuscript, organized by section. This helps the editor and reviewers quickly locate changes.

**Template:**

```
## Summary of Changes

### Section 1: Introduction
- Revised the problem statement to clarify the specific gap
  addressed (Page 1, Lines 12-18)
- Added a reference to [Author] et al. (2024) as suggested
  by Reviewer 1

### Section 3: Methodology
- Added a formal definition of the noise model (Section 3.2,
  Equation 4)
- Included a figure illustrating the fusion pipeline
  (Figure 3, Page 5)

### Section 4: Experiments
- Added results on the Waymo Open Dataset (Table 3, Page 7)
- Added computational cost comparison (Table 5, Page 9)
- Included failure case analysis (Section 4.6, Figure 7)

### Section 5: Discussion
- Added a paragraph discussing limitations of the approach
  under extreme weather (Page 10, Lines 8-22)

### Minor Corrections
- Fixed typos on Pages 2, 5, and 8
- Updated Figure 2 caption for clarity
- Corrected reference formatting throughout
```

---

## Response Strategies by Comment Type

### "Lack of Novelty"

This is the most damaging critique. Respond by sharpening the distinction from prior work.

**Strategies:**
1. Identify the specific prior work the reviewer considers overlapping and explain the concrete technical differences
2. Provide a comparison table: your method vs. the cited prior work, listing dimensions where they differ (problem setting, architecture, loss function, data, evaluation)
3. If the reviewer missed a key novelty, clarify it — but first acknowledge that your original writing may not have made it clear enough
4. Add or strengthen the contributions list in the introduction

**Example phrases:**
- "We appreciate the reviewer raising this important distinction. While [Author] et al. also address [problem], their approach differs from ours in three key ways: (1)..., (2)..., (3)..."
- "We acknowledge that our original manuscript did not sufficiently highlight the distinction from [prior work]. We have revised Section 2 to explicitly clarify..."
- "To our knowledge, our work is the first to [specific novel element]. We have added a comparison table (Table 2) that makes this distinction clearer."

### "Insufficient Experiments"

Reviewers want more evidence. Determine what is feasible within the revision window.

**Strategies:**
1. If the requested experiment is feasible, run it and report results. This is the strongest response.
2. If the requested experiment is partially feasible, provide what you can and explain the limitation honestly.
3. If the requested experiment is infeasible (requires resources or time you do not have), explain why and offer an alternative analysis that partially addresses the concern.
4. If you believe the existing experiments are sufficient, explain why with a clear argument — but also add something to show good faith.

**Example phrases:**
- "Following the reviewer's suggestion, we conducted experiments on [dataset/scenario]. The results (Table X) confirm that..."
- "We agree that evaluation on [benchmark] would strengthen the paper. We have added these results in Table X, which show..."
- "Running the full experiment on [X] requires [resource/time constraint]. As an alternative, we provide [analysis/ablation] that addresses the underlying concern about [Y]."

### "Writing Unclear"

This is an invitation to improve, not a personal attack. The reviewer is telling you where communication failed.

**Strategies:**
1. Never argue that the writing was clear. If a reviewer found it unclear, other readers will too.
2. Rewrite the flagged passages and include the new text in your response.
3. If the confusion stems from missing background, add a brief explanation or a reference.
4. Consider adding a figure or example to illustrate the concept.

**Example phrases:**
- "We agree that this passage was unclear and have rewritten Section X.Y for clarity. The revised text reads: [quote new text]."
- "Thank you for pointing this out. We have added an illustrative example (Example 1, Page X) to clarify the concept."
- "We have reorganized this section to improve the logical flow, moving [topic] before [topic] so that the prerequisites are established first."

### "Missing Related Work"

Usually straightforward to address. Add the references and discuss them.

**Strategies:**
1. Read the suggested papers carefully and cite them appropriately
2. Add a paragraph or sentences in the related work section positioning your work relative to the newly cited papers
3. If the suggested paper is actually not relevant, explain why politely but cite it anyway if possible as a sign of good faith

**Example phrases:**
- "Thank you for bringing [Author] et al. to our attention. We have added a discussion of this work in Section 2 and clarified how our approach differs: [brief explanation]."
- "We have incorporated this reference and updated our related work section. [Author] et al. address [problem X], while our work focuses on [problem Y]. We now explicitly discuss this distinction on Page X."

### "Methodology Concerns"

Reviewers may question the soundness of your approach, the validity of assumptions, or the correctness of derivations.

**Strategies:**
1. If the concern is valid, acknowledge it and fix it. Add a proof, derivation, or clarification.
2. If the concern is based on a misunderstanding, provide a clear explanation with additional detail (possibly in the appendix).
3. If an assumption is questioned, justify it with evidence from literature or your own analysis showing it holds in your setting.
4. Add formal proofs or derivations in supplementary material if the main paper lacks space.

**Example phrases:**
- "The reviewer raises a valid concern about Assumption 2. We have added Proposition 1 (Appendix A) proving that this assumption holds when [condition]. In practice, this condition is satisfied in [X]% of cases in our benchmark."
- "We have added a detailed derivation in Appendix B to clarify the step from Equation 3 to Equation 4."
- "We agree that the original description was ambiguous. We have revised Section 3.2 to include a formal problem statement with explicit assumptions."

### "Statistical Issues"

Concerns about significance, variance, reproducibility, or evaluation protocol.

**Strategies:**
1. Add error bars, confidence intervals, or standard deviations if missing
2. Report results over multiple runs (3-5 runs with different seeds is standard)
3. Perform statistical significance tests if the reviewer requests them
4. Clarify the evaluation protocol (train/val/test splits, cross-validation, etc.)

**Example phrases:**
- "We have re-run all experiments 5 times with different random seeds. The results in Table X now include standard deviations. Our method's improvement of X.X +/- Y.Y over the baseline is statistically significant (p < 0.01, paired t-test)."
- "We have added confidence intervals to all reported metrics and included a statistical significance analysis in Appendix C."

### "Scope Too Broad / Too Narrow"

The reviewer feels the paper tries to cover too much (broad) or the contribution is too limited (narrow).

**Strategies for "too broad":**
- Narrow the claims to match the evidence
- Remove tangential content and focus on the core contribution
- Reframe the paper around one clear message

**Strategies for "too narrow":**
- Add experiments on additional datasets or tasks to show generalizability
- Discuss how the approach extends to related problems
- Add an analysis section showing the method's behavior across different conditions

**Example phrases:**
- "We agree that the original manuscript attempted to address too many aspects simultaneously. We have narrowed the scope to focus on [core contribution] and removed Section X, which was tangential."
- "To demonstrate broader applicability, we have added experiments on [Dataset B] and [Dataset C] (Table X), showing that our method generalizes beyond [original scope]."

---

## Diplomatic Language Guide

Replace aggressive or defensive phrasing with professional alternatives:

| Avoid | Use Instead |
|-------|-------------|
| "The reviewer is wrong about..." | "We respectfully clarify that..." |
| "The reviewer clearly did not read..." | "We may not have communicated this clearly. To clarify..." |
| "This is obvious from the paper." | "We agree this point deserves emphasis and have revised the text to make it more explicit." |
| "We disagree." | "We appreciate this perspective. Our reasoning is as follows..." |
| "The reviewer's suggestion is not feasible." | "We considered this direction carefully. Due to [specific reason], we opted for [alternative]. We have added a discussion of this tradeoff in Section X." |
| "This was already in the paper." | "Thank you for raising this. This is discussed in Section X.Y (Page P, Line L). To improve visibility, we have [added a forward reference / moved the discussion / added emphasis]." |
| "We don't think this experiment is necessary." | "We agree that additional evidence strengthens the paper. We have added [related analysis] to address this concern." |
| "The reviewer misunderstood our method." | "We realize our description may have been ambiguous. We have revised Section X to clarify..." |
| "No changes needed." | "We have strengthened this aspect by [specific action], though we believe the core approach remains sound." |

**General rules:**
- Always lead with agreement or gratitude before any correction
- Frame disagreements as clarifications, not contradictions
- Use "we clarify" instead of "we correct"
- Attribute confusion to your own writing, not to the reviewer's reading
- Never write a one-word or one-sentence response — elaborate enough to show you took the comment seriously

---

## When to Push Back (and How)

Sometimes reviewers are genuinely wrong, request infeasible work, or misunderstand the paper's scope. You can and should push back in these cases, but diplomatically.

### When It Is Appropriate to Push Back

- The reviewer asks for experiments outside the paper's declared scope
- The reviewer makes a factual error about your method or results
- The reviewer requests a comparison against a method designed for a fundamentally different problem
- The requested revision would require resources (compute, data, time) well beyond what is reasonable
- The reviewer's suggestion would actually weaken the paper

### How to Push Back Effectively

1. **Acknowledge first.** Show you understand the reviewer's concern and took it seriously.
2. **Provide evidence.** Support your position with citations, data, or logical arguments — never just opinions.
3. **Offer a compromise.** Even if you do not do exactly what was asked, do something that partially addresses the concern.
4. **Be concise.** Lengthy defenses read as defensive. State your case clearly and move on.

**Template for pushing back:**

```
We appreciate the reviewer's suggestion to [X]. We carefully
considered this approach and note that [evidence/reasoning for
why it is not appropriate in this context]. Specifically, [concrete
reason 1] and [concrete reason 2].

As a compromise, we have [action taken that partially addresses the
concern]. We believe this addresses the reviewer's underlying
concern about [the real issue behind the suggestion].
```

**Example:**

"We appreciate the suggestion to compare against [Method X]. However, [Method X] is designed for indoor scene understanding with RGB-D input, while our work targets outdoor autonomous driving with LiDAR-camera fusion. A direct comparison would not be meaningful due to the fundamentally different input modalities and operating conditions. Instead, we have added a comparison with [Method Y], which addresses a similar outdoor setting (Table 4). We have also added a discussion in Section 2 clarifying the distinction between indoor and outdoor fusion methods."

---

## Conference Rebuttal Specifics

Conference rebuttals (NeurIPS, ICLR, CVPR, ECCV, etc.) have unique constraints:

- **Strict word/page limits:** Often 500-1000 words. Be extremely concise.
- **No major revisions possible:** You cannot submit a revised paper. Promise only what you can include in the camera-ready version.
- **Focus on factual corrections:** Prioritize correcting misunderstandings and providing clarifications. Do not try to address every minor point.
- **Lead with the strongest argument:** Put your most compelling response first. Reviewers may not read the entire rebuttal.
- **Use structured formatting:** Numbered responses matching reviewer comments. Reviewers skim — make it easy.

**Template for conference rebuttal:**

```
We thank all reviewers for their detailed feedback. We address
the main concerns below.

**[R1, R3] Concern about X:**
[Concise response with evidence]

**[R2] Question about Y:**
[Concise response]

**[R1] Missing comparison with Z:**
[Response, possibly with new results if you ran quick experiments]

We will incorporate all suggested improvements in the camera-ready
version.
```

---

## Prompt Templates for Claude

### 1. Categorize and Prioritize Comments

```
Here are the reviewer comments for my paper. Categorize each
comment as Critical, Substantive, Minor, or Misunderstanding.
For each comment, suggest an action (new experiment, text revision,
clarification, or quick fix) and estimate the effort (high/medium/low).

Reviewer 1:
[paste comments]

Reviewer 2:
[paste comments]

Reviewer 3:
[paste comments]
```

### 2. Draft Point-by-Point Response

```
Draft a point-by-point response to the following reviewer comment.
Use this format:
- Quote the reviewer comment in bold
- Write a diplomatic response that addresses the concern
- If text changes are needed, draft the new text to be inserted
- Reference specific sections and page numbers from the paper

My paper is about: [brief description]
The reviewer's comment:
[paste comment]
Relevant section of my paper:
[paste the section the comment refers to]
```

### 3. Diplomatic Rephrasing

```
Rephrase the following draft response to be more diplomatic and
professional. Keep the substance but soften the tone. Ensure I
acknowledge the reviewer's perspective before presenting my own.

My draft response:
[paste your draft response]
```

### 4. Cover Letter Drafting

```
Based on the following reviewer comments and our responses, draft
a cover letter to the editor summarizing the major revisions.
List 3-5 high-level changes. Keep the letter under one page.

Reviewer comments and our responses:
[paste the complete response document]
```

### 5. Conference Rebuttal Compression

```
I have a detailed response to reviewer comments but need to
compress it into a [500/800/1000]-word conference rebuttal.
Prioritize responses to critical concerns and factual corrections.
Drop minor issues. Use the format: **[R#] Concern:** followed by
a concise response.

Full response:
[paste full response]
```

---

## Self-Review Before Submission

### Pre-Submission Self-Review Prompt (from ChatGPT-Academic-Prompt)

Use this prompt to simulate a critical peer review of your own paper before submitting. This helps identify weaknesses that reviewers will catch.

```
The task for you is to write a thorough paper review, as if you were a
senior scientist in the field. The paper under review is on the topic of
[TOPIC]. Please evaluate the following aspects:

1. Summary: Provide a brief summary of the paper's main contributions.
2. Strengths: List the key strengths of the paper (3-5 points).
3. Weaknesses: List the key weaknesses of the paper (3-5 points).
4. Questions for the authors: List specific questions that need
   clarification.
5. Suggestions for improvement: Provide actionable recommendations.
6. Minor issues: Note any typos, formatting issues, or unclear passages.
7. Overall assessment: Rate the paper as Strong Accept / Accept /
   Weak Accept / Borderline / Weak Reject / Reject, with justification.
8. Confidence: Rate your confidence in this review (1-5).

Paper content:
[PASTE YOUR PAPER OR KEY SECTIONS]
```

**When to use this**:
- 1-2 weeks before the submission deadline, after completing a full draft
- After all co-authors have reviewed, as a final quality check
- Before resubmission to a new venue after rejection (to check if you fixed the issues)

### Generating Point-by-Point Response Drafts

When you receive actual reviews, use this prompt to generate a first-draft response:

```
I received the following reviewer comments for my paper on [TOPIC],
submitted to [VENUE]. The decision is [DECISION].

For each reviewer comment below, draft a point-by-point response that:
1. Quotes the reviewer comment verbatim
2. Thanks the reviewer for the specific point raised
3. States whether we agree, partially agree, or respectfully disagree
4. Describes the specific action taken (with section/page references)
5. Includes draft text for any new paragraphs added to the manuscript
6. Uses diplomatic, professional language throughout

Reviewer comments:
[PASTE ALL REVIEWER COMMENTS]

My paper's key method: [BRIEF METHOD DESCRIPTION]
Key results: [BRIEF RESULTS SUMMARY]
```

### Anticipating Reviewer Concerns

Before submission, use this prompt to predict likely reviewer objections:

```
Based on the following paper summary, predict the top 5 concerns
a critical reviewer would raise. For each predicted concern, suggest
a preemptive action I can take before submission.

Paper topic: [TOPIC]
Method: [METHOD SUMMARY]
Evaluation: [DATASETS AND METRICS USED]
Main claims: [LIST 3-4 CLAIMS]
Known limitations: [LIMITATIONS YOU ARE AWARE OF]
```

---

## References

- Elsevier, "How to Respond to Reviewer Comments: A Practical Guide," Researcher Academy
- Noble, "Ten Simple Rules for Writing a Response to Reviewers," PLOS Computational Biology, 2017
- Borja, "Writing the Response to Reviewers Document," International Microbiology, 2015
- Williams & Colomb, "Style: Lessons in Clarity and Grace," Pearson, 12th Edition
- Silvia, "How to Write a Lot," APA LifeTools, 2nd Edition

## Related Skills

- [revision.md](revision.md) — Revising the manuscript itself based on reviewer feedback
- [cover-letter.md](cover-letter.md) — Revision cover letters
- [../peer-review/review-writing.md](../peer-review/review-writing.md) — Understanding the reviewer's perspective
