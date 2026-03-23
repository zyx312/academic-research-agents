# Data Agreement Guide

## Purpose

This skill provides a comprehensive framework for creating, reviewing, and
negotiating data sharing agreements for academic research. It covers types of
agreements (DUA, DTA, MTA, NDA), key clauses, regulatory compliance, negotiation
strategies, and template structures for common data exchange scenarios.

---

## 1. Types of Data Agreements

### Data Use Agreement (DUA)

- **Purpose:** Governs how a data recipient may use data provided by a data owner
- **Direction:** One-way (provider to recipient)
- **Common scenario:** University receives clinical data from a hospital;
  researcher accesses government statistics; company shares proprietary data
  with a research lab
- **Key focus:** Restrictions on use, security requirements, publication rights

### Data Transfer Agreement (DTA)

- **Purpose:** Governs the physical or electronic transfer of data between parties
- **Direction:** One-way or bidirectional
- **Common scenario:** Two universities share data for a collaborative project;
  data transferred across national borders
- **Key focus:** Transfer mechanisms, security during transit, data handling
  after transfer, cross-border compliance

### Material Transfer Agreement (MTA)

- **Purpose:** Governs transfer of physical research materials (biological samples,
  chemical compounds, hardware prototypes) along with associated data
- **Direction:** Usually one-way
- **Common scenario:** University sends cell lines with genomic data to a
  collaborating lab
- **Key focus:** Material handling, derivative works, publication acknowledgment

### Non-Disclosure Agreement (NDA)

- **Purpose:** Protects confidential information shared between parties
- **Direction:** Unilateral or mutual
- **Common scenario:** Industry partner shares proprietary data for a feasibility
  study; pre-collaboration discussions involving trade secrets
- **Key focus:** Definition of confidential information, duration, exclusions

### Comparison Matrix

| Aspect | DUA | DTA | MTA | NDA |
|--------|-----|-----|-----|-----|
| Data only | Yes | Yes | No (material + data) | Yes |
| Physical material | No | Sometimes | Yes | No |
| IP transfer | No | No | Sometimes | No |
| Publication rights | Often restricted | Negotiated | Negotiated | Usually silent |
| Typical duration | Project length | Project length | Varies | 2-5 years |
| Regulatory complexity | Medium-High | High (cross-border) | Medium | Low |

---

## 2. Key Clauses in Data Agreements

### Essential Clauses

```
1. Purpose Limitation
   - What the data may be used for (specific research project)
   - What the data may NOT be used for (commercial, re-identification)
   - Restriction to named project and named personnel

2. Data Description
   - What data is being shared (specific datasets, fields, formats)
   - Volume and format
   - Whether raw, processed, or aggregated
   - Associated metadata and documentation

3. Security Requirements
   - Storage and encryption standards
   - Access control (who may access, authentication methods)
   - Physical security (locked office, secure server room)
   - Network security (firewalls, VPN, air-gapped systems)
   - Incident reporting procedures for data breaches

4. Retention and Destruction
   - How long the recipient may keep the data
   - Destruction method (secure deletion, certificate of destruction)
   - Whether copies may be retained for reproducibility
   - Timeline for destruction after project completion

5. Publication Rights
   - Right to publish findings derived from the data
   - Pre-publication review period for data provider
   - Acknowledgment requirements
   - Restrictions on publishing raw data or identifying information

6. Derivative Works
   - Can the recipient create derived datasets?
   - Who owns derivatives (new annotations, combined datasets)?
   - Can derivatives be shared with third parties?
   - Do derivatives fall under the same agreement terms?

7. Third-Party Sharing
   - Can the recipient share data with collaborators?
   - Requirements for sub-agreements
   - Restrictions on sharing with specific entities

8. Liability and Indemnification
   - Data provided "as is" without warranty
   - Recipient assumes responsibility for compliant use
   - Indemnification for breaches by the recipient
   - Limitation of liability for data quality issues

9. Termination
   - Conditions for terminating the agreement
   - Data handling obligations upon termination
   - Surviving obligations (confidentiality, destruction)

10. Governing Law
    - Which jurisdiction's laws apply
    - Dispute resolution mechanism (arbitration, litigation)
    - Venue for legal proceedings
```

---

## 3. Regulatory Compliance

### GDPR (European Union)

