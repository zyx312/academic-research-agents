# Dataset Release Guide

## Purpose

This skill provides a comprehensive framework for releasing research datasets
publicly. It covers the Datasheets for Datasets documentation framework, README
templates, licensing options, hosting platforms, DOI registration, anonymization,
and citation formatting to ensure released datasets are FAIR, ethical, and
maximally useful to the research community.

---

## 1. Datasheets for Datasets Framework

### Overview

The Datasheets for Datasets framework (proposed by Gebru et al.) recommends that
every dataset be accompanied by a datasheet documenting its motivation, composition,
collection process, recommended uses, and maintenance plan. This promotes
transparency, accountability, and informed dataset selection.

### Datasheet Sections

```
1. Motivation
   - Why was the dataset created?
   - Who created it and on behalf of whom?
   - Who funded the dataset creation?
   - Any other relevant context?

2. Composition
   - What do the instances represent? (images, text, sensor readings, etc.)
   - How many instances are there in total?
   - Does the dataset contain all possible instances or a sample?
   - What data does each instance consist of?
   - Is there a label or target associated with each instance?
   - Is any information missing from individual instances?
   - Are relationships between instances made explicit?
   - Are there recommended data splits (train/val/test)?
   - Are there any errors, noise, or redundancies?
   - Is the dataset self-contained or does it rely on external resources?
   - Does the dataset contain data that might be considered confidential?
   - Does the dataset contain data that could be offensive or harmful?

3. Collection Process
   - How was the data associated with each instance acquired?
   - What mechanisms or procedures were used to collect the data?
   - Who was involved in the data collection process?
   - Over what timeframe was the data collected?
   - Were any ethical review processes conducted?
   - Was informed consent obtained (if applicable)?
   - Was the data collected from human subjects directly or indirectly?

4. Preprocessing/Cleaning/Labeling
   - Was any preprocessing/cleaning/labeling applied?
   - Was the raw data saved in addition to the preprocessed data?
   - Is the preprocessing software available?

5. Uses
   - What tasks has the dataset been used for already?
   - Is there a repository linking to papers or systems using this dataset?
   - What other tasks could the dataset be used for?
   - Are there tasks for which the dataset should NOT be used?
   - Is there anything about the composition or collection that might
     impact future uses?

6. Distribution
   - How is the dataset distributed? (website, API, repository)
   - When was the dataset first released?
   - What license is the dataset distributed under?
   - Are there any fees or access restrictions?
   - Are there export controls or other regulatory restrictions?

7. Maintenance
   - Who is supporting/hosting/maintaining the dataset?
   - How can the maintainer be contacted?
   - Will the dataset be updated? If so, how often?
   - Will older versions remain available?
   - Can users contribute to the dataset? If so, how?
   - Is there an erratum?
```

---

## 2. Dataset README Template

### Comprehensive README Structure

```markdown
# [Dataset Name]

## Description
[2-3 sentence description of the dataset and its purpose]

## Quick Facts
- **Size:** [N instances, M GB]
- **Format:** [file formats used]
- **License:** [license name]
- **DOI:** [DOI link]
- **Paper:** [citation or link to associated paper]
- **Last Updated:** [date]

## Download
[Instructions for downloading, including URLs and checksums]

## Dataset Structure
[Directory tree showing file organization]

```
dataset/
  train/
    images/
    labels/
  val/
    images/
    labels/
  test/
    images/
    labels/
  metadata.json
  README.md
  LICENSE
  datasheet.pdf
```

## Data Format
[Detailed description of file formats, column definitions,
label encodings, coordinate systems, units]

## Statistics
[Key statistics: class distribution, data splits, summary statistics]

## Collection Methodology
[Brief description of how data was collected, including sensors,
protocols, geographic/temporal coverage]

## Annotation
[How labels were generated, IAA scores, annotator qualifications]

## Known Limitations
[Honest description of dataset limitations, biases, gaps]

## Intended Use
[What the dataset is designed for and what it should NOT be used for]

## Citation
[BibTeX entry for citing the dataset]

## License
[Full license text or link]

## Contact
[Maintainer name and email]

## Changelog
[Version history with descriptions of changes]
```

---

## 3. Licensing Options

### Common Dataset Licenses

