# Manuscript Revision Strategy

## Purpose

This skill provides a systematic framework for revising academic manuscripts after peer review. It covers triaging reviewer comments, planning revisions, writing response letters, managing tracked changes, handling major vs. minor revisions, and developing resubmission strategies. A well-executed revision is often the difference between acceptance and rejection.

## Related
- [rebuttal.md](rebuttal.md) - Write rebuttal letters (for conference papers)
- [research-paper.md](research-paper.md) - Original paper writing
- [cover-letter.md](cover-letter.md) - Revision cover letters

---

## Understanding the Decision Letter

### Decision Types

| Decision | Meaning | Typical Expectation |
|----------|---------|-------------------|
| **Accept** | Paper accepted as-is | Rare on first submission; prepare camera-ready |
| **Minor Revision** | Small changes needed | Address all comments; usually no re-review, 2-4 weeks |
| **Major Revision** | Substantial changes needed | Significant work required; likely re-reviewed, 2-3 months |
| **Revise and Resubmit (R&R)** | No guarantee of acceptance | Treat as a new submission with guidance; 3-6 months |
| **Reject with Encouragement** | Not accepted but potential seen | Consider major overhaul and resubmission |
| **Reject** | Not suitable for this journal | Consider a different venue after revision |

### Reading the Decision Letter
1. Read the editor's letter first -- it synthesizes and prioritizes reviewer input
2. Read ALL reviews completely before reacting emotionally
3. Wait 24-48 hours before starting to respond (avoid defensive reactions)
4. Read the reviews again with fresh eyes after the waiting period
5. Identify the editor's own requirements -- these override reviewer suggestions

---

## Step 1: Triage Reviewer Comments

### The Three-Category System

Sort every reviewer comment into one of three categories:

#### Category A: Must-Fix (Address Fully)
- Factual errors in the manuscript
- Missing important references or comparisons
- Methodological concerns raised by multiple reviewers
- Requests explicitly supported by the editor
- Additional experiments that are feasible and valuable
- Clarity issues that genuinely improve the paper
- Compliance requirements (ethics statements, data availability)

#### Category B: Nice-to-Have (Address Reasonably)
- Suggestions that improve the paper but are not essential
- Requests for additional analysis that add value
- Minor restructuring suggestions
- Cosmetic improvements (wording, figure aesthetics)
- Additional context or discussion points

#### Category C: Push-Back (Decline Diplomatically)
- Requests based on misunderstanding of your method
- Demands that fundamentally change your paper's scope
- Requests for experiments that are infeasible within the revision window
- Suggestions that contradict other reviewers' preferences
- Opinions about style or structure where alternatives are equally valid

### Triage Spreadsheet Template

Create a spreadsheet with these columns:

```
| # | Reviewer | Comment Summary | Category | Action Required |
|   |          |                 | (A/B/C)  | What to do      |
|---|----------|-----------------|----------|-----------------|
| Status | Who Does It | Deadline | Where in Paper | Response Draft |
| (todo/done) | (author) | (date) | (section/page) | (brief notes)  |
```

### Priority Rules
1. **If the editor specifically mentions a concern** -> Category A, highest priority
2. **If multiple reviewers raise the same issue** -> Category A, indicates a real problem
3. **If a comment requires new experiments** -> Assess feasibility early; start immediately
4. **If you disagree but the comment is reasonable** -> Address it anyway; reviewers are your test audience

---

## Step 2: Plan the Revision

### Revision Planning Checklist

- [ ] All comments triaged into A/B/C categories
- [ ] New experiments/analyses identified and feasibility assessed
- [ ] Timeline created with milestones
- [ ] Responsibilities assigned among co-authors
- [ ] Draft response letter structure prepared
- [ ] Revised manuscript outline with planned changes mapped to sections

### Timeline Management

#### Minor Revision (typically 2-4 weeks deadline)

| Week | Tasks |
|------|-------|
| 1 | Triage comments, draft responses, make text corrections |
| 2 | Complete all changes, finalize response letter |
| 3 | Internal review by co-authors, polish |
| 4 | Submit revised manuscript + response letter |

