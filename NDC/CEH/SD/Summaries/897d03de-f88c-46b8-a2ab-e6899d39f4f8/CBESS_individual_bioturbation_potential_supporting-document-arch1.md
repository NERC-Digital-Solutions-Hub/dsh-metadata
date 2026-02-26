# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) individual bioturbation potential in mudflat and saltmarsh habitats.

- Purpose
  - Provides an individual bioturbation potential (BPi) metric for mudflat and saltmarsh habitats as part of CBESS.
  - Data enable analysis of species-specific contributions to bioturbation and potential links to ecosystem functioning.

- Study design and locations
  - Data from 6 sites across 2 locations: Essex and Morecambe Bay.
  - Habitats: mudflat and saltmarsh at each location.
  - Saltmarsh sites chosen to represent contrasting soil types (clay in Essex, sandy in Morecambe Bay) and differing inundation/creek structures and vegetation.
  - Mudflat sites distinguished by sediment type (cohesive clays/mud/silt in Essex; coarse/mobile sediments in Morecambe Bay).
  - Monitoring period: winter and summer 2013; no planned repeats.

- Sampling and processing methods
  - Each habitat at each site sampled with 3 cylindrical cores per quadrat (depth: 10 cm; diameter: 10 cm).
  - At each quadrat: identify all fauna to species level (or appropriate taxon) from sieved residue.
  - Abundance: count individuals per species; biomass: weigh individuals after blotting to remove excess liquid.
  - convert abundance and biomass to per square metre using a calibration factor (multiply by 127.323955) to yield per m^2 values.
  - All procedures fixed in formalin, preserved in IMS, and processed under stereo microscopy.
  - Data checked by two people at input; biomass checked against abundance data; BPi calculations double-checked.

- Derived metric and calculations
  - Bioturbation potential per individual (BPi) using: BPi = (sqrt Bi) × Mi × Ri
    - Bi = individual biomass (per m^2)
    - Mi = individual species mobility
    - Ri = individual species reworking
  - BPc = sum of all BPp of all species per m^2, where BPp = BPi × Ai
    - Ai = individual species abundance per m^2
  - The dataset includes species-level BPi values and per-quadrat abundance data for computing BPi, BPc, and related metrics.

- Data structure, fields, and variables
  - Variables include season (Winter W, Summer S), location (Morecambe M, Essex E), site codes (AH, FW, TM for Essex; CS, WS for Morecambe), habitat (Mudflat MF, Saltmarsh SM), quadrat number (1–22), and spatial scales (1 m, 1–10 m, 10–100 m, beyond).
  - Measurement type: BPi (bioturbation potential per individual).
  - Species list with per-species BPi values and per-quadrat abundances (numerical counts) for a wide range of taxa (e.g., Arenicola marina, Hediste diversicolor, Macoma balthica, Corophium volutator, Crangon crangon, various molluscs, crustaceans, polychaetes, nemertea, etc.).
  - Dataset fields include: row number, season, location, site, habitat, quadrat number, scale, and per-species BPi and abundance placeholders.

- Data quality, provenance, and formats
  - Raw data entry conducted by two people with subsequent cross-checks against biomass and abundance records.
  - Calculations for BPi and derived metrics validated through independent checks.
  - Data stored in CSV format; dataset metadata notes NA for applicable calibration or data points.
  - Data and metadata designed to support discoverability and reuse (e.g., detailed site descriptions, habitat context, and measurement units).

- Practical considerations for analysts
  - The dataset supports cross-site, cross-habitat comparisons of bioturbation potential, including species-specific contributions and community-level effects.
  - Useful for exploring correlations between BPi/BPc and environmental context (sediment type, inundation, vegetation) and for informing ecosystem service assessments.
  - Limitations include the finite temporal scope (winter and summer 2013) and lack of planned repeats for longitudinal analyses; scale and accessibility considerations noted in the design (local site-level data with habitat-specific sampling).