| License | Commercial Use | Modification | Share-Alike | Attribution |
|---------|---------------|-------------|------------|-------------|
| CC-BY 4.0 | Yes | Yes | No | Required |
| CC-BY-SA 4.0 | Yes | Yes | Required | Required |
| CC-BY-NC 4.0 | No | Yes | No | Required |
| CC-BY-NC-SA 4.0 | No | Yes | Required | Required |
| CC0 | Yes | Yes | No | Not required |
| ODC-BY | Yes | Yes | No | Required |
| CDLA-Permissive | Yes | Yes | No | Required |
| CDLA-Sharing | Yes | Yes | Required | Required |

### Choosing a License

Decision tree:

```
Do you want to allow commercial use?
  YES --> Do you want derivatives to use the same license?
    YES --> CC-BY-SA 4.0
    NO  --> CC-BY 4.0 (most common for academic datasets)
  NO  --> Do you want derivatives to use the same license?
    YES --> CC-BY-NC-SA 4.0
    NO  --> CC-BY-NC 4.0

Do you want to waive all rights (public domain)?
  YES --> CC0 1.0
```

### License Considerations

- **Funder requirements:** Some funders mandate open licensing (e.g., CC-BY for NIH-funded data)
- **Institutional policy:** University may have default data licensing policies
- **Collaborative data:** If data comes from multiple sources, licenses must be compatible
- **Ethical concerns:** Consider restricting use for harmful applications
- **Commercial partnerships:** Industry collaborators may require NC restriction

### Custom Data Use Agreements

When standard licenses are insufficient:
- Pair a standard license with a supplementary data use agreement (DUA)
- Restrict specific uses (e.g., no facial recognition, no military applications)
- Require ethics review for derivative datasets
- See the data-agreement.md skill for detailed guidance

---

## 4. Hosting Platforms

### Platform Comparison

| Platform | Max Size | DOI | Versioning | Cost | Best For |
|----------|---------|-----|-----------|------|---------|
| Zenodo | 50 GB | Yes | Yes | Free | General research data |
| Figshare | 20 GB (free) | Yes | Yes | Free/paid | Mixed media datasets |
| Hugging Face | No hard limit | Own ID | Yes | Free | ML/NLP datasets |
| IEEE DataPort | 2 TB | Yes | Yes | Free (IEEE) | Engineering datasets |
| Dryad | Variable | Yes | Limited | Fee | Life sciences |
| Harvard Dataverse | 2.5 GB/file | Yes | Yes | Free | Social sciences |
| OpenDataLab | Large | Own ID | Yes | Free | AI/CV (China-based) |
| Google Dataset Search | Index only | N/A | N/A | N/A | Discovery layer |

### Platform Selection Criteria

1. **Dataset size:** Ensure the platform can handle your data volume
2. **DOI support:** Essential for citability and FAIR compliance
3. **Versioning:** Ability to update while keeping old versions accessible
4. **Community:** Where does your research community look for data?
5. **Long-term stability:** Will the platform exist in 10 years?
6. **Access control:** Can you restrict access if needed (embargo, DUA)?
7. **Metadata standards:** Does it support your discipline's standards?
8. **Cost:** Budget for hosting fees if applicable

### Recommended Hosting Platforms in Detail

**Zenodo (zenodo.org)**
- Operated by CERN; backed by the European Commission. Long-term stability assured.
- Automatic DOI assignment upon publication; supports concept DOIs for versioned datasets.
- Free for datasets up to 50 GB per record. Larger datasets can be accommodated via request.
- Integrates with GitHub: create a release on GitHub and automatically archive to Zenodo with a DOI.
- Best for: General research data, code archives, supplementary materials.
- **DOI registration via Zenodo is the simplest way to get a persistent identifier for your dataset.**

**Figshare (figshare.com)**
- Supports all file types including figures, datasets, videos, and code.
- Free accounts allow up to 20 GB of private storage and unlimited public storage.
- Automatic DOI assignment and altmetric tracking.
- Institutional versions available (many universities have Figshare portals).
- Best for: Mixed media datasets, individual figures, and supplementary materials.

**DRYAD (datadryad.org)**
- Focused on research data underlying scientific publications.
- Integrated with many journals: data can be deposited as part of the manuscript submission process.
- Charges a data publishing fee (waived for researchers from some institutions).
- Strong emphasis on data curation: Dryad staff review submissions for quality.
- Best for: Life sciences and ecology datasets associated with journal publications.

