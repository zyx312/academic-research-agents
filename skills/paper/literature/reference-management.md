# Reference Management

## Purpose

This skill provides a comprehensive guide to organizing, formatting, and maintaining academic references. It covers Zotero setup and workflows, BibTeX/BibLaTeX management, collaboration strategies, and integration with writing tools. Good reference management prevents citation errors, saves time during writing, and ensures reproducibility.

## Related
- [literature-search.md](literature-search.md) - Find papers to cite
- [literature-review.md](literature-review.md) - Literature synthesis
- [../paper-writing/research-paper.md](../paper-writing/research-paper.md) - Paper writing

---

## Choosing a Reference Manager

| Tool | Strengths | Weaknesses | Best For |
|------|-----------|------------|----------|
| **Zotero** | Free, open-source, browser integration, group libraries | Limited cloud storage (300MB free) | Most researchers (recommended) |
| **Mendeley** | PDF reader, social features | Elsevier-owned, privacy concerns | Quick setup |
| **EndNote** | Institutional support, mature | Expensive, proprietary | Researchers with institutional licenses |
| **JabRef** | Native BibTeX, open-source | No browser integration | LaTeX-only workflows |
| **Paperpile** | Google Docs integration | Paid only | Google Workspace users |

**Recommendation**: Zotero is the best general-purpose choice for most researchers due to its open-source nature, active development, extensive plugin ecosystem, and strong community.

---

## Zotero Setup and Configuration

### Essential Installation Steps
1. Install Zotero desktop application (zotero.org)
2. Install Zotero Connector browser extension (Chrome/Firefox/Edge)
3. Create a free Zotero account for sync
4. Install essential plugins (see below)

### Essential Plugins

| Plugin | Purpose | Install From |
|--------|---------|-------------|
| **Better BibTeX** | Customizable citation keys, auto-export .bib files | retorque.re/zotero-better-bibtex |
| **ZotFile** (Zotero 6) / Built-in (Zotero 7) | PDF management, file renaming, tablet sync | zotfile.com |
| **Zotero PDF Translate** | In-reader translation for non-English papers | GitHub |
| **Zotero GPT / Aria** | AI-powered paper summarization | GitHub |
| **DOI Manager** | Batch-find missing DOIs | GitHub |
| **Scite Plugin** | See citation context (supporting/contrasting) | scite.ai |

### Better BibTeX Configuration

Set a consistent citation key format:
```
Preferences > Better BibTeX > Citation Keys

Recommended format: [auth:lower][year][shorttitle:lower:skipwords:3]
Example output: zhang2024sotifvalidation

Alternative format: [auth:lower][year]
Example output: zhang2024
```

Key settings:
- Enable "On item change: update citation key"
- Enable "Automatic export: When idle" for .bib file syncing
- Set "Keep citation keys unique" to prevent conflicts

### Better BibTeX: Advanced Configuration

Better BibTeX is the most important Zotero plugin for LaTeX users. Here is a detailed setup guide:

**Installation**: Download from retorque.re/zotero-better-bibtex and install via Zotero > Tools > Add-ons.

**Citation Key Configuration** (Preferences > Better BibTeX > Citation Keys):
```
# Recommended formats by use case:

# Short and memorable (good for solo projects):
[auth:lower][year]
# Output: zhang2024, wang2023

# With short title (good for large libraries to avoid collisions):
[auth:lower][year][shorttitle:lower:skipwords:3]
# Output: zhang2024weatherfusion, wang2023safetyvalidation

# First author + year + first significant word:
[auth:lower][year][Title:skipwords:nopunct:lower:select=1,1]
# Output: zhang2024robust

# For Chinese authors (pinyin-friendly):
[auth:lower:replace=ü,v][year]
# Output: lv2024 (for 吕)
```

