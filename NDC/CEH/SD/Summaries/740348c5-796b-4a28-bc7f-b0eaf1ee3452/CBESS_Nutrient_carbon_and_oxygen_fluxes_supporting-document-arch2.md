# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) nutrient exchange fluxes between sediment cores and overlying site water

## Overview
- Dataset measuring fluxes of oxygen and key nutrients between sediment cores and the overlying water in coastal environments.
- Fluxes include Oxygen, Non Purgeable Organic Carbon (NPOC), Nitrate, Nitrite, Ammonia, Phosphate, and Silicate.
- Experiments involve submerging sediment cores in seawater and tracking changes in the overlying water under light and dark conditions to calculate flux rates.
- Positive flux indicates transfer from sediment to water; negative flux indicates transfer from water to sediment.
- Data produced as flux values per unit area (e.g., μmol/m²/hour) and converted to standard units for cross-comparison.

## Study Sites and Sampling
- Locations: Essex (Abbots Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).
- Coordinates:
  - Essex: Abbotts Hall 51.78°N, 0.87°E; Fingringhoe Wick 51.83°N, 0.97°E; Tillingham Marshes 51.68°N, 0.93°E
  - Morecambe Bay: Cartmel Sands 54.17°N, 3.00°W; Warton Sands 54.13°N, 2.80°W
- Habitats: Saltmarsh (two contrasting soil types: clay in Essex; sandy in Morecambe Bay) and mudflats (cohesive clays in Essex; coarse sediments in Morecambe Bay).
- Represented contrasts: sediment types, inundation frequency, creek structure, and dominant vegetation.
- Sampling campaign: winter and summer 2013.

## Methods and Measurements
- Sediment cores: one core per quadrat, 12 quadrats total per site, using 8 cm diameter plastic pipes; 10 cm headspace above sediment surface.
- Incubations: cores submerged in tanks of locally collected seawater; daylight-simulating lighting with seasonal variation in light and temperature.
- Light vs. dark treatments: cores incubated under both conditions to measure fluxes under different light regimes.
- Oxygen measurements:
  - After acclimation, water samples fixed via Winkler method.
  - Cores incubated for 90 minutes; headspace water sampled and fixed; DO change rates calculated.
- Nutrient measurements:
  - A 50 ml headspace water sample filtered (0.2 μm) and re-sealed; 3-hour incubation.
  - Fluxes for NPOC, NOx (nitrate/nitrite), Ammonia, Nitrite, Phosphate, and Silicate measured with autoanalyzers.
  - Nitrate values derived from NOx and nitrite measurements.
- Calibration and QA:
  - All instruments calibrated with standards; use of reference methods (e.g., Winkler for O2).
  - Adjustments made to convert to flux per unit area; accounted for changes in controls without sediment.
  - No removal of anomalous data points; all flux values retained.
- Data handling:
  - Nutrient and carbon concentrations collected as .txt files; calculations performed in Excel.
  - Final dataset provided as .csv.

## Data Structure and Formats
- Dataset fields include:
  - Row Number (sorting order)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (e.g., Cartmel Sands CS, Warton Sands WS, Essex AH/AH, FW/FW, TM/TM)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A-D; spatial resolution)
  - Flux fields for:
    - Light O2 flux (μmol/m²/hour)
    - Dark O2 flux (μmol/m²/hour)
    - μg Chl a/g (chlorophyll in sediment)
    - Light NPOC flux (μmol/m²/hour)
    - Dark NPOC flux (μmol/m²/hour)
    - Light Phosphate flux (μmol/m²/hour)
    - Dark Phosphate flux (μmol/m²/hour)
    - Light Silicate flux (μmol/m²/hour)
    - Dark Silicate flux (μmol/m²/hour)
    - Light Ammonia flux (μmol/m²/hour)
    - Dark Ammonia flux (μmol/m²/hour)
    - Light Nitrite flux (μmol/m²/hour)
    - Dark Nitrite flux (μmol/m²/hour)
    - Light Nitrate flux (μmol/m²/hour)
    - Light NOx flux (μmol/m²/hour)
    - Dark NOx flux (μmol/m²/hour)
- Data were initially stored as .txt files; final outputs provided as .csv.

## Quality Assurance and Calibration
- Flux calculations based on standardized incubation protocols; oxygen by Winkler method; nutrients by autoanalyzers.
- Cores incubated under light and dark to capture seasonal variation in photodependent processes.
- All machines calibrated with appropriate standards; nitrate values computed from NOx and nitrite.
- Data checked for anomalies but no data points were removed from the dataset.

## Variables, Calculations, and Interpretation
- Flux values indicate exchange rates between sediment and overlying water per unit area.
- Positive values: sediment-to-water flux; Negative values: water-to-sediment flux.
- Fluxes calculated for a suite of chemical species (O2, NPOC, NOx, NH4, NO2, NO3, PO4, Si) under both light and dark conditions.
- Field descriptions provide detailed metadata for each observation (season, location, site, habitat, quadrat, and scale).

## Data Access and Reuse
- Designed for environmental monitoring and cross-site comparisons.
- Encourages integration with broader CBESS datasets to enhance dataset value through data fusion and context with other environmental indicators.
- Underlying data are organized for reuse in policy and ecosystem-service assessment contexts, with clear provenance and measurement methods.

## References and Methodology Notes
- Methodological reference: Thornton et al. 2007. Sediment-water inorganic nutrient exchange and nitrogen budgets in the Colne Estuary (UK) Marine Ecology Progress Series.
- Dataset aims to provide standardized, comparable measurements of sediment-water exchange processes across contrasting coastal habitats.