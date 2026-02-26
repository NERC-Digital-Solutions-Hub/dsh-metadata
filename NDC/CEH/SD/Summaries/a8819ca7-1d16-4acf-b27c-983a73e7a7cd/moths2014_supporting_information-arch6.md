# Moth counts on chalk grassland and surrounding arable fields with agri-environment schemes in Hampshire, 2014

## Aim
- Investigate interactions between chalk grassland patches and surrounding arable fields under agri-environment schemes (AES) and provide data to support landscape-scale conservation insights for macro-moths.
- Data are part of a landscape-scale study and include dates, locations, management, and counts for up to 180 macro-moth species; all data are included to support analyses like those reported in Alison et al. (in press).

## Study design and data scope
- Four landscapes in north-west Hampshire near a large chalk grassland patch (SSSI) with >50% arable land within ~3 km.
- AES interventions examined: 6 m wide buffer strips (AES) and nectar flower mixes (AES) as the most common interventions across landscapes.
- In each landscape: 18 macro-moth survey locations (2 on chalk grassland; 16 on arable field margins or centres across four field pairs).
- Each landscape surveyed over six good-weather nights, with ten light traps operating simultaneously (across locations).
- Within arable fields: margins (AES treatment) vs. centres (controls); on chalk grassland, no margin/centre distinction (surveyed more frequently).

## Methods (collection and instrumentation)
- Macro-moth surveys conducted by a single observer across good-weather nights (min temp >10°C, max wind <20 km/h, low rain risk).
- Ten Heath-style actinic light traps (15 W) with solar sensors; traps placed to minimise recaptures and rotated daily.
- On arable fields: margin locations 5 m from boundary; centre locations ~45 m from boundary; CG locations surveyed twice as often as margins/centres.
- Specimens identified on-site or photographed; GPS used to record trap locations; equipment described (batteries, stands, bags, GPS, transport).

## Data structure and coding
- Date: night of trapping (YYYYMMDD).
- Landscape: three-letter codes (STO, BUR, BRO, DAN) for the four landscapes.
- Field: five-digit field code (landscape code + number + A/B), where A = AES margin (treatment) and B = control margin; for CG, A/B identify different CG sections.
- Location: two levels per field (0 = 45 m from boundary; 1 = 5 m from boundary); on CG, location codes are identifiers rather than true spatial differences.
- OS_x / OS_y: Ordnance Survey coordinates for trap locations.
- Management: habitat status at the survey location (chgr, aesi1, ctrl1, aesi0, ctrl0).
- connect_CG: connectivity to chalk grassland (derived metric; log2-transformed and centered).
- Species: scientific names for 180 macro-moth species recorded.
- Specialism: habitat affiliation (cgr = chalk grassland-associated; gra = grassland-associated; oth = other).
- Count: number of individuals of each species per trap per night.

## Analytical methods
- Connectivity to chalk grassland (CG) computed using a 100×100 m raster of CG coverage; negative exponential dispersal kernel applied with alpha = 2 to represent mean dispersal ~1 km.
- Connectivity for each cell i: Ci = sum over j ≠ i of Aj * exp(-α * dij), with Aj as CG coverage in cell j and dij as Euclidean distance; log2-transformed and centered for analysis.
- Data processing and GIS work performed in ArcMap 10.1; R (v3.0.3) used for connectivity calculations.
- Data used in the main Alison et al. study (in press) and accompanied by supporting information.

## Quality control
- Macro-moth records cross-checked by a local moth recorder.
- Three singleton records flagged as potential misidentifications but retained due to scarcity and uncertainty.

## Fieldwork instrumentation (summary)
- Ten Heath-style actinic traps (15 W) powered by SLA batteries; collapsible wooden stands; GPS (Garmin eTrex 30) for trap locations; transport by vehicle.
- Data capture and specimen handling aimed to minimize recaptures and ensure accurate spatial positioning.

## Data and usage notes
- All data from the moth counts study are included in the accompanying dataset.
- Supporting information and references provide methodological and contextual details (e.g., Merckx et al. 2009; Waring & Townsend 2009; Hanski 1994; Natural England guidelines).
- The dataset enables exploration of AES effectiveness, habitat connectivity, and species-specific habitat associations, with potential to inform self-serve analyses and dashboards for end users.