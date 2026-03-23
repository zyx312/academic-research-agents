# Patent Drafting

## Overview

Draft patent applications including claims, specification, abstract, and drawings
descriptions. Supports Chinese invention patents (CNIPA), US utility patents (USPTO),
European patents (EPO), and PCT international applications. This skill covers the
structure, strategy, and craft of writing patent documents that provide maximum
protection for your inventions.

## Patent Document Structure

A complete patent application consists of these components, each serving a distinct
legal and technical purpose:

### 1. Title of Invention

- Descriptive but concise (typically under 15 words for USPTO, under 25 characters
  recommended for CNIPA).
- Should indicate the technical field and the nature of the invention.
- Avoid marketing language, trademarks, or acronyms.
- Good: "Method and System for Real-Time Obstacle Detection Using Multi-Sensor Fusion"
- Bad: "SuperSense AI-Powered Safety System"

### 2. Abstract

- A concise summary of the disclosure (typically 150 words max for USPTO).
- Must describe the technical problem, the solution, and the principal use.
- Should correspond to the broadest independent claim.
- Written in narrative form, not claim language.
- For CNIPA: Abstract should be under 300 Chinese characters and include a
  representative drawing.

### 3. Specification (Description)

The specification is the heart of the patent document. It must enable a person
skilled in the art to reproduce the invention without undue experimentation.

#### 3a. Background of the Invention

- Describe the technical field.
- Discuss the state of the art and limitations of existing approaches.
- Identify the technical problem that the invention addresses.
- Do NOT disparage your own prior products if you are a company.
- Avoid overly broad statements that could be used against you later.

#### 3b. Summary of the Invention

- Briefly describe the invention and its advantages.
- Should track the independent claims but in narrative form.
- State the technical effect or improvement achieved.
- Avoid unnecessary limitations -- keep it broad.

#### 3c. Brief Description of Drawings

- List each figure with a one-sentence description.
- "FIG. 1 is a block diagram of the system according to one embodiment."
- "FIG. 2 is a flowchart of the method for sensor calibration."

#### 3d. Detailed Description of Embodiments

This is the most substantial section. Requirements:
- Describe at least one preferred embodiment in full detail.
- Include alternative embodiments to support broader claim scope.
- Define every term used in the claims.
- Provide specific examples with concrete values, dimensions, or parameters.
- Describe each element of the claims and how they interact.
- Include enough detail for reproduction by a skilled person.

**Writing strategy:**
- Start with the broadest embodiment, then narrow to specific implementations.
- Use phrases like "in one embodiment," "in another embodiment," "optionally"
  to create flexibility.
- Never use absolute language: avoid "must," "always," "essential," "necessary,"
  "only," "never" -- these limit your claim scope.
- Use "may," "can," "in some embodiments," "optionally" instead.

### 4. Claims

Claims define the legal scope of protection. They are the most critical part of
the patent and are discussed in detail below.

### 5. Drawings

- Must illustrate the invention clearly.
- Black-and-white line drawings (no photographs unless necessary).
- Each element must be labeled with reference numerals.
- Reference numerals must be consistent with the specification.
- For USPTO: formal drawings must meet specific requirements (margin sizes,
  line quality, numbering conventions).
- For CNIPA: similar requirements but allow photographs in some cases.

## Claim Types

### Independent Claims

Stand alone without reference to other claims. Define the broadest scope of
protection. A patent typically has:
- At least one independent method claim
- At least one independent apparatus/system claim
- Optionally, a computer-readable medium claim

**Structure of an independent claim:**
1. **Preamble**: Identifies the category and general purpose.
   "A method for detecting obstacles in autonomous driving..."
2. **Transitional phrase**: "comprising" (open-ended, preferred), "consisting of"
   (closed, restrictive), "consisting essentially of" (middle ground).
3. **Body**: Lists the essential elements or steps and their relationships.

### Dependent Claims

Reference and further limit an independent claim or another dependent claim.
They add specific features, parameters, or alternatives.

**Purpose of dependent claims:**
- Create fallback positions if the independent claim is narrowed during prosecution.
- Cover specific commercially important embodiments.
- Add detail that strengthens enforceability.

