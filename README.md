# PHA4GE Meningitis Metadata Standard

_A community-developed, ontology-anchored metadata standard for harmonised meningitis surveillance, laboratory diagnostics and pathogen genomics._

![Standard version](https://img.shields.io/badge/standard-v1.0-blue)
![Template version](https://img.shields.io/badge/template-v1.1-informational)
![Format](https://img.shields.io/badge/format-Excel-green)
![Community](https://img.shields.io/badge/PHA4GE-community%20standard-orange)

## Table of contents

- [Overview](#overview)
- [Why this standard is needed](#why-this-standard-is-needed)
- [Version 1 scope](#version-1-scope)
- [Community development](#community-development)
- [Ontology-linked semantics](#ontology-linked-semantics)
- [Repository contents](#repository-contents)
- [Data model](#data-model)
- [Getting started](#getting-started)
- [Field requirement levels](#field-requirement-levels)
- [Controlled vocabularies and picklists](#controlled-vocabularies-and-picklists)
- [Current implementation notes](#current-implementation-notes)
- [Versioning and roadmap](#versioning-and-roadmap)
- [Contributing and feedback](#contributing-and-feedback)
- [Citation](#citation)
- [Licence](#licence)
- [Acknowledgements and contact](#acknowledgements-and-contact)

## Overview

The **PHA4GE Meningitis Metadata Standard** provides a harmonised framework for collecting, managing and exchanging contextual metadata associated with meningitis cases, clinical specimens, laboratory diagnostics and pathogen genomic data.

The standard connects patient, specimen, diagnostic, sequencing and bioinformatics information through shared identifiers and consistent terminology. It is intended to support public health surveillance, outbreak investigation, laboratory reporting, genomic epidemiology, research and responsible data sharing across institutions and countries.

Version 1 is supplied as a structured Microsoft Excel implementation with controlled vocabularies, field guidance, requirement levels and a consolidated data dictionary. The current stable data-entry workbook is **`Meningitis_Metadata_Template_v1_1.xlsx`**.

## Why this standard is needed

Meningitis surveillance data are frequently distributed across separate clinical, laboratory and genomic systems. Common challenges include:

- missing or inconsistently captured clinical and epidemiological data, including vaccination history, patient outcomes and travel history;
- weak linkage between patient, specimen, diagnostic and sequence records;
- overlapping or locally developed data-collection forms;
- inconsistent terminology and result representation;
- limited interoperability between national, regional and global surveillance systems; and
- insufficient contextual information for interpreting genomic and molecular results.

The standard addresses these challenges by minimising unnecessary free text, promoting controlled vocabularies, documenting field definitions and guidance, and linking metadata concepts to biomedical ontologies where suitable terms are available.

## Version 1 scope

Version 1 focuses on bacterial and fungal causes of meningitis relevant to public health surveillance and genomic epidemiology.

### Bacterial pathogens

- *Neisseria meningitidis*
- *Streptococcus pneumoniae*
- *Haemophilus influenzae*
- *Streptococcus agalactiae* (Group B Streptococcus)
- *Listeria monocytogenes*
- *Escherichia coli*, including K1-associated disease
- *Klebsiella pneumoniae*

### Fungal pathogens

- *Cryptococcus neoformans*

### Out of scope for Version 1

Viral meningitis metadata are not included in the current release. Viral pathogens, assays and associated reporting variables are planned for Version 2.

The standard is designed primarily for community-acquired and hospital-managed meningitis surveillance. It is not a replacement for clinical case definitions, treatment guidelines, electronic health records, laboratory quality-management systems or regulatory reporting requirements.

## Community development

The standard was developed through the **Public Health Alliance for Genomic Epidemiology (PHA4GE) Data Standards Initiative** using a community-driven process involving specialists in microbiology, laboratory medicine, meningitis surveillance, genomic epidemiology, public health, bioinformatics and data management.

Development included:

- review of existing meningitis surveillance and reporting variables;
- stakeholder workshops and field-by-field domain review;
- agreement on required, recommended and optional fields;
- development and refinement of controlled vocabularies;
- ontology mapping and definition review;
- iterative testing of an Excel-based data-collection template; and
- stakeholder validation of the Version 1 backbone.

The in-person standards workshop held from **4–7 May 2026** advanced the data dictionary, field tiering, controlled vocabularies and organism-specific diagnostic and genomic content.

## Ontology-linked semantics

Stakeholder terminology is preserved while canonical field labels, definitions and ontology identifiers are provided where suitable mappings can be verified.

The curation approach is to:

- retain terminology agreed by the meningitis stakeholder community;
- search authoritative biomedical ontology resources for suitable concepts;
- use verified ontology identifiers and verbatim ontology definitions where appropriate;
- preserve community-defined terms where no suitable ontology concept exists; and
- identify unresolved concepts for future ontology review or New Term Requests.

Ontology-linked fields and values support semantic interoperability with external databases, standards and analytical systems without removing terminology familiar to laboratories and surveillance programmes.

## Repository contents

This repository contains the Version 1 resources that define and support the **PHA4GE Meningitis Metadata Standard**.

```text
.
├── README.md
├── LICENSE
├── CITATION.cff
├── template/
│   └── Meningitis_Metadata_Template_v1_1.xlsx
├── metadata-backbone/
│   ├── Case_Patient_Information_v1.xlsx
│   ├── Specimen_Metadata_v1.xlsx
│   ├── Diagnostic_Methods_v1.xlsx
│   ├── Sequencing_Metadata_v1.xlsx
│   └── Bioinformatics_QC_Metadata_v1.xlsx
└── docs/
    └── Meningitis_Workshop_Report.pdf
```

### Metadata collection template

The [`template/`](template/) directory contains **`Meningitis_Metadata_Template_v1_1.xlsx`**, the Excel data-entry implementation for collecting meningitis metadata across the five Version 1 domains. The workbook includes colour-coded requirement levels, controlled-vocabulary dropdowns, field guidance, linking identifiers and a consolidated data dictionary.

### Metadata backbone

The [`metadata-backbone/`](metadata-backbone/) directory contains the annotated domain specifications that define Version 1:

- **Case / Patient Information:** patient identifiers, demographics, geographic information, clinical presentation, vaccination history, hospital information, outcomes and follow-up.
- **Specimen Metadata:** specimen identifiers, anatomical material, collection and receipt details, collection devices, sampling sites and laboratory provenance.
- **Diagnostic Methods:** macroscopy, microscopy, CSF biochemistry, antigen testing, culture, organism identification, antimicrobial susceptibility testing, serotyping or serogrouping and molecular diagnostics.
- **Sequencing Metadata:** nucleic-acid preparation, sequencing purpose, sequencing laboratory, sequencing approach, library preparation, instruments, primary read files and sequencing quality metrics.
- **Bioinformatics and QC Metadata:** assembly and consensus methods, quality-control metrics, molecular typing, antimicrobial-resistance determinants, virulence determinants, reference genomes and repository accessions.

Each backbone workbook records the stakeholder-facing variable, canonical field name, requirement level, expected data type, applicability, controlled vocabulary, ontology identifier where available, definition, guidance, examples, annotation source and mapping status.

### Supporting documentation

The [`docs/`](docs/) directory contains the stakeholder workshop report documenting the community-development process, technical discussions and decisions that informed Version 1.

### Supporting documentation

The [`docs/`](docs/) directory contains supporting documents describing the community\-development process and the evolution of the standard:

- **Meningitis\_Technical\_Report\_v0.1.pdf** documents the inaugural meningitis metadata stakeholder workshop and the initial rationale, scope, public\-health use cases, tiered metadata model and early field\-level decisions that informed development of the standard.
- **Meningitis\_Workshop\_Report.pdf** documents the subsequent multi\-day standards workshop in which the metadata dictionary, field tiering, controlled vocabularies, diagnostic variables, sequencing metadata and organism\-specific bioinformatics content were further developed and refined.

These documents provide the development history and rationale for the standard. The current Version 1 metadata backbone and data\-collection template remain the authoritative resources for implementation.


### Software and automated template generation

The initial public release focuses on the validated metadata standard, Excel collection template, annotated metadata backbone and supporting documentation. Template-generation software and the planned local browser-based data-capture toolkit are maintained separately while their validation and packaging are completed.

## Data model

The Excel template uses linked domain worksheets rather than one large flat table.

| Worksheet | Unit of observation | Main linking identifier |
|---|---|---|
| `Case_Patient_Data` | One row per patient or case record | `host_subject_ID` / `case_ID` |
| `Specimen_Data` | One row per specimen | `specimen_collector_sample_ID` |
| `Diagnostics_Data` | One row per specimen diagnostic summary | `specimen_collector_sample_ID` |
| `AST_Results` | One row per organism–antimicrobial test | `specimen_collector_sample_ID` |
| `Sequencing_Data` | One row per sequencing run | `specimen_collector_sample_ID` / `sequencing_run_ID` |
| `Bioinformatics_Data` | One row per analysis record | `sequencing_run_ID` |

The same identifiers should be used consistently across worksheets so that patient, specimen, diagnostic, sequence and analysis records remain linkable.

## Getting started

### 1. Download the template

Download [`Meningitis_Metadata_Template_v1_1.xlsx`](template/Meningitis_Metadata_Template_v1_1.xlsx) and open it in Microsoft Excel.

### 2. Review the workbook README

The `README` worksheet explains the workbook structure, linking identifiers, colour coding, date formats and implementation scope.

### 3. Review field definitions

Use the `Data_Dictionary` worksheet and the domain backbone files to review:

- canonical field name;
- stakeholder-facing label;
- requirement level;
- value type;
- definition;
- completion guidance;
- example value; and
- ontology identifier, where available.

### 4. Enter linked records

Start with `Case_Patient_Data`, then add linked records in `Specimen_Data`, `Diagnostics_Data`, `AST_Results`, `Sequencing_Data` and `Bioinformatics_Data` as applicable.

Use the same identifiers across related worksheets. For example:

```text
host_subject_ID: PATIENT-0001
specimen_collector_sample_ID: CSF-0001
sequencing_run_ID: RUN-0001
```

### 5. Use controlled vocabularies

Where a dropdown is provided, select the most appropriate permitted value. Avoid alternative spellings or abbreviations when an approved value is available.

For fields accepting multiple values, enter approved values separated by semicolons unless the implementation platform provides true multi-selection.

### 6. Protect sensitive information

Apply relevant national, institutional and programme requirements for consent, privacy, access control and data sharing. Use de-identified patient and case identifiers wherever possible. Direct personal identifiers should only be recorded where explicitly required, appropriately governed and securely protected.

### 7. Review before sharing

Before sharing or submitting data:

- confirm that all required applicable fields are complete;
- verify that identifiers link correctly across worksheets;
- check dates and measurement units;
- review organism-specific diagnostic and genomic values; and
- remove information that is not authorised for onward sharing.

## Field requirement levels

| Requirement | Colour | Meaning |
|---|---|---|
| **Required** | Yellow | Must be completed where the field applies. Core to reliable reporting, linkage or interpretation. |
| **Recommended** | Purple | Should be completed when available. Adds substantial epidemiological, laboratory or analytical value. |
| **Optional** | White | May be completed to provide additional context. |

Some fields are conditionally applicable. For example, vaccine name is relevant when a patient is vaccinated, culture organism is relevant when culture is positive, and an R2 FASTQ file applies to paired-end sequencing.

## Controlled vocabularies and picklists

The workbook contains consolidated controlled vocabularies for fields including:

- sex and age groups;
- vaccination status and vaccine name;
- clinical signs and symptoms;
- specimen material and collection device;
- organisms and diagnostic results;
- AST methods, standards and interpretations;
- organism–antimicrobial combinations;
- serotypes and serogroups;
- PCR gene targets;
- sequencing platforms and library-preparation kits;
- in-silico typing results;
- AMR determinants; and
- virulence determinants.

Organism-specific supporting vocabularies have been developed for AST bug–drug combinations, serotyping/serogrouping, PCR targets, AMR determinants, virulence determinants and in-silico typing.

## Current implementation notes

The current stable Excel workbook is **template v1.1**. It supports review, pilot implementation and testing of the metadata structure, data model and controlled vocabularies.

Current implementation features and limitations include:

- dropdowns for many controlled fields;
- colour-coded Required, Recommended and Optional fields;
- semicolon-separated entry for multi-valued fields;
- organism-specific vocabulary reference lists for diagnostic and genomic fields; and
- dependent organism-specific dropdowns and advanced conditional validation are not yet fully implemented in v1.1.

A locally deployable browser-based toolkit is planned to provide stronger conditional logic, organism-dependent picklists, multi-select controls, validation and structured export.

## Versioning and roadmap

### Version 1

Version 1 establishes the bacterial and fungal meningitis metadata backbone and Excel implementation across five domains:

1. Case / Patient Information
2. Specimen Metadata
3. Diagnostic Methods
4. Sequencing Metadata
5. Bioinformatics and QC Metadata

### Version 2

Version 2 is planned to:

- add viral meningitis pathogens, diagnostics and genomic variables;
- strengthen conditional and organism-dependent validation;
- extend machine-readable implementation formats;
- support local browser-based data capture and validation; and
- align and integrate with the **GMCP/GMGP meningitis metadata standard** toward a single harmonised standard for the global meningitis community.

The Version 2 alignment process will seek to preserve a practical minimum dataset, country ownership and local adaptability while reducing duplication across existing meningitis metadata initiatives.

### Future implementation formats

The standard is designed to support additional implementation formats, including:

- enhanced Excel templates;
- REDCap data dictionaries and forms;
- DataHarmonizer templates;
- JSON Schema and other machine-readable specifications; and
- a locally deployable browser-based data-capture and validation toolkit.

## Contributing and feedback

Contributions are welcomed from laboratories, surveillance programmes, clinicians, researchers, public health agencies, bioinformaticians, data managers and ontology developers.

Contributions may include:

- proposing new metadata fields;
- improving field definitions or guidance;
- recommending controlled-vocabulary additions;
- identifying missing or incorrect ontology mappings;
- reviewing organism-specific AST, typing, AMR and virulence vocabularies;
- reporting inconsistencies in the template or documentation; and
- contributing to Version 2 viral and international harmonisation work.

To contribute, open an issue or pull request in this repository and describe the proposed change, affected field or vocabulary, rationale, supporting reference and expected implementation impact.

## Citation

If you use the PHA4GE Meningitis Metadata Standard in surveillance, research, software, data harmonisation or other applications, please cite:

> Public Health Alliance for Genomic Epidemiology (PHA4GE). *PHA4GE Meningitis Metadata Standard*. Version 1.0, 2026.

When reporting data generated or harmonised using the Excel implementation, please also specify the template version used, for example:

> Meningitis Metadata Template v1.1.

The accompanying peer-reviewed manuscript describing the development, stakeholder validation, ontology harmonisation and implementation of the standard is in preparation. Repository citation information will be updated following publication.

## Licence

The PHA4GE Meningitis Metadata Standard is provided under the terms specified in the repository [`LICENSE`](LICENSE) file. Users are encouraged to reuse and adapt the standard in accordance with those terms while retaining appropriate attribution and documenting substantive modifications.

## Acknowledgements and contact

The PHA4GE Meningitis Metadata Standard was developed through the **Public Health Alliance for Genomic Epidemiology (PHA4GE) Data Standards Initiative**, with contributions from stakeholders representing microbiology, laboratory medicine, meningitis surveillance, genomic epidemiology, public health, bioinformatics, data management and related disciplines across multiple African countries and institutions.

The standard reflects a community-driven process of stakeholder consultation, technical review, ontology harmonisation, controlled-vocabulary development and iterative validation.

Continued community participation is encouraged to support adoption, identify implementation needs, improve interoperability and guide future versions of the standard.

Questions, implementation feedback, proposed additions and requests for changes can be submitted through the repository **Issues** page.
