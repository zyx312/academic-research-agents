# Data Collection Plan Guide

## Purpose

This skill provides a comprehensive framework for creating research data
collection plans and data management plans (DMPs). It covers the FAIR principles,
DMP templates, data quality assurance, sampling strategies, ethics considerations,
and specific guidance for sensor data collection common in engineering research.

---

## 1. FAIR Data Principles

### Overview

FAIR stands for Findable, Accessible, Interoperable, and Reusable. Data that
meets these principles is more valuable for reuse, reproducibility, and
long-term scientific impact.

### Findable

- **F1:** Data and metadata are assigned globally unique and persistent identifiers (DOIs)
- **F2:** Data are described with rich metadata
- **F3:** Metadata clearly include the identifier of the data they describe
- **F4:** Data and metadata are registered or indexed in a searchable resource

**Practical actions:**
- Register datasets with DOI via Zenodo, Figshare, or institutional repository
- Create comprehensive metadata records with standard vocabularies
- Use discipline-specific metadata standards when available
- Ensure dataset titles and descriptions contain relevant keywords

### Accessible

- **A1:** Data and metadata are retrievable by their identifier using standard protocols
- **A1.1:** The protocol is open, free, and universally implementable
- **A1.2:** The protocol allows authentication and authorization where necessary
- **A2:** Metadata are accessible even when data are no longer available

**Practical actions:**
- Host data on stable platforms with persistent URLs
- Use standard access protocols (HTTP, FTP, API)
- Clearly document access procedures and any restrictions
- Maintain metadata records even if data access is restricted

### Interoperable

- **I1:** Data and metadata use formal, accessible, shared, and broadly applicable language
- **I2:** Data and metadata use vocabularies that follow FAIR principles
- **I3:** Data and metadata include qualified references to other data and metadata

**Practical actions:**
- Use standard file formats (CSV, JSON, HDF5, ROS bags)
- Adopt community data standards and ontologies
- Include cross-references to related datasets and publications
- Document all units, coordinate systems, and encoding schemes

### Reusable

- **R1:** Data and metadata are richly described with accurate and relevant attributes
- **R1.1:** Data and metadata are released with a clear and accessible data usage license
- **R1.2:** Data and metadata are associated with detailed provenance information
- **R1.3:** Data and metadata meet domain-relevant community standards

**Practical actions:**
- Attach a clear license (CC-BY, CC-BY-SA, or similar)
- Document collection methodology, processing pipeline, and known limitations
- Include provenance information (who collected, when, how, why)
- Validate data against community standards and benchmarks

---

## 2. Data Management Plan Template

### DMP Section Structure

```
1. Project Overview
   - Project title and PI
   - Funding agency and grant number
   - DMP version and last update date

2. Data Description
   2.1 Types of data to be collected
   2.2 Data formats and standards
   2.3 Estimated data volume
   2.4 Relationship to existing datasets

3. Data Collection Methods
   3.1 Collection procedures and protocols
   3.2 Instruments and sensors used
   3.3 Calibration procedures
   3.4 Quality control during collection
   3.5 Sampling strategy and coverage

4. Data Organization and Documentation
   4.1 File naming conventions
   4.2 Directory structure
   4.3 Metadata standards used
   4.4 Data dictionaries and codebooks

5. Data Storage and Backup
   5.1 Primary storage location
   5.2 Backup strategy and frequency
   5.3 Storage capacity requirements
   5.4 Security measures (encryption, access control)
   5.5 Disaster recovery plan

6. Data Sharing and Access
   6.1 What data will be shared
   6.2 Access restrictions and reasons
   6.3 Sharing timeline (when will data be available)
   6.4 Sharing platforms and repositories
   6.5 Embargo periods if applicable

7. Data Preservation
   7.1 Long-term archive location
   7.2 Preservation formats
   7.3 Retention period
   7.4 Responsibility for preservation

8. Ethics and Legal Compliance
   8.1 IRB/ethics approval status
   8.2 Informed consent procedures
   8.3 Privacy and anonymization
   8.4 Data use agreements
   8.5 Regulatory compliance (GDPR, China Data Security Law)

9. Roles and Responsibilities
   9.1 DMP oversight (who is responsible)
   9.2 Data collection leads
   9.3 Data management personnel
   9.4 Long-term custodian after project ends

10. Budget for Data Management
    10.1 Storage costs
    10.2 Personnel effort for data management
    10.3 Repository fees
    10.4 Data curation and documentation effort
```

