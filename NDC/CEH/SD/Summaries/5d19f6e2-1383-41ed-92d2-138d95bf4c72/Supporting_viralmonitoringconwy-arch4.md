# Enteric virus concentrations and chemical properties of wastewater, water, sediment and shellfish samples collected along the Conwy River and estuary, North Wales.

## Overview
- Study theme: quantification of enteric viruses and chemical properties across wastewater, surface water, sediment, and shellfish along the Conwy river and estuary, North Wales.
- Timeframe: sampling from 17 May 2016 to 1 August 2017 (four-weekly intervals).
- Sample types: wastewater influent/effluent, surface water, sediment, and 20 mussels per site.
- Collaborators: Welsh Water provided wastewater samples; authors conducted laboratory analyses.
- Data aim: generate integrated data on viral concentrations and physico-chemical properties to support environmental surveillance and risk assessment.

## Sampling regime and collection methods
- Sampling cadence: four-weekly, covering multiple sites along the river, estuary, and shellfish beds.
- Sample collection protocols:
  - Surface water: 10 L collected in disinfected carboys.
  - Sediment: top 1–2 cm sampled in sterile tubes during low tide.
  - Mussels: 20 individuals handpicked during low tide.
  - Wastewater: influent and effluent collected by Welsh Water (provided next day).
- Storage: all samples stored at 4°C for up to 24 hours before processing.
- Documentation: sampling points and sample codes described (e.g., GI/GE for Ganol WWTP influent/effluent; SW1–SW4 for surface waters; Sed/SF for shells/sediment).

## Nature and units of recorded values
- Physicochemical data:
  - pH (unitless)
  - Turbidity (NTU)
  - Conductivity (mS)
- Viral data:
  - Genome copies (gc) per litre for water or per gram for sediment/mussel
  - Negative indicates below detection limit; detected indicates below quantification limit
- Detection/quantification limits:
  - Water: ~100 gc/L
  - Sediment: ~10 gc/g
  - Mussel: ~200 gc/g
- Units and terminology defined for all measurements and data interpretation.

## Concentration, elution, and storage of viral samples
- Water and wastewater concentration: two-step method using KrosFlo tangential flow filtration to reduce volume to ~50 mL, followed by elution with beef extract and precipitation with PEG 6000/NaCl; final concentrates stored at 4°C up to 24 h, then at -80°C.
- Sediment virus elution: similar beef extract/NaNO3 approach with PEG precipitation; storage as above.
- Mussel virus extraction: ISO/TS 15216-1:2013 method; 2 g tissue from 20 mussels, spiked with MgV as control; proteinase K digestion and centrifugation; concentrates stored as above.

## Viral nucleic acid extraction and quantification
- Extraction: viral nucleic acids extracted from 0.5 mL concentrate; final nucleic acid volume 0.1 mL.
- qRT-PCR/qPCR targets:
  - Norovirus GI and GII (NoV GI, NoV GII)
  - Sapovirus GI (SaVGI)
  - Hepatitis A (HAV) and Hepatitis E (HEV)
  - Sapovirus variants (as applicable in triplex assays)
  - Mengovirus (MgV) as process control
  - Human Adenovirus (AdV) DNA
  - JC polyomavirus (JCV) and BK polyomavirus (BKV)
- Assay formats:
  - Triplex and singleplex qRT-PCR assays with one-step or SYBR Green approaches as described
  - Primers and probes listed with literature references
- Reaction details: typical 20 µL reactions, specific primer/probe concentrations, annealing temperatures (56°C or 60°C), and cycling parameters outlined
- Data handling: quantification based on standard curves; results expressed as genome copies per litre (water) or per gram (sediment/mussel).

## Norovirus capsid integrity assay
- Purpose: assess capsid integrity of NoV using porcine gastric mucin-conjugated magnetic beads (PGM-MBs).
- Procedure: positive NoV samples diluted, incubated with PGM-MGs, separated magnetically, heated, and RNA quantified by qRT-PCR.
- Exclusion: mussel samples excluded due to prior processing steps (proteinase K) affecting particles.

## Quality control
- Validation: sediment and water samples validated via spiking experiments with known virus types to assess recovery.
- Reported recoveries:
  - Sediment: 80–100% recovery indicating suitability
  - Water/estuarine samples: 10–100% recoveries indicating suitability for surface water
- Process control: MgV spike used; recovery >10% in all cases, indicating adequate concentration and extraction efficiency.
- General QA: duplicates per run, non-template controls, and plasmid-based dilution series used for quantification and reliability.

## Data structure and metadata
- Data format: dataset provided in a single CSV file.
- Metadata fields (as described in Table 3):
  - Sample_code, Date, Time_GTM, Volume, pH, Turbidity NTU, Conductivity mS
  - Virus targets: NoVGI, NoVGII, HaV, HEV, SaV, AdV, JCV, BKV (with corresponding concentrations and, where applicable, PGM-associated values)
- Data completeness:
  - Some fields may be missing (empty fields represent missing values)
  - Wastewater conductivity not measured (close to 0 mS)
  - BKV targeted only in wastewater samples collected in March 2016
- Documentation references:
  - Tables 1–2 for sampling sites and primers/probes
  - Table 3 for metadata column definitions

## Data reuse potential and context for data leaders
- Integrated data pipeline: from field sampling through lab analytics to a structured dataset, illustrating end-to-end data management for environmental virology.
- Use cases:
  - Environmental surveillance and risk assessment for water quality
  - Longitudinal and spatial analysis of enteric viruses across wastewater, surface water, sediments, and shellfish
  - Cross-study comparison leveraging standardized assays and QA/QC protocols
- Data governance considerations demonstrated:
  - Clear documentation of sampling schemes, laboratory methods, and data representation
  - Emphasis on QA/QC, calibration, detection/quantification limits, and data structure for discoverability and reuse

## Challenges and considerations for data leadership
- Data fragmentation and complexity: multiple sample types, sites, and matrices requiring harmonized metadata and consistent naming (e.g., sample codes).
- Data availability and gaps: partial targeting (e.g., BKV limited to March 2016) and incomplete measurements (e.g., wastewater conductivity not recorded).
- Metadata richness vs. accessibility: reliance on tables for methodological details; need for machine-readable, central metadata catalog to improve discoverability and interoperability.
- Standardization and reproducibility: use of established protocols (e.g., ISO/TS 15216-1:2013) and cited primers/probes; important for cross-study comparability and data integration across networks.