#### Major Revision (typically 2-3 months deadline)

| Week | Tasks |
|------|-------|
| 1-2 | Triage, plan, start new experiments/analysis |
| 3-6 | Run new experiments, collect and analyze results |
| 7-8 | Revise manuscript with new content |
| 9-10 | Draft response letter, internal review |
| 11-12 | Polish, final co-author review, submit |

### When to Request a Deadline Extension
- If new experiments genuinely require more time
- If a co-author has an unavoidable conflict
- Request as early as possible, with a specific new deadline
- Most editors will grant a reasonable extension (2-4 weeks)
- Do NOT request an extension in the final days before the deadline

---

## Step 3: Revise the Manuscript

### Revision Best Practices

#### What to Change
- Fix every factual error or unclear passage identified
- Add requested analyses and experiments when feasible
- Strengthen arguments where reviewers found them weak
- Expand sections where reviewers wanted more detail
- Add missing references and comparisons
- Improve figures and tables based on feedback

#### How to Track Changes
- Use Word's Track Changes feature or LaTeX `\changes` / `latexdiff`
- Create TWO versions of the revised manuscript:
  1. **Clean version**: The final revised paper (for publication)
  2. **Tracked version**: Shows all changes with highlights (for reviewers)
- Color-code changes if responding to multiple reviewers:
  - Blue: Changes for Reviewer 1
  - Red: Changes for Reviewer 2
  - Green: Changes for Reviewer 3
  - Purple: Changes for editor comments

#### LaTeX Change Tracking with `latexdiff` (Detailed)

`latexdiff` is the standard tool for generating tracked-changes PDFs from LaTeX sources. Many journals and reviewers expect a diff PDF showing exactly what changed.

**Installation**:
```bash
# macOS (via Homebrew)
brew install latexdiff

# Ubuntu/Debian
sudo apt-get install latexdiff

# Windows: included with TeX Live and MiKTeX
```

**Basic usage**:
```bash
# Generate a diff .tex file highlighting all changes
latexdiff old_version.tex new_version.tex > diff.tex

# Compile the diff file to PDF
pdflatex diff.tex
bibtex diff
pdflatex diff.tex
pdflatex diff.tex
```

**Handling multi-file projects** (with `\input{}` or `\include{}`):
```bash
# Flatten first, then diff
latexdiff-vc --flatten --git -r HEAD~1 main.tex
# Or manually:
latexpand old/main.tex > old_flat.tex
latexpand new/main.tex > new_flat.tex
latexdiff old_flat.tex new_flat.tex > diff.tex
```

**Common options**:
```bash
# Use a specific markup style
latexdiff --type=CFONT old.tex new.tex > diff.tex    # Default: color + font
latexdiff --type=UNDERLINE old.tex new.tex > diff.tex # Underline additions
latexdiff --type=CHANGEBAR old.tex new.tex > diff.tex # Margin bars

# Exclude certain environments from diffing (e.g., equations, figures)
latexdiff --exclude-textcmd="texttt" old.tex new.tex > diff.tex

# For documents with complex math
latexdiff --math-markup=0 old.tex new.tex > diff.tex
```

**Common issues and fixes**:
- If `diff.tex` fails to compile, try `--math-markup=0` (disables math diffing)
- For `\bibliography{}` changes, regenerate `.bbl` files from both versions
- If using `subfiles` or `standalone`, flatten before diffing
- Color clashes with `hyperref`: load `hyperref` after `latexdiff` preamble

**Manual markup with soul package** (when latexdiff is problematic):
```latex
\usepackage{soul}
\usepackage{xcolor}
\newcommand{\revA}[1]{\textcolor{blue}{#1}}    % Reviewer 1
\newcommand{\revB}[1]{\textcolor{red}{#1}}      % Reviewer 2
\newcommand{\deleted}[1]{\st{#1}}               % Deleted text
```

### Adding New Content During Revision

When adding new experiments or analysis:
- Ensure new results are integrated naturally, not appended awkwardly
- Update the Abstract, Introduction, and Conclusion to reflect new content
- Add new figures/tables with proper references in the text
- Update the Related Work if reviewers suggested new references
- Revise contribution claims if the scope has changed