**Auto-Export Setup** (critical for Overleaf/LaTeX workflows):
1. Right-click your project collection > Export Collection
2. Format: "Better BibLaTeX" (or "Better BibTeX" for legacy)
3. Check "Keep updated" -- this creates a live-syncing .bib file
4. Save to your LaTeX project folder or Overleaf-synced directory
5. The .bib file updates automatically whenever you add/edit references

**Useful settings**:
- `Preferences > Better BibTeX > Export > Fields to omit`: Set to `abstract,file,keywords` to keep .bib files small
- `Automatic export: When idle`: Prevents export during batch imports
- `Citation key formula: On conflict: postfixed`: Adds a/b/c suffixes for key collisions

### ZotFile for PDF Management (Zotero 6)

ZotFile provides advanced PDF management. Note: Zotero 7 has built-in file management, but ZotFile remains useful for Zotero 6 users.

**Key features**:
- Automatically rename PDFs based on metadata (Author_Year_Title.pdf)
- Move PDFs to a custom directory (useful for cloud sync)
- Extract annotations from PDFs into Zotero notes
- Send PDFs to tablet for reading (via cloud folder)

**Recommended rename rules** (ZotFile Preferences > Renaming Rules):
```
{%a}_{%y}_{%t}
# Output: Zhang_2024_Weather Robust Perception for Autonomous Driving.pdf

# Or shorter:
{%a}_{%y}_{%w}
# Output: Zhang_2024_Weather.pdf (first word of title)
```

### Jasminum (茉莉花) Plugin for CNKI

Jasminum is essential for Chinese researchers who use CNKI (知网). It fixes the metadata quality issues that plague CNKI imports.

**What it does**:
- Retrieves correct metadata for CNKI papers (which often import with garbled or incomplete data)
- Splits merged author names into individual entries
- Converts CNKI-specific fields to standard Zotero fields
- Adds Chinese abstracts and keywords

**Installation**: GitHub: l0o0/jasminum. Install via Zotero > Tools > Add-ons.

**Usage**:
1. Import CNKI papers into Zotero (via Connector or .ris export)
2. Select the imported items
3. Right-click > Jasminum > Pull CNKI metadata
4. Jasminum fetches correct metadata from CNKI and updates the records

### Chinese Citation Styles (GB/T 7714)

For Chinese academic papers, the GB/T 7714-2015 standard is mandatory. The `zotero-chinese/styles` project provides properly formatted CSL files.

**Installation**:
1. Visit GitHub: zotero-chinese/styles
2. Download the appropriate style:
   - `gb-t-7714-2015-numeric.csl` — Numeric citation style [1]
   - `gb-t-7714-2015-author-date.csl` — Author-date style (Zhang, 2024)
   - `gb-t-7714-2015-note.csl` — Footnote style
3. Install in Zotero: Preferences > Cite > Styles > + (add from file)

**For LaTeX users**: Use the `gbt7714` package:
```latex
\usepackage{gbt7714}
% Numeric style:
\bibliographystyle{gbt7714-numerical}
% Author-year style:
\bibliographystyle{gbt7714-author-year}
```

### Sync Configuration
- Enable Zotero Sync for library metadata (free, unlimited)
- For PDF storage, choose ONE of:
  - Zotero Storage (300MB free, paid plans available)
  - WebDAV (e.g., via institutional storage or Nextcloud)
  - Linked files with cloud folder (Dropbox/OneDrive/Google Drive) via ZotFile

---

## Library Organization System

### Folder (Collection) Structure

Design your folder hierarchy around projects and workflow stages:

```
My Library/
  |-- Active Projects/
  |     |-- [Project Name 1]/
  |     |     |-- Core Papers
  |     |     |-- Methods
  |     |     |-- Related Work
  |     |-- [Project Name 2]/
  |-- Courses/
  |     |-- [Course Name]/
  |-- Reading Queue/
  |     |-- To Read (High Priority)
  |     |-- To Read (Low Priority)
  |-- Writing Projects/
  |     |-- [Paper Title Draft]/
  |-- Archive/
  |     |-- Completed Projects
```