| Requirement | Implications for Data Agreements |
|-------------|--------------------------------|
| Lawful basis | Agreement must specify legal basis for processing |
| Purpose limitation | Data use must be limited to stated purposes |
| Data minimization | Only necessary data should be transferred |
| Storage limitation | Retention periods must be specified |
| Data subject rights | Procedures for handling access/deletion requests |
| Cross-border transfer | Standard contractual clauses or adequacy decision needed |
| Data Protection Impact Assessment | May be required for high-risk processing |

### China Data Security Law and PIPL

| Requirement | Implications for Data Agreements |
|-------------|--------------------------------|
| Data classification | Important data requires security assessment |
| Cross-border transfer | Security assessment required for important data leaving China |
| Data localization | Certain data must be stored within China |
| Consent | Individual consent required for personal information |
| Purpose limitation | Must specify and limit data processing purposes |
| Data processor obligations | Clear responsibilities for data processors |
| Government access | Data may be subject to government access requests |

### HIPAA (United States)

| Requirement | Implications for Data Agreements |
|-------------|--------------------------------|
| Limited Data Set | DUA required for limited datasets without direct identifiers |
| De-identification | Safe Harbor or Expert Determination method must be documented |
| Business Associate Agreement | Required when sharing PHI with a third party |
| Minimum necessary | Only the minimum data needed should be shared |
| Breach notification | 60-day notification requirement for breaches |

### Multi-Jurisdictional Considerations

When data crosses borders between different regulatory regimes:

1. **Identify applicable regulations** for both data origin and destination
2. **Apply the most restrictive** requirements to the agreement
3. **Include specific cross-border transfer clauses** (SCCs for GDPR)
4. **Document compliance basis** for each jurisdiction
5. **Consider data localization** requirements that may prohibit transfer
6. **Engage legal counsel** familiar with international data law

---

## 4. Negotiation Points

### Common Negotiation Issues

| Issue | Provider Position | Recipient Position | Compromise |
|-------|------------------|-------------------|-----------|
| Publication review | 60-day review, veto power | No review | 30-day review, suggest only |
| Derivative data ownership | Provider owns all derivatives | Recipient owns derivatives | Joint ownership or field-of-use split |
| Commercial use | Prohibited | Unrestricted | Allowed with separate license |
| Data retention | Destroy within 30 days | Keep indefinitely | Keep for 5 years for reproducibility |
| Third-party sharing | Prohibited | Allowed freely | Allowed with sub-agreements |
| Exclusivity | Exclusive access | Non-exclusive | Time-limited exclusivity |
| Indemnification | Full indemnification by recipient | Mutual indemnification | Reasonable mutual indemnification |

### Negotiation Strategy for Academics

```
1. Start with a standard template (FDP DTUA or institutional template)
2. Identify your non-negotiable requirements:
   - Right to publish (essential for academic work)
   - Reasonable review period (not indefinite)
   - Ability to retain data for reproducibility
3. Identify areas of flexibility:
   - Security measures (you can usually meet provider's requirements)
   - Acknowledgment language (easy to accommodate)
   - Destruction timeline (negotiate for reproducibility period)
4. Escalate difficult points to your Office of Research or legal counsel
5. Document all agreed terms in writing before signing
```

### Red Flags in Data Agreements

Watch for these terms that may be problematic for academic research:

- **Perpetual publication veto:** Provider can prevent any publication
- **Assignment of IP:** Recipient must assign all IP to provider
- **Unlimited liability:** Recipient assumes all liability without caps
- **Data return without copies:** Cannot retain data for reproducibility
- **Unilateral modification:** Provider can change terms without notice
- **Overbroad confidentiality:** Prevents discussing any aspect of the data
- **Auto-renewal without exit:** Agreement renews indefinitely with no way out
- **Audit rights without notice:** Provider can inspect your systems anytime

---

## 5. Template Structures

### Simple DUA Template (Between Two Universities)

