# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Overview
- A BACI (before-after-control-impact) study across multiple streams with upstream reference zones and downstream experimental zones.
- Before period (T1): ~61-65 days with no manipulation; both zones treated identically.
- After period (T2): ~57-62 days with leaf litter addition in the experimental zone to simulate natural organic inputs.
- Leaf litter inputs: one tonne bags of oak, birch, alder distributed proportionally to experimental zones; maintained wet weight targets; additional litter (630 kg wet weight) added after two storm events (Feb 12 and Mar 5, 2013).
- Objective: assess how suspended organic matter (SOM) stocks respond to increased organic matter input in upland river systems.

## Experimental design
- Each stream divided into:
  - Upstream reference (control within frame)
  - Downstream experimental zone (receives litter additions)
- Independence between zones ensured by ~20–50 m separation.
- Replication: replicate codes A–F indicate multiple subsamples per site.
- Time framing:
  - T1 (Before): January sampling period included in before phase
  - T2 (After): February–April sampling period after manipulation
- Data collected across multiple streams to capture variability in land use, region, and catchment characteristics.

## Sampling and laboratory methods
- Suspended Organic Matter (SOM): particles >10 µm and <1 mm.
- Collection: 100 L water filtered through 10 µm and 1 mm filters at the lower end of each reach; three replicates per sampling.
- Preservation: samples refrigerated (~4°C) and freeze-dried for 4–72 hours; ground and subsampled for analysis.
- Analyses:
  - Elemental composition: carbon (C) and nitrogen (N)
  - Stable isotopes: delta-13C (d13C) and delta-15N (d15N)
  - Inorganic correction: subset samples combusted at 550°C for 5 h to correct for inorganic content (ash-free conversion).
- Sample processing: detailed lab workflow to obtain mass-based and isotopic data from SOM.

## Data collected and structure
- Primary data type: Coarse Particulate Organic Matter (CPOM) and Fine Particulate Organic Matter (FPOM) measurements.
- Units and metrics:
  - CPOM and FPOM per sample (grams), ash-free dry matter (AFDM), concentrations (mg/L), and related volume filtered.
  - Subsample weights for isotopic and elemental analyses (µg).
  - Isotopic values: cpom.fpom d13C and d15N (with notes/comments where applicable).
  - Discharge: liters per second (L/s)
  - Time indicators: Before/After, sampling month, exact date and time
- Data fields (sample of the 33 columns):
  - site_code, landuse, region, time, date, discharge, reach (Experimental/Control), replicate, cpom.g.per.sample, cpom.afdm.mg.l, cpom.ug.C.per.subsample, cpom.d13C, cpom.d15N, fpom.g.per.sample, fpom.afdm.mg.l, fpom.ug.N.per.subsample, fpom.d13C, fpom.d15N, etc.
- Data files:
  - Suspended organic matter data stored as flatbed CSV with 33 columns.
  - Supporting file: Site Description (site_code, coordinates, catchment, survey campaign, etc.).
  - Miscellaneous supporting documents include the site descriptions with precise metadata and location information.

## Data processing and quality control
- Processing steps:
  - Freeze-drying of SOM samples, grinding, and homogenization before subsampling for analyses.
  - Inorganic correction via combustion to establish ash-free conversion for accurate organic mass.
  - Subsample metadata recorded for traceability of isotopic and elemental analyses.
- Quality control notes:
  - Specific QC procedures are not exhaustively detailed in the provided text.
  - Data structure is explicitly defined to support traceability and reproducibility (e.g., replicate codes, date/time, discharge, region, land use).

## Supporting data and documentation
- Site Description data: a CSV with site_code, name, grid references, latitude/longitude, elevation, survey campaign, and catchment information.
- Additional metadata and documentation accompany the SOM data to support discoverability and reuse.

## Practical takeaways for data governance and usage (Data Leaders perspective)
- End-to-end data lifecycle demonstrated: experimental design (BACI), field sampling, laboratory analyses, data serialization (CSV), and accompanying metadata.
- Emphasizes clear data structure and metadata to ensure discoverability, reuse, and aggregation across studies.
- Highlights importance of:
  - Documenting units, variable naming, and data provenance (sample origin, replicate, time period).
  - Maintaining data in accessible formats (CSV) with comprehensive site-level metadata.
  - Recording environmental context (discharge, land use, region) to enable cross-site comparisons and synthesis.
  - Including site description and supporting documents to enhance data discoverability and interpretability.
- Potential data management considerations:
  - Standardization of column names and units for cross-study integration.
  - Clear versioning and updates to reflect any reprocessing (e.g., ash-free corrections).
  - Ensuring data gaps are documented (e.g., missing metadata fields or QC details) to support reliable downstream analysis.