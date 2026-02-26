# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) individual bioturbation potential in mudflat and saltmarsh habitats.

## Overview and purpose
- Dataset provides individual bioturbation potential (BPi) for coastal invertebrates across mudflat and saltmarsh habitats.
- Aimed at informing environmental health monitoring and policy evaluation under the CBESS program.

## Study design, locations and habitats
- Sampling across 6 sites over 2 locations: Essex and Morecambe Bay.
- Habitats: mudflat and saltmarsh; saltmarsh sites differ in soil type (clay in Essex; sandy in Morecambe Bay) and inundation/vegetation structure.
- Temporal scope: winter and summer 2013, part of the CBESS field campaign; no planned repeats.
- Sampling units: 3 cylindrical cores per quadrat; 22 quadrats per habitat; 4 spatial scales (1 m, 1–10 m, 10–100 m, and 100 m to upper limit).
- Locations described in detail (e.g., Abbotts Hall, Fingringhoe Wick, Tillingham Marshes in Essex; Cartmel Sands and Warton Sands in Morecambe Bay).

## Data collection and processing methods
- Observations: abundance and biomass for each species; bioturbation potential (BPi) calculated per species.
- Field procedure:
  - Extract 3 sediment cores (10 cm depth, 10 cm diameter) per quadrat.
  - Preserve in 4% buffered formalin in seawater; sieve through 0.5 mm mesh.
  - Identify organisms to species (or appropriate taxon); count individuals; store in 70% IMS.
  - Biomass: blot each specimen to remove excess moisture and weigh (0.0001 g precision); small or damaged specimens weighed as 0.0001 g.
  - Convert abundance and biomass to per m^2 using a conversion factor (127.323955).
- Bioturbation calculations:
  - BPi = (sqrt(Bi)) × Mi × Ri, where Bi = biomass per individual, Mi = mobility, Ri = reworking.
  - BPc (community) = sum of BPp (per-species BPi × Ai) across all species per m^2, where Ai = species abundance per m^2.
- Data integrity: two people input raw data and double-check; biomass cross-checked against abundance data; calculations double-checked.

## Data products and structure
- File format: CSV.
- Core dataset: individual BPi values by species per site, habitat, and quadrat, across seasons.
- Dataset fields (example structure):
  - Row Number (for original order)
  - Season (Winter W, Summer S)
  - Location (Morecambe M)
  - Site (e.g., CS, WS, etc.)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A–D; different spatial extents)
  - Measurement Type (BPi; per-species)
  - Species columns (e.g., Arenicola marina, Ampharete lindstroemi, etc.) with BPi per species
- Dataset Field Descriptions provide extensive metadata for each column (site, habitat, quadrat, scale, species, and their BPi values).

## Data quality, validation and governance
- Quality assurance:
  - Raw data input by two people and double-checked.
  - Biomass validated against abundance data (CBESS_macrofauna_abundance.csv) for consistency.
  - BPi and related calculations independently double-checked.
- Calibration:
  - Calibrations are NA where not applicable.
- Documentation of data structure:
  - Detailed dataset field descriptions to facilitate interpretation and reuse.
- Data sharing considerations:
  - Underlying data sharing can be a barrier in some contexts; metadata and dataset provenance are well-documented to support transparency and reuse.

## Staff and responsibilities
- Staff responsible for the dataset: Christina Wood and Martin Solan.
- Clear attribution and methodological transparency to support monitoring framework use.

## Notes for monitoring framework authors
- Strong provenance: comprehensive field and lab methods, with explicit steps and QA checks.
- Rich metadata: extensive habitat, location, spatial scale, and species-level fields enable iso- and cross-site comparisons.
- Potential challenges:
  - Complex metadata and species-level detail require careful data governance to maintain usability.
  - Public sharing of underlying raw data may require governance steps; dataset includes clear documentation to aid reuse even when access is restricted.
- Data structure supports integration into dashboards or reports for policy scrutiny and decision-making.