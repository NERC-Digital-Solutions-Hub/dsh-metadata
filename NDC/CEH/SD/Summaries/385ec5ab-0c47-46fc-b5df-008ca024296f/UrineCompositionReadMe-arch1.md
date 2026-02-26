# UrineComposition.csv

## Overview
- Dataset of Welsh Mountain ewe urine chemical composition and related metadata.
- Collected from two sites with pasture types (semi-improved and improved).
- Aims to support analyses of nitrogen and metabolite fluxes in grazing ewes, potentially informing environmental or agricultural understanding of N cycling.

## Data content and structure
- Records include individual urine events per replicate sheep, across seasons (spring, summer, autumn).
- Key measurements include chemical constituents, physical properties, and metadata about collection.
- Data headers specify both sample metadata and chemical concentration measurements, enabling correlation and modeling across factors like season, site, and sheep.

## Variables and units
- Temporal and event metadata:
  - Season (spring, summer, autumn)
  - Site (semi-improved, improved pasture)
  - Sheep (replicate identifier)
  - Date (dd/mm/yyyy)
  - Time (hh:mm)
  - Vol (volume; ml)
- Chemical and physical measurements (selected):
  - TOC (urine dissolved organic carbon; g C l-1)
  - TN (urine total N; g N l-1)
  - pH (unitless)
  - EC (electrical conductivity; mS cm-1)
  - Urea (g urea-N l-1)
  - Nitrate (mg NO3--N l-1)
  - Ammonium (mg NH4+-N l-1)
  - AA (amino acids; mg amino acid-N l-1)
  - Allantoin (g compound l-1)
  - Creatinine (mg compound l-1)
  - Uric (mg compound l-1)
  - Hippuric (g compound l-1)
  - Benzoic (mg compound l-1)
  - Ca (mg Ca l-1)
  - Na (mg Na l-1)
  - K (g K l-1)

## Sampling design and metadata
- Sample processing:
  - Urine filtered on ice through Whatman No. 1 filter papers (11 μm) to remove large particulates.
  - Samples frozen at -20 °C prior to analysis.
- Analytical methods (highlights):
  - pH and EC measured with standard electrodes.
  - Total N and dissolved organic carbon measured with Multi N/C 2100S analyser.
  - Urea quantified via enzymatic method (Orsenneau et al., 1992).
  - NH4+ and NO3- measured colorimetrically (Mulvaney, 1996; Miranda et al., 2001).
  - Free amino acids detected fluorometrically (Jones et al., 2002).
  - Selected metabolites measured by HPLC (Allantoin, Creatinine, Uric, Hippuric, Benzoic) using a specified C18 column and detection setup.
  - Ion contents (K+, Na+, Ca2+) measured by flame photometry.
- Reference methods provided for replicability.

## Laboratory methods (instrumental detail)
- HPLC: Varian Pro Star 310 System with C18 column; detection at 218 nm; mobile phases A (KH2PO4, pH ~4) and B (60% A, 40% methanol).
- Specifics include sample dilution in mobile phase A as needed.
- Analytical sequence designed to quantify a broad suite of nitrogenous and organic compounds in urine.

## Data processing and quality
- Data entries include explicit units for all measurements.
- Authors and project identifiers provided; reuse requires full citation.
- Metadata supports stratification by season, site, and individual sheep for robust analyses.
- Data likely suitable for correlational and predictive modeling to relate urine composition to environmental and management factors.

## Potential analyses and questions for analysts
- Investigate how urine N forms (Urea, Nitrate, Ammonium, TN) vary by season and pasture site.
- Explore relationships between dissolved organic carbon (TOC), pH, EC and nitrogenous constituents.
- Model predicted emissions or environmental N flux indicators from urine composition.
- Assess intra- and inter-animal variation (within Sheep replicates) in metabolite profiles (AA, Allantoin, Creatinine, Uric, Hippuric, Benzoic).
- Examine correlations between inorganic ions (Ca, Na, K) and organic nitrogen metrics.
- Evaluate data quality across sites and seasons to identify potential biases or processing effects.

## Data accessibility and references
- Data and methods are described with explicit references for measurement techniques:
  - Amino acids: Jones et al. 2002
  - Nitrate/nitrite detection: Miranda et al. 2001
  - Inorganic nitrogen forms: Mulvaney 1996
  - Urea determination: Orsenneau et al. 1992
- Citation guidance included: ensure full citation if data are reused.