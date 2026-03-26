# Data Annotation Guidelines Guide

## Purpose

This skill provides a comprehensive framework for designing annotation schemas,
writing annotation guidelines, training annotators, measuring quality through
inter-annotator agreement, and managing annotation projects for machine learning
research. It covers tools, workflows, and best practices for producing
high-quality labeled datasets.

---

## 1. Annotation Schema Design

### Design Principles

1. **Mutual exclusivity:** Each data point should belong to exactly one category
   (unless multi-label is explicitly designed)
2. **Exhaustiveness:** The schema should cover all possible cases in the data
3. **Clarity:** Categories must be unambiguously defined
4. **Granularity:** Choose a level of detail appropriate for the task
5. **Consistency:** Schema should produce the same labels regardless of annotator

### Schema Design Process

```
Step 1: Define the task
  - What downstream ML task will use these annotations?
  - What is the minimum annotation granularity needed?
  - What output format does the model expect?

Step 2: Draft initial categories
  - Start with broad categories based on domain knowledge
  - Review existing annotation schemas in related work
  - Consult with domain experts

Step 3: Pilot annotation
  - Annotate 50-100 samples yourself
  - Identify ambiguous cases and edge cases
  - Refine category definitions based on difficulties encountered

Step 4: Iterate
  - Have 2-3 different people annotate the same pilot set
  - Compare disagreements and discuss resolution
  - Update schema and guidelines to resolve ambiguities

Step 5: Finalize
  - Lock the schema version
  - Document all decisions and their rationale
  - Create the formal annotation guidelines document
```

### Common Annotation Task Types

| Task | Schema Elements | Output Format |
|------|----------------|---------------|
| Image classification | Class labels, hierarchy | Label per image |
| Object detection | Bounding box + class | [x, y, w, h, class] per object |
| Semantic segmentation | Pixel-level class labels | Mask per class |
| Instance segmentation | Pixel-level instance + class | Mask per instance |
| Text classification | Category labels | Label per document/sentence |
| Named entity recognition | Entity types + boundaries | BIO/BIOES tags |
| Sequence labeling | Token-level labels | Label per token |
| Relation extraction | Entity pairs + relation type | (entity1, relation, entity2) |

---

## 2. Annotation Guidelines Document Template

### Structure

```
Annotation Guidelines v[VERSION]
Project: [PROJECT NAME]
Last updated: [DATE]
Contact: [EMAIL]

1. Overview
   1.1 Project purpose and how annotations will be used
   1.2 Task description in plain language
   1.3 Quick reference summary of label definitions

2. Label Definitions
   For each label/category:
   2.1 Name and code
   2.2 Clear definition (2-3 sentences)
   2.3 Inclusion criteria (what counts)
   2.4 Exclusion criteria (what does not count)
   2.5 Positive examples (3-5 clear cases)
   2.6 Negative examples (3-5 cases that look similar but are not this label)
   2.7 Edge cases with resolution rules

3. Annotation Procedure
   3.1 Step-by-step instructions for using the annotation tool
   3.2 How to handle each data type
   3.3 Required precision (e.g., bounding box tightness)
   3.4 Order of operations (if multiple labels per item)

4. Edge Case Rules
   4.1 Ambiguous cases and how to resolve them
   4.2 Priority rules when multiple labels apply
   4.3 What to do with low-quality data (blurry images, unclear text)
   4.4 When to flag for expert review

5. Quality Expectations
   5.1 Expected agreement rate targets
   5.2 Common mistakes to avoid
   5.3 Time estimates per annotation unit

6. Change Log
   6.1 Version history with dates and changes
   6.2 Rationale for each change
```

### Writing Effective Definitions

A good label definition follows this pattern:

