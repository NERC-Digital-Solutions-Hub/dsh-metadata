# Rainfall catch

## Overview
- Metadata-rich dataset describing rainfall catch, throughfall catch, and stemflow catch collected between 23-May-1990 and 06-Apr-1992.
- Measurements cover a broad set of dissolved constituents (e.g., Al, B, Ba, Cl, Cu, Ca, F, Fe, Mn, Na, NH4, NO3, Si, SO4, Sr, Zn, SRP) with associated units, detection limits, and analytical methods.
- Sampling/workflow involves multiple laboratories (e.g., Wallingford, Field) and varying filtration/preservation procedures.
- Structure indicates separate blocks for Rainfall catch, Throughfall catch, and Stemflow catch, each with consistent start/end dates but differing lab and method details.
- Highly suitable for GIS integration, enabling map-based visualization of hydrology and dissolved chemistry across time and sampling types, though data completeness and standardization vary.

## Data Content and Variables
- Sampling types:
  - Rainfall catch
  - Throughfall catch
  - Stemflow catch
- Analyte families (example subset with consistent metadata structure):
  - Dissolved Al, B, Ba, Br, Cu, Ca, Cl, F, Fe, Mn, Na, NH4, NO3, Si, SO4, Sr, Zn
  - Optional/derived metrics such as SRP (soluble reactive phosphorus)
  - pH
- For each analyte and sampling type, metadata fields include:
  - UNITS, LQDC (lower quantification detection limit), QUOTE TO (quantification factor)
  - START and END dates
  - LAB (laboratory performing the analysis)
  - FILTRATION, PRESERVATION (sample handling specifics)
  - METHOD (analytical technique, e.g., ICP-OES, IC, Autoanalyzer)
  - Measured values (often blank in this record)
- Filtration/preservation specifics vary by analyte (e.g., 47 mm 0.45 µm membranes; storage at 4 °C; acidification to 1% HNO3; field vs lab handling).
- Analytical methods cited include ICP-OES, ion chromatography, automated colorimetry, and gravimetric/volumetric approaches.
- Data organization suggests separate blocks for Rainfall catch, Throughfall catch, and Stemflow catch with aligned timeframes but varying lab/method details.

## Temporal and Spatial Scope
- Timeframe: 23-May-1990 to 06-Apr-1992 (approximately 23 months).
- Locations/Labs: Wallingford; Field (Stemflow catch); indicates multi-site data handling.
- Spatial details are not explicitly georeferenced in the record; mapping requires additional site coordinates or metadata linking samples to catchment areas.

## Data Structure and GIS Use
- Highly structured with uniform metadata schema per analyte and sampling type, enabling GIS attribute table integration.
- Potential GIS layers:
  - Catch type layers (Rainfall catch, Throughfall catch, Stemflow catch) as spatial sampling points or zones
  - Concentration layers for each analyte (e.g., Ca, NO3, SO4, Fe, Al) over time
  - QA/flags layer signaling data completeness and detection limits
- Visualization approaches:
  - Time-enabled maps showing spatial distribution of dissolved constituents
  - Choropleth/chorobar maps by sampling event
  - Temporal sliders to explore 1990–1992 variations
- Data preparation considerations:
  - Standardize units across analytes
  - Manage blanks and non-detects
  - Align Start/End dates with sampling events
  - Integrate with rainfall/hydrology layers to relate catchment processes with chemical signals

## Data Quality, Standards, and GIS Challenges
- Key challenges:
  - Data held in multiple places; integration requires harmonization
  - Incomplete data; many analyte fields contain blanks
  - Inconsistent data standards across analytes and sampling types
  - Large/complex dataset with many parameters; need packaging into manageable chunks
  - Data cleaning and transformation requirements; potential skill gaps in teams
- GIS-specific implications:
  - Requirement for reliable georeferencing of sampling points or catchment areas
  - Clear mappings between sampling types and spatial features
  - Unit and detection limit standardization essential for accurate map-based comparisons

## Practical Guidance for GIS Specialists
- Use the dataset as a basis for multi-layer GIS visualization:
  - Layer 1: catchment locations or sampling points for Rainfall catch, Throughfall catch, Stemflow catch
  - Layer 2+: time-enabled layers (raster or attribute) for key analytes (e.g., Ca, NO3, SO4, Fe, Al)
  - Layer for pH and SRP to assess acidity and nutrient signals
- Data workflow recommendations:
  - Extract analyte metadata (units, LQDC, methods) and join to sample observations
  - Normalize units and consistently handle non-detects/blanks
  - Create time-series visuals to compare dissolved chemistry across sampling types
- Address data gaps:
  - Document missing values and detection limits in GIS attributes
  - Use visual cues to indicate data quality issues and guide improvements
- Documentation and metadata:
  - Preserve provenance by linking analyte data to labs, methods, filtration, and preservation
  - Capture start/end dates to support temporal queries and audits

## Summary of Key Points
- A multi-analyte, multi-sampling-type, metadata-rich dataset for rainfall-related catchments collected 1990–1992.
- Includes detailed procedural metadata (lab, filtration, preservation, method) for numerous dissolved constituents.
- Structured for GIS integration, enabling map-based visualization of hydrology and dissolved chemistry across time and sampling types.
- Highlights data quality and standardization challenges common to complex, multi-site environmental datasets; requires careful QA, harmonization, and georeferencing for effective GIS use.