**Google Dataset Search (datasetsearch.research.google.com)**
- Not a hosting platform but a discovery layer that indexes datasets across the web.
- Datasets hosted on Zenodo, Figshare, Dryad, and other platforms are automatically indexed.
- To ensure your dataset is discoverable: include structured metadata (schema.org/Dataset)
  on your dataset landing page.
- Best for: Increasing discoverability of datasets hosted elsewhere.

**Nature's Recommended Data Repositories**
- Nature maintains a curated list of recommended repositories organized by discipline.
- Using a Nature-recommended repository strengthens the credibility of your dataset.
- For engineering and computer science: IEEE DataPort, Zenodo, Figshare are listed.
- For interdisciplinary work: check the full list at nature.com/sdata/policies/repositories.
- Many journals now require data deposition in a recognized repository as a condition of publication.

### Multi-Platform Strategy

For maximum discoverability:
- **Primary host:** One platform for the actual data files (e.g., Zenodo for DOI and long-term preservation)
- **Discovery layer:** Register on Google Dataset Search (automatic if hosted on major platforms)
- **Community platform:** Mirror on discipline-specific platform (e.g., Hugging Face for ML)
- **Institutional repository:** Deposit in university's repository for compliance
- **Project website:** Link to all hosting locations from the project website
- **Nature-recommended repository:** If publishing in a Nature-family journal, use their recommended repositories

---

## 5. DOI Registration

### Why DOIs Matter

- Persistent identifier that survives URL changes
- Enables citation tracking and impact measurement
- Required by many funders and journals
- Signals professionalism and permanence

### How to Get a DOI

Most repository platforms automatically assign DOIs:

```
1. Upload dataset to a DOI-issuing repository (Zenodo, Figshare, etc.)
2. Fill in metadata (title, authors, description, license, keywords)
3. Platform assigns a DOI upon publication
4. DOI resolves to the dataset landing page

Example DOI: 10.5281/zenodo.1234567
URL: https://doi.org/10.5281/zenodo.1234567
```

### Versioning with DOIs

Use Zenodo's versioning system:
- Each version gets its own DOI
- A "concept DOI" links to all versions
- Users can cite a specific version or the concept (always resolves to latest)

---

## 6. Anonymization Requirements

### When Anonymization Is Required

- Dataset contains personally identifiable information (PII)
- Images show identifiable faces or license plates
- Location data can identify individuals' homes or routines
- Text data contains names, addresses, or other identifiers

### Anonymization Techniques

| Data Type | Technique | Tool |
|-----------|----------|------|
| Face images | Face detection + blurring | OpenCV, Fawkes |
| License plates | Detection + replacement | Custom detector |
| GPS traces | Spatial cloaking, noise addition | Custom scripts |
| Text (names) | Named entity masking | spaCy, Presidio |
| Tabular (demographics) | K-anonymity, generalization | ARX, sdcMicro |
| Audio (voices) | Voice anonymization | McAdams coefficient |

### Anonymization Verification

After anonymization, verify:
- [ ] No faces are identifiable in image data
- [ ] No license plates are readable
- [ ] GPS traces do not reveal specific addresses
- [ ] No names appear in text data
- [ ] Anonymization does not significantly degrade data utility
- [ ] Re-identification attacks have been considered and mitigated
- [ ] Verification was conducted by someone other than the anonymizer

---

## 7. Citation Format

### Dataset Citation Template

```
[Authors]. ([Year]). [Dataset Title] (Version [V]) [Data set].
[Repository Name]. https://doi.org/[DOI]

Example:
Zhang, Y., Li, W., & Wang, H. (2025). Urban Driving Scenarios
Dataset for SOTIF Analysis (Version 2.1) [Data set]. Zenodo.
https://doi.org/10.5281/zenodo.1234567
```

### BibTeX Entry Template

```bibtex
@misc{author2025datasetname,
  author       = {Zhang, Yuxin and Li, Wei and Wang, Hao},
  title        = {Urban Driving Scenarios Dataset for SOTIF Analysis},
  year         = {2025},
  publisher    = {Zenodo},
  version      = {2.1},
  doi          = {10.5281/zenodo.1234567},
  url          = {https://doi.org/10.5281/zenodo.1234567}
}
```

