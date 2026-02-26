# Invertebrate community assembly data across a natural soil temperature gradient in Iceland from May-July 2015

## Overview
- A dataset of environmental measurements, total invertebrate abundance, and mean invertebrate body mass from 60 soil habitat patches in the Hengill geothermal valley, Iceland.
- Sampling occurred May–July 2015, across a natural soil temperature gradient (about 5–22°C on average) with patches located within 2 km of each other.
- Data were collected from four time-points using pitfall traps to assess epigeal invertebrates; specimens were identified to species where possible or to higher taxonomic levels when necessary.
- Temperature was continuously monitored with iButton loggers (hourly data); some loggers (49 of 60) were recovered, leaving NA values for missing data.
- The study complements a broader body of work on how soil temperature influences community structure and dynamics in this system.

## Data structure and files
- Three comma-separated value files, each row representing a single sampling time-point for one of the 60 habitat patches.
- First three columns in all files:
  - 1) stream adjacent to the patch
  - 2) bank (left/right) when facing upstream at the confluence
  - 3) patch number (1–3; closest to the river to farthest)
- Files:
  - hengill_seasonal_environmental_data.csv
    - Column 4: temperature (mean soil temperature during the study)
    - Columns 5–6: total_carbon, total_nitrogen (g kg⁻¹)
    - Columns 7–8: moisture (%), pH
  - hengill_seasonal_abundance.csv
    - Column 4: sampling date
    - Columns 5–128: abundance counts for each invertebrate taxon
  - hengill_seasonal_mass.csv
    - Column 4: sampling date
    - Columns 5–128: mean dry weight (mg) for each invertebrate taxon
- Taxa represented across columns 5–128; data reflect counts or mean body mass per patch at each sampling date.

## Sampling regime and methods
- Patch selection: 60 soil habitat patches across three banks of ten geothermally heated streams.
- Temporal coverage: four sampling dates – 19 May, 4 June, 23 June, and 5 July 2015.
- Environmental measurements:
  - Soil temperature monitored 13 May–3 July 2015 with iButton loggers ( buried 5 cm deep; hourly readings).
  - Soil moisture measured per patch using a time-domain reflectometry probe.
  - Soil samples collected for carbon and nitrogen analysis after drying and milling.
  - Soil pH measured from dried, milled soil.
- Biological sampling:
  - Epigeal invertebrates collected with five pitfall traps per patch, left for 48 hours.
  - Traps were composed of white cups with ethylene glycol and stream water.
  - Invertebrates identified to species where possible; otherwise to higher taxonomic levels (e.g., Diptera, Hymenoptera to family level).
  - Specimens stored in 70% ethanol; data include total abundances and mean dry weights per taxa.

## Key variables and data usability
- Environment: mean soil temperature, soil carbon and nitrogen content, soil moisture, pH.
- Community composition: per-patch, per-date abundances for a wide range of taxa.
- Population attributes: per-taxa mean body mass, enabling analyses of size structure alongside abundance.
- Temporal and spatial alignment: each row represents a patch-time combination, enabling temporal dynamics and temperature-gradient analyses within a tightly clustered spatial area.

## Potential analyses and data use
- Assess effects of soil temperature on invertebrate community structure and diversity across the gradient.
- Examine temporal dynamics of abundance and body size in relation to temperature fluctuations.
- Integrate environmental covariates (moisture, pH, carbon, nitrogen) with community metrics to identify drivers of assemblage change.
- Compare with related publications on temperature effects in this system for broader ecological inferences.

## Data quality and caveats
- Temperature data completeness: 11 of 60 loggers recovered; missing data represented as NA in the environmental file.
- Taxonomic resolution limitations: some taxa identified only to higher taxonomic levels, potentially limiting species-specific inferences.
- Spatial scope: patches are geographically proximate but located along multiple streams; care needed when generalizing beyond this gradient.

## References and context
- Related studies and contextual references provided within the dataset documentation, including methodological details and prior findings on how temperature and warming influence stream and soil invertebrate communities (e.g., Robinson et al. 2018; 2021; O’Gorman et al. series; Friberg et al.; Woodward et al.; Adams et al.; Demars et al.; others).