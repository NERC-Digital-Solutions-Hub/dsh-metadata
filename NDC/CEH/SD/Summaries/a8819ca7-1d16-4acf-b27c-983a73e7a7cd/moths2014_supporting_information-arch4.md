# Moth counts on chalk grassland and surrounding arable fields with agri-environment schemes in Hampshire, 2014

## Overview
- A landscape-scale survey of macro-moths conducted in four landscapes near chalk grassland (CG) in north-west Hampshire, central-southern England, during 2014.
- Investigates interactions between AES-created grassland margins on arable fields and long-standing semi-natural CG habitat, with data on 180 macro-moth species.
- Data include dates, locations, management details, survey results, and contextual site connectivity to CG.

## Study design
- Four landscapes adjacent to a large CG patch within SSSI and with >50% surrounding arable land.
- AES interventions studied: (i) 6-meter buffer strips along arable margins; (ii) nectar flower mixes.
- Each landscape surveyed for six consecutive good-weather nights, using ten light traps simultaneously across 18 survey locations per landscape (2 on CG, 16 on arable margins/centres).
- Layout captures varying connectivity to CG and treatment vs. control margins; aims to relate moth assemblages to AES interventions and landscape connectivity.

## Data collected
- For each trap night: date, landscape code (STO, BUR, BRO, DAN), field code, location (0 = 45 m from boundary; 1 = 5 m from boundary in arable fields; on CG, 0/1 are identifiers without margin/centre distinction).
- Location coordinates: OS_x and OS_y (Ordnance Survey National Grid), accurate to <10 m.
- Management context for each survey location: chgr (CG), aesi1 (AES intervention margin), ctrl1 (control margin), aesi0 (arable field centre near AES), ctrl0 (arable centre near control margin).
- Connectivity to CG (connect_CG), calculated per location.
- Species data: 180 macro-moth species names and their habitat specialism (cgr, gra, oth).
- Abundance data: count of individuals per species per trap per night.

## Collection methods
- Macro-moth trapping on good-weather nights (min > 10°C, max wind < 20 km/h, precipitation risk < 50%).
- Ten Heath-style actinic light traps (15 W) with solar activation at sunset/sunrise.
- On-site identification or photograph-based identification; efforts to minimize recaptures by relocating traps ~50 m between visits.
- Trap locations recorded with GPS; trap height adjusted to improve visibility when vegetation tall.
- On CG, two survey locations per CG patch; on arable margins, survey locations alternate margin vs. centre as described.

## Experimental details and management
- AES interventions defined by NE 2012 guidelines:
  - 6m buffer strips: width 6 m, pay £340/ha, managed by natural regeneration or grasses, annual cutting near crop, no fertiliser, targeted herbicides if needed.
  - Nectar flower mixes: width >6 m, pay £450/ha, sow mixtures with at least four nectar-rich species, half-strip cuts in summer, entire strip cut in autumn, no pesticides/fertilisers, re-establishment as needed.
- Landscapes sampled to capture a gradient of connectivity to CG and varying proximity to AES-treated margins.

## Data structure and metadata
- Data fields include: date, landscape, field, location, OS_x/y, management, connect_CG, species, specialism, count.
- Connectivity to CG computed using a 100×100 m raster of CG coverage; negative exponential dispersal kernel with alpha = 2 to reflect mean dispersal ~1 km.
- Location-level connectivity values log2-transformed and centered around the landscape mean.
- Data quality checks performed; cross-checks by a local moth recorder; three singleton records flagged as likely misidentifications (kept in dataset for transparency).

## Quality control and notes
- Singleton records flagged for potential misidentification; retained due to uncertainty and to maintain dataset completeness.
- Data used to support the analysis in Alison et al. (in press); includes comprehensive supporting information and metadata.

## Access and references
- Supporting information and data are linked via DOIs provided in the document.
- Key references include methods for moth identification, connectivity modeling, and AES guidelines (Merckx et al., Hanski, Natural England NE 2012/2014, Waring & Townsend, etc.).