**Example chain:**
- Claim 1 (independent): A method for sensor fusion comprising steps A, B, C.
- Claim 2 (dependent): The method of claim 1, wherein step B uses a Kalman filter.
- Claim 3 (dependent): The method of claim 2, wherein the Kalman filter is an
  extended Kalman filter with state vector dimension of at least 12.

### Method Claims

Describe a series of steps performed in sequence or in a defined relationship.
- Use active voice: "receiving," "processing," "generating," "transmitting."
- Each step should begin with a gerund (-ing form).
- Define the order only when sequence matters; use "and" for unordered steps.

### Apparatus / System Claims

Describe a physical or logical system with components and their interconnections.
- Define components: "a processor," "a sensor module," "a memory."
- Define relationships: "coupled to," "in communication with," "configured to."
- Use "configured to" instead of "for" to clearly tie function to structure.

### Computer-Readable Medium Claims

"A non-transitory computer-readable medium storing instructions that, when
executed by a processor, cause the processor to perform [method steps]."

This claim type is important for software inventions and provides an additional
avenue for enforcement.

## Claim Drafting Strategies

### Start Broad, Then Narrow

1. Write the broadest defensible independent claim first.
2. Add dependent claims that progressively narrow to your specific implementation.
3. Each dependent claim should cover a feature your competitors might want to copy.

### Use Functional Language Strategically

- "A processing unit configured to..." (broader than specifying a specific processor)
- "A detection module for identifying..." (broader than specifying exact algorithm)
- But ensure the specification supports each functional term with at least one
  concrete implementation.

### Avoid Claim Profanity

Never use these words in claims or specification:
- "essential," "necessary," "must," "required," "critical"
- "always," "never," "only," "solely"
- "invention," "the present invention" (implies the entire disclosure is limited)
- "important," "key," "significant"

These words can be used by opponents to argue that your claims should be narrowly
construed.

### Draft Claims Before Specification

Many experienced patent attorneys recommend drafting claims first, then writing
the specification to support them. This ensures:
- The specification adequately describes every claim element.
- You do not waste time describing unclaimed subject matter.
- The claim scope drives the document, not the other way around.

### Multiple Independent Claims

Consider independent claims of different types:
- Method claim: How the invention operates step by step.
- System claim: The physical or logical components that perform the method.
- Product claim: The tangible output or device.
- Use claim: Application in a specific field (common in CNIPA practice).

## Patent Drawings Requirements

### General Rules (USPTO)

- Black ink on white paper, no color unless petitioned.
- Margins: at least 2.5 cm top, 2.5 cm left, 1.5 cm right, 1.0 cm bottom.
- Each figure on a separate sheet or clearly delineated.
- Reference numerals must be at least 0.32 cm (1/8 inch) high.
- Shading permitted only for cross-sections.
- Use lead lines from reference numerals to features.

### General Rules (CNIPA)

- Similar to USPTO but allows photographs for microstructure, metallography, etc.
- Flowcharts acceptable for method inventions.
- Chinese text in drawings should use standard simplified characters.
- Figure numbers: 图1, 图2, etc.

### Types of Drawings to Include

- **Block diagrams**: System architecture, component relationships.
- **Flowcharts**: Method steps and decision logic.
- **Schematic diagrams**: Circuit designs, mechanical layouts.
- **Timing diagrams**: Signal sequences, communication protocols.
- **Data flow diagrams**: Information processing pipelines.
- **Perspective/exploded views**: Physical devices (mechanical patents).

## Working with Patent Attorneys

### Your Role as Inventor

- Provide clear, complete technical descriptions.
- Review all drafts for technical accuracy.
- Respond to attorney questions promptly.
- Identify the most commercially important features.
- Point out competitors and their approaches.
- Review claims to ensure they capture the invention broadly enough.

### What to Prepare for the Attorney

- Invention disclosure document (see disclosure.md).
- Key prior art references you are aware of.
- A clear statement of what makes your invention different.
- Diagrams or figures illustrating the system or method.
- Any prototype results or performance data.

### Red Flags in Attorney Drafts

