# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) population bioturbation potential in mudflat and saltmarsh habitats.

## Overview
- Dataset on population bioturbation potential (BPp) calculated from field data across 6 sites in 2 locations, covering mudflat and saltmarsh habitats.
- Sampling occurred in winter and summer 2013 as part of the CBESS field campaign.
- Each habitat was sampled with 3 replicates across 22 quadrats, at 4 spatial scales.
- BPp derived from species abundance and biomass data collected from sediment cores.

## Location and habitat scope
- Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).
- Saltmarsh habitats represented by contrasting soil types: three sites with clay soils (Essex) and three with sandy soils (Morecambe Bay).
- Mudflat sites differ by sediment type: cohesive clays, mud and silt (Essex) versus coarse, mobile sediments (Morecambe Bay).
- Geographic coordinates provided for each site.

## Sampling and field methods
- Core sampling: 3 cylindrical cores per quadrat, depth and diameter of 10 cm.
- Fixation and preservation: cores fixed in 4% buffered formalin in seawater; residues preserved in 70% Industrial Methylated Spirit (IMS).
- Biological processing: organisms picked under a stereo microscope, identified to species or appropriate taxon; counts recorded.
- Biomass: organisms weighed, with a precision of 0.0001 g; if too light, a minimum weight of 0.0001 g recorded.
- Data conversion: abundance and biomass values scaled by 127.323955 to express results per square meter and used to compute BPp.

## Variables and data structure
- Primary measurement: BPp (Bioturbation Potential per sample population).
- Abundance data by species (per m^2) and biomass data (per m^2) for each sample.
- Species list includes numerous taxa (e.g., Arenicola marina, Hediste diversicolor, Macoma balthica, Cerastoderma edule, Crangon crangon, Gammarus spp., and many others).
- Dataset fields cover: season (Winter, Summer), location (Essex, Morecambe), site, quadrat, scale (A-D representing various spatial extents), replicate, measurement type (BPp), and species-specific BPp values and counts.

## BPp calculation details
- BPp = BPi × Ai
  - Ai = Individual species abundance per square meter.
  - BPi = (√Bi) × Mi × Ri
    - Bi = biomass per square meter.
    - Mi = individual species mobility.
    - Ri = individual species reworking.
- Abundance and biomass data are used together to derive BPp for each species within each sample.

## Quality control and data validation
- Raw data input by two people with double-checking at input.
- Biomass data cross-checked against corresponding abundance data to ensure consistency.
- BPp calculations independently double-checked.

## Data formats and metadata
- Primary file format: CSV (.csv).
- Detailed dataset field descriptions provided, including row identifiers, season, location, site, quadrat, scale, replicate, measurement type, and species-specific BPp values.

## Access, context, and intended use
- Dataset is part of the CBESS initiative and can be uploaded to data portals with metadata to promote discoverability.
- Intended use: analyse spatial and temporal patterns of bioturbation potential across habitats and sites, informing ecological models and ecosystem service assessments.
- Limitations:
  - No planned follow-up sampling (single campaign year: 2013).
  - Site- and habitat-specific variability may affect generalizability.
  - Data complexity due to numerous taxa and multiple scales and seasons.