---

## 3. Data Quality Assurance

### Quality Control Framework

```
Stage 1: Pre-Collection QA
  - Calibrate all instruments before deployment
  - Test data collection pipeline end-to-end with sample data
  - Define acceptable ranges for each variable
  - Create data validation rules
  - Train all data collectors on protocols

Stage 2: During-Collection QC
  - Monitor incoming data for anomalies in real-time
  - Run automated validation checks on each data batch
  - Log any deviations from protocol with timestamps
  - Perform spot checks on random samples
  - Back up data at defined intervals

Stage 3: Post-Collection QA
  - Run completeness checks (missing values, gaps)
  - Apply statistical outlier detection
  - Cross-validate against known benchmarks or ground truth
  - Document all cleaning and preprocessing steps
  - Maintain both raw and processed versions of data
```

### Data Validation Rules

Define explicit rules for each data field:

| Field | Type | Valid Range | Required | Validation Rule |
|-------|------|------------|----------|----------------|
| timestamp | datetime | project period | Yes | Monotonically increasing |
| vehicle_speed | float | 0-250 km/h | Yes | Non-negative; flag > 200 |
| gps_latitude | float | -90 to 90 | Yes | Within study area bounds |
| sensor_status | enum | {active, standby, error} | Yes | Must be one of three values |
| temperature | float | -40 to 60 C | No | Flag if outside normal range |

### Handling Missing Data

Document your approach to missing data:

1. **Prevention:** Design collection to minimize gaps
2. **Detection:** Automated checks for missing values
3. **Classification:** Why is the data missing? (sensor failure, exclusion criteria, random)
4. **Treatment:** Imputation method or exclusion criteria
5. **Documentation:** Record the proportion and nature of missing data

---

## 4. Sampling Strategies

### Common Sampling Approaches

| Strategy | When to Use | Advantages | Disadvantages |
|----------|-----------|-----------|--------------|
| Random sampling | Representative coverage needed | Unbiased estimation | May miss rare events |
| Stratified sampling | Known subgroups of interest | Ensures subgroup coverage | Requires prior knowledge |
| Systematic sampling | Regular interval coverage | Simple, even coverage | May miss periodic patterns |
| Cluster sampling | Geographically distributed | Cost-effective for field work | Higher variance |
| Convenience sampling | Exploratory or pilot phase | Easy and cheap | Not representative |
| Purposive sampling | Specific phenomena targeted | Captures rare events | Subjective selection |

### Sample Size Determination

Key factors affecting required sample size:

- **Effect size:** Smaller effects need larger samples
- **Desired confidence level:** Typically 95% (alpha = 0.05)
- **Statistical power:** Typically 80% (beta = 0.20)
- **Population variability:** Higher variability needs larger samples
- **Analysis method:** Complex models may need more data

```
Rule of thumb for common analyses:
  - t-test: 30+ per group
  - ANOVA: 20+ per cell
  - Regression: 10-20 observations per predictor
  - Classification (ML): 1,000+ per class (more for deep learning)
  - Object detection: 1,000+ instances per class (10,000+ preferred)
```

---

## 5. Sensor Data Collection Specifics

### Automotive and Robotics Sensor Data

For research involving vehicles, robots, or IoT systems:

**Common Sensor Types and Data Characteristics:**

| Sensor | Data Rate | Format | Storage per Hour |
|--------|-----------|--------|-----------------|
| Camera (1080p) | 30 fps | H.264/H.265, PNG | 5-15 GB |
| LiDAR (32-128 ch) | 10-20 Hz | PCD, LAS, ROS bags | 3-10 GB |
| Radar | 10-20 Hz | CSV, proprietary | 0.1-1 GB |
| IMU | 100-400 Hz | CSV, binary | 0.01-0.1 GB |
| GPS/GNSS | 1-10 Hz | NMEA, RINEX | 0.001 GB |
| CAN bus | Variable | DBC decoded CSV | 0.1-0.5 GB |