```
Label: [NAME]
Code: [NUMERIC OR STRING CODE]

Definition: [WHAT it is in 1-2 clear sentences]

Include when:
  - [Specific criterion 1]
  - [Specific criterion 2]
  - [Specific criterion 3]

Exclude when:
  - [Specific exclusion 1]
  - [Specific exclusion 2]

Examples:
  Positive: [IMAGE/TEXT REFERENCE] -- because [reason]
  Positive: [IMAGE/TEXT REFERENCE] -- because [reason]
  Negative: [IMAGE/TEXT REFERENCE] -- because [reason it is NOT this label]
  Edge case: [IMAGE/TEXT REFERENCE] -- labeled as [X] because [rule]
```

---

## 3. Annotator Training

### Training Program Structure

```
Phase 1: Orientation (1-2 hours)
  - Project overview and motivation
  - Read annotation guidelines document
  - Q&A session with project lead
  - Tool tutorial and practice login

Phase 2: Guided Practice (2-4 hours)
  - Annotate 20-30 training samples with feedback
  - Compare against gold standard annotations
  - Discuss disagreements and learn decision rules
  - Repeat with a second set if needed

Phase 3: Calibration Round (1-2 hours)
  - Annotate 50+ calibration samples independently
  - Measure inter-annotator agreement
  - Review and discuss all disagreements
  - Update guidelines if systematic issues found

Phase 4: Qualification Test
  - Annotate a test set of 30-50 samples independently
  - Must achieve >= 85% agreement with gold standard
  - Those who do not pass receive additional training
  - Document pass/fail for each annotator

Phase 5: Production + Ongoing QC
  - Begin production annotation
  - Regular quality checks on random samples
  - Weekly team meetings to discuss difficult cases
  - Periodic re-calibration (every 2-4 weeks)
```

### Common Training Mistakes to Avoid

1. Skipping calibration rounds
2. Not providing enough edge case examples
3. Assuming annotators will ask when confused (they often do not)
4. Training once and never refreshing
5. Not addressing annotator drift over time

---

## 4. Quality Control and Inter-Annotator Agreement

### Inter-Annotator Agreement (IAA) Metrics

| Metric | Use Case | Range | Interpretation |
|--------|---------|-------|----------------|
| Cohen's Kappa | 2 annotators, categorical | -1 to 1 | > 0.8 excellent, 0.6-0.8 good |
| Fleiss' Kappa | 3+ annotators, categorical | -1 to 1 | Same interpretation as Cohen's |
| Krippendorff's Alpha | Any number, any data type | -1 to 1 | > 0.8 reliable, > 0.667 tentative |
| IoU (Jaccard) | Bounding boxes, segmentation | 0 to 1 | > 0.7 good, > 0.5 acceptable |
| F1 Score | Sequence labeling | 0 to 1 | > 0.8 good agreement |

### Computing Cohen's Kappa

```python
from sklearn.metrics import cohen_kappa_score

# Example: two annotators labeled 100 items
annotator_1 = [labels from annotator 1]
annotator_2 = [labels from annotator 2]

kappa = cohen_kappa_score(annotator_1, annotator_2)
print(f"Cohen's Kappa: {kappa:.3f}")

# Interpretation
if kappa > 0.8:
    print("Excellent agreement")
elif kappa > 0.6:
    print("Good agreement")
elif kappa > 0.4:
    print("Moderate agreement -- review guidelines")
else:
    print("Poor agreement -- significant guideline revision needed")
```

### Quality Control Procedures

```
Real-Time QC:
  - Embed 5-10% "gold standard" items in each annotator's queue
  - Auto-flag annotators whose gold accuracy drops below threshold
  - Monitor annotation speed (too fast = likely low quality)

Overlap-Based QC:
  - Assign 10-20% of items to multiple annotators
  - Compute IAA weekly
  - Flag items with disagreement for adjudication
  - Track IAA trends over time (should remain stable or improve)

Expert Review:
  - Senior researcher reviews random 5% of all annotations
  - Systematic review of flagged items
  - Monthly quality report with per-annotator statistics

Adjudication Process:
  - When annotators disagree, a senior annotator or expert decides
  - Document adjudication decisions and add to guidelines
  - Use majority vote for 3+ annotator overlap
  - Track which types of items generate the most disagreement
```

