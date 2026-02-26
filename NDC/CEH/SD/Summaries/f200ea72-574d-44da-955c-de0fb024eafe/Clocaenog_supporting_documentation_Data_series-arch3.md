# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose of the dataset: Provides supporting documentation for a climate change manipulation experiment (drought and warming) at Clocaenog forest, intended to reflect forecasted climate conditions for upland moorland over the next 20–30 years and to support environmental monitoring and policy evaluation.
- Context of the site: Automated, solar and wind-powered field facility established in 1998; located in North East Wales; dominated by Calluna vulgaris (heather) with other mosses, grasses and shrubs; soil is humo-ferric podzol with variable horizons.

- Experimental design and treatments
  - Structure: 9 plots in total — 3 replicates of each treatment: warming (W), drought (D), and control (C); arranged in blocks (three blocks).
  - Drought treatment: Retractable polyethylene roof reducing rainfall over plots during growing seasons; initially May–Sept (1999–2011) and since 2012 April–October; rainfall reduction typically around 14–20% annually, with substantial reduction during growing seasons (up to ~80% of targeted rain events excluded).
  - Warming treatment: Retractable aluminium-mesh curtains over plots to conserve heat at night; designed to minimize infrared heat loss; rainfall adjustments made to limit unintended rainfall exclusion.
  - Operational constraints: Curtains not used in high winds (>10 m/s); shading controls implemented in control plots to mirror treatment structure effects.

- Data types and datasets collected (overview)
  - AWS meteorological data: Daily on-site weather station measurements (air temperature, relative humidity, rainfall, net radiation, solar radiation, PAR, wind) from 1999–present; sensors mounted at 4 m after 2007.
  - Micro-meteorological plot data: Daily plot-level soil and air temperatures, soil moisture (various methods over time) from 1998–present.
  - Rainfall and rainfall chemistry: Site-level storage rain gauge (biweekly) with laboratory analysis of chemical constituents (pH, nitrate, chloride, sulfate, DOC, ammonium).
  - Throughfall data: Plot-level rainfall collected biweekly; used to derive treatment-specific rainfall adjustments and percent changes per year.
  - Water table depth: Biweekly measurements from 2009–present via permeable tubes down to bedrock.
  - Soil respiration: Fortnightly to frequent measurements (1999–present) using collars; progression from manual to automated LI-COR-based methods; units converted to mg CO2-C m^-2 hr^-1.
  - Trace gases (CH4 and N2O): Measurements using static chambers with gas chromatography; data from 1999–2000 and 2007–2009.
  - Net ecosystem CO2 exchange (NEE): Infrequent measurements (2002–2004, 2009–2011) using closed chambers with PAR/temperature sensors; adjustments for plant biomass made to normalize across plots.
  - Photosynthesis: Infrequent measurements (2001–2003 for C. vulgaris and V. myrtillus; 2001 for E. nigrum) using IRGA and leaf cuvettes; light response and ambient conditions recorded.
  - Vegetation biomass (Pinpoint method): Annual surveys (1998–2012, and specific years beyond); three quadrats per plot; 300 pins per plot; conversion of pin hits to biomass using species-specific calibration.
  - Canopy reflectance: Ground-based spectrometer measurements (NDVI and PRI indices) for selected years (2000–2004, with some 2001–2002 data) to assess canopy condition.
  - Vegetation phenology, growth and pathogens: Spring phenology for C. vulgaris, V. myrtillus, E. nigrum; shoot elongation, budburst, leaf emergence, flowering, and herbivory/pathogen signs; data from 1998–2009 (and beyond).
  - Vegetation chemistry: Analysis of carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose and carbohydrate content in green and senesced material (litter).
  - Litterfall: Monthly collection (1999–2002) with subsequent drying, weighing, and conversion to g m^-2; carbon and nitrogen analyses of litter.
  - Root biomass: Soil cores and destructive sampling across multiple years (2003–2013); various methods across years for root extraction and biomass estimation.
  - Soil microbial biomass: Chloroform-fumigation technique (2000, 2001, 2012) with DOC extraction and correction factors to yield microbial biomass carbon per g soil organic matter.
  - Nitrogen mineralisation: Seasonal measurements (1998–2004) via paired soil cores with KCl extraction to estimate ammonium and nitrate fluxes.
  - SOM, SOC and bulk density: Analyses on paired cores; determinations of SOM and SOC percentages and bulk density; conversions to g m^-2.
  - Soil solution and leachate chemistry: Lysimeters and tensioned samplers installed in 1998; monthly biweekly sampling for pH, NO3, Cl, SO4, DOC, ammonium.

- Data processing, standardization and quality considerations
  - Datasets include detailed methodological notes, measurement frequencies, and time scales; many data are stored in a central data repository (EIDC) with some legacy datasets documented extensively and others requiring direct contact with data custodians.
  - Data processing includes unit conversions (e.g., soil respiration units to mg CO2-C m^-2 hr^-1, NEE conversions, biomass conversions from pin hits), calibration and cross-instrument adjustments, and biomass normalization for NEE.
  - Throughfall and rainfall data require adjustments to estimate plot-level rainfall by applying percent differences to site-level rainfall data; occasional data loss leads to plot-level exclusion or infilling with year-wide averages.
  - Quality control relies on basic visual checks for AWS and micro-meteorological data; explicit automated limits and metadata quality checks are variably documented, reflecting legacy data practices.

- Metadata, governance and access considerations (alignment with monitoring-framework aims)
  - The documentation notes the importance of metadata to verify data suitability and the need for sharing underlying data with appropriate governance; some datasets require direct contact with data managers (e.g., CEH Bangor) for access details.
  - The dataset collection demonstrates comprehensive integration of abiotic and biotic monitoring across short- and long-term timescales, illustrating data governance challenges common in large, complex monitoring programs—such as data silos, data format transformations, and ensuring data openness and standardization.
  - The documentation provides explicit data owners and contact points for data access and clarification (e.g., Sabine Reinsch and Bridget Emmett at CEH Bangor).

- Relevance for monitoring framework authors
  - Illustrates a long-term, multi-disciplinary monitoring framework capturing climate manipulation effects on vegetation, soil processes, carbon fluxes, and ecosystem chemistry.
  - Highlights the need for clear metadata, data provenance, and governance to enable data reuse for policy evaluation and future decision-making.
  - Demonstrates practical challenges in data integration, sharing, and keeping data current across silos and evolving measurement technologies.