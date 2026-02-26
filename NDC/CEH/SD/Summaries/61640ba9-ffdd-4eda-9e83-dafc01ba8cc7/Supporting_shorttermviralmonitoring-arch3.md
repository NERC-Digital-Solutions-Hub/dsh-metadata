# Enteric virus concentrations, pH and turbidity in wastewater discharged to the Conwy River and estuary, North Wales (2016-2017)

## Overview
- Investigates concentrations of enteric viruses, along with pH and turbidity, in wastewater discharged to the Conwy River and estuary during 2016–2017.
- Sampling conducted at three wastewater treatment plants (Betws-y-Coed, Llanrwst, Ganol) with distinct sample types and collection points to represent influent and effluent conditions.
- Aims to support environmental health monitoring by providing a structured dataset for assessing viral contamination and associated water quality parameters.

## Sampling regime and collection methods
- Sampling sites and regime:
  - Betws-y-Coed and Llanrwst: wastewater effluent collected entering the river.
  - Ganol: untreated influent wastewater collected at the WWTP.
- Instrumentation: ISCO automatic water samplers used.
- Sampling schedule: every two hours for three days at each site, yielding 36 samples per site (daily collection).
- Sample handling: samples transported to the laboratory for analysis.

## Measurements and units
- Physicochemical parameters:
  - pH (unitless)
  - Turbidity (Nephelometric Turbidity Unit, NTU)
- Viral measurements: quantified as genome copies per liter (gc/L) for:
  - Norovirus GI (NoVGI) and GII (NoVGII)
  - Sapovirus GI (SaVGI)
  - Hepatitis A (HAV) and E (HEV)
  - Adenovirus (AdV)
  - Mengovirus (MgV) used as process control
- Detection and quantification:
  - Detection limit for viruses: 100 gc/L
  - Quantification limit: ~200 gc/L
  - Negative: below detection limit; Detected: below quantification limit
- Data structure: All viral data expressed per liter of concentrated wastewater; pH is unitless; turbidity in NTU.

## Laboratory instrumentation and processing
- Measurements and equipment:
  - pH: S2K922 Waterproof pocket-sized pH meter
  - Turbidity: T-100 Handheld Turbidity meter
  - Concentration: KrosFlo Tangential Flow Filtration System
  - Nucleic acid extraction: NucliSENS MiniMag System
  - Quantification: Flex 6 Real-time PCR system
- Assay details:
  - Viral RNA quantified by either singleplex or triplex qRT-PCR assays (NoVGI, NoVGII, SaVGI, HAV, HEV, MgV) with specific primer/probe sets and cycling conditions
  - Human Adenovirus DNA quantified by SYBR Green qPCR
- Calibration and quality checks:
  - pH and turbidity meters calibrated with manufacturer standards
  - qPCR/qRT-PCR runs include duplicates, no-template controls, and plasmid dilution series
  - Background noise calibration performed; dyes replaced for multiplexing
- Data processing controls:
  - Process control (mengovirus VMC0) spiked into autumn/winter samples
  - Recovery of process control >10% across tests, indicating reliable extraction and concentration

## Data structure and availability
- Data are stored in a single CSV spreadsheet.
- Metadata fields (Table 3 in the source) describe:
  - Sampling_event (site, season)
  - Sample_type (influent or effluent)
  - Date_Time_GMT
  - pH
  - Turbidity_NTU
  - NoVGI_gc/l, NoVGII_gc/l, SaV_gc/l, HAV_gc/l, HEV_gc/l, AdV_gc/l
- The dataset is designed to be used for subsequent analyses and has been referenced in recent publications (where applicable).

## Quality assurance and validation
- Spiking experiments with Mengovirus to assess process efficiency; recovery>10% confirms methodological reliability.
- Duplicates and appropriate controls used in qRT-PCR/qPCR assays to ensure accuracy and reproducibility.

## Relevance for monitoring frameworks
- Demonstrates an end-to-end monitoring workflow for environmental virology in wastewater contexts, including:
  - Site selection and sample collection regimes
  - Concentration and extraction methods suitable for low-abundance viral targets
  - Multiplex qRT-PCR/qPCR assays with robust QC
  - Clear data structures and metadata for traceability and reuse
- Provides a data-rich basis for environmental health assessments, policy evaluation, and decision-making regarding wastewater management and river/estuary water quality.

## Challenges and considerations for monitoring
- Detection and quantification limits constrain interpretation of low-level viral presence.
- Data management requires careful calibration, standardized protocols, and transparent metadata to ensure comparability across sites and time.
- Public sharing of underlying datasets may present barriers, highlighting the importance of data governance and clear documentation.

## Acknowledgements and references
- Acknowledges Welsh Water for assistance with sample collection and processing support.
- References include methodological sources for primers, probes, and qRT-PCR standards used in the viral assays.