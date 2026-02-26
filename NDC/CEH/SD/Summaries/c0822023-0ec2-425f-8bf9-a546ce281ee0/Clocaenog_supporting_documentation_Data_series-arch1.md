Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Automated climate manipulation experiment at Clocaenog Forest, North East Wales, to simulate drought and warming for the next 20–30 years in upland moorland.
- Established in 1998; powered by solar and wind; replicated drought and warming treatments with control plots.
- Dominant ecosystem: Calluna vulgaris (heather) with a mix of other vegetation; soil type: humo-ferric podzol.

## Experimental design and treatments
- Plot layout: 9 plots in total (3 replicates for each treatment: warming, drought, and control) organized into blocks; each plot 4 m x 5 m.
- Treatments:
  - Drought (D): retractable polyethylene roof reduces rainfall. Timing typically May–September (1999–2011) and April–October since 2012; reduces annual rainfall by ~20% and excludes around 80% of rain during the growing season.
  - Warming (W): retractable aluminium mesh curtains that reflect infrared radiation, reducing night-time heat loss; roof retraction during rain to limit rainfall exclusion. Generally reduces annual rainfall by ~14%. Curtains not operated in winds >10 m/s.
  - Controls (C): scaffolding to mirror shading from treatment structures; replicate shading across controls.
- Annual and seasonal timing details and changes are captured in treatment tables (e.g., drought timing across years; warming GDD data).

## Location and site characteristics
- Location coordinates: SJ019519; 53.055N, 3.465W (53°03'19''N,  -03°27'55''W).
- Ecosystem: Wet upland heath with Calluna vulgaris dominating biomass; other species include Vaccinium myrtillus, Empetrum nigrum, various mosses and grasses.
- Soils: Humo-ferric podzol with variable horizons (E and Bh only sometimes visible); parent material Ordovician–Silurian shale/mudstone.
- Environment: Upland moorland; typical growing season June–August; winter dormancy Nov–Feb.

## Data and datasets collected
- Equipment and data processing focus on a wide range of abiotic and biotic measurements. Summary of data types:
  - AWS meteorological data (daily; 1999–present): air temp, relative humidity, rainfall, wind, net radiation, solar radiation, PAR, barometric pressure; minute-by-minute sensors with hourly averages.
  - Micro-meteorological plot data (daily; 1998–present): plot-level soil and air temperature, soil moisture.
  - Storage rain gauge data and rainfall chemistry (biweekly; 1998–present): site-level rainfall; biweekly chemical analyses (pH, NO3, Cl, SO4, DOC, ammonium).
  - Throughfall data (plot-level rainfall; biweekly; 1999–present): rain captured per plot; used to derive plot-level rainfall by adjusting with site rainfall.
  - Water table depth data (biweekly; from 2009): permeable tubes measuring depth to water table.
  - Soil respiration data (fortnightly; 1998–present): CO2 efflux measured with soil collars; multiple measurement systems used over time (CIRAS-2, LI-COR LI-8100, automated systems).
  - Trace gases (CH4 and N2O) (1999–2000; 2007–2009): static chambers with gas chromatography analysis.
  - Net ecosystem CO2 exchange (NEE) (2002–2004; 2009–2011): chamber-based CO2 flux; adjustments for biomass differences within chambers.
  - Photosynthesis (2001–2003): leaf-level measurements using CIRAS-2 and a light cuvette; standardization for leaf area by species.
  - Vegetation survey data (Pin-point biomass; 1998–2012 with gaps): three quadrats per plot; 300 pins per plot; conversion to biomass using species-specific calibration; yearly updates where available.
  - Canopy reflectance (2000–2001, 2003–2004): ground-based spectroradiometer; NDVI and PRI indices.
  - Vegetation phenology, annual growth and pathogen assessment (1998–present): shoot elongation, budburst, leaf emergence, and signs of herbivory/pathogens; staging for V. myrtillus.
  - Vegetation chemistry (1998–present): carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates in green and litter material.
  - Litterfall (1999–2002; later periods): littertrap collection; drying and weighing; conversion to g m-2; carbon and nitrogen analysis.
  - Root biomass (2003–2013): soil cores and extraction with varying methods across years; analysis to biomass.
  - Soil microbial biomass (2000, 2001, 2012): chloroform fumigation method; conversion to microbial biomass carbon per g soil organic matter.
  - Nitrogen mineralisation (1998–2004): paired cores with nitrate and ammonium analyses; mineralisation and ammonification rates derived.
  - SOM, SOC and bulk density (1999–2004, 2013): core analyses; mass balance for SOM, SOC and bulk density; conversion to g m-2.
  - Soil solution and leachate chemistry (1998–2008): lysimeters and tensioned samplers; pH, nitrate, chloride, sulfate, DOC, ammonium analyses.
- Appendix: Site and plot layout details, including LYS (lysimeters), PQ (pin quadrats), SS (soil suction samplers).

## Data processing, quality, and accessibility notes
- Reference to on-site data processing and quality control:
  - Early data QC used visual inspection in Excel; various legacy processing steps noted.
  - Some datasets are not stored in the EIDC; contact CEH Bangor for access and metadata (Sabine Reinsch, Bridget Emmett).
  - Unit conversions and data harmonization across instruments (e.g., soil respiration unit conversions, NEE conversions) documented (CO2 flux units, conversion factors, gas volumes, and ideal gas law-based calculations).
  - Biomass adjustments in NEE based on chamber biomass measurements; pin-quadrat biomass calibration used for conversion of hits to biomass.
  - Throughfall and rainfall data processing involves adjusting plot rainfall using percent reductions derived from throughfall measurements; occasional data infilling with year-wide averages when data are missing.
- Data limitations and notes:
  - Legacy data may not adhere to current best practices; documentation exists to aid reprocessing.
  - Possible data gaps due to instrument issues or treatment changes (e.g., wind limits stopping curtain operation).
  - Some years have partial replicates or missing measurements; treatment means may exclude plots with compromised data.
  
## Practical considerations for analysts
- This dataset enables analysis of drought and warming effects on carbon and nutrient cycles in upland moorland, including soil respiration, NEE, canopy physiology, and vegetation dynamics.
- Important methodological considerations:
  - Differences in measurement methods across years (e.g., CIRAS-2 vs LI-COR vs automated systems) require careful unit harmonization.
  - Throughfall-derived plot rainfall requires applying percent reductions to site-level rainfall to obtain plot-level data.
  - Biomass-based adjustments are necessary when comparing flux measurements across plots with differing biomass within chambers.
- Metadata availability:
  - Each data category has corresponding supporting documentation files (RTF) detailing methods, instruments, calibration, and time frames.
  - Appendix plots and quadrat layouts provide spatial context for sampling design.

## Key references and contacts
- Supporting documentation and dataset specifics are provided within the document; for data access or clarification, contact CEH Bangor (Sabine Reinsch; sabrei@ceh.ac.uk; Bridget Emmett; bae@ceh.ac.uk).