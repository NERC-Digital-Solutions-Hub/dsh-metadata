# Soil sampling

- This document outlines field sampling and laboratory analyses to quantify soil properties for GIS-based data products and map-ready datasets.

## Sampling design and collection

- Six soil samples per site collected with a 4 cm width auger to a depth of 10 cm where possible.
- Samples passed through a 2 mm sieve to remove stones and roots.
- Soils stored at 5 °C until processing.

## Bulk density

- Bulk density measured from two cores per site at depths 0–5 cm and 5–10 cm.
- Cores dried at 80 °C for 48 hours after sieving; weight recorded.
- Bulk density calculated as mass/volume.

## pH

- pH determined by mixing 5 g fresh soil with Milli-Q water in a 1:1 ratio.
- Measurement performed with a Mettler Toledo FE20 pH meter (LE409 probe).

## Volumetric moisture content

- 5 ± 0.001 g of fresh soil per sample dried at 80 °C for 48 hours.
- Post-drying weight recorded; moisture content calculated as a proportion of the wet weight.

## KCl extractable N and potential mineralisation

- 5 g fresh soil mixed with 25 ml of 1 M KCl; shaken at 150 rpm for 1 hour.
- Solution filtered (Whatman No. 1); filtrate diluted 2:1 and analyzed for DIN (NH4 and NO3) via autoanalyser.
- A second 5 g soil sample incubated in 25 ml of 1 M KCl at 25 °C for 14 days; extraction and analysis performed as above.
- Mineralisation calculated as (NO3 + NH4) × bulk density ÷ days (g m^-2 day^-1).

## Microbial biomass

- 5 g fresh soil fumigated with chloroform in a desiccator for 24 hours; a separate unfumigated control sample is kept.
- After fumigation, nutrients extracted with 25 ml 0.5 M K2SO4, shaken at 150 rpm for 30 minutes; filtered.
- Extracts analysed for DIN, PO4; dissolved carbon measured with TOC-L at corresponding dilutions.
- Values adjusted for water content; extraction efficiency corrected using KE_C = 0.35 and KE_N_E = 0.54.

## Particle size

- Particle size distribution determined by sequential sieving through >3 mm, 2 mm, 0.05 mm, 0.015 mm, and >0.015 mm fractions.

## GIS-relevant outputs and considerations

- Mappable variables (with typical units):
  - Bulk density for 0–5 cm and 5–10 cm depths (mass per volume)
  - pH (unitless, standard pH)
  - Volumetric moisture content (proportion of water per volume)
  - DIN (mg/kg) from KCl extracts
  - Mineralisation rate (g m^-2 day^-1)
  - Microbial biomass indicators (DIN, PO4, dissolved carbon)
  - Organic carbon (via TOC)
  - Particle size fractions (percent by size class)
- Key notes:
  - Calculations and units follow specified formulas (e.g., DIN mg/kg, mineralisation rate).
  - Data are collected per site with depth resolution for BD and moisture.
  - QA considerations include consistent sample handling, calibration, and extraction efficiency corrections for biomass estimates.