# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose and scope
  - Climate change manipulation experiment in upland moorland using automated roof technology to simulate drought and warming for the next 20–30 years.
  - Location: Clocaenog Forest, North East Wales; features replicated drought and warming treatments with controls.
  - Site design supports map-based data visualization and spatial analysis for varied audiences (policy, clients, public).

- Site and experimental design
  - Automates climate treatments on nine plots (4 m x 5 m): three warming (W), three drought (D), three controls (C).
  - Layout features three blocks with replicates; grid reference SJ019519 (53.055N, -3.465W; 53°03'19" N, 3°27'55" W).
  - Treatment specifics:
    - Drought: retractable polyethylene roof reduces rainfall (May–Sept initially; later Apr–Oct since 2012) by roughly 14–80% depending on year; triggers via tipping-bucket sensor; curtains non-operational in high winds.
    - Warming: retractable aluminium curtains minimize infrared radiation at night; rain-triggered retraction to preserve rainfall; typical annual rainfall reduction ~14%.
  - Appendix provides site layout and Quadrat layout (0.5 m2 units); measurement areas include Lysimeters (LYS), Pin-point quadrats (PQ), and Soil suction samplers (SS).

- Data and datasets (types and coverage)
  - AWS meteorological data: daily, 1999–present; multiple sensors (temperature, humidity, rainfall, net radiation, PAR, wind, etc.).
  - Micro-meteorological (plot-level) data: daily soil/air temperature and soil moisture; 1998–present.
  - Rainfall data: site-level storage rain gauge (biweekly) and rainfall chemistry (pH, NO3, Cl, SO4, DOC, ammonium), with biweekly samples.
  - Throughfall data: plot-level rainfall (biweekly); used to derive plot-specific rainfall by applying percent-change adjustments to site rainfall.
  - Water table depth: via permeable tubes; starting 2009; measurements biweekly with maximum detectable depths per plot.
  - Soil respiration: fortnightly measurements (1999–present); both manual and automated (collars); units converted to mg CO2-C m-2 h-1.
  - Trace gases (CH4 and N2O): static chamber measurements; sampling at 0.25, 15, 30 minutes; GC analysis.
  - Net ecosystem CO2 exchange (NEE): 2002–2004, 2011; two different chamber systems; includes adjustments for biomass.
  - Photosynthesis: infrequent measurements (2001–2003) using leaf cuvettes and CIRAS-2; light response data.
  - Vegetation survey data (plant biomass) – Pin-point method: years 1998–2012 (and 2007– onward); biomass conversion factors per species; three fixed quadrats per plot.
  - Canopy reflectance: NDVI and PRI indices from ground spectrometer (2001–2004, 2000–2004); 400–950 nm bands.
  - Vegetation phenology, annual growth and pathogens: shoot elongation and phenophase tracking (1999–2009); species include Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum.
  - Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; analyses on green and litter material.
  - Litterfall: collectors across plots; 1999–2002 (monthly) then less frequent; conversion to g m-2 and C/N analysis at CEH Lancaster.
  - Root biomass: multiple years (2003–2013) using cores; different methodologies over time; detailed processing per year.
  - Soil microbial biomass: chloroform fumigation method (2000, 2001, 2012).
  - Nitrogen mineralisation: 1998–2004; core method with KCl extraction and ammonium/nitrate analyses.
  - SOM, SOC and bulk density: derived from mineral/organic soil cores; volumetric calculations to yield g m-2.
  - Soil solution and leachate chemistry: lysimeters and tensioned samplers; pH, NO3, Cl, SO4, DOC; samples biweekly (1998–2008).

- Data processing, units, and notes
  - Legacy data with heterogeneous processing; multiple measurement systems (CIRAS-2, LICOR 8100, LI-COR, EGM series) with explicit unit conversions to mg CO2-C m-2 h-1 or µmol m-2 s-1 as appropriate.
  - Plant biomass adjustments in NEE based on biomass estimates from above-ground measurements.
  - Throughfall and rainfall data require adjustments to derive plot-level rainfall; data gaps handled with exclusion or infill using year-wide averages.
  - Some datasets are not stored in the EIDC; contact CEH Bangor for complete details.
  - Data quality control described as visual/manual for several AWS and micro-met datasets; emphasis on early prototype testing and feedback loops.

- GIS relevance and spatial considerations
  - Precise plot-level layout and quadrat positions enable spatial visualization of treatments and responses.
  - Appendix 1 (Site layout) and Appendix 2 ( Quadrat layout) provide spatial references for GIS mapping.
  - Grid reference and coordinates facilitate integration with other geospatial datasets (soil properties, vegetation types, topography).
  - Multiple data layers (AWS/wildfire-like microclimates, soil profiles, vegetation structure) suitable for map-based analytics and policy/public-facing mapping.

- Access, contact, and caveats
  - Key contacts: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) for data details.
  - Some datasets described as not fully stored post-June 2015; verify current access and completeness.
  - Observational notes: high wind limitations on curtain operation; occasional data gaps due to equipment, funnel losses, or gear faults.

- End notes
  - Comprehensive, multi-decadal, multi-dataset climatology and ecosystem response data for a drought and warming field experiment.
  - Rich resource for GIS-enabled visualization of climate manipulation effects on upland heath ecosystems.