# Function and taxonomic diversity of mycorrhizas in grassland.

## Overview
- NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biota diversity and functional roles in ecological processes.
- AM fungi diversity studied within grassland microcosms using Plantago lanceolata bioassays to assess how plant communities influence AM fungal diversity and composition.
- Study located at Sourhope field site, Scottish Borders, with controlled microcosm experiments.

## Study design and site
- Site: Sourhope, rendzina soil from limestone grassland; experimental microcosms established at the Buxton Climate Change Impacts Laboratory (Derbyshire/UK).
- Treatments and layout: three vegetated treatments plus bare soil controls:
  - Monoculture of Carex flacca
  - Monoculture of Festuca ovina
  - 12-species mixture (sedges, grasses, forbs)
  - Plus bare soil controls
- Experimental structure: 16 microcosm treatments across four replicates in randomized blocks (14 × 14 plant grid per microcosm; 192 mature plants per box; short turf maintained by clipping).
- Plant species composition represented three functional types common to limestone grasslands.

## Data collection and laboratory methods
- Bioassay: 5-day-old Plantago lanceolata seedlings transplanted into microcosms; grown for 12 weeks.
- AM diversity assessment: roots of bioassay plantlets harvested, DNA extracted, and SSU rRNA gene amplified with:
  - Eukaryotic primer NS31
  - AM fungal-specific primer AM1
- Molecular fingerprinting: ARBUScular mycorrhizal fungi diversity analyzed by TRFLP using:
  - Restriction enzymes: HinFI and Hsp92II
  - Fragment detection on ABI377 sequencer; sizing by GeneScan
- Data resolution: TRF fragments sized 45–450 bp; presence/absence of TRFs recorded (no evenness data used).
- Species richness: reported as presence/absence of TRFs (no abundance/peak height data used).

## Data structure and metadata (Dataset 1005)
- Dataset description: Arbuscular mycorrhizal (AM) fungal diversity dataset from Sheffield microcosm experiment.
- Core columns:
  - MICROCOSMID: sample type (bare soil, monocultures, or 12-species mixture)
  - TREATMENT: Sourhope soil treatment
  - SPECIES: plant composition in microcosm (C. flacca, F. ovina, or 12-species mix)
  - BAND1-60: presence (1) or absence (0) of 60 TRFs detected in P. lanceolata bioassays
- Data type: text/numeric; 60-band diversity signature as binary data
- Purpose: analyze impact of plant communities on AM fungal diversity and community composition via TRFLP fingerprints

## Quality control and limitations
- Quality checks: numeric range verification, data formatting conformity, and logical integrity checks.
- Data governance: data are subject to QA procedures; NERC disclaims liability for accuracy and fitness for purpose; no warranty for data use outcomes.

## Accessibility, references, and related reading
- Key references include:
  - Johnson et al. 2004 New Phytologist on plant communities affecting AM fungal diversity
  - Foundational work on Glomus/AMF genetics and TRFLP methodology (Vandenkoornhuyse & Leyval 1998; Helgason et al. 1998, 1999; Schüßler et al. 2001)
- Additional resources:
  - Sourhope Field Data Handbook (2003)
  - Understanding soil biodiversity in the UK Soil Biodiversity Programme (Usher et al. 2006)
- Data availability notes:
  - Dataset file: P2108_FUNGAL_DIVERSITY2.csv
  - Overall AM fungal diversity dataset associated with microcosm experiment (Dataset 1005)

## GIS and map-based visualization opportunities
- Potential map-based products:
  - Spatially structured representation of AM fungal presence/absence across microcosm plots, linked to plant community treatments.
  - Thematic layers showing TRF richness per microcosm (60-band matrix) and treatment type.
  - Overlay with soil type (rendzina) and microcosm locations to assess spatial patterns of AMF diversity in relation to soil context.
  - Temporal or comparative visuals combining plant composition with AMF diversity signatures in different treatments.
- Data integration ideas:
  - Merge Band1-60 presence/absence with metadata (MICROCOSMID, TREATMENT, SPECIES) for spatial summaries or pollution/management policy visuals.
  - Combine AMF diversity data with other soil biodiversity datasets from the same Sourhope site for multi-layer GIS analyses.
- Considerations:
  - Data are presence/absence of TRFs across controlled microcosms rather than a field-wide GIS network; spatial analysis would focus on experimental layout rather than broad geographic mapping.
  - Limitations include absence of abundance metrics and the microcosm-scale design, which should be reflected in any map-based interpretation.