# Climoor field site in Clocaenog forest Supporting documentation for data

- Overview of the project
  - Climate change manipulation experiment at Climoor using automated roof technology to simulate drought and warming treatments for upland moorland over the next 20–30 years.
  - Automated, solar/wind-powered setup established in 1998 with replicated drought and warming treatments and control plots.
  - Site located in Clocaenog Forest, North East Wales (53°03′19″N, -03°27′55″W); ecosystem dominated by Calluna vulgaris (heather) with additional bryophytes and vascular plants.
  - Treatments: 3 warming plots, 3 drought plots, 3 control plots (9 plots total) arranged in blocks; timing and protocols detailed per year.

- Data holdings and structure (data categories and timing)
  - AWS meteorological data (daily, 1999–present): on-site automatic weather station sensors (temp, RH, rainfall, radiation, PAR, wind, pressure).
  - Micro-meteorological plot data (daily, 1998–present): soil and air temperature, soil moisture (various methods over time).
  - Rainfall and rainfall chemistry (biweekly to monthly, 1998–present): storage rain gauge for site rainfall; Warren spring collectors for chemistry (pH, NO3, Cl, SO4, DOC, ammonium).
  - Throughfall data (plot-level rainfall, biweekly, 1999–present): plot-level rainfall via funnels; used to compute treatment-specific rainfall changes.
  - Water table depth (since 2009): permeable tubes reaching bedrock across plots; biweekly measurements.
  - Soil respiration (fortnightly to weekly; 1999–present): three collars per plot; multiple measurement systems over time (CIRAS-2, LI-COR 8100, automated systems from 2013–2014); flux in mg CO2-C m^-2 h^-1 with unit conversions.
  - Trace gases CH4 and N2O (1999–2000, 2007–2009): static chamber method with gas chromatography analyses.
  - Net ecosystem CO2 exchange (NEE) and photosynthesis (2002–2004, 2011–2011 for NEE; photosynthesis 2001–2003 and additional fixed-Ci/PAR measurements 2001–2007): different chamber setups and data conversions; biomass-adjusted fluxes.
  - Vegetation data (biomass, 1998–2012; Pin-point method): three quadrats per plot; 300 pins per plot year-by-year; biomass calibration links pin hits to biomass (g m^-2).
  - Canopy reflectance (2001–2004): ground-based spectrometry, NDVI and PRI indices calculated (NDVI680, NDVI570, PRI).
  - Vegetation phenology, annual growth, and pathogens (1998–current): leading shoot measurements for C. vulgaris, V. myrtillus, E. nigrum; phenophases and growth metrics.
  - Vegetation chemistry (1998–present): carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates on green and senesced material.
  - Litterfall (1998–2002; sporadically thereafter): monthly collection (12 collectors per plot); litter dried, weighed, and converted to g m^-2; year-by-year carbon and nitrogen analyses.
  - Root biomass (2003–2013): soil cores and various extraction/drying methods across years; detailed root separation by horizon.
  - Soil microbial biomass (2000, 2001, 2012): chloroform fumigation technique with DOC measurements and microbial biomass carbon derived from differences.
  - Nitrogen mineralisation (1998–2004): paired soil cores, initial vs final incubations, KCl extraction for NH4+/NO3- analysis.
  - SOM/SOC and bulk density (1998–2004): soil core analyses across horizons; conversions to g m^-2 using bulk density and soil depth.
  - Soil solution and leachate chemistry (1998–2008): lysimeters and tensioned samplers; pH, NO3, Cl, SO4, DOC measured; samples stored at 4°C before analysis.
  - Appendix: site and plot/layout information (Appendix 1–3) with grid references and plot design (LYS, PQ, SS indicators).

- Data processing, units, and methodology
  - Data processing spans multiple instruments and methods; long-term datasets include:
    - Soil respiration: multiple instruments (CIRAS-2, LICOR 8100, automated systems); conversions to mg CO2-C m^-2 h^-1 using specified factors; daily/weekly campaigns in some years.
    - NEE and photosynthesis: flux conversions between g CO2 m^-2 h^-1 and mg CO2-C m^-2 h^-1; biomass-adjusted fluxes based on above-ground biomass measured within chambers.
    - Trace gases: CH4/N2O analyzed by GC; standardized sampling with headspace volumes and calibration.
  - Data quality control described as visual checks in Excel; acknowledges that more formal scripted validation was not always in place, reflecting legacy data practices.
  - Some legacy notes:
    - 2013 automated soil respiration collars introduced vegetation handling that altered soil moisture conditions.
    - Throughfall data use a normalization approach to translate plot-level rainfall changes to treatment amounts; some plots excluded due to data loss.
    - Trace gas and some older datasets may lack complete documentation of processing steps.
  - Versioning: Document version 4, dated 23/09/2016; references to ongoing data stewardship and updates.

- Data governance, storage, and access
  - On-site AWS and micro-meteorological data are central; additional datasets stored in CEH Bangor environment; not all data is stored in the EIDC (Electronic Data Information Centre); some smaller or post-June 2015 data may reside outside the EIDC.
  - For access and further details, contact CEH Bangor personnel: Sabine Reinsch (sabrei@ceh.ac.uk) or Bridget Emmett (bae@ceh.ac.uk).
  - Site coordinates and layout:
    - Grid reference: SJ019519
    - Latitude/Longitude: 53.055N, -3.465W
    - Appendix 1–3 include detailed plot and quadrat layouts, including LYS (lysimeters), PQ (pin quadrats), SS (soil suction samplers).

- Particular challenges and considerations for data stewardship
  - Incomplete picture of user needs and priorities for datasets compiled across decades.
  - Timely access to data from field campaigns and legacy records.
  - Ensuring standardization across many systems and formats (AWS; micro-mets; soil cores; lysimeters; tank/instrument changes).
  - Handling large, multi-year, multi-dataset collections with varying frequencies and gaps.
  - Managing legacy processing documentation gaps; need for robust data dictionaries, metadata, and provenance trails.
  - Data gaps and potential biases due to instrumentation updates, plot-specific anomalies (e.g., drier soil around automated collars), and throughfall data exclusions.