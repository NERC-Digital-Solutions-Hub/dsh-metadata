# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Automated climate manipulation experiment simulating drought and warming to reflect 20–30 year climate change projections.
- Location: Clocaenog Forest, North East Wales; upland moorland ecosystem dominated by Calluna vulgaris (heather).
- Established in 1998; experimental design includes replicated drought and warming treatments plus controls.

## Experimental design and climate treatments
- Treatments and layout
  - Two climate treatments: drought (D) and warming (W), each with three replicate plots (4 m x 5 m).
  - Three control plots to mirror shading from experimental structures (n = 9 plots total).
  - Experimental design arranged in blocks (Block 1–4; various mappings of treatment and control across blocks).
- Drought treatment
  - Implemented May–September (1999–2011); Apr–Oct since 2012.
  - Mechanism: retractable polyethylene roof activated by tipping-bucket rainfall sensor, reducing annual rainfall by ~20% (and excluding ~80% of growing-season rain).
  - Operative limits: not active in high winds (>10 m s⁻¹).
- Warming treatment
  - Mechanism: retractable aluminum mesh curtains at night, reflecting 96–97% of infrared radiation to reduce heat loss.
  - Rainfall interaction: roof retracted during rain to limit rainfall exclusion; overall ~14% annual rainfall reduction.
  - Operative limits: curtains not used in winds >10 m s⁻¹.
- Site and climate context
  - Location: Grid SJ019519; 53.055°N, 3.465°W.
  - Characteristics: mean annual temperature ~8.0°C; mean control soil temperature ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha⁻¹ yr⁻¹.
  - Ecosystem type: wet upland heath (Calluna vulgaris-dominated).

## Data collected and data types
- Data streams (collected 1998–present or as noted):
  - AWS meteorological data (daily; 1-minute sensors; hourly averages): temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind.
  - Micro-meteorological plot data (daily): soil and air temperature, soil moisture (TDR- or other methods).
  - Rainfall data and rainfall chemistry (biweekly to monthly): site-level storage rain gauge; rain chemistry via warren spring collectors.
  - Throughfall data (plot level rainfall; fortnighly): plot-level rainfall captured with funnels; used to derive treatment-specific rainfall changes.
  - Water table depth (biweekly): permeable tubes to bedrock; depth per plot.
  - Soil respiration (fortnightly; various methods over years): CO2 efflux measured with collars and IRGA/Li-COR systems; data converted to mg CO2-C m⁻² h⁻¹.
  - Trace gases CH4 and N2O (gas chromatography): static chamber measurements; sampling at 0.25, 15, and 30 minutes.
  - Net ecosystem CO2 exchange (NEE) (2002–2004, 2009–2011): Perspex/Li-COR chambers; data converted to mg CO2-C m⁻² h⁻¹; biomass-adjusted fluxes.
  - Photosynthesis (ambient and response curves; 2001–2007): CIRAS measurements; PAR and Ci controlled; leaf area/mass data for standardization.
  - Vegetation biomass (Pin-point method; annual surveys): 3 quadrats per plot; 300 pin-hits per plot; conversion to g m⁻² using species-specific calibration.
  - Canopy reflectance (NDVI and PRI indices): ground-based spectrometer scans (2000–2004).
  - Vegetation phenology, annual growth, and pathogens: shoot elongation and phenophases for Calluna, Vaccinium, Empetrum; herbivory and fungal infection notes.
  - Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; green and senesced material.
  - Litterfall (monthly 1999–2002; later less frequent): litter traps; weight to g m⁻²; carbon and nitrogen analyses.
  - Root biomass: multiple methods across years (2003–2011); soil cores and root extraction; species-specific calibration.
  - Soil microbial biomass (chloroform fumigation, 2000–2001, 2012): DOC difference; microbial biomass carbon expressed per g soil organic matter.
  - Nitrogen mineralisation (1998–2004): initial/final cores; NH4+/NO3− analyses; net mineralisation rates.
  - SOM, SOC and bulk density: soil core analyses; moisture corrections; conversions to g m⁻².
  - Soil solution and leachate chemistry (biweekly): lysimeters and tensioned samplers; pH, NO3−, Cl−, SO4²−, DOC, NH4+ analyses.
- Data handling notes
  - Extensive legacy data with varying documentation quality; some datasets not stored in the on-site EIDC beyond June 2015.
  - Data are stored and managed with a combination of on-site files and CEH Bangor coordination; researchers can contact CEH Bangor for details.

## Data processing, quality assurance and standardization
- Unit conversions and data harmonization
  - Standard conversions between different CO2 flux measurement devices (CIRAS-2, LICOR 8100, etc.) to mg CO2-C m⁻² h⁻¹.
  - 1) LR/CO2 flux units converted using established factors; 2) flux adjustments for biomass differences in NEE calculations using pin-point biomass data.
- Data quality and verification
  - Daily/hourly checks of AWS data via visual inspection; recognition that manual QC can capture site-specific anomalies not caught by automated limits.
  - Throughfall handling includes exclusion of plots with data loss; some infilling with average reductions across years.
  - Legacy data acknowledged for imperfect documentation of data processing steps.
- Data integration and outputs
  - Throughfall changes applied to site rainfall to derive plot-level rainfall changes.
  - Biomass calibration (pin hits to biomass) established via destructive sampling and calibration tables.
  - Canopy reflectance indices (NDVI, PRI) calculated from spectral measurements.

## Data storage, access and contact
- Data storage
  - Primary data stored in designated on-site and CEH Bangor repositories; some smaller datasets may not be stored in the Environmental Information Data Centre (EIDC) post-2015.
- Access and inquiries
  - For details on datasets and data governance, contact Sabine Reinsch (sabrei@ceh.ac.uk) or Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Appendices
  - Appendix covers site and plot layout; includes plot and quadrat configurations.

## Notable considerations for analysts
- The Climoor dataset provides a long-term, multi-dimensional view of climate manipulation effects in an upland heath ecosystem, with standardized outputs across physical (soil, rainfall, gas fluxes) and biological (biomass, phenology, chemistry) domains.
- Data interoperability across methods and years requires careful attention to unit conversions, calibration factors, and biomass adjustments.
- Ongoing data accessibility and completeness depend on dataset provenance and repository availability; cross-referencing with CEH Bangor contacts is recommended for data retrieval and provenance details.