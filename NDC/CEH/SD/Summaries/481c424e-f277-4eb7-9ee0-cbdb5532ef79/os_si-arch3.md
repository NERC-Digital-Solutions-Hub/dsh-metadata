# Oxidative stress markers in banded mongooses at Queen Elizabeth National Park, Uganda, 2017-2021

## Overview and purpose
- Dataset measures oxidative state in banded mongooses to explore relationships with maternal nutrition condition and reproduction.
- Data include multiple oxidative stress markers across different biological matrices.

## Data and variables
- Markers and matrices:
  - Red blood cell glutathione (GSH)
  - Plasma malondialdehyde (MDA_plasma)
  - Plasma protein carbonyls (PC)
  - Red blood cell total superoxide dismutase activity (SOD)
  - Milk malondialdehyde (MDA_milk)
- Datasets and key fields:
  - MDA_milk.csv, MDA_plasma.csv, PC.csv, SOD.csv, GSH.csv
  - Each dataset includes individual identifiers, demographic/group information (e.g., sex, pack), sampling dates, and marker-specific measurements
  - Quality control fields and processing details (e.g., date processed, duplicates, flags for sample quality)
- Metadata structure:
  - Detailed, dataset-specific fields (e.g., sample IDs, concentrations, repeat measurements, processing dates) to support traceability and quality assessment

## Study location and period
- Location: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E)
- Timeframe: 2017–2021

## Data collection methods
- Field sampling:
  - Individuals trapped every 3–6 months using box traps
  - Anesthetized with isoflurane prior to blood collection
  - Blood collected from jugular vein (100–500 μl)
  - Plasma separated and frozen; RBCs stored for later analysis
  - Samples snap-frozen in liquid nitrogen within 10 minutes of collection; transported to UK lab and stored at -80°C
  - Analyses conducted within one year of collection
- Laboratory analyses (overview):
  - MDA: measured in plasma/milk via HPLC with fluorescence detection after TBARs reaction
  - PC: quantified via DNPH reaction; absorbance at 370 nm; results normalized to protein
  - SOD: based on dismutation of superoxide radicals; measured with plate reader
  - GSH: measured using DTNB (Ellman) assay on deproteinized RBC extracts
  - Protein concentration determined (Bradford assay) for normalization
- Data handling for QC:
  - Duplicates included for quality control; repeats and processing dates recorded
  - Some samples flagged for hemolysis (bloody) or turbidity (cloudy)
  - Number of thaws tracked for sample integrity

## Data quality, standardization, and QC
- Duplicate measurements used for within-plate QC; repeats performed if discrepancies exceeded thresholds
- Assays followed kit instructions with pathogen/biochemical assay controls
- Standardization:
  - MDA quantified against external calibration (TEP-derived standards)
  - PC results normalized to protein content
- Storage and handling:
  - Consistent cold-chain management (snap-freezing, -80°C storage, timely transport)
- Documentation aims to ensure traceability and reproducibility across analyses

## Data completeness and limitations
- Sample sizes per marker vary:
  - Some individuals yield incomplete data due to insufficient blood volume or capture challenges
  - Not all markers are available for every individual or time point
- Data gaps may affect longitudinal comparisons and comprehensive coverage across the study period

## Data governance and accessibility considerations
- Project leadership: Principal Investigator Jonathan D. Blount (University of Exeter); Co-investigator Michael A. Cant; postdoctoral researchers collected and analyzed data
- The documentation provides comprehensive methodological detail and metadata, enhancing reproducibility
- Data sharing specifics are not explicitly stated; potential considerations for policy-oriented monitoring include metadata richness and transparency, balanced against data sharing constraints

## Relevance for environmental health monitoring frameworks
- Demonstrates a structured approach to wildlife oxidative stress monitoring as an indicator of environmental health and maternal/reproductive condition
- Highlights the importance of:
  - Clear metadata, standardized lab protocols, and QC procedures
  - Managing data quality, provenance, and processing timelines
  - Acknowledging data gaps due to field/logistical constraints and planning for more complete coverage in monitoring programs
- Provides a potential model for integrating multi-matrix biochemical markers into policy-relevant environmental health assessments, while noting practical data limitations that need addressing in monitoring frameworks