# TA ČR Data Management Plan (DMP) — Questions for research teams

<!-- ## 0. Project Information

- **Project code:** `[ Please enter the project code ]`
- **Project name:** `[ Please enter the project name ]`
- **Date:** `[ Please enter the date ]`
- **Data Management Plan version:** `[ Please fill in the DMP version number ]`
- **Processor of the Data Management Plan:** `[ Please fill in name and contact details ]`

--- -->

## 1. Data Description

> **Main Question:** What data will you create, process, or collect?

- **1.1 Will you create/collect new data?**

  - [ ] **YES**

    - **Describe what data you will create or collect.**
    - **[ Text Box ]**
    - > hint: [Examples of data: software source code, AI model weights/parameters, custom datasets, training logs, or synthetic data - please describe the data in more detail.]
      >
    - > hint: [You may provide a link to a README file in your repository (e.g. GitHub, Zenodo). **Ensure data is machine-readable** (e.g. .csv, .json, .jpg, .pth) and NOT a PDF, Word document, or screenshot of a table.]
      >
  - [ ] **NO**
- **1.2 Will you use existing data?**

  - [ ] **YES**

    - **Describe what data you will process and how. State whether it will be your own or external data and how you will obtain it.**
    - **[ Text Box ]**
    - > hint: [Examples of data: public datasets, API-sourced data, or proprietary archives. Please include the source, any licensing restrictions, and the version of the dataset used.]
      >
    - > hint: [You may provide a link to a README in a repository (e.g. GitHub, Zenodo). **Ensure data is machine-readable** (e.g. .csv, .json, .jpg, .pth) and NOT a PDF, Word document, or screenshot of a table.]
      >
  - [ ] **NO**

---

## 2. Data Management

> **Main Question:** What methods and principles of their management will you use with regard to FAIR principles?

>> **2.1 Findability (max. 3000 characters)**
>>

- **Will the data be in a machine-readable format?**

  - > hint: [As noted in the description section, this means structured data (e.g. .csv, .json, .pth) and not PDFs or screenshots.]
    >

  - [ ] **YES**
  - [ ] **NO**
    - Please explain why the data cannot be provided in a machine-readable format:
      **[ Text Box ]**
