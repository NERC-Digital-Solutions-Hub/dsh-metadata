# Supporting documentation

## Overview
- Dataset of hemispherical canopy photographs used to estimate leaf area index (LAI) at plot level in 0.5 ha permanent plots.
- Context: NORDESTE project in the Caatinga biome of northeast Brazil, a relatively dry region with irregular rainfall; aims to address decades of neglect in biodiversity and ecosystem-function research through Brazil-UK collaboration.
- Key purpose: derive LAI variation across Caatinga plots via hemispherical photography and subsequent processing.

## Scope and Content
- Photographs: hemispherical images of canopy structure to estimate LAI.
- Plot coverage: either 12 plots (sites) with ~36 photos per site, or 14 plots with ~50 photos per site.
- Total: 1132 photos comprising 2607.8 MB.
- Per-plot metadata: table listing plot IDs, names, locations (state, country), coordinates, number of photos, file size, and date.
- Image characteristics: taken with a Nikon D100 camera and Sigma 4.5 mm F2.8 fisheye lens; under overcast conditions; one photo per intersection of four subplots (or at the center of a subplot for other sites); top of camera oriented north at ~1 m height.
- Processing: photos processed to provide a representative LAI value for the whole plot (not subplots), linked to vegetation height and canopy structure.

## Study Context and Timing
- Regions: Caatinga vegetation in Brazil; a warm, seasonally dry climate with droughts.
- Field period: March 2017 to August 2019.
- Notable caveat: for MORO sites, two dates exist (2017 and 2018) and some entries indicate incorrect or inconsistent dates in the JPEG metadata (photos dated 2017 despite actual dates).

## Data Collection and Tools
- Equipment: Nikon D100; Sigma 4.5 mm fisheye lens.
- Sampling design: hemispherical photos at intersections of subplots or at subplot centers; one photo per location; camera height ~1 m; image direction oriented north.
- Variation in data collection: occasional camera trigger failures or sky condition changes reduced the number of usable photos per plot.

## Metadata and File Information
- Plot-level metadata includes:
  - Plot IDs (e.g., BTI_01, CGR_01, CJU_01, etc.)
  - Location details (state, country)
  - Coordinates (latitude/longitude)
  - Number of photos per plot
  - File size per plot
  - Capture date per plot
- Total dataset metadata indicates: 1132 photos and 2607.8 MB of data.
- Note: table formatting in the source has some inconsistencies (e.g., ambiguous coordinate representations and date entries), and some site entries carry special markers (e.g., MOR_01*, MOR_02*). 

## Data Quality and Limitations
- Date metadata issues: some JPEG files have incorrect dates, especially for MOR sites (actual dates may differ from recorded).
- Inconsistencies in table formatting and entry details can affect discoverability and linking of metadata to image files.
- Variable sampling per plot and occasional data gaps due to equipment or sky conditions.
- LAI is inferred from hemispherical photos to produce plot-level estimates, not per-subplot measurements; individual image content may over- or under-represent certain canopy features depending on distance and vegetation height (up to ~20 m from camera).

## Potential Uses and Value
- LAI estimation and variation analysis across Caatinga plots.
- Integration with soil, climate, biomass, phenology, growth, carbon allocation, biodiversity, and ecosystem functioning studies.
- Cross-site comparative analyses to inform ecological models and remote sensing validation.
- Data for policy-related biodiversity and ecosystem-function research within a Brazilian-UK collaborative framework.

## Implications for Data Leaders (Data Strategy and Governance)
- Demonstrates effective cross-institution collaboration and a clear data collection objective tied to policy-relevant biodiversity research.
- Metadata richness supports discoverability and reuse, but requires cleanup and standardization to maximize interoperability (address date inconsistencies and table formatting issues).
- Highlights the importance of maintaining consistent documentation for field campaigns, including instrument settings, sampling density, and data processing steps.
- Suggests opportunities to improve data stewardship: standardized metadata schema, provenance tracking, data quality notes, and robust data access and discovery mechanisms.

## Key Next Steps for Data Leaders
- Clean and standardize metadata: resolve date discrepancies, harmonize plot naming, and formalize coordinate representations.
- Establish a metadata schema for future photogrammetry/LAI datasets to improve discoverability and interoperability across networks.
- Implement data quality assessments and provenance logs, including processing workflows from raw hemispherical images to LAI estimates.
- Create a centralized access point or repository entry for the dataset with clear licensing, usage rights, and citation guidance.
- Explore integration with broader Caatinga biodiversity and ecosystem datasets to support cross-domain analyses and policy-oriented research.