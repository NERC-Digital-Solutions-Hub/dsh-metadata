# LochLeven_SedimentDataset.csv

## Overview
- Dataset from a project investigating cycling of phosphorus between bed sediments and overlying water in Loch Leven, Scotland, during 2004–2005.
- Includes indicators of benthic algal biomass and methods/format for storage and analysis.
- Widely used in publications describing phosphorus mobilisation from bed sediments and the role of benthic microalgae (Spears et al., 2006–2012).

## Sampling regime
- Monthly sampling from April 2004 to April 2005.
- Six permanent sites along a depth transect (2.0, 2.5, 3.5, 5.5, 10.0, 22.0 m).
- Measurements taken in the field or in the laboratory from field-collected samples.
- Core sampling conducted at each site; upper 3 cm of sediment homogenised for analysis.

## List of sites
- Table 1 provides OS grid references, depth, and value counts per site.
  - Example: Site 1 at depth 2.0 m, Count = 500.
  - Other sites (2–6) depths 2.5, 3.5, 5.5, 10.0, 22.0 m with Count = 405 (for most sites).

## List of determinands
- Measurements and units across surface, bottom, pore, and sediment where applicable:
  - Dissolved Oxygen (% sat), Conductivity (mS/cm), pH, Temperature (°C).
  - Soluble Reactive Phosphorus (SRP, µg/L) with locations (Surface, Bottom, Pore, Sediment = S/B/P).
  - Total Soluble Phosphorus (TSP) and Total Phosphorus (TP) with multiple descriptors (e.g., 1 = µg/L; 2 = S/B; 3 = 60 equivalents).
  - Ammonium-N (NH4-N, µg/L) with location descriptors.
  - Silicate (SiO2-Si, mg/L) with location descriptors.
  - Chlorophyll a (µg/L and µg/g dry weight), with sediment and/or water forms.
  - Sediment-P fractions including labile P, reductant-soluble P, reductant soluble SURP, metal oxide P, organic P, apatite-bound P, residual P, and total P fractions (expressed in mg P/gdw or related units).

## Sampling, measurement and analysis methods
- Surface water collected at each site; in situ water quality measurements (DO, temperature, pH, conductivity) with Hydrolab probes.
- Sediment cores collected (approx. 30 cm overlying water, 20 cm sediment); bottom water extracted from cores for analysis.
- Filtration (Whatman GF/C) and storage at 4 °C for chemical analyses; pigments stored for later analysis.
- Analytical methods:
  - SRP: Murphy & Riley (1962).
  - TP: Wetzel & Likens (2000) with additional acidification step for complete digestion.
  - NH4-N: Phenol-hypochlorite method (Wetzel & Likens, 2000).
  - SRSiO2: Golterman et al. (1978).
  - Chlorophyll a: Spectrophotometric quantification with phaeopigment correction; acetone extraction.
  - Sediment-P fractionation: Sequential extraction (Psenner et al. 1988; Farmer et al. 1994) with steps for SRP, reductant-soluble P, metal-oxide adsorbed P, apatite-bound P, and residual P; calculations for organic P from differences between extracts.
- Extractions and analyses performed in the dark at ~20 °C; samples shaken and centrifuged as described.

## Format of stored data
- Single ASCII CSV file with columns:
  - Site, Depth, Month, Date, DO (%sat), Cond (mS cm^-1), pH, Temp (°C),
  - SRP (µg/L), TSP (µg/L), TP (µg/L),
  - NH4 (µg/L), SiO2 (mg/L), Chl a (µg/L),
  - SRP (µg/L), TSP (µg/L), NH4-N (µg/L),
  - Labile (mg P/gdw), Red soluble (mg/gdw), Red sol surp (mg/gdw),
  - Metal oxide (mg/gdw), Organic (mg/gdw), Apatite bound (mg/gdw),
  - Residual (mg/gdw), TP (mg/gdw), Chl a (µg/gdw).

## References
- Standard methods and foundational analyses informing the data:
  - APHA (1992). Standard methods for the examination of water and wastewater.
  - Murphy & Riley (1962); Wetzel & Likens (2000).
  - Golterman et al. (1978); Psenner et al. (1988); Farmer et al. (1994).
- Related publications utilizing the dataset:
  - Spears et al. (2006, 2007a, 2007b, 2009, 2010, 2012) on phosphorus mobility and benthic algae in Loch Leven.
  - Evans et al. (2009) on diatom populations.