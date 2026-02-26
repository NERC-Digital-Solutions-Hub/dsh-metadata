# Invertebrate biomass, vegetation cover, and environmental data from Hengill, Iceland.

## Overview
- A dataset of environmental measurements (soil temperature, moisture, pH, total carbon and nitrogen), vegetation cover, and invertebrate abundance and mean body mass collected from 96 soil habitat patches in the Hengill geothermal valley, Iceland, in July 2013.
- Patches span a soil temperature gradient of 7–38 °C, are within 2 km of each other, and share similar soil moisture, pH, carbon, and nitrogen.
- Linked to a series of ecological studies (e.g., analyses of temperature effects on plant and invertebrate communities).

## Sampling regime and collection methods
- Temperature: soil temperature monitored at each patch with Maxim DS1921G iButton loggers buried 10 cm below the surface; readings every 10 minutes over 48 hours.
- Soil properties: five soil cores (1.5 × 5 cm) per patch from ~10 cm depth; soils dried at 60 °C for 96 hours, milled; total carbon and nitrogen measured with a CN analyser (Flash 1112).
- Vegetation survey: 0.5 × 0.5 m quadrats per patch; random placement; photos analyzed for species cover using a hierarchical class system (0–99% cover classes). Plants identified to species where possible; grasses, mosses, lichens, and litter recorded as a separate group.
- Invertebrates: five pitfall traps per patch (one per corner and one center) with ethylene glycol and stream water; exposed for 48 hours; contents combined per patch, sieved (250 μm), stored in 70% ethanol; specimens identified to species where possible.

## Data structure and files
- Four CSV files, each row representing one of the 96 habitat patches:
  - hengill_environmental_data.csv
  - hengill_vegetation_cover.csv
  - hengill_invertebrate_abundance.csv
  - hengill_invertebrate_mass.csv
- Common first three columns in all files: 
  - stream (identifier linked to prior Hengill stream publications)
  - bank (left or right at the stream confluence, looking upstream)
  - patch (1–3, with 1 closest to the river)
- Additional columns by file:
  - Environmental data: latitude, longitude, temperature (°C), total_carbon (g/kg), total_nitrogen (g/kg), moisture (%), pH.
  - Vegetation cover: non-plant group names (e.g., grasses, mosses, lichens, litter) and plant species names; values are percentage cover.
  - Invertebrate abundance: columns for invertebrate species; values are total counts per patch.
  - Invertebrate mass: columns for invertebrate species; values are mean dry weight (mg) per patch.
- Units:
  - Temperature in °C; total_carbon and total_nitrogen in g/kg; moisture in %; pH as a unitless scale; abundance as counts; body mass as mg.

## Variables, data quality, and provenance
- Data collected with explicit instrumentation and protocols (iButtons for temperature, CN analyser for carbon/nitrogen, standard soil moisture probe, fixed quadrats, and standardized pitfall trapping).
- Geographic coordinates provide patch-level location context; dataset references previous Hengill studies for cross-comparison.
- Detailed description of column positions (1, 2, 3 …) and field definitions facilitates reproducibility and data integration.

## Usage and interpretation
- Suitable for examining links between soil temperature gradients and community structure across plants and invertebrates, including size structure and biodiversity responses.
- Associated with multiple publications (e.g., Robinson et al. 2018; other listed references) that investigate temperature effects on habitat communities and ecosystem processes.

## Data governance and management considerations for Data Stewards
- Metadata and documentation:
  - Ensure a complete data dictionary with definitions, units, and acceptable value ranges.
  - Maintain linkage to original publications and instrument methods for traceability.
- Data sharing and deposition:
  - Assign persistent identifiers (e.g., DOI) and publish in appropriate data portals; document licensing and usage rights.
  - Prepare versioned releases and an update plan if future sampling occurs.
- Data quality and interoperability:
  - Standardize naming conventions for streams, banks, patches, and species to enable cross-study integration.
  - Validate geospatial coordinates and unit consistency across files; handle any missing or ambiguous values transparently.
- Provenance and lineage:
  - Record sampling date (July 2013), methods, and any data transformations (e.g., how abundances were aggregated per patch).
- Accessibility and reuse:
  - Provide clear citation guidance and linkages to related datasets and publications to support secondary analyses.

## Related publications and context
- Linked to a body of work examining temperature effects on community structure and ecosystem function in natural warming experiments and geothermal streams (e.g., Robinson et al. 2018; Adams et al. 2013; O’Gorman et al. 2016, 2017, 2012; Woodward et al. 2010; and others).