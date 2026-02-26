# Invertebrate community assembly data across a natural soil temperature gradient in Iceland from May-July 2015

- Overview
  - A dataset combining environmental measurements, total invertebrate abundance, and mean invertebrate body mass across 60 soil habitat patches in the Hengill geothermal valley, Iceland, collected May–July 2015.
  - Patches span a natural soil temperature gradient (approximately 5–22 °C) but are spatially proximate (within 2 km) and share similar soil moisture, pH, total carbon, and total nitrogen.
  - Designed to examine how soil temperature affects community structure and dynamics; linked to multiple related studies and publications.

- Sampling regime and collection methods
  - Temperature: soil temperature monitoring for each patch using Maxim Integrated DS1921G iButtons; hourly measurements, buried 5 cm below the surface; data collected 13 May–3 July 2015. 49/60 loggers recovered; missing data represented as NA.
  - Soil properties: moisture measured with a soil moisture probe; five soil cores per patch (10 cm below surface) were collected, dried at 60 °C for 96 hours, and milled for analyses. Soil pH measured from 10 g of dry, milled soil (1:5 soil-to-water), using a pH meter. Total carbon and total nitrogen measured (CN analyzer) on 5 g subsamples.
  - Invertebrate sampling: epigeal invertebrates collected with five pitfall traps per patch, left for 48 hours, at four time-points (19 May, 4 June, 23 June, 5 July 2015). Traps consisted of white cups with ethylene glycol and stream water, samples combined per patch, stored in 70% ethanol.
  - Taxonomic resolution: terrestrial invertebrates identified to species where possible, often to higher taxonomic levels (e.g., Diptera, Hymenoptera to family level) due to feasibility.
  - Documentation and references: detailed sampling procedures and related analyses are described across Robinson et al. (2018, 2021) and O’Gorman et al. publications.

- Data structure and contents
  - Data provided as three CSV files; each row represents a single sampling time-point for one of the 60 habitat patches.
  - Common first columns in all files: (1) stream, (2) bank, (3) habitat patch (1–3), with coding aligned to prior Hengill stream publications.
  - hengill_seasonal_environmental_data.csv
    - Column 4: temperature (mean soil temperature during the study period, °C)
    - Column 5: total carbon (g kg−1)
    - Column 6: total nitrogen (g kg−1)
    - Column 7: moisture (%)
    - Column 8: pH
  - hengill_seasonal_abundance.csv
    - Column 4: sampling date
    - Columns 5–128: abundance counts for each invertebrate taxon (per patch, per sampling date)
  - hengill_seasonal_mass.csv
    - Column 4: sampling date
    - Columns 5–128: mean dry weight (mg) for each invertebrate taxon (per patch, per sampling date)
  - Taxa columns (5–128) correspond to the names of the taxa quantified; values are the total number of individuals (abundance) or mean dry weight (mass) per patch.
  - Taxonomic resolution: species-level where possible; otherwise higher-level groupings.

- Temporal and spatial design
  - Spatial: 60 soil habitat patches distributed across 10 geothermally heated streams; patches sampled on both banks (left/right) with 3 patches per bank per stream.
  - Temporal: four sampling events across May–July 2015, enabling assessment of community responses across a natural temperature gradient and seasonal dynamics.

- Data quality, limitations, and governance
  - Temperature data completeness: 11 of 60 loggers not recovered, resulting in NA entries for some temperature measurements.
  - Metadata and comparability: dataset includes explicit column descriptions and consistent coding aligned with prior publications; however, as with many ecological time-series datasets, taxonomic resolution varies by specimen group.
  - Data accessibility and reuse: structured in CSV with clear provenance, facilitating reuse in monitoring analyses, cross-study comparisons, and policy-relevant assessments.
  - Data provenance: linked to a substantial body of related works (multiple Adams et al., Demars et al., Friberg et al., O’Gorman et al., Robinson et al., Woodward et al.), supporting broader interpretation and integration.

- Relevance for monitoring frameworks and policy decisions
  - Provides a climate-temperature gradient, high-resolution, field-based dataset to monitor how soil invertebrate communities respond to warming at fine spatial scales.
  - Enables tracking of ecosystem structure (species abundance and biomass) in relation to soil properties (carbon, nitrogen, moisture, pH) under varying temperatures.
  - Supports analyses of temporal dynamics and potential tipping points or shifts in community composition under warming, informing policy on climate adaptation and biodiversity management in soils.
  - The dataset’s structured metadata and multi-variable measurements help overcome common barriers in monitoring data (data availability, metadata completeness, and data governance), and its public availability aligns with data-sharing and transparency requirements.

- References (context for data use)
  - Related studies and datasets that utilize these data include works by Adams et al., Demars et al., Friberg et al., O’Gorman et al., Robinson et al., and Woodward et al., among others, illustrating temperature effects on community structure and function across streams and warming experiments.