### Tagging System

Use a consistent tagging convention with prefixes:

| Prefix | Purpose | Examples |
|--------|---------|---------|
| `topic:` | Research topic | `topic:SOTIF`, `topic:perception` |
| `method:` | Methodology | `method:simulation`, `method:deep-learning` |
| `status:` | Reading status | `status:unread`, `status:pass1`, `status:pass2`, `status:pass3` |
| `quality:` | Assessment | `quality:seminal`, `quality:key`, `quality:minor` |
| `use:` | Intended use | `use:cite-intro`, `use:cite-method`, `use:background` |
| `project:` | Project association | `project:phd-thesis`, `project:safety-review` |

### Color Coding (Optional)
- Red: Must read / critical papers
- Yellow: In progress
- Green: Fully read and noted
- Blue: Reference only (not deeply read)

---

## Adding References: Best Practices

### Quality Control at Import

Poor metadata in = poor citations out. Follow this hierarchy for importing:

1. **Best**: Use the Zotero Connector on the publisher's official page (direct from journal website)
2. **Good**: Import via DOI (right-click > Add Item by Identifier)
3. **Acceptable**: Import from database export (WoS, Scopus .ris/.bib files)
4. **Last resort**: Manual entry (error-prone, avoid when possible)

### Post-Import Checklist
After adding any reference, verify:
- [ ] Authors: Full names, correct order, no duplicates
- [ ] Title: Correct capitalization (sentence case for BibTeX)
- [ ] Year: Correct publication year (not online-first year unless appropriate)
- [ ] Journal/Conference: Full official name (not abbreviation, unless you configure abbreviation lists)
- [ ] Volume, issue, pages: Complete for journal articles
- [ ] DOI: Present and correct
- [ ] Abstract: Present (useful for searching your library)
- [ ] PDF: Attached and correctly named

### Batch Import from Database Exports
1. Export from WoS/Scopus in .ris or .bib format
2. Import into Zotero via File > Import
3. Run duplicate detection: right-click collection > "Find Duplicates"
4. Merge duplicates, keeping the record with best metadata
5. Batch-verify DOIs using DOI Manager plugin

---

## BibTeX and BibLaTeX Management

### Auto-Export Setup (for LaTeX/Overleaf Users)

1. In Better BibTeX preferences, set auto-export to "When idle"
2. Right-click your project collection > Export Collection
3. Choose "Better BibLaTeX" or "Better BibTeX" format
4. Check "Keep updated" to auto-sync changes
5. Save the .bib file in your LaTeX project directory

### BibTeX vs. BibLaTeX

| Feature | BibTeX | BibLaTeX |
|---------|--------|----------|
| Unicode support | Limited | Full |
| Entry types | Basic set | Extended (online, software, dataset) |
| Customization | Limited | Highly flexible |
| Backend | bibtex | biber (recommended) |
| Recommendation | Legacy projects | New projects |

### Common BibTeX Entry Types

```bibtex
@article{zhang2024sotif,
  author  = {Zhang, Yuxin and Li, Wei},
  title   = {Title of the Journal Article},
  journal = {IEEE Transactions on Intelligent Transportation Systems},
  year    = {2024},
  volume  = {25},
  number  = {3},
  pages   = {1234--1248},
  doi     = {10.1109/TITS.2024.XXXXXXX}
}

@inproceedings{wang2024safety,
  author    = {Wang, Ming},
  title     = {Title of Conference Paper},
  booktitle = {Proceedings of the IEEE Intelligent Vehicles Symposium (IV)},
  year      = {2024},
  pages     = {100--106},
  doi       = {10.1109/IV51234.2024.XXXXXXX}
}

@phdthesis{liu2024thesis,
  author = {Liu, Chen},
  title  = {Dissertation Title},
  school = {Jilin University},
  year   = {2024}
}
```