### Handling Contradictory Reviewer Comments

When Reviewer 1 says "add more detail" and Reviewer 2 says "too long":
1. Identify the specific aspect each reviewer is addressing
2. Address the substance of both: add detail where needed, cut elsewhere
3. In your response, acknowledge both perspectives and explain your balance
4. Let the editor know you received conflicting advice and describe your resolution

---

## Step 4: Write the Response Letter

### Response Letter Structure

```
Dear [Editor Name],

Thank you for the opportunity to revise our manuscript entitled
"[Title]" (Manuscript ID: [ID]). We sincerely appreciate the
constructive feedback from the reviewers, which has significantly
improved our manuscript.

We have addressed all comments point-by-point below. For clarity:
- Reviewer comments are shown in [italic/bold]
- Our responses are shown in regular text
- Changes to the manuscript are indicated with [page/line numbers]
- New or revised text is shown in [blue/highlighted] in the
  tracked-changes version

[Note: A summary of major changes can optionally go here]

---

## Response to Reviewer 1

**Comment 1.1**: [Paste the reviewer's exact comment]

**Response**: [Your response]

We thank the reviewer for this comment. [Address the substance].
In the revised manuscript, we have [specific change made].
Please see [Section X, page Y, lines Z-W] for the updated text.

[If you added a figure/table]: We have added [Figure X / Table Y]
to address this point (see page Z).

[If you ran a new experiment]: We conducted [new experiment] as
suggested. The results show [findings], which are now presented
in [Section X].

---

**Comment 1.2**: [Next comment]
...

## Response to Reviewer 2
...

## Response to Editor Comments (if any)
...
```

### Response Writing Principles

#### Tone and Style
- **Always thank first**: "We thank the reviewer for this insightful comment"
- **Be respectful**: Even for misguided comments, treat them as opportunities
- **Be specific**: Reference exact sections, pages, and line numbers
- **Be concise**: Answer the question directly, then provide detail
- **Never be defensive**: "The reviewer misunderstood..." -> "We apologize for the lack of clarity..."

#### Responding to Each Category

**Category A (Must-Fix)**:
```
We agree with the reviewer and have [made the following changes].
The revised [section/figure/analysis] can be found on page X.
[Briefly explain what was changed and why it improves the paper.]
```

**Category B (Nice-to-Have)**:
```
We appreciate this suggestion and have incorporated it by
[description of change]. See [location in revised manuscript].
```

**Category C (Push-Back)**:
```
We thank the reviewer for raising this point. After careful
consideration, we respectfully maintain our current approach for
the following reasons:

1. [Reason 1 with evidence/references]
2. [Reason 2 with evidence/references]

However, we have added a discussion of this alternative perspective
in [Section X, page Y] to provide readers with a more complete
picture. We hope this addresses the reviewer's concern.
```

### How to Disagree Professionally

**Never say**: "The reviewer is wrong about..."
**Instead say**: "We appreciate this perspective. We would like to clarify that..."

**Never say**: "This request is unreasonable because..."
**Instead say**: "While we recognize the value of this suggestion, [practical constraint] prevents us from implementing it in the current study. We have acknowledged this as a limitation and avenue for future work."

**Never say**: "The reviewer clearly did not read our paper carefully."
**Instead say**: "We apologize that our original presentation was not clear on this point. We have revised [section] to better explain [concept]."

### Formatting Tips for Response Letters
- Number all comments consistently (e.g., R1.1, R1.2, R2.1)
- Use clear visual separation between reviewer comments and your responses
- Bold or italicize reviewer comments to distinguish them
- Include direct quotes from the revised manuscript when helpful
- Keep the response letter as a separate document from the manuscript
- Typical length: 5-20 pages depending on the number of comments

---

## Step 5: Quality Control Before Resubmission

### Pre-Resubmission Checklist

