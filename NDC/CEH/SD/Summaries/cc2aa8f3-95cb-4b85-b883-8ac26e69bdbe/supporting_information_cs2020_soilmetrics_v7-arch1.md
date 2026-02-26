# UKCEH Countryside Survey data 2020

## Overview
- Countryside Survey is a long-running UK-wide study of countryside natural resources, with rolling sampling since 2019 to monitor soil condition and function and how multiple pressures interact.
- The program provides data and maps on soil condition, enabling analysis of trends in soil health, carbon, pH, nutrient status, and vegetation interactions.
- The dataset described focuses on soils and associated vegetation metrics collected on a national scale, with a framework designed for cross-year comparability.

## Survey design and rolling program
- Rolling survey adopted: repeat every five years or after 500 squares completed, to detect changes while buffering against climate year-to-year variation.
- Sample frame: 500 x 1km squares across Great Britain, stratified by the Land Classification of Great Britain; 100 squares visited annually.
- Exclusions: squares with >75% urban land or >90% sea are excluded.
- The design continues the lineage of earlier Countryside Surveys (1978, 1998, 2007) to enable long-term comparisons.

## Covid disruption 2020
- The 2020 field season was disrupted (May–June), with some rescheduling in July–August.
- Result: 50 squares were reselected from England only to complete the rolling cycle.

## Sample collection and site details
- Within each survey area, soil samples are collected from 5 randomly dispersed locations coincident with vegetation plots, using a 15 cm C-core (top 0–15 cm).
- Historical positioning: markers and coordinates were used to relocate sampling sites across survey years; plots have shifted slightly over time for consistency.
- Soil samples are refrigerated and sent to laboratories for analysis.

## Metrics, laboratory protocols and analytical methods
- Field and laboratory methods are standardized and documented (field manual referenced).
- Core soil metrics include:
  - Soil pH: measured in deionised water and in 0.01 M CaCl2 (1:2.5 soil-to-solution ratio). Quality control uses internal standards and duplicates.
  - Electrical conductivity (EC): measured on soil slurry after a set equilibration.
  - Loss on Ignition (LOI) and derived carbon: measured via thermogravimetric analysis (TGA) to estimate soil organic matter, hygroscopic water content, and CaCO3; carbon concentration derived from LOI with a regression-based conversion to %C.
  - Bulk density, stones, and porosity: calculated from core weights, stone mass, and volumes; porosity derived from bulk and particle densities.
  - Water content metrics: volumetric and gravimetric water contents computed from bulk density and gravimetric moisture data.
  - Olsen-phosphorus (Olsen-P): soil extraction with NaHCO3 and colorimetric analysis; quality control includes standards and blanks.
  - Total phosphorus (TP): H2O2/H2SO4 digestion followed by colorimetric analysis.
  - Total soil organic carbon (SOC) and nitrogen: after inorganic carbon removal, C and N are measured by elemental analysis; QA uses in-house references and calibration standards.
- Data quality control includes internal standards, duplicates (roughly 10%), blanks, and specific recovery checks for CaCO3 and LOI.
- Detailed data management and calculation notes cover multiple derived fields (e.g., carbon concentration from LOI, units conversions, and stock calculations).

## Data structure and annual analyses
- Data structure: fields include SQ_ID (1km survey square), PLOT_ID (plot within square), land classification, habitat descriptors, year, depth-related metrics, and a broad set of soil metrics (pH, EC, LOI, C, N, P, bulk density, porosity, etc.), with -9999 indicating missing samples.
- Longitudinal analysis: rolling program contributes annual updates; historical comparisons (LOI, pH in water) are used to illustrate soil change over time.
- UKCEH Countryside Survey data 2020 Summary Figures highlight relationships such as:
  - Porosity vs. LOI
  - Porosity vs. LOI on a log scale
  - Bulk density vs. LOI
  - pH (water) vs. LOI
  - pH (CaCl2) vs. LOI
  - EC vs. LOI
  - Calcite vs. LOI
  - LOI vs. gravimetric volumetric water content
  - LOI vs. porosity distributions
- Figures are designed to convey patterns across depth classes (e.g., non-peat vs. peat categories) and to illustrate the distribution of LOI and key soil properties over time.

## Data access, provenance and management
- The program emphasizes tracking data sources, standardization, and making datasets discoverable with metadata.
- Data are collected, processed, and archived under CEH/UKCEH governance, with named staff roles for field collection, laboratory analysis, data management, rolling program design, and analysis.

## Practical implications for analysis
- The dataset supports analyses of how soil condition and function respond to multiple pressures (e.g., land use, deposition, climate).
- Researchers can examine changes in soil carbon pools, pH trends, phosphorus dynamics, compaction signals, and topsoil carbon-nitrogen dynamics across habitats and over time.
- The data structure supports cross-year comparisons, stratification by land class, and derivation of soil stock metrics (e.g., carbon stocks per hectare) with clear unit conventions.

## References and further reading
- Extensive citations to foundational Countryside Survey reports, methods, and related soil science literature, including Emmett et al. (2010), Reynolds et al. (2013), Scott (2008), Ruehlmann (2020), and related UKCEH documentation.