# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation experiment at Clocaenog Forest (upland moorland) using automated roof technology to create drought and warming treatments reflecting 20–30 year climate predictions. Established 1998 with replicated drought and warming treatments plus controls. Powered by solar and wind.

## Study design and climate treatments

- Treatments and replication:
  - Drought: 3 plots
  - Warming: 3 plots
  - Controls: 3 plots
  - Each plot 4 m x 5 m; arranged in 3 blocks.
- Drought treatment:
  - Annually May–September (1999–2011; since 2012 Apr–Oct)
  - Retractable polyethylene roof excludes rainfall when triggered by a tipping-bucket sensor, reducing annual rainfall by ~20% (≈80% of rain excluded during drought periods).
- Warming treatment:
  - Retractable aluminium mesh curtains over plots; reflect 96–97% of IR to reduce nighttime heat loss; rain retraction occurs when rain detected (lag can exclude some rainfall; ~14% annual rainfall reduction).
  - Curtains not operated in winds >10 m/s to prevent damage.
- Treatments designed to mimic UK drought and warming scenarios for the century.

## Site characteristics

- Location: Clocaenog Forest, North East Wales (53°03′19″N, -03°27′55″W).
- Ecosystem: Wet upland heath dominated by Calluna vulgaris (heather); other species include Vaccinium myrtillus and Empetrum nigrum; bryophytes present.
- Soil: Humo-ferric podzol with variable horizons (eluvial E, illuvial Bh); typical horizon depths mentioned.
- Vegetation cover and biomass tracked since 1998; included extensive species lists, life forms, and biomass data across years.

## Data collection and datasets

- Automated weather and microclimate data (3.0 Equipment section):
  - AWS meteorological data: minute sampling, hourly averages; sensors for temperature, humidity, rainfall, pressure, radiation (net and PAR), wind.
  - Micro-meteorological plot data: soil/air temperature and soil moisture (PMD/TD methods); daily or sub-daily logging; data since 1998.

- Rainfall and chemistry:
  - Storage rain gauge data (site-level rainfall): biweekly collection; robust against logger/power issues.
  - Rainfall chemistry: biweekly samples analyzed for pH, NO3, Cl, SO4, DOC, NH4+, using standard lab methods.

- Throughfall rainfall: plot-level rainfall using funnels; biweekly. Data used with percent-difference methods to derive plot-level rainfall; plot data excluded if measurements lost; infilling used where appropriate.

- Hydrology:
  - Water table depth: perforated tubes to bedrock; biweekly measurements; maximum depths per plot documented.

- Soil and ecosystem fluxes:
  - Soil respiration: fortnightly measurements via collars; multiple instrument evolutions (CIRAS-2, LICOR 8100, automated LI-COR system); fluxes expressed as mg CO2-C m-2 hr-1 with unit conversions described.
  - Trace gases (CH4, N2O): static chambers on the same collars; gas sampling at 0.25, 15, 30 minutes; GC analysis.
  - Net ecosystem CO2 exchange (NEE): 2002–2004 and 2011; two chamber systems; adjustments for biomass to normalize fluxes.
  - Photosynthesis: ambient measurements and response curves (PAR and Ci); multiple years; leaf-area considerations for three species; data in CIRAS outputs and CSVs.

- Vegetation and phenotype:
  - Vegetation survey data (Pin-Point biomass): annually from 1998–2012; three quadrats per plot; 300 pins per plot; pin-hits converted to biomass using calibration factors; standardization across years.
  - Canopy reflectance: NDVI and PRI from ground-based spectrometry (2001–2004); spectral bands 400–950 nm; calibration with grey standard.
  - Phenology, annual growth, pathogens: shoot elongation and growth stages for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; budburst, leaf counts, and infection/herbivory notes across select years.
  - Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; green and senesced material; lab analyses.

- Litter and roots:
  - Litterfall: 12 collectors; monthly 1999–2002; later less frequent; pooled per quadrat; converted to g m-2.
  - Root biomass: multiple methods across years (2003–2013) including soil cores, washing, imaging; analyses described in detail per year.

- Soil biogeochemistry:
  - Soil microbial biomass: chloroform fumigation-extraction (2000, 2001, 2012); DOC quantified; microbial biomass carbon calculated with correction.
  - Nitrogen mineralisation: sporadic 1998–2004; paired cores with KCl extractant to measure NH4+ and NO3-; net mineralisation rates derived.
  - SOM, SOC and bulk density: cores analyzed for SOM, SOC; bulk density from core volumes; results converted to g m-2.
  - Soil solution and leachate chemistry: lysimeters and tensioned samplers; pH, NO3-, Cl-, SO4, DOC; weekly/biweekly sampling; lab analyses described.

- Appendices:
  - Appendix 1: Site layout
  - Appendix 2: Quadrat layout (D3, E4, E7) and plotting
  - Appendix 3: Plot layout with quadrats and measurement areas

## Data processing, QA, and standardization

- Data processing:
  - Conversion and standardization of flux units (e.g., soil CO2 efflux to mg CO2-C m-2 h-1; NEE conversions to mg CO2-C m-2 h-1).
  - Biomass normalization: above-ground biomass measured in chambers by pin-point methods; biomass used to adjust flux measurements for plot biomass differences.
  - Pin-hit to biomass calibration: species-specific slopes with R-squared values noted; bryophytes pooled.
- Data quality and legacy notes:
  - Data quality control largely visual (Excel) rather than automated QC scripts; some legacy data may not follow modern best practices; data provenance and processing steps are documented with file names and methods.
  - Throughfall and plot-level data may exclude certain plots or data points if integrity is compromised; infilling applied selectively.
- Data storage and access:
  - Data summary indicates most data are stored in on-site master files and later archived; not all datasets stored in a single public portal.
  - Key contacts for data access: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.

## Accessibility and usage considerations for analysts

- Primary outputs:
  - Time-series of environmental drivers (temperature, rainfall, moisture, radiation) aligned with manipulated treatments.
  - Fluxes and ecosystem-level responses (NEE, Rs, CH4/N2O fluxes) with biomass-normalized adjustments.
  - Vegetation responses (biomass, phenology, chemistry, litterfall) integrated with soil and microbial data.
- Data considerations:
  - Legacy data may require careful interpretation; unit conversions and method changes across years documented.
  - Throughfall-based rainfall adjustments require understanding of plot-level rainfall reductions and data exclusion rules.
- Potential uses:
  - Assess treatment effects on soil respiration, NEE, and trace gas fluxes under drought and warming.
  - Link vegetation dynamics (growth, chemistry, phenology) to soil processes and carbon balance.
  - Cross-dataset analyses combining climate treatment data with soil, litter, and microbial data to evaluate ecosystem responses over time.

## Appendix: Layout references

- Appendix 1: Site layout for the experimental site
- Appendix 2: Quadrat layout and measurement areas
- Appendix 3: Plot layout with quadrats and measurement areas
- 2012 Climoor plot layout including lysimeters, pin quadrats, and soil suction samplers