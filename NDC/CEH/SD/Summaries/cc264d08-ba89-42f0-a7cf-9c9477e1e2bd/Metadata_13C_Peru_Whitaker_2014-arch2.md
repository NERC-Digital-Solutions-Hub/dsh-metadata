# Metadata for data associated with dataset 'Measurements of carbon cycling processes in tropical forest soils varying in soil abiotic and biotic properties' (13C_Peru_fluxes.csv, 13C_Peru_soils.csv and 13C_PLFA_incorporation.csv)

## Overview
- Provides metadata and methods for a dataset investigating carbon cycling in tropical forest soils across an elevation gradient in Peru.
- Integrates soil abiotic properties with microbial community structure and carbon inputs using 13C-labelled substrates.
- Focuses on partitioning CO2 fluxes into substrate-derived and primed components and linking them to PLFA-based microbial groups.

## Data structure and key variables
- Site and soil properties
  - Elevation (m asl)
  - pH (soil, 1:2.5 w:v)
  - TotC (total carbon, %)
  - TotN (total nitrogen, %)
  - Cnratio (C/N)
  - BulkDensity (g cm-3)
  - TotPLFA (total phospholipid-derived fatty acids)
  - FPLFA (fungal PLFA)
  - BPLFA (bacterial PLFA)
  - FB (F:B ratio)
  - GP (Gram-positive PLFA)
  - GN (Gram-negative PLFA)
  - GPGN (GP:GN)
  - Substrate and SubsName (substrate identity)
- Experimental outputs
  - ActualFlux (CO2-C per g soil dry weight per day)
  - Basal24, Basal48, Basal168 (basal respired C at 24, 48, 168 h)
  - Subs24, Subs48, Subs168 (substrate-derived respired C at 24, 48, 168 h)
  - Prime24, Prime168 (primed SOM-derived respired C at 24 and 168 h)
- Isotopic and PLFA-derived data
  - BPLFA13C, FPLFA13C, GP13C, GN13C, Unspec13C (13C in PLFAs)
  - TotPLFA13C (total PLFA 13C)
  - PLFA_RESPC (carbon-use efficiency metric for PLFA 13C incorporation)
  - 13CPLFA_PC (percent 13C-labelled PLFA)
- Derived measures and corrections
  - δ13C values for CO2 and individual PLFAs
  - % substrate-derived C in CO2 (mixing model)
  - Primed C calculations (change in SOM utilization)
  - 13C incorporation into PLFAs (µg 13C g-1 soil dwt)
  - Microbial C-use efficiency (CUE)

## Study site and sampling design
- Ten sites along an elevation gradient on the east flank of the Peruvian Andes (210–3400 m asl).
- Forest types range from lowland Amazonian rainforest to upper montane cloud forest.
- Organic soil layer sampled from 5 sub-plots within each 1 ha plot per site.
- Samples stored at 4°C for subsequent laboratory analyses.

## Abiotic soil property analyses
- pH (soil:water)
- Gravimetric moisture content (105°C, 24 h)
- Bulk density
- Total C and N via CN analysis
- Maximum water holding capacity (WHC) calculated per elevation
- Soils homogenized and prepared for incubation and analyses

## Microbial assimilation and mineralisation experiments
- 10 soils incubated with four 13C-labelled substrates for 7 days: xylose, glycine, vanillin, hemicellulose.
- Substrates chosen to span labile to complex carbon, with varying C quality.
- Soils adjusted to 75% WHC; incubated at 20°C in the dark.
- Replicates: 5 soil replicates per substrate per elevation.
- Headspace CO2 sampled at 24, 48, and 168 hours; CO2 analysed for total flux and δ13C.

## Isotope and PLFA analyses
- CO2 quantified by GC-FID; δ13CO2 measured by IRMS after pre-concentration.
- PLFAs extracted and quantified by GC-MS; fungal (SP/ECM) and bacterial markers identified by specific FA signatures.
- δ13C values of PLFAs determined by GC-C-IRMS after derivatization corrections.
- Quality control includes blanks, standard references, and duplicate analyses; precision for δ13C ±0.2‰.

## Calculations and outputs
- Isotopic enrichment expressed as δ13C (‰) for CO2 and PLFAs.
- Substrate-derived CO2 calculated via mixing model using δ13C of treated vs. control CO2 and substrate δ13C.
- Primed C calculated as total respiration in treated soils minus control respiration minus substrate-derived respiration.
- 13C incorporation into PLFAs used to determine which microbial groups assimilated substrate carbon.
- Microbial C-use efficiency (CUE) computed as the ratio of 13C assimilated into total PLFAs to 13C respired.
- Data prepared for statistical analyses to test effects of substrate, soil properties, and time on carbon fluxes and microbial incorporation.

## Statistical analyses
- Analyses performed in R (version 2.14.0).
- Three-way ANOVA (substrate × soil × time) on cumulative substrate-derived C and primed C; data square-root transformed as needed.
- Tukey's HSD for post-hoc comparisons.
- Two-way ANOVA to assess effects of substrate and soil on microbial incorporation of 13C substrates (actual incorporation, relative 13C into microbial groups, and CUE).

## Data quality and QA
- Calibration of GC and IRMS with certified standards; daily instrument calibration.
- Blanks and QC standards run before batches; duplicate analyses after every 15 samples.
- Isotopic corrections for methanolysis during PLFA analyses.
- Exponential fits used to derive CO2 fluxes due to non-linearity in treated soils.

## Applications for environmental monitoring and analysis
- Enables consistent assessment of carbon release in tropical soils across environmental gradients.
- Links abiotic soil properties and microbial community composition to carbon processing under different substrate inputs.
- Provides a framework for comparing priming effects and microbial substrate use across sites and studies.
- Supports data integration and synthesis with standardized metadata and analytical workflows.

## Data provenance and availability
- Data sources: Maximum Prime study by Whitaker et al., 2014; field sampling in January 2012; lab analyses detailed in the methods.
- Datasets mentioned: 13C_Peru_fluxes.csv, 13C_Peru_soils.csv, 13C_PLFA_incorporation.csv.
- Metadata describe measurements, units, data processing, and calculation methods to ensure reproducibility and cross-study comparability.