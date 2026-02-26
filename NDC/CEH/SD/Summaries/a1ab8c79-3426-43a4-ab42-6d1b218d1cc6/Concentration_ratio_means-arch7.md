# Sample_Code, Explanation = Unique sample identifier.

## Overview and purpose
- A data dictionary/template describing sample metadata and concentration data for a suite of elements and isotopes.
- Aimed at organizing data used for GIS-based map visualisations and spatial analysis of environmental or radiological samples.
- Emphasises linking samples to species, RAP (Reference Animals/Plants), and description of the analysed portion.

## Key fields and structure
- Sample_Code: Unique identifier for each sample (no units/methodology specified; notes unavailable).
- Species: Latin name of sampled species.
- RAP: Reference Animals and Plants category from ICRP RAP framework.
- Sample_Description: Part of the sample that was analysed.
- Mean_Value: Indicates whether the reported mean is geometric or arithmetic.
- Standard_Deviation_I-127, Standard_Deviation_Li, Standard_Deviation_Be, etc.: Geometric or arithmetic standard deviation as identified by Mean_Value.
- Concentration ratios by element (example elements): I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, U, U-related fields.
  - For each element, the data conventions specify:
    - 1 = Mean concentration ratio
    - 2 = unitless
    - 3 = Geometric or arithmetic mean as identified by Mean_Value
- Additional placeholders indicate where specific values and metadata would be populated (e.g., variations by element, standard deviations, and notes).

## Data quality and consistency considerations
- Data appear as a template with many placeholder entries (., 1, 2, 3) indicating required field values rather than present data.
- Mean type (geometric vs arithmetic) is defined per sample and per element via Mean_Value.
- Standard deviations are element-specific and tied to the identified Mean_Value.
- RAP and species fields rely on standardized taxonomic and radiological reference data (ICRP RAP) for consistency across GIS layers.

## GIS-relevant implications
- Suitable for creating point-based GIS layers where each sample is a feature with attributes:
  - Sample_Code, Species, RAP, Sample_Description
  - For each element: mean concentration ratio, unit type (unitless), and confidence measure (standard deviation)
- Possible map products:
  - Spatial distribution of mean concentration ratios per element.
  - Comparative maps showing geometric vs arithmetic means across sites.
  - RAP- and species-based thematic maps showing sampling coverage and data availability.
- Data integration needs:
  - Consolidate data from multiple sources as data are often held in many places.
  - Standardize units, mean types, and formatting across samples.
  - Link to related GIS layers (sampling locations, RAP classifications, species distributions).

## Recommended data preparation workflow
- Validate and fill in missing values for Sample_Code, Species, RAP, Sample_Description, and per-element statistics.
- Harmonize Mean_Value definitions across all samples; ensure consistent interpretation of geometric vs arithmetic means.
- Normalize units to a common scale (focus on unitless concentration ratios per element).
- Clean and transform data to map-ready formats (e.g., CSV/GeoDB with spatial coordinates or site IDs linked to a separate geospatial layer).
- Quality assure by cross-checking against source metadata and ensuring alignment with RAP framework.

## End notes and practical next steps
- This document describes the schema and conventions for a rich, map-ready dataset of sample concentrations across many elements, anchored by RAP classifications.
- To maximise GIS utility, complete data population, enforce consistent standards, and integrate with location data to enable effective spatial analysis and visualisation.