- [ ] Every reviewer comment has a response (none skipped)
- [ ] All Category A changes are implemented in the manuscript
- [ ] Category C push-backs are justified with evidence/references
- [ ] Tracked changes version matches the response letter claims
- [ ] Clean version has all track-changes accepted and formatting is correct
- [ ] New references are added to the bibliography
- [ ] Abstract updated to reflect any scope changes
- [ ] Figures and tables updated and referenced correctly
- [ ] Page numbers and line numbers in response letter are accurate
- [ ] Response letter proofread for tone (professional, not defensive)
- [ ] All co-authors have reviewed and approved the revision
- [ ] Cover letter for revision is prepared
- [ ] Supplementary materials updated if applicable

### Common Revision Mistakes
1. **Missing a comment**: Reviewers notice and editors take it seriously
2. **Superficial changes**: Adding a sentence where a paragraph is needed
3. **Inconsistency**: Changing something in one section but not updating related sections
4. **Wrong tone**: Being defensive or dismissive alienates reviewers
5. **Over-revising**: Changing things no reviewer asked about (raises new concerns)
6. **Wrong file versions**: Submitting the draft version instead of the final
7. **Stale tracked changes**: Not regenerating the diff from the correct baseline
8. **Ignoring the editor**: Editor comments take priority over reviewer comments

---

## Handling Special Situations

### When You Are Rejected

1. **Do not submit elsewhere immediately**: Take time to genuinely revise
2. Read reviews carefully for actionable feedback even in rejection
3. Consider whether a different type of journal is more appropriate
4. Make substantial revisions before resubmitting elsewhere
5. Do NOT submit the same manuscript to another journal without changes
6. If you resubmit to the same journal, it is treated as a new submission

### When You Receive Conflicting Reviews

- Identify the substance of each disagreement
- Check if the editor's letter favors one side
- Address both perspectives in your response
- If truly contradictory, implement the more conservative option
- Ask the editor for guidance if the conflict is irreconcilable

### When Additional Experiments Are Requested

- Assess feasibility within the revision timeline
- If feasible: run the experiment and present results fully
- If partially feasible: run what you can and explain constraints
- If infeasible: explain why with specifics (not just "too hard")
  - e.g., "This experiment requires [specific resource] which is unavailable"
  - Offer an alternative analysis that addresses the underlying concern
- Always offer to include the suggestion as future work

### Second Round of Reviews (R2)

If you receive another round of reviews after major revision:
- Typically, reviewers will focus on whether their original comments were addressed
- New comments at R2 are rarer and usually minor
- The same response letter format applies
- Address new comments with the same rigor
- Do NOT introduce major new content at R2 unless the editor requests it

### Escalation: Appealing an Editor's Decision

- Appeals are rare and should be reserved for clear errors
- Write a formal appeal letter to the editor-in-chief
- State specific factual errors in the review or decision process
- Provide evidence (references, data) supporting your case
- Be professional -- never attack reviewers personally
- Accept the outcome gracefully if the appeal is denied

---

## Timeline and Deadline Management

### Key Dates to Track

```
| Milestone | Date | Status |
|-----------|------|--------|
| Decision received | [DATE] | Done |
| Cool-off period ends | [DATE + 2 days] | Done |
| Triage complete | [DATE] | |
| New experiments started | [DATE] | |
| New experiments complete | [DATE] | |
| Manuscript revision draft | [DATE] | |
| Response letter draft | [DATE] | |
| Co-author review | [DATE] | |
| Final polish | [DATE] | |
| Submission deadline | [DATE] | |
| Target submission (2 days early) | [DATE] | |
```

### Buffer Time
- Always plan to submit 2-3 days before the deadline
- Allow 3-5 days for co-author review of the revision
- Allow 1-2 days for formatting and upload issues
- System downtime and upload errors happen at deadlines

---

## Polishing Revised Text

After making substantive changes, polish the revised passages for academic quality. Use these prompts from the gpt_academic project.

### English Polishing Prompt for Revised Sections

```
Below is a paragraph from a revised academic paper. This text was
rewritten to address reviewer feedback. Polish the writing to meet
the academic style, improve the spelling, grammar, clarity, concision
and overall readability. When necessary, rewrite the whole sentence.
Firstly, you should provide the polished paragraph. Secondly, you should
list all your modification and explain the reasons to do so in markdown table.

Revised paragraph:
[PASTE YOUR REVISED PARAGRAPH]
```

