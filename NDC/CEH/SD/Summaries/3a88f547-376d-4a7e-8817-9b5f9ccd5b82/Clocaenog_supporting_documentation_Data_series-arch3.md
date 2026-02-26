# Climoor field site in Clocaenog forest Supporting documentation for data

- Climoor is a climate change manipulation experiment at Clocaenog Forest, North-East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years. It is solar/wind powered, established in 1998, and comprises replicated drought and warming treatments with control plots to mirror shading effects.

## Experimental design and site context

- Location and ecosystem: upland moorland dominated by Calluna vulgaris (heather); soil is humo-ferric podzol with variable E and Bh horizons.
- Treatments: three replicates each of warming and drought, plus three control plots to mimic shading effects (9 plots total including controls).
- Drought treatment: operated May–Sept (1999–2011) and April–October since 2012; uses retractable polyethylene roof to exclude rainfall, reducing site rainfall by ~20% and excluding ~80% of rain during the growing season.
- Warming treatment: uses retractable aluminum mesh curtains to reduce nighttime heat loss; reduces infrared radiation and lowers heat loss; rainfall exclusion occurs during rain events due to a sensor-triggered retraction. Curtains do not operate in winds above 10 m/s.
- Baseline climate: long-term site data (1997–2014) presented for mean air and soil temperatures, rainfall, and deposition context.
- Plot structure: each treatment/replicate is 4 m x 5 m; treatment allocation detailed in site tables.

## Data collection and data types

- Data management: on-site automated systems and manual sampling across abiotic and biotic domains; data quality controlled, with efforts to ensure metadata, data provenance, and openness where feasible.
- Data types and frequency:
  - AWS meteorological data (daily; minute-sampled sensors, hourly averages; 1999–present): temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
  - Micro-meteorological plot data (daily): soil temperature at 5, 10, 20 cm; soil moisture (TDR and earlier methods).
  - Rainfall and rainfall chemistry (biweekly): site-level storage rain gauge; chemical analyses of rainwater (pH, NO3, Cl, SO4, DOC, ammonium).
  - Throughfall data (plot level rainfall; biweekly): plot-level rainfall collection; used to derive treatment-specific rainfall changes; some data gaps may lead to exclusion of plots from treatment means.
  - Water table depth (since 2009): measurements via permeable tubes; occasional manual measurements.
  - Soil respiration (CO2 flux; 1999–present with transitions in method): three collars per plot; static chamber methods and IRGA/Li-Cor systems; automated campaigns from 2013 onward.
  - Trace gases (CH4, N2O; 1999–2000, 2007–2009): static chamber measurements with gas chromatography; legacy data with varying documentation quality.
  - Net ecosystem CO2 exchange (NEE; 2002–2004, 2009–2011): chamber-based flux measurements; different chamber systems used across years; adjustments for biomass differences in calculations.
  - Photosynthesis (ambient and response curves; 2001–2003): leaf-level measurements in Calluna and Vaccinium; PAR and Ci treatments; some data flagged as unreliable above certain Ci.
  - Vegetation survey data (Pin-point biomass; 1998–2012): three quadrats per plot; 100 pins per quadrat; species hits by height; biomass conversions using species-specific calibration.
  - Canopy reflectance (NDVI and PRI; 2000–2004): ground-based spectrometry to derive NDVI680, NDVI570, and PRI.
  - Vegetation phenology, annual growth, and pathogens (1998–present): shoot elongation, budburst, and phenophase records; maximum growth measurements for dominant shrubs.
  - Vegetation chemistry (annual; 1998–present): carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates on green and senesced material.
  - Litterfall (1999–2002; later sporadic): monthly collection and drying/weighing; conversion to g m^-2; carbon and nitrogen analyses on pooled annual samples.
  - Root biomass (2003–2004, 2008, 2011): soil cores and root extraction; multiple soil depths and methods; analysis includes WinRHIZO for some cores.
  - Soil microbial biomass (2000, 2001, 2012): chloroform fumigation extraction; DOC measurement and correction to microbial biomass carbon.
  - Nitrogen mineralisation (1998–2004): paired soil cores with initial and final analyses; ammonium and nitrate via autoanalyser; comparisons yield net mineralisation rates.
  - SOM, SOC and bulk density (from N-mineralisation cores): soil moisture, organic/inorganic layer separation, ash-free measurements; bulk density calculations for g m^-2 basis.
  - Soil solution and leachate chemistry (1998–2008): lysimeters and tensioned samplers; pH, NO3, Cl, SO4, DOC via TOC; controls on sample handling and storage.
- Data processing notes:
  - Legacy data with varying documentation; multiple equipment generations (CIRAS-2, LICOR 8100, LI-COR 8100A, automated systems).
  - Unit conversions detailed for flux calibrations (mg CO2-C m^-2 h^-1, µmol m^-2 s^-1, etc.).
  - Quality control often involves visual inspection; some data processed with site-specific calibration factors and biomass adjustments.
  - Throughfall and rainfall data sometimes require infilling or exclusion when data are incomplete or compromised.

## Data governance, accessibility, and challenges

- Metadata and data quality: efforts to verify data provenance and maintain quality; some datasets lack complete processing documentation (legacy data caveats).
- Data availability: most datasets are described as stored with CEH Bangor or related data repositories; some not stored in a central data repository (EIDC) after June 2015; direct inquiries to CEH staff recommended for details.
- Barriers and challenges for monitoring frameworks reflected in this dataset:
  - Data availability and standardization across years and methods.
  - Metadata completeness and dataset provenance for long-term series.
  - Public sharing requirements potentially hampering use of certain rainfall data or harmonization across datasets.
  - Data modernization needs (updating methods, harmonizing units, ensuring consistent governance).
  - Data gaps due to equipment theft, power/logger downtime, weather conditions, and data loss requiring exclusion or infilling.
  - Transforming diverse data types (abiotic and biotic) into comparable indicators across plots and treatments, with biomass-adjusted fluxes and treatment-specific rainfall adjustments.

## Appendix and site layout

- Appendix 1: Site layout coordinates and grid references (SJ019519, 53.055N, -3.465W).
- Appendix 2: Quadrat layout and plot measurement areas (LYS, PQ, SS markers).
- Appendix 3: Plot layout with quadrats and measurement areas indicated.
- 2012 Climoor plot layout summary: LYS (Lysimeters), PQ (Point quadrats), SS (Soil suction samplers).