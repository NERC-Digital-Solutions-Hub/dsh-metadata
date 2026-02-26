# LochLeven_SedimentDataset.csv

## Overview
- Dataset describing measurements from a project on phosphorus cycling between bed sediments and overlying water in Loch Leven, Scotland (2004–2005).
- Includes indicators of benthic algal community biomass.
- Used in numerous publications to describe phosphorus mobilisation and the role of benthic microalgae.
- Data stored as a single CSV file with standardized sampling and analysis methods.

## Spatial and Temporal Coverage
- Location: Loch Leven, a lowland, shallow, freshwater eutrophic lake in Scotland, UK.
- Timeframe: Monthly sampling from April 2004 to April 2005.
- Sites: Six permanent sampling sites along a water-depth transect.
  - Site details include OS grid references and depth: 12303 01311 (2.0 m), 12689 01211 (2.5 m), 13497 01189 (3.5 m), 14804 01092 (5.5 m), 14195 02640 (10.0 m), 14090 03981 (22.0 m).
  - Counts per site vary (e.g., 500 values at the shallowest site, 405 at several deeper sites).

## Data Content and Structure
- Determinands measured (by substrate: surface, bottom, pore, sediment where applicable):
  - Dissolved Oxygen (%sat), Conductivity (mS/cm), pH, Temperature (°C)
  - Soluble Reactive Phosphorus (SRP, µg/L)
  - Total Soluble Phosphorus (TSP), Total Phosphorus (TP)
  - Ammonium-N (NH4-N)
  - Silicate (SiO2)
  - Chlorophyll a (µg/L) with sediment/gdw corrections
  - Sediment phosphorus fractions including labile P, reductant-soluble P, reductant-soluble unreactive P, metal oxide P, organic P, apatite-bound P, residual P, and related totals
- Data includes both water column measurements (surface/bottom) and sediment analyses (pore/sediment), with specific sampling dates and month identifiers.

## Sampling Regime and Methods
- Sampling cadence: Monthly visits to the six sites over the 12-month period.
- Field measurements: Surface water collected in acid-washed bottles; in situ measurements of depth profiles for temperature, DO%, pH, and conductivity using Hydrolab equipment.
- Sediment sampling: Single sediment cores (approx. 30 cm overlying water, 20 cm sediment) collected with a Jenkin sampler; core contents processed in the lab.
- Laboratory processing:
  - Filtration of surface waters for chemical analyses; pigments stored for later analysis.
  - Upper 3 cm of sediment homogenised for pore water chemistry and pigment analyses.
  - Chlorophyll a extracted from sediment/water using acetone, with phaeopigment correction.
  - Phosphorus fractions measured via sequential chemical extraction (Psenner et al. 1988; Farmer et al. 1994) with multiple steps to separate labile, reductant-soluble, metal-oxide bound, apatite-bound, and residual P; organic P inferred from NaOH extracts.
- Analytical methods and references include Murphy & Riley (1962) for SRP, Wetzel & Likens (2000) for TP, APHA (1992) standard methods, and other established techniques for chlorophyll and silicate analyses.

## Data Format
- Storage: Single ASCII text file in CSV format.
- Columns (representative): Site, Depth, Month, Date, DO (%sat), Conductivity (mS/cm), pH, Temp (°C), SRP (µg/L), TSP (µg/L), TP (µg/L), NH4 (µg/L), SiO2 (mg/L), Chl a (µg/L), labile (P fraction, mg P/gdw), red sol (mg/gdw), red sol surp (mg/gdw), Metal oxide (mg/gdw), Organic (mg/gdw), apatite bound (mg/gdw), Residual (mg/gdw), TP (mg/gdw), Chl a (µg/gdw).
- Data scope supports spatial (site/depth) and temporal (monthly) analysis, enabling GIS-based visualization of phosphorus dynamics and algal biomass indicators.

## Key References and Context
- Foundational methods and context for analyses and interpretation, including:
  - APHA (1992) Standard Methods
  - Murphy & Riley (1962) SRP determination
  - Wetzel & Likens (2000) TP methods
  - Psenner et al. (1988); Farmer et al. (1994) sediment P fractionation
  - Golterman et al. (1978); other cited methodological references
- Related publications detailing spatial and temporal variation, phosphorus mobility, and sediment–water interactions in Loch Leven and similar ecosystems.

## GIS Relevance and Potential Uses
- Geospatial aspect: six fixed sampling sites with precise OS grid references and depth, suitable for GIS mapping and spatial analysis.
- Time-series: monthly data allows tracking of seasonal dynamics in water quality and sediment phosphorus fractions.
- Multivariate visualization: map-based representations of SRP, TP, and sediment P fractions across depth transects; integration with bathymetry, lake morphology, and benthic biomass indicators (Chl a) to assess phosphorus mobilisation and ecological status.
- Data integration: combine with additional layers (e.g., water depth, substrate type, abiotic factors) to support policy-relevant insights and water quality management.

## Practical Considerations for GIS Specialists
- Ensure alignment of OS grid references and depth to accurate georeferencing for mapping.
- Consider splitting by substrate (surface, bottom, pore, sediment) to preserve contextual meaning in GIS visualizations.
- Use temporal dimension in GIS (time-enabled layers) to display monthly changes and trends in phosphorus fractions and chlorophyll a.
- Validate column mappings when importing the CSV to preserve unit consistency (e.g., SRP in µg/L, TP in µg/L, P fractions in mg/gdw).