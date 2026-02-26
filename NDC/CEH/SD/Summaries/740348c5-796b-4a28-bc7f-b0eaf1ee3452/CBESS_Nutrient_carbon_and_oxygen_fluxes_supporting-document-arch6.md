# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) nutrient exchange fluxes between sediment cores and overlying site water

- Purpose: Dataset of fluxes describing exchange of Oxygen and multiple nutrients between sediment cores and the overlying seawater, across two contrasting coastal habitats, to support understanding of sediment–water nutrient dynamics.

## Study design and locations

- Study areas: 
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) representing mudflat and saltmarsh with clay soils.
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS) representing saltmarsh with sandy soils.
- Habitat contrasts: Essex (clay-dominated, higher inundation frequency; cohesive mudflats) vs Morecambe Bay (sandy sediments; different creek structure and vegetation).
- Monitoring period: Winter and Summer 2013 field campaign.
- Sampling units: One sediment core from each of twelve quadrats per site, plus three water-control cores (no sediment) per setup.
- Core setup: 8 cm diameter tubes, 10 cm sediment headspace; cores submerged in tanks with locally sourced seawater and daylight-simulating lighting.

## Variables and measurements

- Primary fluxes measured (per unit area, μmol/m2/hour):
  - Oxygen fluxes: Light O2 flux and Dark O2 flux.
  - Nutrients and related carbon: Light NPOC flux, Dark NPOC flux, Light Phosphate flux, Dark Phosphate flux, Light Silicate flux, Dark Silicate flux, Light Ammonia flux, Dark Ammonia flux, Light Nitrite flux, Dark Nitrite flux, Light Nitrate flux, Dark Nitrate flux, Light NOx flux, Dark NOx flux.
  - Chlorophyll indicator: μg Chl a/g measured in the surface sediment (top 5 mm) per unit dry mass (for some cores).
- Methodology:
  - Oxygen: After acclimation, water samples fixed and Winkler-determined; headspace samples fixed; 90-minute incubations to derive oxygen change rates.
  - Nutrients: 3-hour incubations with headspace water sampled before/after, filtered (0.2 μm) to measure dissolved NPOC, NOx, Ammonia, Nitrite, Phosphate, and Silicate via autoanalyzers.
  - Calculations: Fluxes adjusted for controls without sediment; nitrate values derived from NOx and nitrite measurements.
- Output units: Fluxes converted to standard units per area; final data reported as CSV. Missing values indicated as NA.
- Notes on interpretation: Positive flux indicates release from sediment to overlying water; negative flux indicates uptake from water into sediment.

## Data processing and quality control

- Data processing: All calculations performed in Excel; nutrient data in .txt format; final dataset delivered as CSV.
- Quality control: 
  - All instruments calibrated with appropriate standards.
  - Data quality checks conducted; no removal of anomalous flux values (extreme values retained).
  - Documentation links to Thornton et al. 2007 for detailed methodological background.

## Data structure and fields

- File formats:
  - Nutrient and carbon concentrations initially stored as .txt files.
  - Final dataset provided as CSV for analysis.
- Dataset fields (examples in table-like description):
  - Row Number: Original data order for sorting.
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Specific sites (e.g., CS, WS, WP in Morecambe; AH, FW, TM in Essex).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m and up).
  - Flux measurements: 
    - Light O2 flux, Dark O2 flux
    - Light NPOC flux, Dark NPOC flux
    - Light Phosphate flux, Dark Phosphate flux
    - Light Silicate flux, Dark Silicate flux
    - Light Ammonia flux, Dark Ammonia flux
    - Light Nitrite flux, Dark Nitrite flux
    - Light Nitrate flux, Dark Nitrate flux
    - Light NOx flux, Dark NOx flux
  - Additional measurement: μg Chl a/g (chlorophyll content) in the top sediment layer (where applicable).

## Data provenance and references

- Staff responsible for dataset: Anne Cotton, Graham Underwood, John Green, Terry McGenity, and Alex Dumbrell.
- Data source citation/tooling: See Thornton, D.C.O., Dong, L.F., Underwood, G.J.C., Nedwell, D.B. (2007) for sediment–water inorganic nutrient exchange and nitrogen budgets in estuarine systems (as a methodological reference).

## How this supports data use

- Facilitates self-serve analysis of sediment–water nutrient exchange across different habitats and seasons.
- Supports cross-site comparisons of oxygen and nutrient fluxes, enabling synthesis for ecosystem service and biodiversity studies.
- Provides a reproducible data structure (flux per unit area, standardized units) suitable for integration with other environmental datasets.