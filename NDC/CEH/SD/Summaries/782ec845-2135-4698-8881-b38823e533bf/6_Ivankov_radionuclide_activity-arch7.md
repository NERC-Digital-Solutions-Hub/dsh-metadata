# Mapping the contamination of Ivankiv district territory with radionuclides

## Overview
- Data dictionary for radionuclide contamination measurements used to map Ivankiv district contamination.
- Includes sample weights, activity concentrations (per kg and per area), uncertainties, recoveries, and detection limits.
- Provides guidance for transforming measurements into map-ready GIS attributes and layers.
- References a final reporting document (2013–2014) underpinning the data.

## Data schema and fields (key variables)
- Weight-related fields:
  - Full_weight_kg: Total weight of soil samples; Notes indicate composite samples (5 samples by 37 mm corer to at least 20 cm depth).
  - Sample_weight_kg: Weight of the sample used for activity measurement.
- Activity concentration (per mass):
  - 137Cs_Bq_kg
  - 90Sr_Bq_kg
  - 40K_Bq_kg
  - 226Ra_Bq_kg
  - 232Th_Bq_kg
- Activity concentration (per area):
  - 137Cs_kBq_m2
  - 90Sr_kBq_m2
- Uncertainty and quality:
  - Relative_uncertainty_137Cs_%
  - Relative_uncertainty_90Sr_recovery_%
  - Relative_uncertainty_90Sr_%
  - Relative_uncertainty_40K_%
  - Relative_uncertainty_226Ra_%
  - Relative_uncertainty_232Th_%
  - Relative_uncertainty_137Cs_kBq_m2_%
  - Relative_uncertainty_90Sr_kBq_m2_%
  - Relative_uncertainty_226Ra_%, 95% CI
  - Relative_uncertainty_232Th_%, 95% CI
  - Relative_uncertainty_137Cs_kBq_m2_%, 95% CI
  - Relative_uncertainty_90Sr_kBq_m2_%, 95% CI
- Recovery and ratios:
  - Fraction_90Sr_recovered
  - Ratio_Cs:Sr, 95% CI
- Detection limits and nondetects:
  - Values indicated as "<" denote activity concentrations below minimum detectable activity (MDA) for the corresponding measurement.
- Identifiers:
  - Site identifier: Used to link measurements to specific locations or sampling sites.

## Measurements, units, and interpretation
- Weights: kilograms (kg) for sample totals and individual samples.
- Activity concentrations: bequerels per kilogram (Bq_kg) and kilobequerels per square metre (kBq_m2).
- Uncertainty: percentage terms representing the 95% confidence interval where specified.
- Non-detects: "<" values indicate censored data below the MDAs.
- Density of contamination: expressed as 137Cs_kBq_m2 and 90Sr_kBq_m2.

## Sampling and data quality notes
- Sampling detail: composite soil samples created from multiple sub-samples (example given: 5 samples by 37 mm corer) to a depth of at least 20 cm.
- Uncertainty and detection: multiple isotopes have associated relative uncertainties (often at 95% CI); some isotopes report 95% CI specifically for certain measurements (e.g., 226Ra, 232Th, 137Cs_kBq_m2, 90Sr_kBq_m2).
- Recovery: Fraction_90Sr_recovered provides an efficiency measure for strontium-90 recovery.

## Spatial data integration considerations for GIS
- Site identifiers enable linking measurements to spatial features (points or polygons) in a GIS.
- Both mass-based (Bq_kg) and area-based (kBq_m2) measurements support different map visualizations (e.g., per-site contamination vs. surface density).
- Handling censored data ("< MDA") is required when creating continuous surfaces or performing interpolation.
- Uncertainty fields can be used to create confidence ribbons, error surfaces, or to weight analyses.
- Ratio_Cs:Sr offers a comparative map of Cs to Sr contamination across sites.

## Data provenance and reference
- Source: Kashparov, V. A. et al. Mapping the contamination of Ivankiv district territory with radionuclides. Final report, November 2013–September 2014, UIAR, contract No.2013-04.
- Data framed to support GIS-based mapping and visualization of radionuclide contamination.

## Practical guidance for GIS specialists
- Import and join datasets by Site identifier to appropriate spatial geometries.
- Choose visualization scales:
  - Color by 137Cs_Bq_kg, 90Sr_Bq_kg, 40K_Bq_kg, etc., or by 137Cs_kBq_m2 and 90Sr_kBq_m2 for density maps.
  - Create separate layers or bundled symbology for mass-based vs. area-based measurements.
- Represent uncertainties:
  - Include Relative_uncertainty fields as overlays or as uncertainty buffers.
  - Consider creating an accompanying uncertainty layer or using graduated symbols with error bounds.
- Handle nondetects:
  - Use censoring-aware methods or flag those sites for special treatment in interpolation.
- Analyze ratios:
  - Generate a Ratio_Cs:Sr layer to highlight spatial variation in Cs vs. Sr contamination.
- Documentation:
  - Tag fields with units, notes (e.g., sampling depth, composite sample details), and detection-limit handling for reproducibility.
- Quality and reproducibility:
  - Reference the original report for methodological context when documenting map products and data usage.