```
DATA USE AGREEMENT

1. PARTIES
   Provider: [University A, Department, Contact Person]
   Recipient: [University B, Department, Contact Person]

2. DATASET
   Description: [Specific dataset being shared]
   Format: [File formats, delivery method]
   Volume: [Size and number of records]

3. PURPOSE
   The data shall be used solely for: [Specific research project title
   and description]

4. AUTHORIZED USERS
   Access is limited to: [Named individuals and their roles]

5. SECURITY
   The Recipient shall:
   a. Store data on password-protected systems
   b. Encrypt data at rest and in transit
   c. Restrict access to authorized users only
   d. Report any security incidents within 48 hours

6. USE RESTRICTIONS
   The Recipient shall NOT:
   a. Attempt to re-identify any de-identified data
   b. Use data for commercial purposes
   c. Share data with any third party without written consent
   d. Use data for any purpose other than stated in Section 3

7. PUBLICATIONS
   a. Recipient may publish findings derived from the data
   b. Provider shall receive manuscripts 30 days before submission
   c. Recipient shall acknowledge the data source in all publications

8. RETENTION AND DESTRUCTION
   a. Data shall be retained for [N years] after project completion
   b. Data shall be securely destroyed after the retention period
   c. Recipient shall provide a certificate of destruction

9. TERM AND TERMINATION
   a. This agreement is effective from [DATE] to [DATE]
   b. Either party may terminate with 30 days written notice
   c. Sections 5, 6, and 8 survive termination

10. GOVERNING LAW
    This agreement shall be governed by the laws of [JURISDICTION]

SIGNATURES
Provider: _________________ Date: _________
Recipient: ________________ Date: _________
```

### Industry-Academic DUA (Additional Clauses)

When data comes from an industry partner, add:

```
ADDITIONAL CLAUSES FOR INDUSTRY DATA

11. INTELLECTUAL PROPERTY
    a. Background IP remains with the originating party
    b. Foreground IP arising from the research shall be [owned by / licensed to]
    c. Provider receives a non-exclusive license to academic publications

12. CONFIDENTIALITY
    a. Proprietary data shall be treated as confidential
    b. Confidentiality obligations survive for [N years] after termination
    c. Exclusions: publicly available information, independently developed,
       required by law

13. EXPORT CONTROL
    a. Data may be subject to export control regulations
    b. Recipient shall comply with all applicable export control laws
    c. Recipient shall not transfer data to embargoed countries or persons

14. INDEMNIFICATION
    a. Each party shall indemnify the other against claims arising from
       its own breach of this agreement
    b. Neither party shall be liable for indirect or consequential damages
    c. Total liability shall not exceed [AMOUNT or the value of the data]
```

---

## 6. IP Considerations

### Who Owns What?

| Data Element | Typical Ownership | Negotiable? |
|-------------|------------------|-------------|
| Raw data | Data provider | Rarely |
| Annotations added by recipient | Recipient | Yes |
| Models trained on data | Recipient | Yes, often contested |
| Derived datasets | Negotiated | Yes |
| Published findings | Authors (academic norm) | Usually not |
| Software tools developed | Developer | Yes |
| Patents from research | Inventor's institution | Yes |

### Protecting Academic Freedom

Ensure the agreement preserves:

1. **Right to publish:** Findings can be published after reasonable review period
2. **Thesis use:** Student theses can include results based on the data
3. **Conference presentations:** Results can be presented at academic conferences
4. **Follow-on research:** Insights gained can inform future work
5. **Teaching use:** Anonymized or aggregated examples can be used in courses

---

## 7. Agreement Lifecycle Management

### Process from Request to Execution

```
Week 1-2: Initiation
  - Identify data needs and potential providers
  - Make informal contact and gauge willingness
  - Determine which type of agreement is needed

Week 3-4: Drafting
  - Start with institutional or FDP template
  - Customize terms for specific data and project
  - Internal review by PI and research administration

Week 5-8: Negotiation
  - Exchange drafts with the other party
  - Negotiate contentious terms
  - Involve legal counsel for complex issues
  - Document all agreed changes

Week 9-10: Approval and Execution
  - Final review by authorized signatories
  - Obtain required institutional approvals
  - Execute (sign) the agreement
  - Distribute copies to all relevant parties

Ongoing: Compliance
  - Implement security measures as agreed
  - Train authorized users on their obligations
  - Monitor compliance with use restrictions
  - Report any incidents promptly
  - Prepare for data destruction when term ends
```

### Annual Compliance Review

For long-term agreements, conduct an annual review:

