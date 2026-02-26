# Enteric virus concentrations and chemical properties of wastewater, water, sediment   and   shellfish   samples   collected   along   the Conwy   River   and estuary, North Wales.

## Overview
- Dataset reporting enteric virus concentrations and basic water chemistry (pH, turbidity, conductivity) across wastewater, surface water, sediment, and shellfish along the Conwy River and estuary, North Wales.
- Timeframe: four-weekly sampling from 17 May 2016 to 1 August 2017.
- Analytes include multiple human enteric viruses and algae-related controls: Norovirus GI and GII, Sapovirus GI, Hepatitis A (HAV) and E (HEV), Sapovirus GI, NoV GI/GII, Mengovirus (MgV) as process control, Adenovirus (AdV), JC and BK Polyomaviruses (JCV, BKV), among others.
- Data are complemented by quality control, calibration details, and methods for viral concentration, extraction, and quantitative PCR assays.
- Purpose aligned with data stewardship needs: structured data, traceable methods, and metadata to enable discovery, reuse, and governance.

## Sampling regime and sample collection details
- Sample types and volumes: surface water (10 L), sediment (10 g), mussel tissue (20 individuals); wastewater influent and effluent provided by Welsh Water.
- Sampling locations coded and described (Table 1), with coordinates for each site (e.g., Ganol, Betws-y-Coed, Llarwst, Tal-y-Bont wastewater plants; multiple surface-water sites SW1–SW4; shellfish beds and sediments).
- Sample handling: collected at low tide where appropriate; stored at 4°C for up to 24 hours before processing.
- Handling of wastewater samples: taken by Welsh Water; processed after receipt.
- Timing: four-weekly sampling window across roughly 2016–2017.

## Data capture, processing, and laboratory methods
- Instrumentation for measurements:
  - pH: S2K922 Waterproof pocket meter
  - Turbidity: T-100 handheld turbidity meter
  - Conductivity: 4520 Conductivity meter
  - Water concentration: KrosFlo Tangential Flow Filtration system
- Nucleic acid work:
  - Extraction: NucliSENS MiniMag system; Safe Aspiration station; Thermomixer
  - Quantification: Flex 6 Quant Studio Real-time PCR system
- Virus concentration and processing:
  - Water and wastewater: two-step concentration using tangential flow filtration; elution and precipitation steps to obtain viral concentrates
  - Sediment: elution using beef extract method; PEG precipitation; final resuspension in PBS
  - Mussels: ISO/TS 15216-1:2013 method; tissue digestion, centrifugation, extraction of viral concentrates
  - Nucleic acid extraction: 0.5 mL of concentrates; final RNA/DNA solution volume 0.1 mL
- qRT-PCR and qPCR assays:
  - Norovirus GI/GII, Sapovirus GI, HAV, HEV, Sapovirus GI, Mengovirus quantification via triplex or singleplex qRT-PCR assays
  - Adenovirus and Polyomaviruses (JC, BK) quantified via TaqMan or SYBR Green qPCR
  - Primer and probe sequences provided (Table 2); some dyes modified for multiplexing
- Capsid integrity assay:
  - Norovirus capsid integrity assessed with porcine gastric mucin-conjugated magnetic beads (PGM-MBs) on selected water and sediment positives
- Quality control and calibration:
  - pH calibration with manufacturer-provided pH 7 solution; turbidity calibration with standard NTU solutions
  - Real-time PCR runs include duplicates, non-template controls, and plasmid-based standards
  - External controls and process controls (MgV) used to monitor recovery and extraction efficiency

## Data structure and units
- Data are stored in a single CSV file; metadata fields described in Table 3 (Table 3 columns listed below).
- Key columns and their meanings:
  - Sample_code (sample identifier), Description
  - Date, Time_GTM
  - Volume or weight processed
  - pH (unitless)
  - Turbidity (NTU)
  - Conductivity (mS)
  - Viral targets (gc/UnitVol or gc/g for water, sediment, and mussel): NoVGI, NoVGII, HaV, HEV, SaV, AdV, JCV, BKV, MgV
  - NoVGI_PGM, NoVGII_PGM (capsid integrity proxies)
  - Additional notes: detection vs. quantification status; missing values indicated
- Units and interpretation:
  - Viral data expressed as genome copies (gc) per liter for water or per gram for sediment/mussel
  - Detection limit examples: 100 gc/L water; 10 gc/g sediment; 200 gc/g mussel
  - Quantification limit examples: ~200 gc/L water; ~100 gc/g sediment; ~500 gc/g shellfish
  - “Negative” indicates below detection limit; “Detected” indicates above quantification limit
- Metadata completeness:
  - Includes sampling site coordinates, sample type, and processing details
  - Some fields may be empty due to missing values (as noted in the dataset description)
  - BKV targeted only in wastewater samples from March 2016; not pursued subsequently

## Quality control, validation, and data integrity
- Recovery and method validation:
  - Sediment: about 80–100% recovery in spiking experiments, indicating suitability for sediment virus extraction
  - Surface waters: 10–100% recovery in spiking experiments, suitable for surface water virus extraction
  - Process control (MgV) recovery >10% across all sample types, indicating acceptable concentration and extraction efficiency
- Replicates and controls:
  - All qPCR runs performed in duplicates
  - Inclusion of non-template controls and standard dilution series in each run
- Capsid integrity assay and data interpretation:
  - CAPSID integrity assessed on водewater and sediment samples; mussel samples excluded due to proteinase K treatment affecting particles
- Documentation and references:
  - Primers/probes and assay references provided; calibration and assay conditions described to support reproducibility

## Data governance, access, and reuse
- Data structure and accompanying metadata enable discovery, interpretation, and reuse by data stewards and end users.
- The dataset includes precise sampling locations, sampling times, and complete methodological references, supporting provenance and reproducibility.
- Usage notes:
  - Data are described comprehensively with detection/quantification definitions and limits
  - Table 3 metadata fields facilitate integration with other environmental virology datasets
  - Recent publications citing or utilizing this dataset are listed as N/A in the document; users should cite the original source when reusing
- Limitations and caveats:
  - Some fields are empty; certain measurements (e.g., wastewater conductivity) were not measured due to low expected values
  - Data represent a specific geographic region and time frame; applicability to other settings requires careful contextualization

## Acknowledgements and references (high level)
- Acknowledges Welsh Water for providing wastewater samples and the field/processing team
- Provides references for primers, methods, and prior validation studies used to generate and interpret the dataset
- The dataset is a basis for environmental virology research and public health surveillance in wastewater and receiving waters