### Citation Style Selection

| Style | Used By | LaTeX Package |
|-------|---------|---------------|
| IEEE | Most engineering journals/conferences | `\bibliographystyle{IEEEtran}` |
| APA 7th | Social sciences, some interdisciplinary | `biblatex-apa` |
| Vancouver (numbered) | Medical journals | `\bibliographystyle{vancouver}` |
| Author-year (Harvard) | Many science journals | `natbib` with `authoryear` |
| GB/T 7714-2015 | Chinese academic standards | `gbt7714` package |
| Chicago | Humanities | `biblatex-chicago` |

**Rule**: Always check the target journal's "Instructions for Authors" for the required citation style BEFORE formatting your bibliography.

---

## PDF Annotation Workflow

### In-Zotero Annotation (Zotero 7+)
1. Double-click a PDF attachment to open in Zotero's built-in reader
2. Use highlighting colors consistently:
   - Yellow: Key findings / important claims
   - Red: Methodology details
   - Green: Definitions / key concepts
   - Blue: References to follow up
   - Purple: Ideas for your own research
3. Add sticky notes for your commentary
4. Annotations are automatically searchable within Zotero

### Extracting Annotations to Notes
1. Right-click the PDF > "Add Note from Annotations"
2. Zotero creates a structured note with all highlights and comments
3. Use these extracted notes for literature review drafting

### Integration with Note-Taking Apps
- **Obsidian**: Use the Zotero Integration plugin (citations + annotations)
- **Notion**: Export notes manually or via Notero plugin
- **Logseq**: Use the Zotero Integration plugin

---

## Collaboration with Group Libraries

### Setting Up a Group Library
1. Go to zotero.org/groups and create a new group
2. Choose visibility: Private (recommended for research groups)
3. Invite collaborators by Zotero username or email
4. Set permissions: Who can add/edit items vs. read-only

### Best Practices for Group Libraries
- Agree on a tagging convention before starting
- Assign one person as "library curator" to maintain quality
- Use sub-collections for different aspects of the shared project
- Do NOT use group libraries as your primary personal library
- Sync regularly to avoid conflicts

---

## Integration with Writing Tools

### Overleaf Integration
1. Export your collection as .bib with Better BibTeX auto-export
2. Upload the .bib file to your Overleaf project
3. Use `\cite{key}` in your LaTeX document
4. For auto-sync: use Overleaf's Git integration + local .bib auto-export

### Microsoft Word Integration
1. Install Zotero Word Plugin (included with Zotero)
2. Use the Zotero tab in Word to insert citations
3. Select your citation style in Document Preferences
4. Click "Add/Edit Bibliography" to generate the reference list

### Google Docs Integration
1. Install the Zotero Connector for your browser
2. Use the Zotero menu in Google Docs toolbar
3. Insert citations and bibliography as with Word

---

## Backup and Data Safety

### Backup Strategy
- **Zotero Sync**: Backs up library metadata to Zotero servers (free)
- **Local backup**: Periodically copy your Zotero data directory
  - Location: `~/Zotero/` (check Preferences > Advanced > Files and Folders)
- **Export backup**: Periodically export entire library as Zotero RDF or BibTeX
- **PDF backup**: If using linked files, ensure your cloud sync covers them

