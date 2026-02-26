# Moth counts on chalk grassland and surrounding arable fields with agri-environment schemes in Hampshire, 2014

## Aim and scope
- Landscape-scale study in north-west Hampshire assessing interaction between grassland AES-managed margins and surrounding arable fields.
- Four landscapes near Andover; each includes a protected chalk grassland patch within an arable-dominated matrix.
- Dataset includes 180 macro-moth species observed across 18 survey locations per landscape (totaling 72 locations) during 24 nights of sampling in 2014.
- Data used to support analysis of AES effectiveness for macro-moths (published in Journal of Applied Ecology).

## Data collection and sampling design
- Survey period: June 2 to July 22, 2014 (six consecutive nights per landscape, across four landscapes).
- Experimental design: AES interventions consisting of either 6m buffer strips or nectar flower mixes; treatment margins vs control margins in arable fields.
- Sampling framework: 18 macro-moth survey locations per landscape (two on chalk grassland, 16 on arable field margins/centres across four field pairs, with varying connectivity to chalk grassland).
- Each night used ten light traps to sample one survey location at each arable field and two locations on chalk grassland.
- On arable fields, margin locations were 5m from the boundary (treatment) or 5m from a boundary with no AES (control); arable field centres were 45m from boundaries.

## Data structure and metadata
- Core fields include:
  - date (YYYYMMDD)
  - landscape (STO, BUR, BRO, DAN)
  - field (unique code per landscape and location; A/B denotes AES margin vs centre/CG sections)
  - location (0 = 45m from boundary, 1 = 5m from boundary)
  - OS_x / OS_y (Ordnance Survey coordinates; accurate to <10m)
  - management (chgr, aesi1, ctrl1, aesi0, ctrl0)
  - connect_CG (connectivity to chalk grassland; derived metric)
  - species (180 macro-moth species)
  - specialism (oth, gra, cgr)
  - count (number of individuals per species per trap per night)
- Data include 180 macro-moth species, with taxonomy aligned to Waring & Townsend (2009).
- Connectivity metric: calculated using a 100×100 m raster of chalk grassland cover and a negative exponential dispersal kernel (alpha = 2; mean dispersal ~1 km); values log2-transformed and centered.

## Collection methods and instrumentation
- Macro-moth surveys conducted by J. Alison using ten Heath-style actinic light traps (15 W) with solar activation at sunset/sunrise.
- Traps powered by lead-acid batteries; traps moved >50 m on subsequent visits to minimize recaptures.
- Trap locations recorded with GPS; on-site identification or photographic verification used for species.

## Data processing and analysis
- Spatial connectivity to chalk grassland quantified per survey location via GIS and R workflows.
- Species classification into habitat specialisms (CG-associated, grassland-associated, or other) based on Waring & Townsend (2009).
- Data processing includes standardization of field codes and alignment with landscape-level AES interventions.

## Quality control and validation
- Macro-moth records cross-checked by a local moth recorder.
- Three singleton records flagged as potential misidentifications (Apamea anceps, Ceramica pisi, Photedes fluxa) but retained due to uncertainty and rarity.
- Data integrity supported by accompanying supporting information, methods, and external data sources.

## Data accessibility and reuse
- Data and supporting information are accessible via DOIs provided in the work (including supplementary materials and data dictionaries).
- Dataset structured for reuse in GIS and statistical analyses (ArcMap 10.1, R 3.0.3) with clearly defined metadata and coding schemes.
- Suitable for meta-analyses on agri-environment schemes and moth connectivity, or for validating or extending similar AES impact studies.

## Considerations for data governance and stewardship
- Comprehensive metadata and a detailed data dictionary accompany the dataset, aiding discoverability and interoperability.
- Clear data lineage from field collection to processed metrics (e.g., connectivity) supports reproducibility.
- Long-term governance would benefit from explicit versioning and APIs or portals to facilitate updates and integration with related habitat/land-use datasets.