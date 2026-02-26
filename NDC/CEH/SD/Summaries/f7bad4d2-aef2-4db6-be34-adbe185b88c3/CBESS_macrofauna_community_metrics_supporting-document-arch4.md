# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal community metrics - total abundance (TA), total biomass (TB), species richness (SR), evenness (J) and community bioturbation potential (BPc) in mudflat and saltmarsh habitats.

## Overview
- A CBESS dataset detailing macrofaunal community metrics across mudflat and saltmarsh habitats.
- Metrics included: total abundance (TA), total biomass (TB), species richness (SR), evenness based on abundance (Jabundance) and biomass (Jbiomass), and community bioturbation potential (BPc).
- Derived from field data collected at multiple sites, with rigorous data processing and quality checks to produce per-square-meter metrics.

## Data scope and design
- Spatial coverage: 6 sites across 2 locations (Essex and Morecambe Bay).
- Habitat coverage: mudflat and saltmarsh at each location.
- Saltmarsh specifics: contrasting soil types (Essex clay vs. Morecambe Bay sand) and differing inundation/vegetation structure.
- Mudflat specifics: Essex cohesive clays/mud/silt vs. Morecambe Bay coarse sediments.
- Temporal coverage: winter and summer observations in 2013.
- Sampling design: 3 replicates across 22 quadrats, at 4 spatial scales (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100–upper).
- Staff responsible for data: Christina Wood and Martin Solan.
- Data are cross-site and cross-habitat, enabling comparisons and broader ecosystem assessments.

## Sampling and data collection
- Core sampling: 3 cylindrical sediment cores per quadrat, 10 cm depth and diameter.
- Preservation and processing: cores fixed in 4% buffered formalin, sieved (0.5 mm), preserved in 70% IMS; species-level identification when possible.
- Abundance measurement: counts of all individuals per species, stored in vials with 70% IMS; minor debris categorized with presence noted.
- Biomass measurement: blotted to remove excess moisture, weighed to 0.0001 g; for very small specimens, a minimum weight of 0.0001 g recorded.
- Unit conversion: abundance and biomass converted to per m^2 using a factor of 127.323955; rounding applied (abundance to whole individuals, biomass to 0.0001 g).
- Data handling: raw data input by two people with double-checks; biomass validated against abundance data before metric calculations.

## Variables and metrics
- Core variables observed/derived:
  - Total abundance (TA) per m^2
  - Total biomass (TB) per m^2
  - Species richness (SR) per m^2
  - Evenness based on abundance (Jabundance) and based on biomass (Jbiomass)
  - BPc: community bioturbation potential per m^2
- Derived calculations:
  - H' max = ln(SR)
  - H' (abundance) and H' (biomass): Shannon-Wiener indices
  - J' (abundance) = H' / H' max; J' (biomass) = H' / H' max
  - BPc = sum of BPp across species per m^2
  - BPp for a species: BPi × Ai, where Ai is species abundance per m^2 and BPi = sqrt(Bi) × Mi × Ri
  - Bi = biomass per m^2; Mi = species mobility; Ri = species reworking
- Data fields and metadata:
  - Row Number (sorting key)
  - Season (Winter W or Summer S)
  - Location (Morecambe M or Essex E)
  - Site (AH, FW, TM, CS, WS, WP)
  - Habitat (Mudflat MF or Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A–D; 1 m to upper-range)
  - Replicate (1–3)
  - TA, TB, SR
  - H' max, H' (abundance), Jabundance
  - H' (biomass), Jbiomass
  - BPc

## Data processing and quality control
- Data entry: two-person input with double-checking.
- Consistency checks: biomass cross-validated against abundance data (in CBESS_macrofauna_abundance.csv) to ensure alignment.
- Calculations: metrics recalculated and double-checked for accuracy.
- File formats: CSV for data files.

## Documentation and data formats
- Comprehensive dataset field descriptions included (Season, Location, Site, Habitat, Quadrat Number, Scale, Replicate, and all metric columns).
- Two main data representations:
  - Raw abundance/biomass records (e.g., CBESS_macrofauna_abundance.csv)
  - Derived metrics per m^2 (TA, TB, SR, Jabundance, Jbiomass, H' values, BPc)

## Provenance and responsibilities
- Staff: Christina Wood and Martin Solan.
- Locations and sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Precisely geolocated observations (lat/long provided for each site) to support spatial analyses and integration with other datasets.

## Reuse, integration and governance
- Facilitates cross-site, cross-habitat analyses of macrofaunal communities and bioturbation potential.
- Supports data governance through explicit data processing steps, QA checks, and metadata-rich fields.
- Suitable for integration with other CBESS datasets and for informing ecological models and policy analyses.

## Gaps, challenges and considerations for data leaders
- Temporal limitation: observations restricted to winter and summer 2013 with no planned repeats.
- Data availability and discoverability: dataset references a raw abundance file; ensure access to both raw and derived data for full transparency.
- Data standardization: mindful of varying habitat soils and inundation regimes that may affect comparability across sites.
- Metadata completeness: maintain comprehensive field-level descriptions, units, and calculation methods to enable reuse by other teams.