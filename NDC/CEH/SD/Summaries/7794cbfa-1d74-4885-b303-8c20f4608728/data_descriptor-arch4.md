# Photosynthetic pigments in water samples from 20 lochs in Scotland, May-June 2022

## Overview
- Dataset of photosynthetic pigment concentrations (µg L-1) in surface water from 20 Scottish lochs, collected May–June 2022.
- Purpose: develop a calibration model to derive pigment concentrations from hyperspectral images captured with a mobile imager.
- Data integrity: the first author (corresponding author) is responsible for correctness and reliability of the data.

## Data and file structure
- Main data file: pigment_results.csv.
- Columns include: sampling dates, sampled loch names, sample identification numbers, replicate subsamples, and sample volumes for each replicate used in HPLC and spectrophotometry.
- Sampling dates and sites are detailed in Table 1, with multiple lochs, sampling points, and coordinates (WGS84, captured with a mobile device).

## Sampling and sample handling
- Sampling method: grab sampling from the surface water layers of the listed lochs.
- Sample handling: stored at +4 °C and processed within 48 hours; water temperature recorded with a digital handheld thermometer.
- Field-data linkage: each sample has an identification number to match field observations.

## Laboratory analysis: chlorophyll and carotenoids
- Phytoplankton pigments measured by High-Performance Liquid Chromatography (HPLC) after acetone extraction; an internal standard (vitamin E) used.
- Sample processing: filters stored on ice, flash-frozen in liquid nitrogen, then stored at -80 °C; shipped on dry ice to the analysis lab (DHI, Denmark) and analyzed within 4–6 months of collection.
- HPLC setup: Shimadzu LC-10A HPLC with LC Solution software; pigment list includes chlorophylls (a, b, c1, c2, pheophytins), carotenoids and xanthophylls (e.g., neoxanthin, violaxanthin, lutein, fucoxanthin, β-carotene, α-carotene, etc.), and related pigments.

## Laboratory analysis: phycocyanin
- Phycocyanin analyzed from filters stored at -20 °C prior to shipping on dry ice; analysis performed within 3–6 months.
- Extraction: samples ground in extraction buffer (prepared from specific NaH2PO4 and Na2HPO4 stock solutions, pH 6.7–6.8), total extraction volume 9–18 mL; samples frozen and thawed, then sonicated on ice.
- Clarification: centrifuged at 3500 g; supernatant filtered (0.2 µm) and injected into a cuvette for spectrophotometric measurement.
- Measurement: absorbance at 615 nm, 652 nm, and 750 nm (against buffer) using a Shimadzu UV-1800 spectrophotometer.
- Calculation: phycocyanin concentration Ce = [(A615 − A750) − 0.474 × (A652 − A750)] / 5.32, following Bennett and Bogorad (1973).

## Data provenance and quality considerations
- Data collection spans multiple dates and sites, with explicit field-logged coordinates (iPhone-recorded, WGS84).
- Clear traceability: sampling dates, loch names, site descriptions, and sample IDs linked to laboratory analyses.
- Chain of custody: samples shipped on dry ice; strict storage conditions (-80 °C) and re-analysis windows documented.
- Metadata supports reproducibility and re-use, particularly for integrating pigment results with hyperspectral calibration efforts.

## Usage notes and limitations
- Applicable for cross-site pigment concentration comparisons and calibration workflows with hyperspectral imaging data.
- The document specifies a robust laboratory workflow and data linkage, but users should verify the specific pigment list and ensure consistent units and lab methods if integrating with external datasets.
- Data ownership and responsibility are attributed to the corresponding author; users should consider this in data governance and attribution.

## Relevance for data leaders
- Demonstrates end-to-end data lifecycle: field sampling, metadata capture, sample preservation, laboratory analyses with detailed protocols, and data storage in a defined CSV structure.
- Highlights the importance of metadata richness (dates, sites, coordinates, replicates, volumes) to enable reproducibility, data discovery, and cross-functional use (e.g., linking pigment data to hyperspectral calibration models).
- Illustrates practical considerations for data quality, provenance, and access (clear documentation of procedures, storage, and transport).