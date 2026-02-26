# Invertebrate biomass, vegetation cover, and environmental data from Hengill, Iceland.

## Overview
- A dataset combining environmental variables, vegetation cover, invertebrate abundance, and invertebrate body mass.
- Collected from 96 soil habitat patches in the Hengill geothermal valley, Iceland, in July 2013.
- Covers a natural soil temperature gradient of 7–38 °C, with patches closely spaced (within 2 km) and similar soil moisture, pH, total carbon, and total nitrogen.
- Focuses on linking soil temperature and other abiotic factors to plant and invertebrate community structure and diversity.
- Related analyses include studies on temperature effects and community size structure (e.g., Robinson et al. 2018).

## Study design and sampling regime
- 96 habitat patches sampled across 16 geothermally heated streams, with three patches per bank (left/right) per stream.
- Temperature gradient established by geothermal influence; mean soil temperature measured per patch.
- Soil conditions (moisture, pH, total carbon, total nitrogen) and vegetation were surveyed to characterize habitat context.
- Invertebrate communities assessed via pitfall traps at each patch.

## Data collection methods (environmental and biological)
- Soil temperature: Maxim Integrated DS1921G Thermocron iButtons buried 10 cm deep; readings every 10 minutes over 48 hours in July 2013.
- Soil moisture: Imko TRIME-TDR soil moisture probe used at each patch.
- Soil chemistry: Five 1.5 × 5 cm cores from ~10 cm depth; soils dried at 60 °C for 96 hours, milled; total carbon and total nitrogen measured with a CN analyser.
- Vegetation survey: 0.5 × 0.5 m quadrats placed randomly at each patch; photographs analyzed for percentage cover using a 9-class scale (0–99% steps); vascular plants identified to species where possible; non-plant groups (grasses, mosses, lichens, litter) quantified.
- Invertebrates: Five pitfall traps per patch (arranged at corners and center of a 1 m² area); traps filled with ethylene glycol and stream water; left for 48 hours; contents combined, sieved (250 μm), and preserved in 70% ethanol; identification to species level where possible with microscopy.

## Data structure and files
- Data are provided in four CSV files; each row corresponds to one of the 96 habitat patches.
- Common first three columns across files:
  - 1) Stream identifier (links to prior Hengill stream publications)
  - 2) Bank (left or right at the stream confluence)
  - 3) Patch number (1–3, closest to the river to farthest)
- File-specific columns:
  - hengill_environmental_data.csv
    - Columns 4–5: latitude and longitude (decimal GPS)
    - Column 6: mean soil temperature (°C)
    - Columns 7–8: total carbon (g kg⁻¹) and total nitrogen (g kg⁻¹)
    - Columns 9–10: soil moisture (%) and pH
  - hengill_vegetation_cover.csv
    - Columns 4–38: names of non-plant groups (grasses, mosses, lichens, litter) and plant species; percent cover values
  - hengill_invertebrate_abundance.csv
    - Columns 4–82: names of invertebrate species; values are total number of individuals per patch
  - hengill_invertebrate_mass.csv
    - Columns 4–82: same species as abundance; values are mean dry body mass (mg) per species per patch

## Measurements and instrumentation details
- Temperature loggers: iButtons deployed at 10 cm depth; 48-hour monitoring with 10-minute intervals.
- Soil moisture: TRIME-TDR probe for each habitat patch.
- Soil chemistry: CN analyser used for carbon and nitrogen content after drying and milling.
- Vegetation: photographic survey with quadrats; cover estimated via standardized classes.
- Invertebrates: standardized pitfall traps with ethylene glycol preservation; 48-hour sampling window; identification with microscopy.

## Data quality and context
- Data derived from a structured, repeatable monitoring regime consistent with established studies in the Hengill system.
- Linked to a body of work on temperature effects and community structure in geothermal streams (e.g., Robinson et al. 2018; O’Gorman et al. various; Friberg et al. references).
- Dataset design supports cross-patch comparisons and integration with broader environmental monitoring efforts.

## Relevance for Analysts Monitoring the Environment
- Provides standardized, multi-factor measurements across a natural thermal gradient suitable for assessing environmental health and climate-related ecological responses.
- Enables analyses of links between abiotic conditions (temperature, moisture, soil chemistry) and biotic communities (plants and invertebrates) at fine spatial scales.
- The file structure facilitates data aggregation, temporal comparisons (with related studies), and integration with other environmental datasets for enhanced monitoring and policy-relevant assessments.