# Climoor field site in Clocaenog forest Supporting documentation for data

- The Climoor field site is a climate change manipulation experiment using automated roof technology to simulate drought and warming conditions predicted for the next 20–30 years.
- Location: Clocaenog Forest, North East Wales (coordinates provided). The site represents upland west-atlantic moorland dominated by Calluna vulgaris (heather) with Vaccinium myrtillus, Empetrum nigrum, and other bryophytes and mosses.
- Establishment and design: Established in 1998; replicated drought and warming treatments with three plots per treatment plus three control plots (9 plots total). Control plots include scaffolding to mirror shading from the treatment structures.
- Ecosystem and soil context: Humo-ferric podzol soil with variable eluvial (E) and illuvial (Bh) horizons; diverse plant and bryophyte communities; typical moorland biomass distribution including shrub, moss, and bryophyte components.

## Climate change treatments

- Treatments and replication
  - Drought (D): three plots
  - Warming (W): three plots
  - Control (C): three plots
- Treatment layout
  - 4 m x 5 m plots; arranged in blocks with a total of 9 plots (3 per treatment type)
- Drought treatment details
  - Operated May–September (1999–2011); since 2012, April–October
  - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor; reduces annual rainfall by ~20% and excludes ~80% of rain during the drought period
  - Wind considerations: curtains do not operate in winds >10 m/s
- Warming treatment details
  - Mechanism: retractable aluminium mesh curtains over warming plots; reflection of 96–97% of infrared radiation; reduces night heat loss by ~64%
  - Rainfall interaction: roof retraction after rain to minimize rainfall reduction; overall annual rainfall reduction ~14%
  - Wind considerations: curtains also not operated in high winds
- Temporal evolution
  - Drought timing and intensity tracked across multiple years (1997–2016 provided in tables); 1997–2014 site climate data summarized
  - Warming growing degree days (GDD) tracked from 1997 onward; 2015–2016 notes on data gaps due to logger issues or refurbishment
  - 2016 drought roofs not in operation due to refurbishment
- Data context
  - The site records climate and ecosystem responses to these treatments, enabling analyses of drought and warming impacts on plant communities, soil processes, and carbon and nitrogen cycling

## Data collected and data types

- On-site automated weather station (AWS) meteorological data
  - Variables: air temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
  - Frequency: daily; data from 1999–present (with ongoing updates)
- Micro-meteorological plot data
  - Soil and air temperature; soil moisture
  - Frequency: daily; data from 1998–present (with post-2016 half-hourly logging in some cases)
- Rainfall data and rainfall chemistry
  - Storage rain gauge at site level; biweekly sampling for chemical analyses (pH, nitrate, chloride, sulfate, dissolved organic carbon, ammonium)
- Throughfall data
  - Plot-level rainfall collected biweekly via plot-level collectors; used to compute treatment-specific rainfall changes by applying percent differences to site rainfall
- Water table depth
  - Permeable tubes installed to bedrock (from 2009); biweekly measurements
- Soil respiration
  - CO2 efflux measured using closed-chamber systems with soils collars; multiple measurement systems over time (CIRAS-2, LI-COR LI-8100, automated campaigns in 2013–2014)
  - Output: mg CO2-C m^-2 h^-1; adjustments for biomass differences across plots
- Trace gases (CH4 and N2O)
  - Measured with same collars using static chambers; gas sampling and GC analysis
- Net ecosystem CO2 exchange (NEE)
  - Measured in selected years (2002–2004, 2011) with different chamber systems; fluxes converted to mg CO2-C m^-2 h^-1; photosynthesis estimated from NEE minus respiration, adjusted for biomass
- Photosynthesis
  - Ambient measurements and response curves (A/Ci and PAR response) for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; data collected 2001–2003 and earlier years; leaf area estimated via leaf dry mass
- Vegetation biomass and canopy reflectance
  - Pin-point vegetation surveys (1998–2012; multiple years) to estimate biomass; conversion from pin hits to biomass using species-specific calibration factors
  - Canopy reflectance indices (NDVI and PRI) from ground-based spectrometry
- Vegetation phenology and growth
  - Phenophase recording, shoot elongation, leaf counts, herbivory, and fungal infection indicators; sampling across several years (1999–2009, etc.)
- Vegetation chemistry
  - Green and senesced tissue chemical analysis for carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates
- Litterfall
  - Litter traps (monthly to yearly sampling; 1999–2002; later intervals less frequent); oven-dried and weighed; carbon and nitrogen analyses
- Root biomass
  - Various methods across years (2003–2011) including soil cores and root extraction; freezing and subsequent analysis; depth- and segment-specific root measurements
- Soil microbial biomass
  - Chloroform fumigation incubation to determine microbial biomass carbon; analysis via DOC difference
- Nitrogen mineralisation
  - Field incubations with initial and final cores; extractants and analyses for ammonium and nitrate; rates calculated from core comparisons
- Soil organic matter (SOM), soil organic carbon (SOC), and bulk density
  - SOM and SOC determined from cores; mass-based calculations converted to g m^-2 using bulk density
- Soil solution and leachate chemistry
  - Lysimeters and tension samplers; biweekly to monthly sampling; analyses for pH, NO3, Cl, SO4, DOC
- Data structure and accessibility
  - Data summarized in multiple files (RTF and CSV) with detailed sensor methods, time scales, and units
  - Not all data stored in the EIDC (Environmental Information Data Centre); some smaller or post-June 2015 datasets are outside the portal
  - Primary contacts for data access and details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor

## Data processing, quality, and notes

- Data processing
  - Field data collected with a variety of instruments over time; legacy data may lack uniform documentation of processing steps
  - Soil respiration data converted across measurement systems using specified formulas; CO2 flux conversions account for units from CIRAS-2 and LICOR 8100
  - Pin-hit to biomass conversion factors provided for multiple species; calibration via destructively harvested plots
  - Throughfall and rainfall data reconciled using percent-change calculations and infilling when necessary
- Quality and limitations
  - Data quality control relied on visual checks in Excel; not all automated quality thresholds were applied
  - Some measurements were added during technology transitions (e.g., evolving soil respiration equipment)
  - Earlier datasets (pre-2008) may have inconsistent sampling methods; “legacy data” note applies to processing documentation
- Documentation and appendices
  - Appendix 1: Site layout; Appendix 2: Quadrat layout; Appendix 3: Plot layout with quadrats and measurement areas
  - Tables detail treatment timings, site characteristics, and conversion factors

## Practical considerations for analysts

- The dataset offers rich, multi-decadal, multi-treatment data linking climate manipulations (drought and warming) to ecosystem responses across plants, soil processes, and biogeochemical cycles.
- Key analytical opportunities
  - Assess drought vs warming effects on plant biomass, phenology, and canopy indices
  - Link rainfall manipulation to soil respiration, NEE, trace gas fluxes, and soil solution chemistry
  - Explore how biomass and litter inputs mediate carbon and nutrient cycling under altered climate conditions
- Data access and governance
  - Some data are not in the EIDC; contact CEH Bangor researchers for access to complete datasets and metadata
  - Reference files and data collection methods are documented, with explicit conversion factors and protocols to support reproducibility

- Appendix resources
  - Site and plot layout diagrams provide spatial context for experiments and measurement areas