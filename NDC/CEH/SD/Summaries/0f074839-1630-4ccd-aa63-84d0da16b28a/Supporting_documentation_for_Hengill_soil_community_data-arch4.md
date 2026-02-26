# Invertebrate biomass, vegetation cover, and environmental data from Hengill, Iceland.

## Overview
- A dataset of environmental variables, vegetation cover, total invertebrate abundance, and mean invertebrate body mass.
- Collected from 96 soil habitat patches in the Hengill geothermal valley, Iceland.
- Sampling occurred in July 2013 along a soil temperature gradient of 7–38 °C; patches are near each other with similar moisture, pH, carbon, and nitrogen.

## Sampling regime and collection methods
- 96 habitat patches were sampled (3 patches per bank of 16 geothermally heated streams).
- Soil temperature: measured at each patch using iButton loggers buried 10 cm deep; readings every 10 minutes over 48 hours.
- Soil moisture: measured with a soil moisture probe (Imko TRIME-TDR) at each patch.
- Soil chemistry: five cores per patch (about 10 cm depth) were dried and milled; total carbon and total nitrogen measured by CN analyser after drying.
- Vegetation survey: 0.5 × 0.5 m quadrats randomly placed at each patch; photos analyzed for percentage cover using defined classes; vascular plants identified to species; grasses, mosses, lichens, and litter recorded as well.
- Invertebrate sampling: five pitfall traps per patch arranged around a 1 m^2 area; traps contained ethylene glycol and stream water, left for 48 hours; samples combined, stored in ethanol; terrestrial invertebrates identified to species where possible.

## Data structure and file descriptions
- Data are provided in four CSV files; each row represents one of the 96 habitat patches.
- Common first three columns across files: 
  - 1) stream identifier
  - 2) bank (left or right)
  - 3) patch number (1–3)
- hengill_environmental_data.csv
  - 4-5: latitude, longitude (GPS coordinates)
  - 6: temperature (mean soil temperature in °C)
  - 7-8: total_carbon, total_nitrogen (g kg^-1)
  - 9-10: moisture (%), pH
- hengill_vegetation_cover.csv
  - 4-38: names of non-plant groups and plant species; values are percentage cover
- hengill_invertebrate_abundance.csv
  - 4-82: invertebrate species names; values are total individuals per patch
- hengill_invertebrate_mass.csv
  - 4-82: invertebrate species names; values are mean dry body mass (mg) per patch

## Data quality, provenance, and context
- Methods and structure are documented to facilitate reproducibility and cross-study comparability.
- The dataset underpins analyses of how soil temperature and other abiotic factors shape plant and invertebrate communities; related findings are reported in Robinson et al. (2018) and other cited works.
- Data are structured for straightforward integration with other Hengill studies, supporting meta-analyses across gradients and time.

## References and context
- Data collection and context linked to numerous publications exploring temperature effects, community structure, and ecological responses in geothermal streams and surrounding environments (e.g., Adams et al., Demars et al., Friberg et al., O’Gorman et al., Woodward et al.; Robinson et al. 2018).

## Relevance for Data Leaders
- Demonstrates a well-documented, multi-taxa ecological dataset with clear metadata, enabling system-wide data governance and integration.
- Provides high-value, gridded patch-level data with precise geolocation, facilitating discoverability, reuse, and cross-team collaboration.
- Illustrates the importance of standardized data structure (consistent patch-level rows, explicit column definitions) to support data quality, metadata discoverability, and updates.
- Highlights potential for cross-network collaboration through shared datasets and referenced publications, aligning with goals of coherent data ecosystems, user-oriented product development, and community of practice growth.