### Citing Datasets in Papers

- Cite the dataset in the references section like any other source
- Include the DOI in the citation
- If there is an associated data paper, cite both
- Specify the exact version used in the methodology section

---

## 8. Pre-Release Checklist

### Technical Readiness

- [ ] Data files are in documented, standard formats
- [ ] Directory structure is clean and logical
- [ ] File naming follows a consistent convention
- [ ] Checksums (MD5 or SHA-256) are generated for all files
- [ ] Data loads correctly in common tools (Python, R, MATLAB)
- [ ] Train/val/test splits are defined and documented

### Documentation Readiness

- [ ] README.md is complete with all sections
- [ ] Datasheet for Datasets is complete
- [ ] Data format documentation covers all fields and encoding
- [ ] License file is included
- [ ] BibTeX citation is provided
- [ ] Known limitations are honestly documented
- [ ] Changelog is initialized

### Legal and Ethical Readiness

- [ ] License is selected and applied
- [ ] Anonymization is complete and verified
- [ ] IRB/ethics compliance is confirmed
- [ ] Data use agreement is prepared (if needed)
- [ ] No proprietary data included without permission
- [ ] All contributors have agreed to the release
- [ ] Funder data sharing requirements are met

### Platform Readiness

- [ ] Repository account is set up
- [ ] Metadata is prepared for the platform
- [ ] Upload tested with a small subset
- [ ] DOI reservation (some platforms allow pre-registration)
- [ ] Landing page reviewed for accuracy

---

## Claude Prompt Templates

### Datasheet Generator

```
Help me create a Datasheets for Datasets document.

Dataset information:
- Name: [DATASET NAME]
- Domain: [RESEARCH DOMAIN]
- Size: [NUMBER OF INSTANCES, FILE SIZE]
- Data types: [IMAGE / TEXT / SENSOR / TABULAR / etc.]
- Collection method: [DESCRIBE]
- Annotation method: [DESCRIBE]
- Intended use: [PRIMARY ML TASK]
- Time period: [WHEN DATA WAS COLLECTED]
- Geographic scope: [WHERE]

Generate a complete datasheet following the Gebru et al. framework,
addressing all seven sections (Motivation, Composition, Collection,
Preprocessing, Uses, Distribution, Maintenance) with specific details
based on the provided information.
```

### README Writer

```
Write a comprehensive README.md for a research dataset release.

Dataset: [NAME]
Description: [2-3 SENTENCES]
Key statistics: [SIZE, CLASSES, SPLITS]
Format: [FILE FORMATS]
Collection: [METHOD SUMMARY]
License: [LICENSE TYPE]
DOI: [DOI IF AVAILABLE]
Paper: [ASSOCIATED PAPER CITATION]

Generate a README that includes:
1. Quick facts table
2. Download instructions
3. Directory structure diagram
4. Detailed data format specification
5. Statistics summary with class distribution
6. Known limitations section
7. Citation in BibTeX format
8. Contact information placeholder
```

### License Advisor

```
Help me choose an appropriate license for releasing a research dataset.

Dataset characteristics:
- Contains personal data: [YES / NO]
- Funded by: [FUNDER]
- Involves industry partner: [YES / NO]
- Contains data from other licensed sources: [LIST]
- Desired commercial use policy: [ALLOW / RESTRICT / UNDECIDED]
- Desired modification policy: [ALLOW / REQUIRE SAME LICENSE / RESTRICT]

Recommend:
1. The most appropriate license with justification
2. Any additional terms needed (data use agreement)
3. Compatibility issues with source data licenses
4. Funder requirements that affect license choice
5. The license text to include in the release
```

### Pre-Release Review

```
Review a dataset release package for completeness and quality.

Provided materials:
- README.md: [PASTE OR SUMMARIZE]
- License: [LICENSE TYPE]
- Data format: [DESCRIBE]
- Sample data: [PASTE SMALL SAMPLE]
- Datasheet: [PASTE OR SUMMARIZE]

Evaluate:
1. Documentation completeness (what is missing?)
2. FAIR compliance assessment
3. Ethical review (any privacy or bias concerns?)
4. Technical quality (format standards, organization)
5. Citability (DOI, BibTeX, version)
6. Specific recommendations for improvement before release
```