---

## 5. Annotation Tools

### Tool Comparison

| Tool | Task Types | Deployment | Cost | Best For |
|------|-----------|-----------|------|----------|
| Label Studio | Image, text, audio, video | Self-hosted / cloud | Free (OSS) | Versatile, customizable |
| CVAT | Image, video detection/segmentation | Self-hosted / cloud | Free (OSS) | Computer vision projects |
| Prodigy | NLP (NER, classification, spans) | Local | Licensed | NLP with active learning |
| Labelbox | Image, video, text, geospatial | Cloud | Freemium | Large-scale production |
| V7 Darwin | Image, video, DICOM | Cloud | Licensed | Medical and industrial |
| Doccano | Text classification, NER, seq2seq | Self-hosted | Free (OSS) | Simple NLP projects |
| Supervisely | Image, video, point cloud | Cloud / self-hosted | Freemium | 3D and autonomous driving |
| BRAT | Text, relation annotation | Self-hosted | Free (OSS) | Linguistic annotation |

### Tool Selection Criteria

1. **Task compatibility:** Does it support your annotation type?
2. **Data format support:** Can it import and export your data formats?
3. **Collaboration:** Does it support multiple annotators with task assignment?
4. **Quality control:** Built-in IAA computation and gold standard checking?
5. **Integration:** API for automated quality checks and ML pipeline integration?
6. **Cost:** Budget constraints and team size considerations
7. **Security:** Can data remain on-premises if required?
8. **Scalability:** Can it handle your data volume?

---

## 6. Handling Edge Cases

### Edge Case Management System

```
1. Discovery
   - Annotators flag uncertain items during annotation
   - Quality review identifies systematic disagreements
   - New data reveals previously unseen patterns

2. Discussion
   - Weekly team meeting reviews all flagged items
   - Project lead proposes resolution rules
   - Team discusses and reaches consensus

3. Documentation
   - Add resolved edge cases to the guidelines with examples
   - Create an "edge case FAQ" appendix
   - Version the guidelines and communicate updates

4. Verification
   - Re-annotate previously labeled edge cases with updated guidelines
   - Check if new rules improve IAA
   - Iterate if needed
```

### Common Edge Case Patterns

- **Boundary ambiguity:** Object partially visible or partially occluded
- **Category overlap:** Item could reasonably belong to two categories
- **Low quality input:** Blurry image, noisy audio, garbled text
- **Rare events:** Classes that appear very infrequently
- **Context dependence:** Label depends on surrounding context
- **Subjective judgment:** Cases where reasonable people would disagree

---

## 7. Version Control for Annotation Schemas

### Schema Versioning Strategy

```
Version numbering: MAJOR.MINOR.PATCH

MAJOR: Breaking changes (categories added, removed, or redefined)
MINOR: Non-breaking additions (new edge case rules, more examples)
PATCH: Typo fixes, clarifications with no label impact

Examples:
  v1.0.0 -- Initial release
  v1.1.0 -- Added edge case for partially occluded objects
  v1.2.0 -- New examples added for "pedestrian" category
  v2.0.0 -- Split "vehicle" into "car", "truck", "bus" (breaking change)
```

### Change Management Protocol

When updating the annotation schema:

1. Document the proposed change and rationale
2. Assess impact on existing annotations (do they need re-labeling?)
3. Test the change on a small sample set
4. Announce to all annotators with clear effective date
5. Provide updated guidelines document
6. Decide whether to re-annotate existing data under new schema
7. Tag all annotations with the schema version used

---

## 8. Crowdsourcing vs Expert Annotation

### Decision Framework