- **Will they have a persistent identifier (PID) or digital object identifier (DOI)?** <sub>A persistent identifier is required to guarantee permanent access, prevent broken links over time, and enable direct, trackable citations of the dataset in future research.</sub>

  - [ ] **If already available**:  Provide a link to your published repository entry with assigned identifier
  - [ ] **If planned**: State your target repository and the means of acquiring a PID/DOI
  - [ ] **NO** -> explain why: **[ Text Box ]**

  * > hint: [Repositories like Zenodo assign a DOI automatically]
    >
  * > hint: [If the data is software itself there are 2 ways of obtaining an identifier through the same provider [SoftwareHeritage](https://www.softwareheritage.org/) -> assigns a SWHID (software hash identifier):
    >
    > 1. [Zenodo/GitHub integration](https://help.zenodo.org/docs/github/)
    > 2. [How to archive reference code](https://www.softwareheritage.org/how-to-archive-reference-code/)]
    >
- **Where and how is (or will) your research metadata (be) provided in a standard, findable format?**

  - > hint: [What is metadata?](https://www.openaire.eu/what-is-metadata?highlight=WyJtZXRhZGF0YSJd)
    >

  - [ ] **If already available**: Provide a link to your published repository entry (e.g. Zenodo) or GitHub repo containing a <em>CITATION.cff</em> or <em>.zenodo.json</em> file.
  - [ ] **If planned**: State your target repository (e.g. Zenodo) or write: "Data/code will be deposited in a FAIR repository like Zenodo using DataCite metadata."

  - **Guide for GitHub users**: Zenodo Guide: [Making a GitHub Repository Citable](https://zenodo.org/records/22101577)

  - >**Checklist of metadata items to account for:**

   - **Required Metadata by TA ČR** (see [TACR_requirements.pdf](https://tacr.gov.cz/wp-content/uploads/documents/2026/06/19/1781873126_Research%20data%20and%20open%20access%20to%20outputs_results.pdf#page=6)): Name of the data, full names of creators and contributors, information about the funding provider, programme, and project, publication date, language of the data, length of embargo, persistent (permanent) identifier (e.g. Digital Object Identifier / DOI)
    - **Recommended Metadata**: License conditions, permanent identifiers of persons, permanent identifiers of organisations, permanent identifiers of funding
    - **Repository Information for Reuse & Validation**: Other research results, tools and instruments needed to reuse or validate research data -> README.md file in most cases

>> **2.2 Accessibility**
>>
- **Will you store data in a repository? Which one?**

  **Select all that apply**:

      [ ] Zenodo
      [ ] GitHub
      [ ] GitLab
      [ ] Hugging Face
      [ ] Other: [ Text Box ]

    **Note**: GitHub/GitLab/Hugging Face are "code repositories" in software engineering, they do not not meet the scientific definitions of a trusted digital repository though. They lack permanent preservation guarantees, immutable version snapshots, and native persistent identifiers (DOIs).
    <!-- TODO: reference software heritage, possibly merge with the question referring to persistent identifiers - elegant solution: [Software Heritage Save Action](https://github.com/sdruskat/swh-save-action) -->
      
>> **2.3 Interoperability**
>>

- **How will you ensure your data and software can be easily opened, exchanged, and integrated with other tools (interoperability)? (Select all that apply)**

  [ ] **Open File Formats**: Non-proprietary, open formats (e.g. .csv, .json, .py, .txt, .pdf).

  [ ] **Proprietary / Software-Specific Formats**: Formats requiring specific commercial software or specialized hardware (e.g. MATLAB .mat, LabVIEW, CAD binaries).

  >[ If selected ]: Please briefly explain why proprietary formats are necessary (e.g. hardware restrictions) and if open exports (e.g. CSV) or conversion tools will be provided - or provide a link to your README.md where this is documented. [ Text Box ]

  [ ] **Controlled Vocabularies / Ontologies**: Discipline-specific taxonomies, subject headings, or standard variable naming schemes.

  [ ] **APIs / Standard Protocols**: Programmatic access endpoints or REST APIs.

  [ ] **Undecided / Assistance Needed**: No specific interoperability standards planned yet (a Data Steward will reach out to offer guidance). -> (**make this an exclusive option that deselects previous options**)

>> **2.4 Reusability**
>>

>> Access, Licensing & Reusability (better heading as it covers all of those)
>>

- **How will your data and software be made available for third-party reuse, and under what terms?**

  (Select the option that best describes your primary sharing strategy)

  [ ] **Open Access (Standard Open License)**: Freely available immediately upon publication or project completion under a standard open license.

    Selected license (if known):

      Data: [ ] CC BY 4.0  [ ] CC0 (Public Domain)  [ ] Other: [ Text Box ]

      Code/Models: [ ] MIT  [ ] Apache 2.0  [ ] GPL v3  [ ] Other: [ Text Box ]

  [ ] **Embargoed Access**: Restricted during the project, but will be released under an open license after a set period.

  >Planned release date / event: [ e.g. 12 months post-project / upon paper acceptance ]
  Reason for embargo: [ Text Box ]

  [ ] **Restricted / Controlled Access**: Available only upon request or under bilateral agreement (e.g. NDA) due to specific constraints.

  >Reason for restriction: [ ] Industrial Partner IP / Trade Secret  [ ] Patent Pending  [ ] GDPR / Sensitive Data

  >How to request access: [ Text Box - e.g. contact PI / project management office under formal DPA/NDA ]

  [ ] **Closed**: Cannot be shared with third parties due to strict commercial IP, partner contracts, or legal restrictions.

---

## 3. Data Storage

> **Main Question:** How will you store the data during the project implementation and keep it after the end of the project? How will the data be secured?

>> **3.1 Storage**
>>
- **Where will active working data, raw captures, code, and model checkpoints live during development?** (Select all that apply)

  [ ] **Institutional Storage / NAS**: CIIRC ČVUT central servers or lab NAS arrays (automatically backed up).

  [ ] **Code Versioning Platforms**: GitHub / GitLab (strictly for source code, scripts, and small config files).

  [ ] **High-Performance Computing (HPC)**: National/international HPC clusters (e.g. IT4Innovations, EuroHPC, Metacentrum).

  [ ] **Commercial Cloud Storage**: AWS, Azure, Google Cloud, or specialized GPU cloud platforms.

  [ ] **Local Workstations / Hardware Testbeds**: NVMe/SSDs on local machines, edge hardware, or physical test rigs.

  >[If selected]: Briefly explain how local files are backed up to prevent data loss (e.g. automated daily sync to CIIRC NAS). [ Text Box ]

  [ ] **Industrial Partner Infrastructure**: On-premise servers or hardware provided directly by commercial partners under NDA (Non-Disclosure Agreement).

>> **3.2 Security**
>>
- **Does your project handle sensitive, personal (GDPR), or NDA-restricted industrial data?**

  (NDA: Non-Disclosure Agreement, RBAC: Role-Based Access Control)

  [ ] **NO** Project uses non-sensitive public datasets, synthetic data, or open-source software. (Standard CIIRC IT security applies)

  [ ] **YES** Protected using the following measures (select all that apply):

      [ ] Restricted Access: Limited to authorized project staff (RBAC / password protection).

      [ ] Contractual & Legal: Governed by partner NDAs or formal data-sharing agreements.

      [ ] Anonymization / Privacy: Personal identifiers stripped or pseudonymized before processing.

      [ ] Encrypted / Secure Storage: Stored on encrypted drives or non-public secure servers.

---
<!-- 
## 4. Costs & Output Utilization -> TODO to be clarified internally

> **Main Question:** What will be the costs of data management and ensuring FAIR principles? How will you cover these costs?

>> **4.1 Costs**
>>

- **What will be the costs of data management?**
  - Publishing on GitHub/Zenodo is free of charge.
    Internal repositories storage are paid by internal resources.
- **How will you cover these costs?** -->

---

## 4. Responsible Person

> **Main Question:** Will you have a person responsible for data management within your project?

>> **5.1 Responsible Person**
>>
- Do you have someone in your organization who is responsible for data management?

  [ ] **NO**

  [ ] **YES**
  - **Please indicate his/her position/role in the project.**
  
    [ Text Box ]

<!-- - ~~**Please indicate his/her position/role in the project.**~~ -->

---

<!-- ## 6. TODO Results documentation - TA ČR excel sheet - only in Czech...

see [Document](https://www.dropbox.com/scl/fi/mhwra6z0jmp7yq5c9drdz/1752427291_1748344328_Informace-o-otev-en-m-p-stupu-k-v-sledk-m-a-dat-m.xlsx?rlkey=qzty30hog34w58hgad8d6zfvn&dl=0) -->

<!-- ## 6. Conclusion

- **6.1 Additional Information (max. 3000 characters):** Enter any additional information relating to the Data Management Plan.
- **6.2 Comments / Feedback (max. 3000 characters):** Enter any comments or suggestions on how to improve the form. -->
