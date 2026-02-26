# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) nutrient exchange fluxes between sediment cores and overlying site water

## Overview
- Dataset of fluxes between sediment cores and overlying coastal water, focusing on Oxygen and nutrient fluxes (NPOC, NOx, Ammonia, Nitrite, Nitrate, Phosphate, Silicate) measured in incubation experiments.
- Purpose: quantify sediment–water inorganic nutrient exchange across different sites and habitats.

## Study Design and Location
- Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).
- Habitat contrasts: saltmarsh and mudflat with differing soil types (clay in Essex; sandy in Morecambe Bay) and varying inundation, creek structure, and vegetation.
- Temporal scope: field campaigns in winter and summer 2013.
- Sampling design: twelve quadrats per site, one sediment core per quadrat; cores incubated in tanks of locally collected seawater under daylight-simulating conditions.

## Measurements and Methods
- Oxygen flux: measured via Winkler titration on samples from the headspace and overlying water after 90 minutes; positive flux indicates sediment-to-water transfer, negative indicates water-to-sediment.
- Nutrients: after 3-hour incubations, headspace water samples filtered (0.2 μm) and analyzed for NPOC, NOx, Ammonia, Nitrite, Phosphate, and Silicate using autoanalyzers.
- Treatment conditions: light and dark incubations to capture varying fluxes; data include both conditions.
- Quality assurance: cores incubated under controlled light/temperature conditions; calibrations and standards applied; nitrate values derived from NOx and nitrite.

## Data Processing, Quality Control, and Documentation
- Flux calculations convert concentrations to flux per unit area (μmol/m2/hour); adjustments made for changes observed in water controls without sediment.
- Data quality: calibration of measurement instruments; inclusion of all measurements (no removal of anomalous data points).
- Documentation reference: Thornton et al. 2007 for context on nutrient exchange and budgets.

## Data Structure, Formats, and Metadata
- Data formats: nutrient and carbon concentrations stored as .txt files; calculations performed in Excel; final dataset provided as a .csv file.
- Dataset fields include: Season (Winter/Summer), Location (Essex/Morecambe), Site (AH, FW, TM, CS, WS, WP), Habitat (Mudflat, Saltmarsh), Quadrat Number, Scale (A–D), and flux variables (Light/Dark O2 flux, Light/Dark NPOC flux, Light/Dark Phosphate flux, Light/Dark Silicate flux, Light/Dark Ammonia flux, Light/Dark Nitrite flux, Light/Dark Nitrate flux, Light/Dark NOx flux) with corresponding units (e.g., μmol/m2/hour; μg Chl a/g).
- Data quality indicators: NA values denote missing measurements.

## Implications for Data Strategy and Stewardship
- Demonstrates end-to-end data lifecycle: robust field data collection, detailed methodological description, unit conversions, and per-core flux calculations with clear provenance.
- Highlights importance of comprehensive metadata for cross-site comparability (locations, habitats, quadrats, scales, seasonal context).
- Emphasizes data discoverability and reuse potential across collaborations by documenting data formats, processing steps, and QA procedures.
- Provides a clear example of how to link data collection with published context (references) to support reproducibility and integration into broader data ecosystems.