- [ ] All authorized users are still actively involved in the project
- [ ] Security measures are still in place and current
- [ ] Data is stored only in approved locations
- [ ] No unauthorized sharing has occurred
- [ ] Publication review requirements have been followed
- [ ] Agreement is still within its term period
- [ ] No regulatory changes require agreement updates

---

## 8. Special Scenarios

### Cross-Border Data Transfer (China to/from International)

Key considerations:
- China Data Security Law requires security assessment for important data
- PIPL requires consent and security assessment for personal information
- Standard contractual clauses may be needed
- Data localization requirements may restrict transfer
- Consider anonymizing or aggregating data to reduce regulatory burden
- Engage legal counsel familiar with both jurisdictions

### Multi-Party Data Sharing

When more than two parties share data:
- Consider a master data sharing agreement with all parties
- Define a data governance committee
- Assign a data custodian responsible for compliance
- Clarify which parties may share with which other parties
- Define procedures for adding new parties

### Student and Postdoc Access

When students or postdocs need data access:
- Name them as authorized users in the agreement
- Ensure they sign individual confidentiality agreements
- Plan for their departure (data access revocation, destruction)
- Determine whether thesis use is permitted
- Define what happens to their work products after departure

---

## Claude Prompt Templates

### DUA Drafter

```
Help me draft a Data Use Agreement for an academic research data exchange.

Parties:
- Data Provider: [NAME, INSTITUTION, COUNTRY]
- Data Recipient: [NAME, INSTITUTION, COUNTRY]

Data description:
- Dataset: [DESCRIPTION]
- Format: [FILE TYPES]
- Size: [VOLUME]
- Contains personal data: [YES / NO]
- Contains proprietary data: [YES / NO]

Research project: [TITLE AND BRIEF DESCRIPTION]
Duration: [START TO END DATE]
Authorized users: [LIST OF NAMES AND ROLES]

Specific requirements:
- Publication rights: [DESCRIBE ANY RESTRICTIONS]
- Security level: [STANDARD / HIGH / VERY HIGH]
- Cross-border transfer: [YES / NO, WHICH COUNTRIES]
- Applicable regulations: [GDPR / PIPL / HIPAA / OTHER]

Generate a complete DUA with all standard clauses, customized for
these specific circumstances.
```

### Agreement Review Checklist

```
Review the following data agreement and identify potential issues.

Agreement text:
[PASTE AGREEMENT]

My role: [DATA PROVIDER / DATA RECIPIENT]
Institution type: [UNIVERSITY / COMPANY / GOVERNMENT]
Country: [COUNTRY]

Evaluate:
1. Are all essential clauses present? (List any missing)
2. Are any terms potentially problematic for academic freedom?
3. Are security requirements reasonable and achievable?
4. Is the publication clause acceptable for academic use?
5. Are IP ownership terms clear and fair?
6. Is the liability allocation reasonable?
7. Are there any regulatory compliance gaps?
8. Are there any red flags or unusual terms?
9. What terms should be negotiated before signing?
10. Overall risk assessment: [Low / Medium / High]
```

### Negotiation Position Paper

```
Help me prepare a negotiation position for a data agreement.

My institution: [NAME, TYPE]
Other party: [NAME, TYPE]
Data involved: [DESCRIPTION]
Current draft issues: [LIST PROBLEMATIC TERMS]

For each issue:
1. Why the current term is problematic
2. What we ideally want
3. What we could accept as a compromise
4. Arguments supporting our position
5. What we can offer in exchange

Also provide:
- Overall negotiation strategy recommendation
- Priority ranking of issues (must-win vs nice-to-have)
- Language suggestions for revised clauses
```

### Compliance Assessment

```
Assess regulatory compliance for a planned data sharing arrangement.

Data characteristics:
- Contains personal data: [YES / NO, WHAT KIND]
- Data origin country: [COUNTRY]
- Data destination country: [COUNTRY]
- Data sensitivity level: [LOW / MEDIUM / HIGH]
- Data subjects: [DESCRIBE WHOSE DATA IT IS]

Applicable regulations to check:
[LIST OR SAY "ALL POTENTIALLY APPLICABLE"]

For each applicable regulation:
1. Key requirements that apply to this data sharing
2. Current compliance status: [compliant / gap identified]
3. Required documentation or approvals
4. Steps needed to achieve compliance
5. Timeline estimate for compliance activities
6. Whether legal counsel should be consulted
```
