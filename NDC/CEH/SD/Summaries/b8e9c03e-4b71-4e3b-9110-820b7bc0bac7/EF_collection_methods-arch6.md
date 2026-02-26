# Soil sampling

- Six soil samples were taken per site using a 4 cm width augur, to a depth of 10 cm where possible.
- Samples were sieved (2 mm aperture) to remove stones and roots.
- Stored at 5 °C until ready for processing.

## Sampling and measurement plan

- Bulk density (BD):
  - From two cores per site, split into 0–5 cm and 5–10 cm depths.
  - Dried at 80 °C for 48 hours after sieving.
  - Weighed to calculate BD as mass/volume.

- pH:
  - 5 g fresh soil mixed with Milli-Q water in a 1:1 ratio.
  - Measured with a Mettler Toledo FE20 pH meter (LE409 probe).

- Volumetric moisture content:
  - 5.0 ± 0.001 g fresh soil per sample dried at 80 °C for 48 hours.
  - Post-drying weight used to calculate moisture content as a proportion of the wet weight.

## Chemical and microbial analyses

- KCl extractable N and potential mineralisation:
  - 5 g fresh soil with 25 mL of 1 M KCl, shaken at 150 rpm for 1 hour.
  - Filtrate filtered (Whatman No. 1), diluted 2:1, analysed for DIN (NH4+ and NO3−) by autoanalyser.
  - A second 5 g soil sample incubated at 25 °C for 14 days; extracted and analysed as above.
  - Mineralisation calculated as (NO3 + NH4) × bulk density ÷ number of days (g m⁻² day⁻¹).
  - DIN adjusted to soil moisture using:
    DIN mg/kg = (raw AA value × (water content of sample + extract vol) × dilution factor) / dry weight of soil.

- Microbial biomass (fumigation-extraction):
  - 5 g soil fumigated with chloroform in a desiccator for 24 h to lyse microbes.
  - A parallel unfumigated 5 g sample processed as control.
  - Nutrients extracted with 25 mL 0.5 M K₂SO₄, shaken, filtered.
  - Extracts analysed (DIN and extractable PO₄) at appropriate dilutions (4:1 for fumigated, 2:1 for unfumigated) on autoanalyser.
  - Dissolved organic carbon measured via TOC-L at the same dilutions.
  - Values adjusted for water content; recovery corrections applied using KE_C (0.35) and KE_N (0.54) to adjust extraction efficiency.

- Particle size:
  - Soil passed through sieves >3 mm, 2 mm, 0.05 mm, 0.015 mm, and >0.015 mm to determine size distribution.

## Data outputs and key variables

- Extractable nitrogen and mineralisation metrics (DIN in mg/kg; mineralisation rate in g m⁻² day⁻¹).
- pH (unitless; measured in water as 1:1 suspension).
- Bulk density (g cm⁻³) by depth (0–5 cm, 5–10 cm).
- Volumetric moisture content (dimensionless fraction).
- Microbial biomass indicators:
  - DIN and extractable PO₄ from fumigated and unfumigated samples.
  - Dissolved carbon (TOC).
  - KE-adjusted microbial biomass estimates (C and N components).
- Particle size distribution across defined fractions.

## Data quality, standardization and reuse

- Use consistent units across sites (e.g., DIN in mg/kg, mineralisation in g m⁻² day⁻¹).
- Document site, depth interval, date, and any deviations from protocol.
- Apply moisture adjustments and extraction efficiency corrections as specified to enable cross-site comparisons.
- Outputs suitable for dashboarding and self-serve analysis (e.g., comparing N mineralisation, microbial biomass, pH, BD, moisture across sites and depths).

## Potential data products and end-user applications

- Dashboards or pivot tables summarizing site- and depth-specific soil properties (BD, pH, moisture, N forms, mineralisation, microbial biomass, PO₄, TOC).
- Comparative reports across sites to identify patterns in mineralisation rates and microbial activity.
- Maps or spatial summaries if site coordinates are available, illustrating variability in soil properties.
- Data dictionaries and metadata to support reuse by non-specialists and other teams (e.g., councils or private organizations).