# Metadata for data associated with dataset 'Measurements of carbon cycling processes in tropical forest soils varying in soil abiotic and biotic properties' (13C_Peru_fluxes.csv, 13C_Peru_soils.csv and 13C_PLFA_incorporation.csv)

## Overview
- Describes metadata and methods for a dataset examining how soil abiotic and biotic properties influence microbial processing of carbon inputs in tropical forest soils.
- Data files cover soil properties, CO2 fluxes and 13C labeling, and PLFA-based microbial assimilation (13C-PLFA) across a elevation gradient.

## Study site and field sampling
- Ten sites along a tropical elevation transect on the east flank of the Peruvian Andes, 210–3400 m above sea level.
- Forest cover ranges from lowland Amazonian to upper montane cloud forest; mean annual temperature decreases with elevation; annual precipitation 1700–3200 mm.
- At each site, organic soil was sampled from five sub-plots within established 1 ha plots; organic layer removed, soils stored at 4°C for up to 6 weeks before experiments.

## Data files and variables
- 13C_Peru_fluxes.csv and 13C_Peru_soils.csv contain:
  - Elevation, Replicate
  - Abiotic soil properties: pH, TotC, TotN, C:N, BulkDensity
  - Microbial/biomarker variables: totPLFA, FPLFA, BPLFA, FB, GP, GN, GPGN
  - Substrate identifiers: Substrate, SubsName
  - Respiration metrics: ActualFlux, Basal24/48/168 (basal respiration at 24, 48, 168 h)
  - Substrate-derived respiration: Subs24/48/168
  - Priming metrics: Prime24, Prime168 (and related primed SOM-derived respiration)
  - Isotopic/plFA related: 13CPLFA_PC and various 13C-weighted PLFA fields
- 13C_PLFA_incorporation.csv (implied by the metadata) provides data on 13C incorporation into PLFAs, including:
  - 13C-labeled PLFA measurements for bacterial and fungal markers
  - Primed SOM-derived 13C respired in PLFAs (e.g., FPLFA13C, GP13C, GN13C, Unspec13C, TotPLFA13C)
  - Calculations of carbon-use efficiency (CUE) from 13C assimilation vs respiration
- Substrates:
  - Substrate codes: 1=control, 2=xylose, 3=glycine, 4=vanillin, 5=hemicellulose
  - SubsName provides substrate names
- Measurements:
  - CO2-C flux (µg g-1 soil dwt day-1)
  - Substrate-derived CO2 and priming values over time
  - PLFA concentrations and taxonomic markers; Fungal:Bacterial (F:B) and GP:GN ratios
  - δ13C values for CO2 and PLFAs

## Experimental design
- Soils incubated with four 13C-labelled substrates plus control, across 10 sites.
- Each site contributed five subplots treated as independent replicates (total 50 incubations per substrate/time point).
- Soils adjusted to 75% of maximum water-holding capacity; substrates added to a final carbon concentration of 0.2 mg C g-1 soil.
- Headspace flushed, bottles sealed and over-pressurized; incubated at 20°C in the dark for 7 days.
- Headspace sampling for 13CO2 and CO2 at 24, 48, and 168 hours; soils frozen for PLFA and δ13C analyses.

## Analytical methods
- CO2 and 13CO2 analyses:
  - CO2 quantified by gas chromatography with a flame ionization detector after methanation; calibration with standards; CO2 flux reported as CO2-C.
  - δ13C of CO2 measured with isotope ratio mass spectrometry (IRMS) after pre-concentration; daily calibrations and QC were performed.
- PLFA analysis:
  - Phospholipid fatty acids extracted from soils; identified by GC-MS; concentrations calculated with internal standard.
  - Biomarkers used to designate microbial groups: GP bacteria (specific branched fatty acids), GN bacteria (specified markers), SP/ECM fungi (18:2ω6,9 and 18:1ω9); total PLFA computed from identified PLFAs.
  - F:B and GP:GN ratios used as indicators of microbial community structure.
  - δ13C values for individual PLFAs determined by GC-C-IRMS on selected elevations; methylation corrections applied.
- Isotopic calculations:
  - Enrichment expressed as δ13C (per mille); substrate-derived CO2 calculated using a mixing model: % Csubstrate-derived = [(δC − δT) / (δC − δL)] × 100.
  - Primed C: difference between treated and control respiration minus substrate-derived respiration.
  - 13C incorporation into PLFAs used to quantify actual assimilation into fungi, GP, GN, and total PLFAs; CUE computed as assimilated 13C in PLFAs divided by respired 13C.

## Calculations and metrics
- 13CO2 and PLFA enrichment calculations to determine substrate-derived respiration and incorporation.
- Priming effects quantified (Primed C) as a measure of priming by substrate addition on SOM respiration.
- 13C-PLFA calculated for key microbial groups (fungi, GP bacteria, GN bacteria, unspecific PLFAs) and total PLFA.
- Carbon-use efficiency (CUE) derived from the ratio of carbon incorporated into PLFAs (13C assimilated) to carbon respired (13C).

## Statistical analysis
- All analyses performed in R (version 2.14.0).
- Primary questions addressed with three-way ANOVA to test effects of substrate, soil (elevation/abiotic/biotic properties), and time on cumulative substrate-derived C and primed C (and their ratio).
- Data transformations: square-root transform (with constant added for primed C).
- Post-hoc: Tukey HSD for pairwise comparisons within interactions.
- For microbial incorporation: two-way ANOVA examining substrate and soil effects on 13C incorporation into PLFAs, including proportions into fungi, GP, GN, and overall CUE.

## Data quality and provenance
- Standardized field and lab protocols described; calibration, blanks, and QC measures noted for isotopic analyses.
- Replicates, substrate treatments, and time points designed to link microbial community composition, substrate quality, and soil properties to carbon flux and priming responses.
- Data and analyses facilitate understanding of how microbial community structure and substrate inputs govern tropical soils’ carbon release dynamics along an elevation gradient.

## References (context for methods and interpretations)
- Whitaker et al., 2014; and multiple foundational references on PLFA biomarkers, stable isotope techniques, soil carbon analyses, and statistical approaches cited throughout the metadata.