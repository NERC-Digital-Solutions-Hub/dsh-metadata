# Nitrous oxide and methane fluxes from different riparian restoration treatments in Oil Palm plantations in Riau, Indonesia 2019-2021

## Objective and relevance for GIS specialists
- Quantify greenhouse gas fluxes (N2O, CH4, CO2) under four riparian restoration treatments to inform policy and grower practices.
- Provide geolocated, time-stamped data along river margins to support map-based analyses of riparian management, biodiversity, and ecosystem services.
- Context: riparian buffers are regulated and linked to sustainability certification; understanding spatial patterns aids spatial planning and regulation updates.

## Experimental design and study sites (geospatial context)
- Riparian Ecosystem Restoration in Tropical Agriculture (RERTA) project within BEFTA, collaboration between Cambridge University and SMARTRI.
- Two experimental sites (Kandista:2016; Ujung Tanjung:2019); this study uses Ujung Tanjung.
- Four treatments arranged in 50 x 400 m zones on both sides of a river in a plantation slated for replanting:
  1) Immature oil palm – no restoration, replanting to river margin
  2) Mature oil palm – no restoration, 50 m buffer of mature palms
  3) Native trees – enrichment planting with forest trees in a 50 m buffer, removal of all mature oil palm
  4) Mature palms + native trees – enrichment planting with forest trees and maintenance of mature palms
- 40 static chambers across zones (6 replicates per treatment, 16 in surrounding plantation).

## Field collection and geolocation (data capture)
- Chambers: round collars (40 cm diameter) installed to ~7 cm depth; lids closed for sampling with air-tight seal.
- Sampling: 0, 15, 30, 45 minutes; 100 mL samples stored in vials; analysis in the UK using GC.
- Spatial data: GPS coordinates for chamber locations; three soil moisture readings per chamber; dates of installation and sampling.
- Permits: Indonesian research permits covering multi-year scope.

## Analytical methods and data products (flux calculation)
- Gas chromatography with μECD for N2O and FID for CH4/CO2; calibration with four-point mixed standards.
- Fluxes computed from concentration changes using the RCFlux R package, fitting six models and selecting the best fit (highest R^2).
- Flux units: micromoles m^-2 s^-1; each flux accompanied by 95% confidence interval.
- Quality control: visual checks of regression plots; data marked valid/invalid; rare exclusions based on reliability.

## Data outputs and schema (ready for GIS integration)
- rerta_ghg_rcflux.csv
  - Contains flux values per chamber (1-40) for each sampling occasion (monthly, Jan 2019–Sep 2021).
  - Columns include: gasName, flux_linear, flux_quadratic, flux_linear2nd, flux_quadratic2nd, flux_asymptotic, flux_HMR, flux_bestfit, ci95lo_* and ci95hi_* for models, adjr2_* metrics, bestFitMethod, year, mon, mday, chamber, RERTA_code, position, plot, treatment_zone, treatment, date_planted, date_installed, soil_moisture, diameter_cm, height_cm, area_m2, volume_m3, lat, lon, ele_m.
  - Notes: NA indicates missing data; best-fit method specifies the model used for flux estimation.

- rerta_chambers.csv
  - Details for the 40 static chambers (CH4 and N2O sampling).
  - Columns include: RERTA_code, position (East/West of river), plot (oil palm vs riparian buffer), treatment_zone, treatment, date_planted, chamber, in_circle (inside/outside harvesting circle), date_installed, lat, lon, ele_m.
  - Provides spatial and contextual metadata needed for GIS joins and spatial analyses.

## Data quality, limitations, and processing notes
- Early-stage data quality checks prioritized, with exclusion only when clearly unreliable.
- Breaks in sampling occurred (April–Oct 2019 for felling/replanting; Jan–Jun 2021 due to COVID-19), leading to gaps in time series.
- Multiple models used for flux estimation; the best-fit model selected for each chamber and gas, with uncertainty quantified via 95% CIs and adjusted R^2.

## Potential GIS applications and considerations
- Map and analyze spatial distribution of GHG fluxes across riparian treatments and river margins.
- Overlay chamber locations with land-use, buffer width, restoration status, and replanting schedules to assess spatial policy impacts.
- Integrate with soil moisture and microclimate layers to explore drivers of gas flux patterns.
- Use time-stamped data to visualize temporal dynamics of fluxes across treatment zones.
- Consider data gaps due to sampling breaks when performing time-series analyses.

## References and project context
- BEFTA programme collaboration; key methodological references include RCFlux flux estimation, static chamber protocols, and related riparian buffer research informing policy and ecological understanding.