### Chinese Polishing Prompt for Revised Sections

```
作为一名中文学术论文写作改进助理，你的任务是改进所提供文本的拼写、语法、清晰、
简洁和整体可读性，同时分解长句，减少重复，并提供改进建议。请先提供文本的更正版本，
然后在markdown表格中列出修改的内容，并给出修改的理由。

修改后的段落：
[粘贴你修改后的段落]
```

### Consistency Check After Revision

```
I have revised my paper based on reviewer feedback. Here are the key
changes I made:
[LIST OF CHANGES WITH SECTION REFERENCES]

Please check the following sections for internal consistency:
1. Abstract — does it still accurately reflect the paper content?
2. Introduction contributions list — do they match the actual results?
3. Conclusion — does it match the revised claims?
4. Cross-references — are section/figure/table numbers still correct?

Abstract: [PASTE]
Introduction contributions: [PASTE]
Conclusion: [PASTE]
```

---

## Prompt Templates for Claude

### Triage Reviewer Comments
```
I received reviews for my paper "[TITLE]" submitted to [JOURNAL].
The decision is: [MAJOR REVISION / MINOR REVISION / R&R].

Here are the reviewer comments:

Reviewer 1:
[PASTE ALL COMMENTS]

Reviewer 2:
[PASTE ALL COMMENTS]

Editor comments:
[PASTE EDITOR COMMENTS]

Please help me:
1. Categorize each comment as: A (must-fix), B (nice-to-have), or C (push-back candidate)
2. Identify comments that multiple reviewers raise (highest priority)
3. Flag any comments that require new experiments or analysis
4. Identify contradictory comments between reviewers
5. Suggest a priority order for addressing the comments
6. Estimate the scope of work (minor vs. major effort for each)
```

### Draft Response to a Specific Comment
```
Reviewer [NUMBER] said:
"[EXACT REVIEWER COMMENT]"

Context: My paper is about [TOPIC], and this comment refers to [SECTION/ASPECT].

I plan to respond by [YOUR PLANNED ACTION].

Please help me draft a professional response that:
1. Thanks the reviewer appropriately
2. Addresses the substance of the comment
3. Describes the specific changes made (or justifies not making them)
4. References the relevant section/page in the revised manuscript
5. Maintains a respectful, non-defensive tone
```

### Write Complete Response Letter
```
I have categorized all reviewer comments and planned my responses:

[PASTE YOUR TRIAGE SPREADSHEET OR CATEGORIZED COMMENTS WITH PLANNED ACTIONS]

Please draft a complete point-by-point response letter that:
1. Opens with a professional summary of key changes
2. Addresses every comment numbered consistently (R1.1, R1.2, etc.)
3. Uses appropriate response formats for accept/revise/push-back
4. References specific sections, pages, and figures in the revised manuscript
5. Maintains consistent professional tone throughout
6. Flags where I need to insert specific data or page numbers
```

### Handle a Difficult Review
```
I received this reviewer comment that I disagree with:
"[PASTE THE COMMENT]"

My reasons for disagreeing:
[YOUR REASONS]

Please help me draft a response that:
1. Acknowledges the reviewer's perspective
2. Explains my position with evidence and references
3. Offers a compromise (e.g., adding a discussion paragraph)
4. Maintains a professional, non-defensive tone
5. Avoids creating adversarial dynamics with the reviewer
```

### Plan Revision Timeline
```
I received a [DECISION TYPE] for my paper at [JOURNAL].
The revision deadline is [DATE], which gives me [X] weeks.

The required changes include:
- [LIST OF REQUIRED CHANGES WITH ESTIMATED EFFORT]

Number of co-authors: [X]
New experiments needed: [YES/NO, describe if yes]

Please help me create:
1. A week-by-week revision timeline
2. Task assignments (what can be parallelized)
3. Milestones for checking progress
4. A plan for quality control before resubmission
5. Contingency if a new experiment takes longer than expected
```