- Claims that are too narrow (specific to only your exact implementation).
- Specification that uses absolute language unnecessarily.
- Missing alternative embodiments that you discussed verbally.
- Inconsistent reference numerals between drawings and text.
- Claims that do not match the specification terminology.

## Filing Strategies

### Provisional vs. Non-Provisional (US)

**Provisional Application:**
- Establishes a priority date at lower cost.
- Valid for 12 months; must file non-provisional to continue.
- No formal claims required (but recommended to include them).
- Not examined by the USPTO.
- Use when: you need to publish or present soon but need more time.

**Non-Provisional Application:**
- Full application that enters examination.
- Must include formal claims, specification, drawings, and oath/declaration.
- Examination typically begins 12-18 months after filing.

### PCT International Filing

- File one application that preserves the right to enter national/regional
  phases in 150+ countries.
- Must enter national phase within 30 or 31 months from the priority date
  (varies by country).
- Includes international search report and written opinion.
- Use when: you want to delay country-specific decisions and costs.

### China-Specific Filing (CNIPA)

- **Invention patent (发明专利)**: Substantive examination, ~2-4 years to grant.
- **Utility model (实用新型)**: Preliminary examination only, ~6-12 months to grant.
  Lower threshold but narrower scope (product structure/shape only, no methods).
- **Design patent (外观设计)**: Protects ornamental design.
- Strategy: File utility model for quick protection, then file invention patent
  for the same subject matter for longer-term, broader protection.

### Continuation and Divisional Applications

- **Continuation**: New claims based on the same specification. Use to pursue
  different claim scope after the parent issues.
- **Divisional**: Required when the examiner restricts claims to one invention.
  File a divisional for the restricted claims.
- **Continuation-in-part (CIP)**: Adds new matter to the specification. The
  new matter does not get the original priority date.

## Prompt Templates for Claude

### Draft Independent Patent Claims

```
Draft independent patent claims for the following invention:

Technical field: [FIELD]
Invention summary: [DESCRIPTION]
Key novel features: [LIST OF NOVEL ELEMENTS]
Type of claims needed: [method / apparatus / system / all three]

Requirements:
- Use "comprising" as the transitional phrase
- Each claim should be one sentence (standard patent format)
- Avoid absolute language (must, essential, only)
- Use functional language where appropriate (configured to, adapted to)
- Aim for broad scope while maintaining patentability over known prior art:
  [LIST KEY PRIOR ART]
```

### Write Detailed Description Section

```
Write the detailed description section for a patent specification:

Invention: [DESCRIPTION]
Figures to reference: [LIST FIGURES WITH BRIEF DESCRIPTIONS]
Key embodiments to describe:
1. [PRIMARY EMBODIMENT]
2. [ALTERNATIVE EMBODIMENT]
3. [SIMPLIFIED EMBODIMENT]

Requirements:
- Use reference numerals consistently (e.g., processor 102, sensor 104)
- Include alternative embodiments with "in another embodiment" language
- Never use absolute language
- Define all technical terms on first use
- Ensure every claim element is described in detail
- Include specific examples with concrete parameter values
```

### Generate Dependent Claim Chain

```
Given the following independent claim, generate a chain of 5-8 dependent claims
that progressively narrow to the specific implementation:

Independent claim:
[PASTE INDEPENDENT CLAIM]

Specific implementation details:
[DESCRIBE YOUR ACTUAL IMPLEMENTATION]

Commercially important features to protect:
[LIST KEY FEATURES COMPETITORS MIGHT COPY]

Each dependent claim should cover one additional feature and reference
the appropriate parent claim.
```

### Review Patent Draft for Weaknesses

```
Review the following patent claims and specification for potential weaknesses:

[PASTE CLAIMS AND RELEVANT SPECIFICATION SECTIONS]

Check for:
1. Absolute language that could limit claim scope
2. Inconsistencies between claims and specification
3. Missing support in the specification for claim elements
4. Claims that are unnecessarily narrow
5. Missing claim types (method, apparatus, medium)
6. Prior art vulnerabilities based on: [KNOWN PRIOR ART]
```

## Related

- [patent-mining.md](patent-mining.md) - Prior art and novelty assessment
- [disclosure.md](disclosure.md) - Invention disclosure
- [office-action.md](office-action.md) - Office action responses
