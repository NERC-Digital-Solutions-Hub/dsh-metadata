# Yield Constraint Score (YCS) for the effect of five crop stresses on global production of four staple food crops.

## Purpose and scope
- Global assessment of yield constraints from five stresses (ozone, pests and diseases, soil nutrients, heat, aridity) on four staple crops (maize, rice, soybean, wheat).
- Outputs are gridded at 1° by 1° resolution, with separate shapefiles per crop.
- Provides per-grid-cell YCS for each stress (1–5 scale) and a total YCS (sum across stresses).

## Data collection and generation
- Grid construction: 1° by 1° grid; crop production data from FAO GAEZ (year 2000) with irrigated/non-irrigated split; 2010–2012 average production estimates using national conversion factors.
- Crop selection: maize, rice, soybean, wheat; only grid cells with >500 tonnes production included.
- Ozone yield constraint (YCS): calculated per cell using EMEP MSC-W model (POD3 IAM) for 2010–2012; yields converted to percentage losses using a wheat-based dose–response and relative sensitivities for other crops (soybean, rice, maize) relative to wheat; final Ozone YCS mapped to 1–5.
- Pests and diseases YCS: derived from Oerke et al. loss estimates (regional, 2002–2004); categorized into 1–5.
- Soil nutrient YCS: derived from HWSD v1.1 by combining topsoil and subsoil nutrient availability and retention (via GAEZ v3); assigns one of five classes per grid cell after majority-rule.
- Heat stress YCS: 30-day thermal-sensitive period based on crop-specific growing periods; daily heat stress index (f HSd) calculated from hourly temperature data (1990–2014); 30-day average mapped to five categories (1–5).
- Aridity YCS: mean Aridity Index (1950–2000) from CGIAR-CSI; climate classes (Humid to Hyper-arid) mapped to five stress levels.

## Calculation and data processing details
- Ozone YCS: uses POD3 IAM values, baseline subtraction (0.1), slope 0.64 to compute percent yield loss; wheat-based dose–response extended to other crops via relative sensitivity.
- Pests and diseases: regional mean losses (2002–2004) used directly to assign 1–5.
- Soil nutrients: five-class scheme based on combined topsoil/subsoil nutrient availability and retention; majority class per cell used.
- Heat: daily temperatures converted to daily effective temperature; per-cell 30-day average heat stress index used to assign 1–5.
- Aridity: five-class aridity from the Aridity Index; mean index per cell used to assign 1–5.
- Outputs: four GIS shapefiles (one per crop) with 1° grids and eight attribute columns, including per-stress and total YCS.

## Data structure and outputs
- Four Yield Constraint Score GIS shapefiles (maize, rice, soybean, wheat).
- Each cell includes 8 attributes:
  - ID: unique grid cell identifier
  - Long_Lat: grid cell center coordinates
  - Ozone: YCS for ozone (1–5)
  - Nutrient: YCS for soil nutrient stress (1–5)
  - Aridity: YCS for aridity stress (1–5)
  - Heat: YCS for heat stress (1–5)
  - Pests: YCS for pests and diseases (1–5)
  - Total: sum of all five stresses (overall YCS)

## Quality control and validation
- EMEP model validation described in Mills et al. (2018b): comparison of model outputs with Global Atmosphere Watch data showing good spatial and temporal agreement; Dmax and M7 values aligned with observations (r² 0.88–0.93 after outlier handling).
- Stomatal uptake proxy validation: strong correlation (r² = 0.63) between proxy metrics and modeled POD3 IAM/M7.
- Uncertainty discussions address species-specific flux data gaps (maize, rice, soybean), data currency for pests, soil data limitations (HWSD), and aridity/heat data choices.

## Uncertainty and limitations
- No species-specific ozone uptake data for maize, rice, soybean; wheat-based flux approach applied with relative sensitivity adjustments.
- Maize yield loss has higher uncertainty due to limited M7-based data.
- Pest and disease losses based on 2002–2004 literature; may overestimate current losses due to changes in crop protection.
- Soil nutrient YCS relies on HWSD-derived classifications with potential regional inconsistencies.
- Heat and aridity assessments depend on chosen climate datasets and time windows; aridity index averaged 1950–2000 may diverge from 2010–2012 conditions.
- Co-occurrence of stresses (heat and aridity) acknowledged; disentangling effects can be challenging.

## Governance, metadata, and stewardship considerations
- Provenance: data integrated from multiple sources (EMEP EMEP MSC-W model, FAO GAEZ, HWSD, WorldClim, CGIAR-CSI Aridity, USDA/FAO climate data).
- Data lineage and reproducibility: clearly documented processing steps (grid creation, period selections, 90-day growing windows, dose–response equations) enabling replication.
- Data formats: GIS shapefiles with clearly defined attributes; suitable for cataloging, mapping, and integration into broader datasets.
- Metadata needs for stewardship:
  - Data sources and versions (model versions, dataset revisions)
  - Temporal coverage and aggregation details
  - Spatial resolution and grid conventions
  - Calculation formulas and thresholds (e.g., POD3 IAM baseline, 0.1 baseline, 0.64 slope)
  - Quality flags and uncertainty notes
  - Access rights, licensing, and usage terms
- Recommendations for ongoing stewardship:
  - Maintain versioned releases with updated inputs and re-calculated YCS
  - Provide machine-readable metadata and a data dictionary
  - Document any policy changes, updated climate or soil datasets, or revised dose–response relationships
  - Enable data updates and clear notices about limitations and applicability

## References and sources (high level)
- Core methodology and validation papers (Mills et al., 2018a, 2018b) on global ozone yield gaps and model validation.
- Supporting datasets and tools: EMEP MSC-W model; FAO GAEZ; HWSD; WorldClim; CGIAR-CSI Aridity; USDA climate data; GAW observations.
- Related methodological foundations: dose–response relationships for ozone, heat stress indices, aridity classifications.