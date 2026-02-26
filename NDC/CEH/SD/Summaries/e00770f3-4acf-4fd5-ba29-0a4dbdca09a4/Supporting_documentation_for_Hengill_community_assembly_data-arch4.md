# Invertebrate community assembly data across a natural soil temperature gradient in Iceland from May-July 2015

## Overview
- Dataset combining environmental measurements, total invertebrate abundance, and mean body mass.
- Collected May–July 2015 from 60 soil habitat patches in the Hengill geothermal valley, Iceland.
- Temperature gradient across patches ranges 5–22 °C on average; patches are within ~2 km of each other and share similar soil moisture, pH, total carbon, and total nitrogen.
- Sampling design tied to existing freshwater/soil temperature studies in the region.

## Sampling regime and collection methods
- 60 patches sampled across 10 geothermally heated streams; three patches per bank (left or right) of each stream, giving 6 patches per stream.
- Soil temperature monitored at each plot from 13 May to 3 July 2015 using iButton loggers (hourly measurements; buried 5 cm deep). 49 of 60 loggers recovered; missing data recorded as NA.
- Soil moisture measured with a TRIME-TDR probe; soil cores collected (five 1.5 × 5 cm cores per patch), dried, milled, and analyzed for total carbon and total nitrogen (CN analyser); soil pH measured from dry, milled soil.
- Epigeal invertebrates sampled with five pitfall traps per patch, deployed for 48 hours at four time points: 19 May, 4 June, 23 June, 5 July. Traps used ethylene glycol and stream water; samples combined and stored in 70% ethanol.
- Taxonomic identification to species level where possible, often to higher taxonomic groups (e.g., Diptera and Hymenoptera to family level) due to feasibility constraints.

## Data structure and files
- Three CSV files, each row representing one sampling time point for a given patch (out of 60 patches):
  - hengill_seasonal_environmental_data.csv
    - Core columns: stream, bank, patch
    - Additional columns: temperature (mean soil temp during study), total_carbon, total_nitrogen, moisture, pH
  - hengill_seasonal_abundance.csv
    - Core columns: stream, bank, patch
    - Column 4: sampling date
    - Columns 5–128: taxa names; values = total number of individuals per taxon per patch per sampling date
  - hengill_seasonal_mass.csv
    - Core columns: stream, bank, patch
    - Column 4: sampling date
    - Columns 5–128: taxa names; values = mean dry weight per taxon per patch per sampling date (mg)
- Taxa columns (5–128) correspond to the same taxa across abundance and mass datasets.
- Location context linked to Hengill stream references from prior publications.

## Data quality and limitations
- Temperature data gaps: 11 of 60 loggers not recovered; NA values present in temperature data.
- Taxonomic resolution limited for some groups (e.g., Diptera, Hymenoptera often identified only to family level).
- Data represent a single geographic region and time window; external validity may depend on similar geothermal-gradient systems.

## How this data supports data-driven decision making
- Enables analysis of how soil temperature gradients influence invertebrate community structure and biomass during the growing season.
- Facilitates examination of temporal dynamics across snowmelt-related periods with environmental covariates (temperature, moisture, pH, carbon, nitrogen).
- Provides a structured dataset suitable for cross-study integration within the Hengill system or for meta-analyses of temperature–community relationships.

## Related references and context
- The dataset is linked to broader work on temperature effects in Hengill streams and surrounding ecosystems (e.g., Robinson et al., O'Gorman et al. multiple publications), providing context for interpretation of community responses to natural warming.