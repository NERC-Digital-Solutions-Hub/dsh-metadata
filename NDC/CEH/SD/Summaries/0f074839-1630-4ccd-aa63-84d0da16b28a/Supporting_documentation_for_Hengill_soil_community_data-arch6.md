# Invertebrate biomass, vegetation cover, and environmental data from Hengill, Iceland.

## Overview
- Dataset combining environmental conditions, vegetation cover, invertebrate abundance, and invertebrate body mass from 96 soil habitat patches in the Hengill geothermal valley, Iceland.
- Sampling along a natural soil temperature gradient of 7–38 °C, with patches close in proximity (within 2 km) and generally similar soil moisture, pH, total carbon, and total nitrogen.
- Patches were collected in July 2013 across three patches on each bank of 16 geothermally heated streams, providing a broad context for studying temperature effects on communities.
- Related analyses on temperature effects and community structure are documented in linked publications (e.g., Robinson et al. 2018).

## Sampling regime and collection methods
- Soil temperature: monitored at each patch with Maxim iButton DS1921G loggers buried 10 cm deep; measurements every 10 minutes over a 48-hour period.
- Soil moisture and pH: measured at each patch using an Imko TRIME-TDR moisture probe; soil cores collected for carbon and nitrogen analyses (CN analyzer).
- Soil carbon and nitrogen: five soil cores (1.5 × 5 cm) taken around 10 cm depth, dried at 60 °C for 96 hours, milled, and analyzed for total carbon and total nitrogen.
- Vegetation survey: 0.5 × 0.5 m quadrats per patch; photographed and analyzed for percentage cover using a nine-class system (0–99% coverage). Vascular plants identified to species; grasses, mosses, lichens, and litter also recorded.
- Invertebrate sampling: five pitfall traps per patch (placed at corners and center of a 1 m² area), traps filled with ethylene glycol and stream water; left for 48 hours. Samples combined, stored in 70% ethanol, and identified to species where possible.
- Identification: invertebrates identified to species where feasible using a microscope; detailed methods described in Robinson et al. (2018).

## Data structure and files
- Four CSV files; each row represents one of the 96 habitat patches.
- Common header structure: first three columns identify patch by stream, bank, and patch number (1–3).
- hengill_environmental_data.csv
  - Columns 4–5: latitude and longitude (decimal degrees).
  - Column 6: mean soil temperature (°C) from iButtons.
  - Columns 7–8: total carbon (g kg⁻¹) and total nitrogen (g kg⁻¹).
  - Columns 9–10: moisture (%), pH.
- hengill_vegetation_cover.csv
  - Columns 4–38: names of non-plant groups quantified (e.g., grasses, mosses, lichens, litter) and plant species; data are percentage cover per patch.
- hengill_invertebrate_abundance.csv
  - Columns 4–82: names of invertebrate species quantified; data are total number of individuals per patch.
- hengill_invertebrate_mass.csv
  - Columns 4–82: same species names as abundance file; data are mean dry weight per species (mg) per patch.

## Content details by file
- Environmental data: geographic coords, soil temperature, soil carbon and nitrogen, moisture, and pH for each patch.
- Vegetation cover: percentage cover for non-plant groups and for plant species identified in the vegetation survey.
- Invertebrate abundance: counts of individuals per species per patch from pitfall traps.
- Invertebrate mass: mean dry weight per species per patch.

## Use cases and analyses
- Explore relationships between soil temperature gradient and community structure for plants and invertebrates.
- Link vegetation composition with invertebrate communities and soil geochemistry.
- Create self-serve data products (dashboards, pivot tables) to compare patches or to visualize spatial patterns across the thermal gradient.
- Integrate with related Hengill studies to examine broader ecological responses to natural warming.
- Meta-analyses or cross-study comparisons leveraging the standardized patch-based design.

## Notes on data quality and scope
- Snapshot data collection: temperature and other variables reflect measurements within a 48-hour window in July 2013.
- Patch-based design across 96 patches provides robust spatial replication within the thermal gradient, but temporal dynamics are not captured beyond the sampling period.
- Identification depth varies by taxon depending on specimen availability and identification feasibility.