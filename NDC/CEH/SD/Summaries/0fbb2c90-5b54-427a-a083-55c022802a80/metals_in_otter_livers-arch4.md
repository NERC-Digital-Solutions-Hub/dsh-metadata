# Otter Collection and Post Mortem Examination

## Executive overview
- A study of otter carcasses submitted by local authorities, environmental groups, and the public to the Cardiff University Otter Project.
- For each otter: location (National Grid Reference), collection date, and a standardized post-mortem with phenotypic data (sex, length, weight, age class) and a condition score (scaled mass index).
- Liver tissue samples collected and archived at -20°C; 278 liver samples from otters that died between 2006 and 2017 were analyzed as a stratified random sub-sample, mainly from England and Wales with three cases from Scotland.
- Aims to quantify liver concentrations of 13 elements and relate findings to environmental and anthropogenic data available across spatial scales.

## Data collection and sample processing
- Post-mortem protocol and phenotypic measurements documented consistently (sex, length, weight, age class; sSMI condition score).
- Liver tissue sampling: two 1 g subsamples per otter, one for trace element analysis (acid digestion and ICP-MS), one for dry matter determination (drying at 105°C for 18 hours).
- Elemental concentrations reported on a μg/g dry weight basis; measurements not recovery-corrected but with generally satisfactory recoveries across years.
- Yearly sampling occurred (liver analyses conducted in 2009, 2011, and 2017 with method refinements over time).

## Analytical methods
- Analyzed 13 elements in otter livers: Ag, As, Cd, Cr, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Se, Zn (plus Sr and V listed in the data dictionary).
- ICP-MS used for elemental concentrations; results tied to batch information and otter identifiers (e.g., UWCRef, Batch).
- Comprehensive metadata captured for each otter, including body weight, sSMI, and geographic coordinates.

## Spatial data and geospatial integration
- Spatial data compiled on biochemistry of streams/soils, weather, and anthropogenic contaminant sources from multiple sources.
- A model-derived map of predicted nanosilver concentrations in surface water used as a spatial predictor.
- Data mapped in ArcGIS ArcMap (v10.4.1) as continuous raster layers or point data.
- Otters’ potential spatial exposure area approximated by a 20-km-diameter circle (centered on carcass) within their riverine home range; data extracted for each otter area using Geospatial Modelling Environment.
- For each otter area, environmental variables summarized as means (e.g., soil elements, soil pH, stream pH, rainfall, nanoparticle concentrations, population density) or sums (e.g., number of consented discharges, annual metal inputs).
- Distance to the coast calculated by least-distance along rivers; otters within a defined coastal zone retained, others excluded if relevance to river catchment was uncertain.

## Data attributes and provenance
- Core identifiers and measurements per otter include:
  - UWCRef (unique otter carcass ID)
  - Sex, AgeClass, Year, Batch
  - Weight and sSMI (condition index)
  - X and Y coordinates (National Grid references)
  - DM (liver dry matter content)
  - Concentrations for each metal (e.g., Al, Mn, Fe, Co, Ni, Cu, Zn, Se, Sr, Mo, Cd, Sb, Pb, Hg, Cr, As, V, Ag)
  - Soil and sediment chemistry: SoilC, SoilpH, RiverpH, SedCaO, SedAs, SedCr, SedNi, SedPb, SoilAg, SoilAs, SoilCd, SoilCl, SoilCr, SoilNi, SoilPb, SoilS, Rain, dCoastR, and others
  - Anthropogenic indicators: USD6 (total consented discharges within 10 km), Mine (presence/absence of mining near otter), PopD (population density)
- The data dictionary provides detailed column explanations and units (e.g., μg/g dry weight for metals, g/kg for soil carbon, mm for rainfall).

## Data quality, limitations, and notes
- Some environmental parameters have NA (not applicable) or ND (not detected) values; the meaning is dataset-specific (no data extracted for the otter’s area, or non-detection).
- Data spans multiple years with methodological refinements; not all metals may have identical coverage across all otters.
- Four otters were excluded from coastal distance scoring due to uncertainty about river catchment relevance.
- The study integrates diverse data sources with varying spatial resolutions and time frames, which may influence comparability across sites.

## Data governance, accessibility, and references
- Provisions for data provenance include explicit mapping to archival tissues, analytic batches, and a robust set of external data sources (geochemical atlases, government datasets, mining inventories, population grids, rainfall datasets, etc.).
- Key references for methods and spatial data sources include: geospatial modelling tools (Geospatial Modelling Environment), nanosilver surface water prediction (Dumont et al. 2015), soil geochemical baselines (G-BASE), various Welsh/UK environmental data agencies, and standard otter post-mortem protocols (Simpson 2000).
- The dataset is curated to support cross-study comparisons and future analyses of contaminant exposure in otters relative to landscape-level biogeochemical drivers.