**Synchronization Requirements:**
- Hardware time synchronization across all sensors (PTP or GPS time)
- Software timestamp alignment post-collection
- Maximum acceptable time offset between sensors
- Synchronization validation procedure

**Calibration Documentation:**
- Intrinsic camera parameters (focal length, distortion)
- Extrinsic transforms between sensors (rotation and translation)
- Calibration date and conditions
- Calibration validation results
- Re-calibration schedule

### File Naming Convention for Sensor Data

```
[date]_[session]_[sensor]_[sequence].[ext]

Example: 20250315_session01_camera_front_000001.png
         20250315_session01_lidar_top_000001.pcd
         20250315_session01_metadata.json
```

---

## 6. Ethics and Compliance

### IRB/Ethics Considerations

- **Human subjects:** Any data involving identifiable individuals requires IRB approval
- **Vehicle testing:** May need safety review board approval
- **Public space recording:** Check local laws on surveillance and privacy
- **Minors:** Additional protections required for data involving children
- **Informed consent:** Required for direct participation; may be waived for
  public observation with IRB approval

### Data Privacy Requirements

| Regulation | Jurisdiction | Key Requirements |
|-----------|-------------|-----------------|
| GDPR | European Union | Consent, right to erasure, data minimization |
| China Data Security Law | China | Data classification, security assessment, cross-border transfer |
| PIPL | China | Consent, purpose limitation, data localization |
| HIPAA | United States | PHI protection, de-identification |

### Anonymization Techniques

- **Face blurring** in images and video
- **License plate removal** or replacement
- **GPS coordinate fuzzing** (add noise to precise locations)
- **Timestamp shifting** (offset by random amount)
- **K-anonymity** for tabular data (ensure k identical records per group)
- **Differential privacy** for statistical queries

---

## 7. Data Collection Workflow

### End-to-End Process

```
Planning:
  1. Define data requirements from research questions
  2. Design collection protocol
  3. Select instruments and configure settings
  4. Create file naming and organization scheme
  5. Obtain ethics approval
  6. Train data collectors

Collection:
  7. Calibrate instruments
  8. Conduct pilot collection (small-scale test)
  9. Review pilot data for quality
  10. Refine protocol based on pilot
  11. Execute full data collection
  12. Monitor quality in real-time

Post-Collection:
  13. Validate data completeness and quality
  14. Clean and preprocess data
  15. Generate metadata documentation
  16. Archive raw data separately from processed
  17. Prepare data for sharing (anonymize, format)
  18. Register dataset with DOI
```

---

## 8. DMP Tools and Resources

### DMP Authoring Tools

- **DMPTool** (dmptool.org): Free tool with funder-specific templates
- **DMP Online** (dmponline.dcc.ac.uk): UK-based DMP tool
- **Data Stewardship Wizard** (ds-wizard.org): Guided questionnaire
- **RDMO** (rdmorganiser.github.io): Research Data Management Organiser

### Nature's Recommended Data Repositories

Nature Scientific Data maintains a curated, discipline-organized list of
recommended data repositories. Using a repository from this list:
- Satisfies journal data availability requirements for most top-tier journals
- Signals to reviewers that your data management follows best practices
- Ensures long-term data preservation and discoverability

Key categories and recommended repositories:

| Discipline | Recommended Repositories |
|-----------|------------------------|
| General / Multidisciplinary | Zenodo, Figshare, Dryad, Harvard Dataverse |
| Engineering | IEEE DataPort, Zenodo |
| Genomics / Bioinformatics | GenBank, SRA, ArrayExpress |
| Earth / Environmental | PANGAEA, NOAA NCEI |
| Chemistry | Cambridge Structural Database, ChEMBL |
| Social Sciences | ICPSR, UK Data Archive |
| Neuroscience | OpenNeuro, DANDI |

Always check the current list at nature.com/sdata/policies/repositories
as it is updated regularly.

### ORCID Integration for Data Management

