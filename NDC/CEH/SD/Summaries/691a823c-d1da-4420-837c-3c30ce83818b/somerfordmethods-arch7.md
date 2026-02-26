# Somerfordmethods.docx

## Overview
- Documents the results of a grazing experiment in a restored floodplain meadow (Somerford Mead) on the River Thames, upstream of Oxford.
- Timeframe: data collected 1987-2013; final survey in 2014 by UKCEH.
- Experimental design: three grazing treatments (Cattle, Sheep, No grazing) with three replicates each, totaling 9 plots; each plot sampled with 10 fixed 1 m x 1 m quadrats (90 quadrats total). Plots are permanently marked with metal pegs.

## Spatial design and location
- Plot locations and coordinates provided as National Grid Reference (NGR) values in Table 1.
- Figure 1 shows the position of recording quadrats within a 10 m x 10 m stand.
- Data are structured for GIS use with fixed spatial units (plots and quadrats) enabling time-series spatial analysis.

## Data collection methods and formats
- Each quadrat records all plant species and an abundance estimate.
- 1987-1989 (baseline): abundance based on number of 16 cells within each quadrat where the species occurred (scale 1-16).
- 1991-2013 (response data): same 16-cell subdivision and scale (1-16).
- 2014 (final survey): abundance based on percentage ground-area cover for each species (scale 1-100); final column records total species per quadrat.
- Field data were collected by Dr. Alison McDonald or trained student helpers; field sheets are held by Floodplain Meadows Partnership.

## Data structure and representation
- Each file presents a table: columns = species names; rows = quadrats (first column names the quadrat).
- Cells contain abundance values for the named species in the named quadrat; blanks indicate absence.
- Final column = total number of species identified in each quadrat.
- Three data variants reflect different time periods and measurement scales:
  - 1987-1989: baseline, 1-16 scale.
  - 1991-2013: response to treatments, 1-16 scale.
  - 2014: final survey, 1-100 percentage cover.

## Experimental design details
- Each plot center is marked with a buried steel scaffolding pole; plotted locations include precise NGR coordinates.
- Quadrats within each plot are arranged according to a fixed schema (Figure 2 shows the 16-cell subdivision of a 1 m x 1 m quadrat).
- Data collection recorded on paper field proformas; digital database stores presence/abundance per quadrat per species.
- Notes indicate standardization and documentation of recording practices, including the fixed recording order of stands (1, 2, 3, …).

## Quality control and data corrections
- Taxonomic standardization completed in 2022 to align with Stace’s New Flora of the British Isles (4th ed., 2019); synonyms updated.
- Field data checked for arithmetic errors; cross-checks performed by Dr. M.J. Stone; annual QA by Dr A. McDonald (1987-2013) or J.O. Mountford (2014).
- Documented corrections for numerous discrepancies (e.g., 1994, 1999, 2000, 201) including:
  - Resolution of mismatches between field sheets and summaries.
  - Reassignment and clarification of pseudospecies and bryophyte entries.
  - Reconciliation of genus-level identifications with species-level data where possible.
  - Handling of non-numeric entries (e.g., +, tick marks) by converting to presence indicators (e.g., "p").
- Some years (1987-1989) lack field data sheets; data sourced from other records and later reconciled.

## Corrections, assumptions and notes
- 1997-2013 data use a 1-16 abundance scale; 2014 data use a 1-100 percentage cover scale.
- Several taxonomic name changes and clarifications (e.g., Lotus uliginosus to L. pedunculatus; Leontodon sp.; Elytrigia/Deschampsia references).
- Some species identifications remain at genus level, or are pseudospecies (noted and retained in the database with appropriate qualifiers).
- Several entries contain non-numeric indicators; these have been standardized in the database to reflect presence or approximate abundance.

## Data provenance and access
- Raw field sheets and original proformas are held by the Floodplain Meadows Partnership.
- Methodology and data quality described in McDonald (2001); taxonomic references updated to Stace (2019).

## Relevance for GIS and data products
- Provides a time-series, spatially explicit dataset suitable for map-based analyses of species distributions under different grazing treatments.
- Requires taxonomic harmonization for integration with other datasets; offers per-quadrat abundance data that can be aggregated to plots or mapped at the quadrat level.
- Ideal for visualization of spatial patterns, species turnover, and treatment effects across multiple years, with a clear spatial framework (plots, quadrats, fixed coordinates).