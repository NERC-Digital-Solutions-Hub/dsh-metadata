# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment colloidal carbohydrate concentration in saltmarsh and mudflat habitats

## Overview
- Dataset measuring concentration of colloidal carbohydrates in surface sediments, reported as glucose equivalents (µg g⁻¹).
- Winter and summer 2013 sampling as part of the CBESS field campaign.
- Five replicates per quadrat for both mudflat and saltmarsh habitats.

## Study Sites and Spatial Coverage
- Regions: Essex (southeast Atlantic UK) and Morecambe Bay (west UK).
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Site selection reflects contrasting habitat types and sediment characteristics:
  - Saltmarsh: two soil types (three with clay in Essex; three sandy in Morecambe Bay).
  - Mudflat: Essex with cohesive clays/mud/silt; Morecambe with coarse, mobile sediments.
- Location coordinates are provided for each site.

## Sampling Design and Temporal Coverage
- Habitat types: saltmarsh and mudflat at each site.
- Temporal scope: winter and summer 2013; no planned repeat sampling.
- Quadrats: 22 quadrats per site, each 1 m × 1 m, with random allocation.
- Spatial scales (based on quadrat separation):
  - A: 1 quadrat (1 m scale)
  - B: 3 quadrats (1–10 m apart)
  - C: 6 quadrats (10–100 m apart)
  - D: 12 quadrats (100 m–1,000 m or site maximum apart)

## Data Collected and Measurements
- Primary variable: colloidal carbohydrate concentration (µg g⁻¹) in surface sediment (glucose equivalents).
- Replication: five replicates per quadrat.
- Additional measurements: wet/dry weights to calculate water content; standard deviations for each site/quadrat.
- Laboratory method: Dubois phenol-sulphuric assay on dried sediment samples after preparatory processing (freeze with liquid nitrogen, remove unfrozen sediment, freeze-dry, weigh).
- Sample processing: sub-sample (50–500 mg) treated with distilled water, vortexed, centrifuged; color developed with sulfuric acid and phenol; absorbance read at 486.5 nm.
- Calibration/quality control: regression against glucose standards; spectrophotometer calibrated with standard dilutions.

## Data Format and Metadata
- File format: CSV.
- Data fields include: Season (Winter W, Summer S), Location (Essex E, Morecambe M), Site (AH, FW, TM, CS, WS, WP), Habitat (Mudflat MF, Saltmarsh SM), Quadrat Number (1–22), Scale (A–D), Colloidal Carb (µg g⁻¹), StDev, plus row/column descriptors.
- NA indicates missing data due to inaccessibility of a quadrat.
- Metadata details cover sampling protocol, site descriptions, and data processing steps; location descriptions and scale definitions are documented.

## Data Quality and Considerations
- Zeros indicate colloidal carbohydrate concentration below detectable level.
- Data were collected at a single time point per season; no longitudinal repeats within the dataset.
- Random quadrat placement and multiple spatial scales enhance representativeness but require careful interpretation when aggregating across scales.

## Accessibility and Use
- Data are organized with clear provenance (staff responsible, site descriptions, sampling methods).
- Intended for integration into data portals with metadata; ready for analysis in statistical software (CSV format) and potential model development to explore spatial/seassonal patterns.

## Practical Implications for Analysts
- Useful for examining correlations between sediment type, habitat, and colloidal carbohydrate concentration across two UK regions.
- Facilitates comparisons of saltmarsh vs. mudflat carbohydrate dynamics under contrasting inundation and sediment conditions.
- Can inform exploratory models of ecosystem service provisioning linked to sediment biochemistry.
- Consider the single-time-point limitation when inferring trends; potential for combining with other CBESS datasets or future repeats for temporal analysis.