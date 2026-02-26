# Farm management and longitudinal data on antibiotic use and antibiotic resistant E. coli for 53 dairy farms in the South-West of England between 2017-2019.

- Overview
  - A cleaned, combined dataset on antibiotic use and antibiotic-resistant E. coli from 53 dairy farms in South-West England (2017–2019), part of the OH-STAR project.

- Data sources and scope
  - Merges data from:
    - Farm demographics and management questionnaires
    - On-farm sample collection (time of sampling and context)
    - Laboratory results for E. coli resistance (antibiotic screening and genetic analysis)
    - Prescription records from veterinary practices and farm records
  - Population and context
    - Convenience sample of 53 dairy farms; UK-comparable metrics ( herd size, milk yield, somatic cell count) provided for context
    - Antibiotic purchasing metrics reported as mg/PCU (EU surveillance standard)

- Sampling, collection, and laboratory methods
  - Sampling schedule and sites
    - Monthly visits Jan 2017–Dec 2018 across multiple environments: adult milking cows, dry cows, replacement heifers, pre-weaned calves, and relevant farm footpaths
    - Large number of samples from environmental and animal habitats
  - Laboratory workflow
    - Samples processed after refrigeration; cultured on TBX media with various antibiotic conditions
    - E. coli identified by blue colonies; up to five isolates per plate advanced to CTX-R screening on CTX-TBX
    - PCR used to detect β-lactamase genes ( blaCTX-M groups ); AmpC hyperexpression screened
  - Data provenance
    - Methodology aligns with Schubert et al. (2021)

- Data structure, variables, and metadata
  - dataset type
    - Cleaned, merged dataset with both sample-level and farm-level data
  - Key fields and coding
    - Sample identifiers, farm codes (3-letter), visit numbers, collection dates, location context
    - Resistance indicators (CTX-M presence, AmpC detection, and resistance to specific antibiotics: ciprofloxacin, tetracycline, cephalexin, etc.)
    - Quantitative measures (e.g., plain E. coli counts, mg/PCU antibiotic usage, various continuous/ordinal variables)
    - Farm-level management and environment variables (e.g., waste milk feeding, vaccination programs, calving practices, housing, grazing, water sources, manure management)
    - Derived variables and recoding
      - Multiple-choice responses condensed to simpler categories (e.g., cleaning frequency)
      - Binary and categorical encodings (e.g., 1/0 for presence of a feature; farm codes; ordinal scales)
  - Data dictionary characteristics
    - Extensive metadata describing each variable, units, and data type
    - Clear documentation of lab results vs. field-collected data
    - Some lab details noted as awaiting final lab details ( AmpC detection method pending)

- Data quality, cleaning, and governance
  - Data cleaning
    - Standardization across sources; consolidation of overlapping fields
    - Creation of derived variables to enable cross-source analyses
  - Data quality considerations
    - Some lab details noted as pending (AmpC details); overall, dataset designed for interoperability across farms and sampling periods
  - Provenance and replication
    - Dataset references a published methodology (Schubert et al., 2021), enabling traceability and reproducibility

- Access, usage, and references
  - Methodology and data context described in
    - Schubert H, Morley K, Puddy EF, et al. Reduced Antibacterial Drug Resistance and blaCTX-M βLactamase Gene Carriage in Cattle-Associated Escherichia coli at Low Temperatures, at Sites Dominated by Older Animals, and on Pastureland: Implications for Surveillance. Applied and Environmental Microbiology. 2021;87:e01468-20
  - This dataset is positioned for longitudinal analyses of antibiotic usage, resistance patterns, and farm-management factors influencing AMR

- Governance implications and reuse notes for Data Stewards
  - Provenance and lineage
    - Clear origins from farm surveys, sampling campaigns, and veterinary prescription records; linked to standardized antibiotic usage metrics (mg/PCU)
  - Metadata completeness and discoverability
    - Rich, field- and lab-level metadata; comprehensive variable descriptions and coding schemes (including farm codes and sampling context) facilitate discovery and reuse
  - Interoperability and standardization
    - Standardized units (mg/PCU), consistent coding for binary/ordinal fields, and a detailed data dictionary support cross-dataset integration
  - Data quality management
    - Ongoing considerations include finalizing AmpC lab details and maintaining versioned data records as new lab results or re-analyses become available
  - Potential for reuse
    - Suitable for AMR surveillance analyses, modelling relationships between antibiotic usage and resistance, and evaluating how farm-management practices relate to resistance outcomes
  - Compliance and ethics
    - While not detailed here, the data structure is designed to support responsible sharing with clear provenance; ensure appropriate governance for farm-level data and any privacy considerations in dissemination

- Summary takeaway
  - This is a well-documented, multi-source, longitudinal dataset on antibiotic use and E. coli resistance across 53 dairy farms, with rigorous laboratory methods, detailed metadata, and a strong foundation for stewardship-driven data sharing, governance, and reuse in antimicrobial resistance research.