| Factor | Crowdsourcing | Expert Annotation |
|--------|--------------|-------------------|
| Cost per item | Low (cents) | High (dollars) |
| Speed | Very fast (days) | Slower (weeks) |
| Quality per annotator | Variable | Consistently high |
| Domain knowledge needed | Low | High |
| Scalability | Excellent | Limited |
| Best for | Simple tasks, large scale | Complex tasks, small scale |

### Hybrid Approaches

1. **Experts define, crowd executes:** Experts create guidelines and gold
   standard; crowd annotators do bulk work; experts adjudicate disagreements
2. **Crowd then expert:** Crowd provides initial labels; experts review
   and correct difficult cases
3. **Active learning loop:** ML model identifies uncertain samples;
   experts annotate only those; iterate

### Crowdsourcing Quality Controls

- Qualification tests before granting access
- Gold standard items embedded in tasks (honeypots)
- Majority vote (3-5 annotators per item)
- Annotator reputation tracking
- Payment bonuses tied to quality metrics
- Block annotators who fail quality checks repeatedly

---

## Claude Prompt Templates

### Annotation Schema Designer

```
Help me design an annotation schema for a machine learning dataset.

Task: [CLASSIFICATION / DETECTION / SEGMENTATION / NER / etc.]
Domain: [DOMAIN, e.g., autonomous driving, medical imaging, NLP]
Downstream model: [MODEL TYPE, e.g., YOLO, BERT, Mask R-CNN]
Data format: [IMAGE / TEXT / VIDEO / POINT CLOUD / etc.]
Approximate dataset size: [NUMBER OF SAMPLES]

Known categories: [LIST ANY PREDEFINED CATEGORIES]
Edge cases anticipated: [DESCRIBE]

Design:
1. Complete category taxonomy with definitions
2. Inclusion and exclusion criteria for each category
3. Edge case resolution rules
4. Annotation format specification (output format)
5. Quality targets (minimum IAA score)
6. Estimated annotation time per item
```

### Annotation Guidelines Writer

```
Write comprehensive annotation guidelines for a labeling project.

Schema: [PASTE ANNOTATION SCHEMA]
Task type: [DESCRIBE THE ANNOTATION TASK]
Tool being used: [TOOL NAME]

Include:
1. Project overview in plain language
2. Label definitions with inclusion/exclusion criteria
3. Three positive and two negative examples per category
4. Step-by-step annotation procedure
5. Edge case handling rules (at least 10 edge cases)
6. Common mistakes to avoid
7. Quality expectations and metrics
8. FAQ section addressing anticipated annotator questions
```

### IAA Analysis Report

```
Analyze inter-annotator agreement data and provide recommendations.

Annotation task: [DESCRIBE]
Number of annotators: [N]
Number of overlapping items: [N]

Agreement data:
[PASTE: item_id, annotator_1_label, annotator_2_label, ...]

Compute and report:
1. Overall agreement percentage (raw)
2. Cohen's Kappa or Krippendorff's Alpha (chance-corrected)
3. Per-category agreement rates
4. Most frequently confused category pairs
5. Annotators with consistently low agreement
6. Specific items with high disagreement (for review)
7. Recommendations for improving agreement
8. Whether the guidelines need revision and where
```

### Annotation Project Planning

```
Help me plan an annotation project from start to finish.

Dataset: [SIZE, TYPE, FORMAT]
Task: [ANNOTATION TASK DESCRIPTION]
Budget: [TOTAL BUDGET]
Timeline: [AVAILABLE WEEKS]
Team: [NUMBER OF AVAILABLE ANNOTATORS, SKILL LEVEL]

Create:
1. Annotation schema recommendation
2. Guidelines document outline
3. Annotator training plan with timeline
4. Quality control strategy
5. Tool recommendation with justification
6. Milestone timeline (schema design -> pilot -> production -> QC)
7. Budget allocation (tools, annotator compensation, QC)
8. Risk assessment and mitigation plan
```
