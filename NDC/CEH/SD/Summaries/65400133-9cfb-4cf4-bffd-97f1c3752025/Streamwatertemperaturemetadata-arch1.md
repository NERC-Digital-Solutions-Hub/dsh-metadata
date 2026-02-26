# Seasonal river water temperatures and climatic drivers for 35 sites on 21 rivers and streams (1984 - 2007)

- Purpose: Combine observed river water temperatures with modeled climate data to understand how climate and basin properties control seasonal WT variability, informing water and land management under climate change.

## Dataset coverage and structure
- 35 water temperature monitoring sites across 21 rivers in 16 basins, Great Britain.
- Time period: 1984–2007; data are seasonal (three-month averages) with six modeled climate variables.
- Data columns include: UID, Year, Season (1 winter; 2 spring; 3 summer; 4 autumn), Num Days, WT (°C), AT (°C), SWR (W/m2), WS (m/s), SH (kg/kg), P (kg/m2/d), LWR (W/m2), Time (season index), Dataset, Basin, River, Site, NGR, Easting, Northing.

## Climate data and data sources
- Climate drivers derived from CHESS (Climate Hydrology and Ecology research Support System): six variables per 1-km grid cell, daily time series for 1971–2007; CHESS cells matched to study sites.
- CHESS acts as the forcing dataset for JULES (UK land surface model) with downscaling from 40-km MORECS inputs, except precipitation based on rain-gauge data.
- Water temperature data collated from CEH-led projects and various initiatives (e.g., Frome, Great Ouse, Tadnoll; Plynlimon forestry and UKAWMN; LOCAR).

## Seasonal series derivation and processing
- Sub-daily WT data are averaged to daily; some spot measurements represent daylight conditions.
- Daily WT and climate data are temporally matched; seasonal averages computed for all variables.
- Seasons defined as: winter (Dec–Feb), spring (Mar–May), summer (Jun–Aug), autumn (Sep–Nov).
- Winter of year y uses Dec of year y−1 to Feb of year y (e.g., Dec 1975–Feb 1976 for 1976 winter).

## Scientific context and aims
- WT directly/indirectly affects ecology, biogeochemistry, and water-related services (e.g., cooling for power plants, recreation).
- Aims to unravel large-scale spatial and temporal variability in climate–WT associations and how basin properties modify these relationships.
- Enables assessment of river thermal sensitivity to climate variability and change.

## Applications and implications
- Supports climate change mitigation/adaptation planning and water/land management decisions.
- Provides a basis for evaluating how different climatic drivers contribute to seasonal WT patterns across multiple basins.

## Limitations and considerations
- Temporal resolution varies across source datasets; integration across multiple projects may introduce heterogeneity.
- Some measurements reflect daylight conditions only; representativeness may vary by site.
- Spatial resolution of climate drivers is 1-km (CHESS), which may influence fine-scale interpretations.
- Data quality and standardization issues inherent in combining historical datasets.

## Key references and context
- Includes foundational work on JULES model description, riparian shade effects, river temperature variability, and hydro-ecological studies relevant to the dataset and its interpretation.