### Data Directory Location
- macOS: `~/Zotero/`
- Windows: `C:\Users\[username]\Zotero\`
- Linux: `~/Zotero/`

### What to Back Up
- `zotero.sqlite` (the database -- most critical)
- `storage/` folder (attached PDFs and files)
- Better BibTeX auto-export .bib files

---

## Common Citation Errors to Avoid

1. **Inconsistent author names**: "Zhang, Y." in one entry, "Yuxin Zhang" in another
2. **Missing DOIs**: Always include DOIs when available
3. **Wrong entry type**: Using @article for conference papers or vice versa
4. **Incomplete page numbers**: "pp. 1-10" should be "1--10" in BibTeX
5. **Journal name inconsistency**: Mixing full names and abbreviations
6. **Citing retracted papers**: Check Retraction Watch database
7. **Self-plagiarism in citations**: Citing your own unpublished work without proper attribution
8. **Orphan citations**: References in the bibliography not cited in text, or vice versa
9. **Incorrect year**: Using online-first date instead of publication date
10. **Missing conference location**: Required by some styles for @inproceedings

---

## Maintenance Checklist (Monthly)

- [ ] Run duplicate detection and merge any duplicates
- [ ] Check for items missing DOIs; batch-retrieve with DOI Manager
- [ ] Verify auto-export .bib files are current
- [ ] Review "Unfiled Items" and organize into collections
- [ ] Clean up "Reading Queue" -- move completed items
- [ ] Back up Zotero data directory
- [ ] Update Zotero and plugins to latest versions
- [ ] Review and clean up tags (merge synonymous tags)

---

## Prompt Templates for Claude

### Convert Formatted References to BibTeX (from gpt_academic)

```
Convert the following formatted references into BibTeX entries.
For each reference:
1. Determine the correct entry type (@article, @inproceedings, @book, etc.)
2. Extract all fields: author, title, journal/booktitle, year, volume,
   number, pages, doi
3. Generate a citation key in the format [firstauthor_lowercase][year]
4. Protect proper nouns in titles with {braces}
5. Use standard BibTeX field names and formatting

References to convert:
[PASTE YOUR REFERENCE LIST HERE]
```

This is especially useful when:
- Converting a bibliography from a Word document to LaTeX
- Importing references from a PDF where metadata extraction fails
- Converting Chinese GB/T 7714 formatted references to BibTeX

### Clean BibTeX Entries
```
Here are BibTeX entries from my .bib file that may have errors:

[PASTE BIBTEX ENTRIES]

Please:
1. Check each entry for completeness (authors, title, year, venue, pages, DOI)
2. Fix capitalization (protect proper nouns with {braces} in BibTeX)
3. Standardize author name format to {Last, First}
4. Identify the correct entry type (@article, @inproceedings, etc.)
5. Flag any entries that appear to be duplicates
6. Add missing fields where you can infer them from context
```

### Generate Citation Keys
```
I use the Better BibTeX citation key format: [auth:lower][year][shorttitle:lower:skipwords:3]

Please generate consistent citation keys for these references:
[LIST OF REFERENCES WITH AUTHOR, YEAR, TITLE]

Ensure no duplicates and that keys are memorable and consistent.
```

### Convert Between Citation Formats
```
I have references in [FORMAT A: APA / IEEE / BibTeX / GB/T 7714] format:

[PASTE REFERENCES]

Please convert them to [FORMAT B] format, maintaining all bibliographic details.
For BibTeX output, use the correct entry types and include DOIs.
```

### Organize References for a Paper Section
```
I am writing the [SECTION: Introduction / Related Work / Methods] of a paper on [TOPIC].

Here are the references I plan to cite in this section:
[LIST REFERENCES WITH ONE-LINE SUMMARIES]

Please help me:
1. Suggest a logical ordering for citing these references
2. Group them by theme or approach
3. Draft citation sentences that introduce each group naturally
4. Identify any gaps where additional citations would strengthen the section
```

### Audit Bibliography Before Submission
```
Here is the bibliography for my paper being submitted to [JOURNAL/CONFERENCE]:
[PASTE BIBLIOGRAPHY OR .BIB FILE]

Please audit for:
1. Completeness of each entry (no missing fields)
2. Consistency of formatting (journal names, author names)
3. Correct entry types
4. Any entries that might be from predatory journals
5. Recency -- flag if too many references are older than 5 years
6. Self-citation ratio (flag if > 20% are self-citations)
7. Balance of citation sources (not over-relying on one group)
```
