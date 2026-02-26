# Invertebrate community assembly data across a natural soil temperature gradient in Iceland from May-July 2015

## Overview
- Dataset of environmental data, total invertebrate abundance, and mean invertebrate body mass.
- 60 soil habitat patches in the Hengill geothermal valley, Iceland; sampling occurred May–July 2015.
- Habitat patches span a natural soil temperature gradient (5–22 °C on average) while remaining geographically close (within ~2 km) and having similar soil moisture, pH, total carbon, and total nitrogen.
- Data collected include soil temperature (hourly), soil moisture, soil pH, total carbon, total nitrogen, and epigeal invertebrate communities sampled via pitfall traps.
- Invertebrates were identified to species where possible; many were identified to higher taxonomic levels (e.g., Diptera, Hymenoptera to family level).
- Data are provided in three CSV files: environmental data, seasonal abundance, and seasonal mean mass.

## Sampling regime and collection methods
- Study site: Hengill geothermal valley; 10 geothermally heated streams with three habitat patches sampled on each bank (left/right) per stream, totaling 60 patches.
- Temporal design: four sampling time-points (19 May, 4 June, 23 June, 5 July 2015).
- Temperature monitoring: Maxim Integrated DS1921G Thermocron iButtons buried 5 cm below the soil surface; hourly measurements; 13 May–3 July 2015; 49 of 60 loggers recovered; missing data represented as NAs.
- Soil and soil chemistry: five soil cores per patch (1.5 × 5 cm) collected ~10 cm below surface; homogenised, dried at 60 °C for 96 h, milled; soil moisture measured with a TRIME-TDR probe; pH measured from 10 g dry, milled soil; total carbon and total nitrogen measured via CN analyzer.
- Invertebrate sampling: five pitfall traps per patch, left for 48 hours; traps are white plastic cups with ethylene glycol and stream water; samples from five traps combined per patch, stored in 70% ethanol; sampling occurred at four time-points as above.
- Identification: terrestrial invertebrates identified to species where possible; otherwise to higher taxonomic levels (e.g., Diptera and Hymenoptera often at family level).

## Data structure and files
- Files:
  - hengill_seasonal_environmental_data.csv
  - hengill_seasonal_abundance.csv
  - hengill_seasonal_mass.csv
- Common structure:
  - First three columns in all files: 1) stream, 2) bank, 3) habitat patch (1–3; closest to river to farthest).
- hengill_seasonal_environmental_data.csv:
  - Column 4: temperature (mean soil temperature during the study period).
  - Columns 5–6: total_carbon, total_nitrogen (g kg^-1).
  - Columns 7–8: moisture (%), pH.
- hengill_seasonal_abundance.csv:
  - Column 4: sampling date.
  - Columns 5–128: taxa names; values are total number of individuals per patch per time point.
- hengill_seasonal_mass.csv:
  - Column 4: sampling date.
  - Columns 5–128: taxa names; values are mean dry weight per individual in milligrams.

## Spatial context and design
- 60 patches across 10 geothermally heated streams; each patch has data for four time-points.
- Patch numbering reflects proximity to the river Hengladalsá (1 = closest; 3 = farthest).
- Temperature gradient exists across patches, enabling analysis of temperature-related community changes.

## Data quality and limitations
- Temperature data: 11 loggers not recovered; missing values represented as NA.
- Taxonomic resolution: some taxa identified only to family or higher levels due to identification feasibility.

## How to use for GIS and data visualization
- Map patch coordinates and associated variables: temperature, moisture, pH, carbon, nitrogen, and invertebrate metrics (abundance and mean mass) at the patch level.
- Examine spatial patterns along the natural soil temperature gradient and across streams and banks.
- Combine with other geospatial layers (e.g., stream networks, land cover, or climate layers) to explore drivers of invertebrate community structure.
- Use time-series aspect to visualize changes in abundance and mass across sampling dates for each patch.
- Integrate with additional ecological datasets from the Hengill system to explore spatial-temporal dynamics.

## References
- Adams, G., Pichler, D.E., Cox, E.J., et al. (2013). Diatoms can be an important exception to temperature-size rules at species and community levels of organization. Global Change Biology, 19, 3540-3552.
- Demars, B.O.L., Manson, J.R., Ólafsson, J.S., et al. (2011). Temperature and the metabolic balance of streams. Freshwater Biology, 56, 1106-1121.
- Friberg, N., Dybkjær, J.B., Ólafsson, J.S., et al. (2009). Relationships between structure and function in streams contrasting in temperature. Freshwater Biology, 54, 2051-2068.
- O'Gorman, E.J., Ólafsson, Ó.P., Demars, B.O.L., et al. (2016). Temperature effects on fish production across a natural thermal gradient. Global Change Biology, 22, 3206-3220.
- O'Gorman, E.J., Pichler, D.E., Adams, G., et al. (2012). Impacts of warming on the structure and functioning of aquatic communities: individual- to ecosystem-level responses. Advances in Ecological Research, 47, 81-176.
- O'Gorman, E.J., Zhao, L., Pichler, D.E., et al. (2017). Unexpected changes in community size structure in a natural warming experiment. Nature Climate Change, 7, 659-666.
- Robinson, S.I., McLaughlin, Ó.B., Marteinsdóttir, B., & O'Gorman, E.J. (2018). Soil temperature effects on the structure and diversity of plant and invertebrate communities in a natural warming experiment. Journal of Animal Ecology, 87, 634-646.
- Robinson, S.I., Mikola, J., Ovaskainen, O., & O'Gorman, E.J. (2021). Temperature effects on the temporal dynamics of a subarctic invertebrate community. Journal of Animal Ecology.
- Woodward, G., Dybkjær, J.B., Ólafsson, J.S., et al. (2010). Sentinel systems on the razor's edge: effects of warming on Arctic-geothermal stream ecosystems. Global Change Biology, 16, 1979-1991.