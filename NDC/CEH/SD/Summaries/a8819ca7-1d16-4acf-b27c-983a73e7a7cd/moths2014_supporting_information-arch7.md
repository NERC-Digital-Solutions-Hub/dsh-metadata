# Moth counts on chalk grassland and surrounding arable fields with agri-environment schemes in Hampshire, 2014

## Overview
- Landscape-scale study in north-west Hampshire assessing interactions between chalk grassland (CG) and adjacent arable fields under agri-environment schemes (AES).
- Focus on macro-moth responses to AES interventions and habitat connectivity to CG.
- Dataset includes dates, locations, AES management, and counts for 180 macro-moth species collected during 2014.

## Experimental design and study area
- Four landscapes selected near a large CG patch (SSSI) with >50% arable land within ~3 km.
- AES interventions studied: 6 m buffer strips (EE3) and nectar flower mixes (EF4).
- Each landscape surveyed for six nights using 18 macro-moth survey locations (two on CG, 16 on arable field margins/centres across four field pairs).
- Field pair design: within each landscape, arable fields included both treatment margins (AES present) and control margins (no AES); margins contrasted with field centers (45 m from margins).
- Survey period: June 2 – July 22, 2014.

## Data collection and instrumentation
- Macro-moth surveys conducted with ten Heath-style actinic light traps per night on good-weather nights (min temp >10°C, wind <20 km/h, low precipitation risk).
- Traps deployed in two modes: arable margins (5 m from boundary) and field centres (45 m from boundary); CG locations sampled twice as often (no margin/centre distinction there).
- Traps relocated 50 m between visits to minimize recaptures; GPS recorded trap locations; moths identified on-site or via photographs (Waring & Townsend references).
- Species classification into habitat specialisms using Waring & Townsend (2009): CG species, grassland species, or other.
- Equipment details: Heath-style actinic traps powered by SLA batteries; collapsible wooden stands; GPS (Garmin eTrex 30); field transport via a Vauxhall Meriva.

## Data structure
- Date: night of sampling (YYYYMMDD).
- landscape: three-letter codes (STO, BUR, BRO, DAN) corresponding to landscapes a–d.
- field: five-digit field code (landscape code + 1–5 + A/B). A = AES marginal treatment on arable fields; B = control margin or CG subfield identifiers.
- location: six-digit location code (field code + 0/1). 0 = 45 m from boundary; 1 = 5 m from boundary (arable only; CG uses both identifiers for internal reference).
- OS_x, OS_y: Ordnance Survey National Grid coordinates (meters).
- management: habitat/management context (chgr, aesi1, ctrl1, aesi0, ctrl0).
- connect_CG: connectivity to CG, derived metric (scaled; see GIS analysis).
- species: Latin names of 180 macro-moth species observed.
- specialism: habitat association category (oth, gra, cgr).
- count: number of individuals caught in a trap on a given night at a given location.

## GIS analysis and connectivity
- Connectivity to chalk grassland (CG) estimated by creating a 100 × 100 m raster of CG coverage using HBIC/Natural England data.
- Connectivity for each cell calculated with a negative exponential dispersal kernel (alpha = 2, representing mean dispersal ~1 km); connectivity for each survey location extracted, then log2-transformed and centered.
- Tools: ArcMap 10.1 for raster creation; R 3.0.3 for connectivity calculations.
- Output enables spatial interpretation of moth occurrence relative to CG availability and landscape structure.

## Quality control and data validation
- Macro-moth records cross-checked by a local moth recorder.
- Three singleton records flagged as potential misidentifications (Apamea anceps, Ceramica pisi, Photedes fluxa); retained due to uncertainty and rarity.

## Potential applications for GIS specialists
- Integrate this dataset with other environmental layers (land cover, habitat patches, AES boundaries) to map moth distributions and habitat connectivity.
- Reproduce or adapt the connectivity analysis using the same or alternative kernels, resolutions, and alpha values.
- Assess spatial targeting of habitat creation and its relation to moth assemblages across landscapes with varying CG connectivity.
- Use the data structure as a template for structuring similar species-by-site-by-date GIS datasets with integrated metadata and analytical variables.

## Data provenance and references
- Primary data: Alison, J. et al. 2016. Moths were surveyed by J Alison; supporting information accompanies the dataset.
- DOI: http://doi.org/10.5285/a8819ca7-1d16-4acf-b27c-983a73e7a7cd
- Related methods and data references include Merckx et al. 2009; Hanski 1994; Waring & Townsend 2009; Natural England and HBIC data sources; ArcMap 10.1 and R 3.0.3.