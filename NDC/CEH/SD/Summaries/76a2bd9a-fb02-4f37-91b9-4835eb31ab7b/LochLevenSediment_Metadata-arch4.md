# LochLeven_SedimentDataset.csv

## Overview
- Describes the dataset LochLeven_SedimentDataset.csv from a project on phosphorus cycling between bed sediments and the overlying water column in Loch Leven (2004–2005).
- Includes indicators of benthic algal community biomass.
- Loch Leven is a shallow, lowland, eutrophic freshwater lake in Scotland, UK.
- The document outlines data nature, sampling and analysis methods, and storage format, with these data cited in numerous publications on phosphorus mobilisation and benthic microalgae roles.

## Sampling regime and Sites
- Monthly sampling from April 2004 to April 2005.
- Six permanent sites along a water-depth transect.
- Site details include OS grid references, depth, and the number of values (Counts) per site.
- Depths sampled: 2.0, 2.5, 3.5, 5.5, 10.0, and 22.0 meters.

## Determinands and Measurements
- Measurements cover surface, bottom, pore, and sediment contexts with various parameters:
  - Physical/chemical: Dissolved Oxygen (%sat), Conductivity (mS/cm), pH, Temperature (°C).
  - Nutrients in water: Soluble Reactive Phosphorus (SRP), Total Soluble Phosphorus (TSP), Total Phosphorus (TP), Ammonium-N (NH4-N), Silicate (SiO2).
  - Primary production proxy: Chlorophyll a.
  - Phosphorus fractions in sediment: labile P, reductant-soluble P, metal oxide P, organic P, apatite-bound P, residual P, and related SRP/TSP values for some fractions.
- Data include depth-specific and site-specific records; some parameters have separate records by sample type (Surface, Bottom, Pore, Sediment).

## Methods (Sampling, Measurement, and Analysis)
- Monthly field sampling at six sites along the depth transect; in situ measurements of temperature, DO, pH, and conductivity; collection of sediment cores with overlying water.
- Laboratory analyses:
  - SRP and TP via colorimetric methods (Murphy & Riley; Wetzel & Likens with digestion for TP).
  - NH4-N via phenol-hypochlorite method.
  - SRSiO2 via specified colorimetric method.
  - Chlorophyll a quantified after pigment extraction with acetone and corrected for phaeopigments.
  - Sediment P fractionation by sequential extraction (Psenner et al. 1988; Farmer et al. 1994) across five steps: labile P, reductant-soluble P and TSP, metal-oxide P and SRP, apatite-bound P, and residual P; organic P derived from NaOH extractions.
- Core processing details include splitting, filtration, storage, and in-lab processing of pore water and sediments.

## Data Format, Structure, and Storage
- All data stored in a single ASCII CSV file.
- Columns labeled: Site, Depth, Month, Date, DO, Cond, pH, Temp, SRP, TSP, TP, NH4, SiO2, Chl a, SRP (second set), TSP (second set), NH4-N, labile, red sol, red sol surp, Metal oxide, Organic, apatite bound, Residual, TP (gdw), Chl a (gdw).
- Data provenance includes references for measurement methods and standard procedures.

## Data Provenance and References
- Methods and analyses grounded in established literature and standard methods:
  - APHA (1992) Standard Methods for the Examination of Water and Wastewater.
  - Murphy & Riley (1962) phosphate determination.
  - Wetzel & Likens (2000) Limnological Analyses methods.
  - Psenner et al. (1988); Farmer et al. (1994) for phosphorus fractionation.
  - Spears et al. and related works (2006–2012) on phosphorus mobility and sediment–water interactions.
- Several publications (Spears et al., 2006–2012) have used these data to describe phosphorus mobilisation and the role of benthic microalgae.

## Usage, Impact, and Access
- The dataset has been used in multiple publications to describe phosphorus mobilisation from bed sediments and the regulation by benthic microalgae.
- Stored as a CSV to support discoverability and reuse; includes site and depth metadata via OS references and depth values.

## Considerations for Data Leaders
- Temporal scope is limited to a single 12-month period, with six sites along a depth transect; may affect longitudinal applicability.
- Data are site-specific to Loch Leven; potential gaps or variability in records across determinands (noted by per-determinant record counts) should be considered for analyses.
- Provenance and methodological rigor are well-documented, enabling replication or re-use within the data ecosystem.