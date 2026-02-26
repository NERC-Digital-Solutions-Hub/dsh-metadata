# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment chlorophyll concentrations in saltmarsh and mudflat habitats

## Overview
- Datasets record surface sediment chlorophyll concentrations (µg g-1) for chlorophyll a, b, and c1+c2 in MPB-associated communities.
- Sampling occurred across saltmarsh and mudflat habitats during winter and summer 2013.
- Two UK regions: Essex (saltmarsh and mudflat) and Morecambe Bay (saltmarsh and mudflat), with contrasting sediment types and inundation characteristics.

## What was measured
- Chlorophyll concentrations in surface sediment (top 2 mm): 
  - Chlorophyll a (µg g-1)
  - Chlorophyll b (µg g-1)
  - Chlorophyll c1+c2 (µg g-1)

## Sampling design and locations
- Replicates: Five replicates per quadrat for both habitat types and seasons.
- Sites and regions:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitat types: Saltmarsh (SM) and Mudflat (MF).
- Spatial arrangement: 22 randomly allocated 1x1 m quadrats per site (per habitat type), using R to define four spatial scales.
- Geographic coordinates provided for each site (Essex and Morecambe Bay).

## Data collection and processing
- Field sampling: Surface sediments (2 mm) collected with a contact corer; samples flash-frozen with liquid nitrogen and stored in darkness below -80°C.
- Laboratory processing: 
  - Samples dried via freeze-drying (Edwards EF4 Modulyo).
  - Chlorophyll extracted from ~100 mg sub-sample using acetone.
  - Quantification with Cecil CE3021 spectrophotometer at 630, 647, 664, and 750 nm.
  - Concentrations derived using standard equations.
- Spatial allocation: Quadrats randomly assigned; 22 per site per habitat type.

## Data structure and formats
- File formats: CSV.
- Core fields (examples):
  - Season (Winter, Summer)
  - Location (Essex or Morecambe)
  - Site (AH, FW, TM, CS, WS, WP)
  - Habitat (Mudflat or Saltmarsh)
  - Quadrat Number (1–22)
  - Scale (A-D; e.g., A=1 m, B=1–10 m, C=10–100 m, D=100–upper limit)
  - Chl a (µg g-1) – Average and StDev
  - Chl b (µg g-1) – Average and StDev
  - Chl c1+c2 (µg g-1) – Average and StDev
- Dataset notes: Missing data indicated as NA where samples were inaccessible.

## Quality control and calibration
- Calibration: Scales calibrated according to laboratory protocols; spectrophotometer accuracy verified with standard chlorophyll solutions.
- Data entry and QC: Readings entered into spreadsheets; spectrophotometer software (Cecil Datastream) used for absorption data.
- Documentation of procedures: Detailed methodological steps and field/lab protocols recorded to support reproducibility.

## Notes and caveats
- No repeat sampling planned beyond the 2013 winter/summer campaign.
- Data include potential variability across sites, habitats, and seasons; some site descriptions highlight contrasting sediment types and inundation regimes that could affect chlorophyll concentrations.
- Random quadrat allocation aids statistical analysis but may still reflect patchiness in MPB-associated chlorophyll.

## Potential data use and integration
- Suitable for cross-site comparisons of MPB chlorophyll content across saltmarsh and mudflat habitats.
- Can be combined with metadata on sediment type, inundation, and vegetation to explore drivers of chlorophyll variability.
- Useful for time-point analyses within 2013 winter and summer, and as a baseline for future comparisons if additional sampling is undertaken.