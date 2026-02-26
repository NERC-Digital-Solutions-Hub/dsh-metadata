# Spatial and temporal variations in aquatic organic matter composition in UK surface waters

## Overview
- Investigates how aquatic organic matter (DOM) composition varies across space and time in UK surface waters (2018–2021).
- Combines field sampling, in situ water chemistry, and detailed DOM analysis to characterize both site metadata and chemical composition.

## Data collection and study design
- Fieldwork conducted 2018–2021 at four locations in England and Scotland; sampling across peat/organic-soil-influenced water bodies (pools, headwaters, streams, reservoirs, lakes, inlets/outlets).
- At each site: in situ measurements of pH, conductivity, dissolved oxygen, water temperature; air temperature, pressure, humidity.
- Sampling protocol: grab water (50 mL) filtered in the field through 0.45 µm filters; samples kept cold and dark, transported in cool conditions, stored at 4 °C for laboratory analysis.
- Analyses included: dissolved/particulate organic carbon, inorganic nutrients, cations, metals, anions.
- Organic matter processing: large-volume water filtered to collect particulate organic matter (POM); filtrate concentrated to ~100 mL; water evaporated to dryness to isolate dissolved/colloidal organic matter (DOM).
- DOM analysis: elemental composition (C, H, N, O) via Elementar Vario MICRO; subset analyzed by negative-mode electrospray FT-ICR MS.
- QA: 10% of samples re-analyzed; instrument/calibration checks; replicate data compared; averages used if replicates agree within 95%; non-concordant replicates re-analyzed; derived CHNO metrics restricted by physical properties.

## Datasets and data structure
- UK_Sites: site-level metadata with anonymized location details due to reservoir access constraints; fields include ID, Visit, Month, Year, Group, PEAT_AREA, ELEVATION, Type_4 (water body type), LAND_USE, VEG_COVER, POSITION, CATCHMENT_AREA, HOSTPEAT, DISTANCE_SEA, etc.
- UK_DOM: composition metrics derived from carbon, hydrogen, oxygen, nitrogen content in DOM; includes DOM_PROP_C, DOM_COX, DOM_OR, DOM_DBEC, C/N, H/C, O/C, Assigned_formula, Mean_mz, Std_mz, Mean_ai, Mean_nosc, diversity indices (Simpson, Shannon), PERC_LIPID, PERC_CARBO, PERC_AMINO, PERC_PEPTI, PERC_OXYAR, MS_DBEC.
- UK_Water: environmental variables and water chemistry per sample; includes ID, Visit, pH, CONDUCTIVITY, DISS_O2, WATER_TEMP, AIR_TEMP, HUMIDITY, AIR_PRES, BANK_TEMP, DOC, various anions/cations (Cl, SO4, CA, K, MG, NA, AL, MN, FE, etc.), DON, DIN, DOP, DIP, SUVA254, E4E6, and other measured parameters; dual fields exist for some variables (1 and 2).
- Location handling: site locations intentionally not disclosed to protect access-sensitive reservoirs; datasets are structured for controlled sharing while preserving essential metadata.

## Data quality assurance and governance
- QA processes include calibration checks at run start, repeated checks throughout, and 10% replicate analyses.
- Data analysis QA includes comparing all replicates; if within 95% agreement, an average is used; if not, samples are re-analyzed.
- Derived metrics (e.g., CHNO) restricted by physical property constraints to ensure meaningful values.
- Documentation accompanies each dataset to support reuse and interpretation.

## Stewardship and sharing implications
- Data are organized to be discoverable and reusable, with clear metadata and documentation.
- Datasets (UK_Sites, UK_DOM, UK_Water) are suitable for upload to relevant data portals and catalogues; metadata and data formats are designed to support reuse, interoperability, and future updates.
- Anonymity/privacy considerations are applied to site locations; datasets are prepared with versioning and update pathways.

## Challenges relevant to data stewards
- Incomplete or evolving understanding of user needs for these datasets.
- Timely access to data from multiple data creators; coordination required for updates.
- Ensuring metadata completeness and consistency across datasets.
- Interoperability across diverse systems and formats; handling large, high-dimensional DOM data (e.g., FT-ICR MS results) and metadata.
- Managing data with access constraints (anonymized locations) while maintaining scientific usefulness.

## References
- Moody, Catherine S., 2025. Spatial and temporal variations in aquatic organic matter composition in UK surface waters. Environmental Science and Technology Water, in press.
- Moody, Catherine S., 2020. A comparison of methods for the extraction of dissolved organic matter from freshwaters. Water Research.