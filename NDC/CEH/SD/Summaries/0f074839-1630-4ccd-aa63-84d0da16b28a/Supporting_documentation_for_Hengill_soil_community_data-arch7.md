# Invertebrate biomass, vegetation cover, and environmental data from Hengill, Iceland.

## Overview
- Dataset of environmental variables, vegetation cover, and invertebrate metrics from 96 soil habitat patches in the Hengill geothermal valley, Iceland (July 2013).
- Patch set spans a soil temperature gradient from 7–38 °C, with patches located within 2 km of each other across 16 geothermally heated streams.
- Data types include: soil temperature, moisture, pH, total carbon, total nitrogen; vegetation cover (non-plant groups and plant species); invertebrate abundance and mean body mass.

## Sampling regime and collection methods
- Soil temperature: monitored at each habitat patch in July 2013 using Maxim iButton loggers buried 10 cm deep; readings every 10 minutes over 48 hours.
- Soil moisture and pH: measured at each patch; moisture via probe, pH via standard soil-water extraction.
- Soil chemistry: total carbon and total nitrogen determined from dried, milled soil using a CN analyser.
- Vegetation survey: 0.5 x 0.5 m quadrats placed randomly per patch; photographs analyzed for percentage cover across defined classes (0–99% in classes 1–9); vascular plants identified to species where possible (graminoids excluded from species-level identification); cover recorded for grasses, mosses, lichens, and litter.
- Invertebrate sampling: five pitfall traps per patch (four corners + center) using white cups with ethylene glycol and water; traps deployed for 48 hours; samples pooled and preserved in ethanol; invertebrates identified to species where possible.

## Data structure and file descriptions
- Data are provided in four CSV files; each row represents one of the 96 habitat patches.
- Common schema across files:
  - Columns 1–3: stream identifier, bank (left/right), patch number (1–3).
  - Patch-specific data follow (variable by file):
    - hengill_environmental_data.csv: latitude, longitude, temperature (mean soil temp in °C), total_carbon (g/kg), total_nitrogen (g/kg), moisture (%), pH.
    - hengill_vegetation_cover.csv: columns for non-plant groups (e.g., grasses, mosses, lichens, litter) and plant species; percentage cover values (0–100%).
    - hengill_invertebrate_abundance.csv: columns for invertebrate species; 4–82 correspond to species; values are total individuals per patch.
    - hengill_invertebrate_mass.csv: columns for invertebrate species; 4–82 correspond to species; values are mean dry mass in milligrams per patch.

## Spatial scope and context
- 96 habitat patches across 16 streams; patches sampled on both banks (left/right) of each stream.
- GPS coordinates provided for each patch enable GIS mapping and spatial analyses.
- Study location linked to broader freshwater and soil-ecology research in the Hengill geothermal system.

## Uses, integration, and workflows for GIS
- Ideal for map-based analyses of spatial patterns in environmental conditions, vegetation structure, and invertebrate communities along a natural thermal gradient.
- Can be joined with other geospatial layers using stream identifiers, bank, patch, or coordinates to create integrated GIS products.
- Facilitates exploration of relationships between soil temperature, chemistry, vegetation cover, and invertebrate community metrics (abundance and body mass).

## Data quality, limitations, and notes
- Data collected during a single month (July 2013); temporal coverage is limited to a short sampling window.
- Species identifications are to the extent possible; some taxa may be identified only to higher taxonomic levels.
- The dataset provides a detailed, patch-level snapshot suitable for spatial analyses but not for long-term trend assessment without additional temporal data.

## References
- The dataset and related findings are connected to multiple publications, including Robinson et al. (2018) on temperature effects in plant and invertebrate communities and broader works on warming effects in streams and aquatic ecosystems (e.g., O'Gorman et al., Friberg et al., Woodward et al., among others).