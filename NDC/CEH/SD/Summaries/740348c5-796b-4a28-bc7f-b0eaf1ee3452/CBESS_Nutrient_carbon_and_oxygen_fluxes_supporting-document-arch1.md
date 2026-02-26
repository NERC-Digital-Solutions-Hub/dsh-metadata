# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) nutrient exchange fluxes between sediment cores and overlying site water

## Overview
- Fluxes of oxygen and multiple inorganic nutrients between sediment cores and overlying seawater were measured to assess sediment-water exchanges.
- Measurements collected under two light conditions (light and dark) across winter and summer 2013.

## Study sites and design
- Essex region (UK): Abbotts Hall, Fingringhoe Wick, Tillingham Marshes — saltmarsh with clay soils; mudflat sites with cohesive clays, mud, and silt.
- Morecambe Bay region (UK): Cartmel Sands, Warton Sands — saltmarsh with sandy soils; mudflat sites with coarse, mobile sediments.
- Habitat types include Saltmarsh (SM) and Mudflat (MF); sites chosen to reflect contrasting sediment types, inundation frequency, creek structure, and vegetation.
- Sampling involved 12 quadrats per core setup, across multiple sites, during winter and summer 2013.

## Variables and measurements
- Primary fluxes: Oxygen (Light O2 flux, Dark O2 flux) per unit area.
- Nutrients and related measures: NPOC, NOx, Ammonia, Nitrite, Nitrate, Phosphate, Silicate.
- Additional measure: Chlorophyll a (μg Chl a/g) in the top sediment layer.
- Flux sign convention: Positive indicates flux from sediment to overlying water; negative indicates flux from water to sediment.
- Nitrate values derived from NOx and nitrite measurements.

## Methods and data processing
- Core collection: One sediment core per quadrat (8 cm diameter) with a 10 cm headspace; three water control cores without sediment.
- Incubation: Cores submerged in tank seawater under daylight-simulating lighting; both light and dark conditions tested.
- Oxygen: Acclimation of at least 1 hour, then water samples fixed and fixed headspace samples analyzed via Winkler titration; DO change rates calculated.
- Nutrients: 50 ml headspace samples filtered (0.2 μm), incubated for 3 hours, then analyzed with autoanalyzers.
- Data conversions: Fluxes converted to units of μmol m^-2 h^-1; carbonate and nutrient concentrations adjusted for controls without sediment; nitrate calculated from NOx and nitrite.
- Quality control: Calibrations with standards; no anomalous data points removed; QA procedures ensured autoanalyzer accuracy.
- Reference: Thornton et al. (2007) for methodological details.

## Data formats and structure
- Raw data: Nutrient and carbon concentrations stored as .txt files.
- Calculations: Performed in Excel.
- Final data: Delivered as a .csv file; NA indicates missing measurements.

## Dataset fields (structure overview)
- Metadata fields: Row Number, Season (Winter or Summer), Location (Morecambe or Essex), Site (e.g., CS, WS, AH, FW, TM), Habitat (Mudflat or Saltmarsh), Quadrat Number (1–22), Scale (A–D; e.g., 1 m, 1–10 m, etc.).
- Flux measurements: Light O2 flux, Dark O2 flux, Light NPOC flux, Dark NPOC flux, Light Phosphate flux, Dark Phosphate flux, Light Silicate flux, Dark Silicate flux, Light Ammonia flux, Dark Ammonia flux, Light Nitrite flux, Dark Nitrite flux, Light Nitrate flux, Dark Nitrate flux, Light NOx flux, Dark NOx flux.
- Additional metric: μg Chl a/g (chlorophyll content in top sediment layer).

## Data quality, limitations, and considerations
- All machines calibrated with appropriate standards; quality control applied to nutrients.
- No data points removed due to aberrant values; all flux measurements included.
- Spatial and temporal scope: winter and summer 2013 across selected Essex and Morecambe Bay sites; may limit interpretation for other seasons or unrepresented habitats.
- Data scale: field plot-level cores with multiple quadrats; extrapolation to broader local scales should consider variability in habitat and inundation.

## How analysts can use this dataset
- Identify correlations between sediment type, habitat, inundation regime, and sediment-water fluxes.
- Compare oxygen and nutrient exchange between saltmarsh and mudflat habitats across regions.
- Develop predictive models of nutrient cycling under different seasonal and environmental conditions.
- Integrate with other CBESS datasets to assess broader ecosystem service implications and biodiversity outcomes.