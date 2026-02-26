# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Guidance for mapping habitat types, landscape features, and attributes for Countryside Survey 2007 (CS2007) using digital GIS methods.
- Introduces CS Surveyor, an ArcGIS extension, for recording habitat extent, change, and Broad/Priority Habitats in 1 km squares.
- Emphasizes time-series data, standardized data capture, and reporting aligned with policy frameworks; prioritizes reproducibility and data reuse.

## Aims for Analysts Monitoring the Environment
- Use standardized data to demonstrate environmental condition and policy performance over time.
- Report land-cover and feature changes within a framework aligned to UK Biodiversity Action Plans (PHs and BHs).
- Increase value and reusability of datasets by storing data and enabling access to underlying data beyond final outputs.

## Data Model and Classification
- Broad Habitats (BH) form the primary classification; Priority Habitats (PH) are nested within BHs where applicable.
- Detailed attribute keys:
  - Vegetation: primary/secondary habitat attributes based on plant composition.
  - Woodland types/features: belts, clumps, woodland/forest, hedges, lines of trees, etc.
- BH categories cover a wide range of landscapes (e.g., BH1–BH18, with mosaic as needed). PHs are mapped when detectable or supported by historical GIS data.

## Data Collection and Digital Mapping System
- CS2007 enables digital data capture for all habitat attributes, consolidating themes into a single editable digital map per 1 km square.
- CS Surveyor (ArcMap extension) supports viewing/editing polygons (areas), lines (linear features), and points; enforces recording of genuine landscape changes.
- Data storage to appropriate data portals; supports updates, splits, merges, and attribute copies.
- Spatial accuracy prioritizes correct habitat extent and change representation; minimum mapping unit (MMU) is 0.25 ha (400 m2).

## Field Procedures and Workflow
- Square-level mapping aims to describe habitats and landscape features, map changes since the last survey, and produce a denser dataset than earlier CS iterations.
- Enclosed (lowland) vs unenclosed (upland) habitats have different attribute strategies; where possible, integrate 1990 CS data and CS1998 mappings.
- Reporting by BHs and PHs is integral for monitoring outputs and policy alignment.
- New Wales squares are added to enable country-wide reporting.

## Pond Mapping and Sampling
- All ponds in each square are identified; basic pond attributes recorded on a CS2007 Pond Mapping Recording Sheet.
- One pond per square is selected as the survey pond for detailed condition assessment and sampling by freshwater surveyors; selection may come from CS2000 data or be randomly chosen.
- The pond dataset tracks pond ID, area, water presence, reasons for loss/creation, and notes; pond boundaries, basins, and wetland indicators inform classification.

## Points, Areas, and Linear Features (Data Collection Studio)
- Points: capture individual trees, standing water bodies, ponds, etc.; edited at ≤1:5000 scale; veterans and buffer zones recorded with detailed attribute limits.
- Areas: map habitat extents; require careful editing for change, merging, and updating; minimum polygon size 0.25 ha; can contain multiple components with BH/PH attributes.
- Linear Features: record woody hedges, fences, walls, ditches, and other long features; minimum length 20 m, width up to 5 m; events along lines carry attributes (length, vegetation, species, cover) and can be copied/updated; margins/buffers documented (typical 6 m).

## Data Quality, Change Management, and Access
- Change status per attribute change: REAL change, ERROR correction, or new baseline PH; guidance differentiates genuine ecological change from prior mapping errors.
- For unenclosed habitats, older CS data (1990) merged with 1998 data to enhance detail and PH allocations.
- Edits are stored in the CS Surveyor database; sessions should be saved regularly to ensure reproducibility.
- Emphasis on reproducibility and time-series comparability to support monitoring and policy evaluation.
- Procedures exist for handling data issues (e.g., looping anomalies) and ensuring integrity before publication.

## Outputs, Monitoring, and Policy Uses
- Produces high-resolution maps, reports, and datasets detailing habitat extent, change, and BH/PH reporting.
- Framework supports UK Biodiversity Action Plans and environmental health/policy performance assessments through auditable time-series data.
- Aims to improve data accessibility and re-use by storing underlying data and enabling access via appropriate portals.

## Historical Context and Legacy Data
- CS2000/CS1990 contexts provide historical reference for attribute coding and parcel numbering, with mappings across themes and codes to support longitudinal analyses.
- Where possible, legacy data are integrated to enhance temporal coverage and PH allocations.

## Practical Implications for Analysts
- Rely on standardized classifications (BH/PH) and time-series architecture to compare conditions and policy outcomes over time.
- Leverage CS Surveyor for consistent, auditable data capture and change tracking across 1 km squares.
- Ensure data management practices enable underlying data sharing and reuse, aligning with policy monitoring needs.