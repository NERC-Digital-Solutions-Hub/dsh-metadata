# Metadata for data associated with dataset 'Measurements of carbon cycling processes in tropical forest soils varying in soil abiotic and biotic properties' (13C_Peru_fluxes.csv, 13C_Peru_soils.csv and 13C_PLFA_incorporation.csv)

## Overview
- A field- and lab-based dataset from ten sites along an elevational gradient on the east flank of the Peruvian Andes (210–3400 m asl) investigating how microbial communities and soil properties control carbon release in tropical forest soils.
- Includes abiotic soil properties, microbial community indicators (PLFA and isotopic data), CO2 flux measurements, and 13C-labeled substrate incorporation to quantify substrate-derived respiration and priming effects.
- Derived metrics include substrate-derived CO2, primed carbon, substrate-derived PLFA carbon, and microbial carbon-use efficiency (CUE).

## Geospatial and sampling context
- Study area spans a tropical elevation transect from lowland Amazonian rainforest to upper montane cloud forest; continuous forest cover with tree-line near ~3500 m.
- At each site: organic soil layer sampled from 5 sub-plots within established 1 ha plots; organic layer removed from a 40 x 40 cm area in each sub-plot.
- Soil samples collected January 2012, stored at 4°C for up to 6 weeks before experimentation.
- Elevation is a key gradient controlling temperature and precipitation across sites.

## Data types and key variables
- Soil abiotic properties (from organic soil samples):
  - Elevation (m asl)
  - pH (soil water, 1:2.5 w:v)
  - Gravimetric moisture content
  - Bulk density
  - Total C (TotC, %)
  - Total N (TotN, %)
  - Carbon-to-nitrogen ratio (Cnratio)
  - Maximum water holding capacity (WHC)
- Microbial and community indicators:
  - Total PLFA (totPLFA)
  - Fungal PLFA (FPLFA)
  - Bacterial PLFA (BPLFA)
  - F:B PLFA ratio (FB)
  - GP (Gram-positive) PLFA
  - GN (Gram-negative) PLFA
  - GP:GN PLFA ratio (GPGN)
  - Substrate-related PLFA data including 13C-enriched measures (e.g., BPLFA13C, FPLFA13C, GP13C, GN13C, Unspec13C, TotPLFA13C)
  - 13C-PLFA detailed values and corrections for methylation
  - 13CPLFA_PC (percentage of PLFA carbon labeled)
- Substrates and treatments:
  - Substrate (coded 1–5)
  - SubsName (substrate name)
  - 13C-labeled substrate incorporation metrics
- CO2 flux and isotopic measurements:
  - ActualFlux (CO2-C per g soil dry weight per day)
  - Basal and substrate-derived respiration at 24, 48, and 168 hours (Basal24, Basal48, Basal168; Subs24, Subs48, Subs168)
  - Primed respiration at 24 and 168 hours (Prime24, Prime168)
  - Substrate-derived fraction of respired CO2 at 24, 48, 168 hours (derived via δ13C mixing model)
  - δ13C values for CO2 (control and treated) and substrate
- Isotopic calculations and derived metrics:
  - Percent substrate-derived C in CO2
  - Primed C (increase in respiration not explained by substrate-derived CO2)
  - 13C incorporation into PLFAs (µg 13C PLFA g-1 soil dwt)
  - Microbial carbon-use efficiency (CUE) as ratio of 13C assimilated into total PLFAs to total respired 13C
- Analytical and data processing notes:
  - Gas analyses: CO2 by GC-FID with methaniser; δ13C by IRMS; calibration and blanks per batch
  - PLFA analyses: GC-MS with internal standard; identification of GP and GN markers; 13C-PLFA corrections
  - Data analyzed in R (version 2.14.0); three-way ANOVA to test effects of substrate, soil, and time; post-hoc Tukey tests; transformations applied as needed
- Subsets and related references:
  - Data files: 13C_Peru_fluxes.csv, 13C_Peru_soils.csv, 13C_PLFA_incorporation.csv
  - Core study: Whitaker et al., 2014 (Maximum Prime) and related methodological references

## Methods workflow (high-level)
- Field sampling: ten sites along a tropical elevation gradient; collect organic soil from multiple sub-plots within 1 ha plots.
- Abiotic analysis: measure pH, moisture, bulk density, TotC, TotN, C/N, WHC.
- Incubation experiment: incubate 5 g fwt soil with one of four 13C-labeled substrates or control; adjust to 75% WHC; incubate for 7 days at 20°C; headspace sampled at 24, 48, 168 hours.
- CO2 and isotopic analyses: quantify CO2 flux (CO2-C) and δ13C of CO2; determine substrate-derived CO2 using a mixing model.
- PLFA and 13C-PLFA analysis: extract PLFAs, identify fungal vs bacterial markers, determine total PLFA and isotopic enrichment; calculate substrate-derived PLFA C and CUE.
- Calculations: derive primed C as total respiration change minus substrate-derived respiration; compute 13C-PLFA enrichments and the distribution of substrate-derived C across microbial groups.
- Statistics: use R for three-way ANOVA (substrate × soil × time) and two-way ANOVA for microbial composition effects; apply square-root transformations as needed; post-hoc comparisons with Tukey’s HSD.

## How this supports GIS visualization and data products
- Provides spatially-explicit, elevation-graded data on soil carbon processes and microbial community responses, enabling map-based visualization of:
  - Variations in primed C and substrate-derived respiration across sites
  - Distribution of microbial functional groups (fungi vs bacteria; GP vs GN) along the elevation gradient
  - Relationships between abiotic soil properties and carbon-cycling metrics
- Data are complemented by explicit units, data descriptions, and metadata to facilitate integration with GIS layers (e.g., site elevations, soil properties, microbial indicators, and respiration metrics).
- Clear, programmatic workflows and statistical treatments support reproducible mapping analyses and cross-site comparisons.