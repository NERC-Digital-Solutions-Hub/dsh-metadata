# SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-death data collated from other sources

## Overview
- A dataset of SARS-CoV-2 qPCR and water chemistry measurements from wastewater at six sites in Wales and Northwest England, collected March–July 2020.
- Includes associated Covid-19 clinical data (positive tests and related deaths) collated from other sources.
- Aimed at enabling environmental health monitoring and policy evaluation through integrated wastewater and clinical indicators.

## Data access and licensing
- Data accessible via DOI: https://doi.org/10.5285/ce40e62a-21ae-45b9-ba5b-031639a504f7
- Open Government Licence (OGL) terms.
- Must cite the dataset: Hillary et al. (2021). SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-deaths data collated from other sources. NERC Environmental Information Data Centre. https://doi.org/10.5285/ce40e62a-21ae-45b9-ba5b-031639a504f7

## Data description and structure
- Two CSV files:
  - data_table.csv: main wastewater dataset with weekly samples
    - Key fields: Week, Date, Site_Name, Flow (m3 per population equivalent), gc_100ml (SARS-CoV-2 N1), E_gene_100ml, Crass_gc_100, Crass_Recovery, NO3, NH4, PO4, pH, EC, Deaths, Deaths_100k, Daily_Cases_100k, Population_Equivalent, Rolling_Sum_100k, Local_Authority_Population, cov_class, cov_detect, E_class
    - Units: SARS-CoV-2 genome copies per 100 mL; inorganic/physico-chemical measurements in mg/L or μS/cm as described; population- and rate-based metrics per local authority
  - cases.csv: clinical testing data for same period
    - Key fields: Site_Name, Date, Local_Authority_Population, Daily_Cases, Cumulative_Cases, Rolling_Sum, Daily_Cases_100k, Rolling_Sum_100k, Week
- Sampling sites and timeframe
  - Six WWTPs serving Gwynedd, Cardiff, Liverpool, Manchester, the Wirral, and Wrexham
  - Timeframe: March–July 2020; weekly influent samples; Wirral site also collected as a 24-hour composite
  - Population served: ~3 million
- Notable measurements
  - SARS-CoV-2 RNA quantified via N1 (CDC) and E-gene (Sarbeco) assays
  - CrAssphage used as a marker for human fecal load
  - Additional wastewater chemistry: NO3, NH4, PO4, pH, EC
  - Public health data: Covid-19 deaths and daily positive tests, plus rolling 7-day sums and population-adjusted metrics

## Sampling and laboratory methods
- Sampling
  - Untreated influent collected weekly; Wirral site used 24-hour composite (autosampler); others used grab samples collected on weekdays 08:00–09:00
  - Treated effluent sampled periodically
  - Samples transported on the same day or next day on ice; stored at 4 °C and processed within 24 h
  - Aliquots frozen at -80 °C for downstream analyses
- Physicochemical analyses
  - Ammonium: colorimetric (Mulvaney, 1996)
  - Nitrate: colorimetric (vanadate; Miranda et al., 2001)
  - Molybdate-reactive phosphate: (Murphy & Riley, 1962)
  - Electrical conductivity (EC) and pH measurements
- Concentration and nucleic acid extraction
  - Duplicate samples processed; separation into supernatant and pellet after centrifugation
  - Concentration methods:
    - Influent: Centriprep 50 kDa MWCO
    - Effluent: tangential flow ultrafiltration (100 kDa) + Centriprep concentration
  - Viral RNA extraction control: murine norovirus (MNV) spike-in (~4×10^5 gc)
  - Extraction and q(RT-)PCR performed in separate labs to minimize contamination
  - Nucleic acids stored at -80 °C prior to q(RT-)PCR
- qPCR/qRT-PCR assays
  - Instruments: QuantStudio Flex 6 Real-Time PCR System
  - Targets:
    - SARS-CoV-2: N1 and E gene (duplex or triplex with MNV as control)
    - CrAssphage (human fecal marker)
    - MNV (extraction control)
  - Reaction setup: detailed composition (including primers, probes, BSA, etc.)
  - Standards and controls:
    - Plasmid standards for SARS-CoV-2 targets
    - Custom oligonucleotide standards for MNV and CrAssphage
    - Negative controls with molecular-grade water
  - Replication: all samples run in duplicate; mean of extraction replicates used
  - LoD and LoQ:
    - SARS-CoV-2 N1 LoD: 1.7 gc/µL; LoQ: 11.8 gc/µL
    - SARS-CoV-2 E LoD: 3.8 gc/µL; LoQ: 25.1 gc/µL
    - MNV LoD/LoQ: 3.1 gc/µL and 32.1 gc/µL
- Assay details
  - Primer/probe sequences and q(RT-)PCR cycling parameters provided in the document for N1, E, MNV, and CrAssphage
  - Primer/probe sets and parameters referenced from CDC, Corman et al., and related methods

## Quality assurance and governance
- Quality controls
  - MNV recovery used to monitor extraction efficiency and inhibition
  - Inhibition retests performed only when MNV recovery <1%; chosen not to adjust sensitivity by altering reaction volume
  - Duplicate measurements and use of standards/controls in all runs
- Data integrity considerations
  - Separate laboratories for extraction and qPCR to reduce contamination risk
  - Detailed methodological description enabling reproducibility and cross-site comparability
- Data governance and openness
  - Data designed to support monitoring frameworks with transparent methods and open access licensing
  - Metadata and data-sharing considerations discussed as part of reporting

## Relevance for monitoring frameworks
- Provides a connected view of environmental surveillance (wastewater) and clinical indicators (positive tests, deaths)
- Enables normalization and interpretation of wastewater signals using CrAssphage as a fecal-load marker
- Includes site- and time-specific population metrics and flow data to contextualize measurements
- Documented QA/QC and assay limits support standardized interpretation and comparability across monitoring programs
- Licensing and citation requirements support reproducibility and policy-informed decision-making

## Limitations and considerations for users
- Limited to six wastewater treatment plants; spatial coverage is regional
- Sampling frequency is weekly (with Wirral as a 24-hour composite; others grab samples), which may affect temporal resolution
- Early-pandemic context; assay performance and population behaviors may limit generalizability to later waves
- Data interpretation requires consideration of LoD/LoQ and fecal loading normalization

## References and supporting materials
- CDC and Corman et al. assay references for targets and protocols
- Methodological prior work on CrAssphage as a human fecal marker and wastewater concentration/extraction techniques
- Supplementary materials containing extended assay details and standard curves