**ORCID (Open Researcher and Contributor ID)** is a persistent identifier
for researchers. Integrating ORCID into your data management workflow:

1. **Register at orcid.org** if you do not already have an ORCID iD.
2. **Link datasets to your ORCID profile:**
   - Most major repositories (Zenodo, Figshare, Dryad) support automatic
     ORCID linkage during upload.
   - Enable the auto-update feature to have new DataCite DOIs automatically
     added to your ORCID record.
3. **Use ORCID in all data publications:**
   - Include your ORCID iD in dataset metadata when depositing.
   - This ensures proper attribution and prevents name ambiguity issues.
4. **Benefits for data management:**
   - Creates a single authoritative record of all your datasets across platforms.
   - Enables funders and institutions to track data outputs from grants.
   - Facilitates proper credit when others reuse your data.
   - Many funders (NSFC, EU Horizon, NSF) now accept or require ORCID.
5. **Include ORCID in your DMP:**
   - List ORCID iDs for all team members responsible for data management.
   - Specify that ORCID will be used for dataset metadata.

### Data Repositories

| Repository | Discipline | Max Size | DOI? | Cost |
|-----------|-----------|----------|------|------|
| Zenodo | General | 50 GB | Yes | Free |
| Figshare | General | 20 GB (free) | Yes | Free/paid |
| Dryad | Life/earth sciences | Variable | Yes | Fee per dataset |
| IEEE DataPort | Engineering | 2 TB | Yes | Free for IEEE members |
| Hugging Face | ML/AI | Variable | No (own ID) | Free |
| OpenDataLab | AI/CV | Variable | No | Free |
| Google Dataset Search | Discovery layer | N/A | N/A | Free (indexes other repos) |

---

## Claude Prompt Templates

### DMP Generator

```
Help me create a Data Management Plan for a research project.

Project information:
- Title: [TITLE]
- Research domain: [DOMAIN]
- Funding agency: [FUNDER]
- Data types to collect: [LIST]
- Estimated data volume: [SIZE]
- Duration: [YEARS]
- Team size: [N]

Generate a complete DMP covering:
1. Data description (types, formats, volumes)
2. Collection methods and quality assurance procedures
3. Storage and backup strategy
4. Data sharing plan with timeline
5. Preservation strategy with archive location
6. Ethics and compliance requirements
7. Roles and responsibilities
8. Budget estimates for data management activities
```

### Data Quality Assessment

```
Evaluate the quality of a research data collection plan.

Data collection plan:
[PASTE PLAN]

Assess against these criteria:
1. FAIR compliance: How well does the plan address each FAIR principle?
2. Quality assurance: Are validation procedures comprehensive?
3. Documentation: Will the metadata be sufficient for reuse?
4. Ethics: Are privacy and consent adequately addressed?
5. Sustainability: Will the data be preservable and findable long-term?

Provide specific recommendations for each criterion with priority levels.
```

### Sensor Data Collection Protocol

```
Help me design a sensor data collection protocol for a research project.

Sensors to use:
[LIST: sensor type, model, data rate, format]

Collection scenario:
[DESCRIBE: environment, conditions, duration, coverage requirements]

Requirements:
- Synchronization method: [hardware / software / both]
- Storage constraints: [available capacity]
- Real-time processing needs: [yes / no]
- Privacy requirements: [list applicable regulations]

Generate:
1. Sensor configuration specifications
2. Calibration procedures
3. Collection protocol (step-by-step)
4. File naming and organization scheme
5. Quality control checklist
6. Estimated storage requirements
7. Post-collection validation procedures
```

### FAIR Assessment Checklist

```
Assess the FAIR compliance of an existing dataset or data management plan.

Dataset/Plan description:
[PASTE DESCRIPTION OR SUMMARY]

Current data management practices:
[DESCRIBE]

For each FAIR principle (F1-F4, A1-A2, I1-I3, R1-R1.3):
1. Current compliance level: [fully / partially / not compliant]
2. Specific gaps identified
3. Recommended actions to improve compliance
4. Effort estimate for each improvement (low / medium / high)
5. Priority ranking based on impact and effort
```
