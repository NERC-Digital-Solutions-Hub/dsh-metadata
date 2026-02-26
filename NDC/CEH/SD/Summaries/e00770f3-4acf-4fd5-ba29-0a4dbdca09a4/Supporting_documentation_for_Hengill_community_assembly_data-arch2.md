# Invertebrate community assembly data across a natural soil temperature gradient in Iceland from May-July 2015

## Overview
- A dataset of environmental data, total invertebrate abundance, and mean invertebrate body mass.
- Collected at 60 soil habitat patches along a natural soil temperature gradient (average 5–22 °C) in the Hengill geothermal valley, Iceland.
- Sampling period: May–July 2015; temperature monitoring from 13 May to 3 July 2015.
- Context: within 2 km of each other with similar soil moisture, pH, total carbon, and total nitrogen; linked to prior and subsequent studies on stream and terrestrial invertebrate responses to warming.

## What was measured and where/when
- Habitat patches: 60 patches (3 patches per bank of 10 geothermally heated streams).
- Temperature: mean soil temperature per patch during the study period (hourly iButton loggers buried 5 cm deep).
- Soil characteristics: moisture, pH, total carbon, total nitrogen per patch.
- Invertebrate data: epigeal invertebrates collected with five pitfall traps per patch (operated 48 hours) at four time-points (19 May, 4 June, 23 June, 5 July).
- Taxonomic resolution: terrestrial invertebrates identified to species where possible; many Diptera and Hymenoptera to family level.

## Sampling regime and collection methods
- Temperature monitoring: Maxim iButton data loggers, hourly measurements; 49 of 60 loggers recovered (missing data represented as NA).
- Soil sampling: five soil cores per patch (5 cm diameter × 1.5 × 5 cm), homogenised, dried at 60 °C for 96 hours, milled for analysis.
- Soil analysis: total carbon and total nitrogen via combustion (CN analyzer); moisture via soil moisture probe; pH via 1:5 soil-water ratio.
- Invertebrate sampling: five pitfall traps per patch, traps filled with ethylene glycol and stream water, combined per patch, stored in ethanol; specimens prepared and identified as described.
- Related work: linked to Robinson et al. (2018, 2021) and other Hengill stream ecosystem studies.

## Data structure and files
- Data are provided as three CSV files; each row corresponds to one sampling time-point for one patch (60 patches × multiple time-points).
- Common first three columns across files: 
  - 1) Stream identifier
  - 2) Bank (left/right)
  - 3) Patch number (1–3)
- hengill_seasonal_environmental_data.csv
  - Additional columns: (4) temperature (mean soil temp during study period), (5-6) total carbon, total nitrogen, (7-8) moisture, pH.
- hengill_seasonal_abundance.csv and hengill_seasonal_mass.csv
  - Column 4: sampling date
  - Columns 5–128: taxa names (or higher taxonomic groups) quantified
  - hengill_seasonal_abundance.csv: counts of individuals per taxon per patch/date
  - hengill_seasonal_mass.csv: mean dry weight (mg) per taxon per patch/date

## Variables and measurements
- Environmental variables: temperature (°C), total carbon (g kg−1), total nitrogen (g kg−1), soil moisture (%), soil pH.
- Biological variables: total invertebrate abundance; mean body mass (mg) per taxon per patch/date.

## Data quality and limitations
- Temperature data gaps: 11 loggers not recovered; missing values are NA.
- Taxonomic resolution: some groups identified to family or higher levels due to identification constraints.
- Documentation: explicit column definitions and data description provided to assist downstream analysis and data portal integration.

## Relevance for monitoring and analysis
- Standardized, multi-layer dataset suitable for assessing how soil temperature gradients influence invertebrate community structure and body size dynamics.
- Enables temporal and spatial comparisons within Hengill and across similar geothermal gradients.
- Compatible with integration into broader environmental monitoring datasets; supports analyses referenced in Robinson et al. (2018, 2021) and related warming studies.
- Data are organized for reproducible analyses and potential upload to environmental data portals.

## References
- Adams et al. (2013); Demars et al. (2011); Friberg et al. (2009); O’Gorman et al. (2012, 2016, 2017); Robinson et al. (2018, 2021); Woodward et al. (2010) among others.