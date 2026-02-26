# Soil sampling

## Overview
- Six soil samples per site were collected using a 4 cm width augur, aiming for 10 cm depth where possible.
- Samples were sieved through a 2 mm aperture to remove stones/roots.
- Samples were stored at 5 °C until processing.

## Sample preparation and storage
- Bulk density (BD) measured from two cores per site, at 0–5 cm and 5–10 cm depths; samples dried at 80 °C for 48 h after sieving; BD calculated as mass/volume.
- For all analyses, samples were prepared following specific extraction protocols (see respective sections).

## Bulk density
- Two cores per site used for BD; defined depth intervals 0–5 cm and 5–10 cm.
- Dried at 80 °C for 48 h post-sieving.
- BD computed from measured mass and known volume.

## Volumetric moisture content
- From each sample, 5 ± 0.001 g of fresh soil were weighed.
- Dried at 80 °C for 48 h; post-drying weight recorded.
- Moisture content calculated as proportion of wet weight.

## Water extractable nitrogen and carbon (N and C)
- 5 g fresh soil mixed with 25 ml Milli-Q water; shaken at 150 rpm for 1 h.
- Filtrate filtered through Whatman No. 1 paper.
- Undiluted filtrate analyzed for DIN (NH4+, NO3-, total N) via autoanalyser and for DOC via TOC analyzer.
- Concentrations adjusted to soil moisture using:
  DIN or DOC mg/kg = (raw value × [water content + extract volume] × dilution factor) / dry soil mass.

## KCl extractable nitrogen and potential mineralisation
- 5 g soil with 25 ml 1 M KCl; shaken 1 h; filtered.
- Filtrate diluted 2:1 and analyzed for DIN (NH4+, NO3-) via autoanalyser.
- Moisture-adjusted DIN mg/kg calculated similarly to water extractable N.
- Additional 5 g soil placed in extraction bottles, covered, and incubated at 25 °C for 14 days.
- Post-incubation extracts analyzed as above.
- Mineralisation calculated as: (NO3 + NH4) × BD ÷ number of days → g m^-2 day^-1.

## Microbial biomass
- Fumigation-extraction: 5 g soil placed in a desiccator with chloroform to lyse cells for 24 h.
- A second 5 g soil sample served as unfumigated control.
- After fumigation, nutrients extracted with 25 ml 0.5 M K2SO4; shaken 30 min and filtered.
- Filtrate analyzed at 4:1 dilution (fumigated) and 2:1 (unfumigated) for DIN and extractable PO4; dissolved carbon measured by TOC at same dilutions.
- Values adjusted for water content; corrected for extraction efficiency using KE_C = 0.35 and KE_N = 0.54.

## Data calculations and standardization
- All calculations include moisture corrections and, where applicable, dilution factors.
- Outputs include bulk density (mass/volume), volumetric moisture content (dimensionless), water-extractable DIN/DOC (mg/kg), KCl-extractable DIN and mineralisation (mg/kg and g m^-2 d^-1), and microbial biomass indicators (DIN, PO4, DOC with fumigation correction).

## Relevance for GIS and data products
- The dataset provides site- and depth-specific soil properties suitable for map-based visualization (BD, moisture, N and C pools, mineralisation rates, microbial biomass).
- Standardized protocols enable cross-site comparability and integration into GIS layers for policy, client, or public-facing maps.
- Clear unit definitions and correction factors (e.g., moisture adjustments, extraction efficiency corrections) support reproducible data products and reliable spatial analyses.