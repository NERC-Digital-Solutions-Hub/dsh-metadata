# Plant biomass, soil conditions and stable isotope concentrations in soil, roots and shoots from a microcosm experiment [NERC Soil Biodiversity Programme] Cole, L., Staddon, P.L., Sleep, D. and Bardgett, R.D.

## Overview
- Describes a microcosm experiment within the NERC Soil Biodiversity Programme to understand how soil fauna diversity influences soil microbial properties and plant–microbe competition for organic nitrogen.
- Focuses on plant biomass, soil nutrients, microbial biomass, and stable isotope (15N/13C) dynamics after feeding a labelled glycine pulse.
- Data are structured for integration with GIS-like analyses of spatially organized experimental units (pots, blocks) and associated measurements.

## Context and aims
- Site: Sourhope field site, Cheviot Hills, southeast Scotland (grid NT8545019630).
- Primary aim: Elucidate how soil biota diversity affects soil processes (carbon and nitrogen cycles) and plant–microbial competition for organic nitrogen.
- Scope: 24 projects within the Soil Biodiversity Programme; this dataset (Project 2133) contributes to understanding diversity, biomass, and function of soil microarthropod communities.

## Experimental design and setup
- Microcosms: 7 cm diameter × 6 cm depth pots filled with 134 g dry-weight soil; 100 μm mesh base; defaunated by freezing, re-inoculated with microbes, moisture adjusted to 60% w/w.
- Plant system: Agrostis capillaris grown in a 2:1:1 mix (defaunated Sourhope soil: coarse silica sand: Terragreen) with bone meal phosphorus; AM fungal inoculum included.
- Faunal treatments: eight individual microarthropod species in monoculture and multi-species communities (2, 4, and 8 species), plus a predatory mite; species selected for field commonality and identifiability.
- Replication and layout: 190 microcosms in a randomized block design, with 10 replicates per treatment; protection to prevent inter-pot movement; regular watering.
- Timeline: plant establishment and growth over several months; final harvest in April 2002 after imposed faunal treatments.

## Data collected and key variables
- Faunal treatments and presence/absence indicators for each species (e.g., Onychiuridae and Isotomidae taxa; Pseudisinna etc.).
- AM fungal abundance and root colonization percentages.
- Plant biomass: shoot and root dry weights.
- Soil properties: extractable ammonia, nitrate, phosphate; total nitrogen; total soil carbon; microbial biomass carbon (MBC) and nitrogen (MBN).
- Stable isotopes: 15N and 13C ratios in roots, shoots, and soil; isotopic enrichment from glycine-213C-15N pulse.
- Microbial activity/dynamics: microbial biomass measurements post-fumigation-extraction; allocation of 15N to microbial and plant pools.
- Additional measurements: leaf/root laboratory analyses and locations tied to specific microcosms.

## Methods and measurements (highlights relevant to GIS fine-scale data)
- Isotopic labelling: glycine-213C-15N pulse with final 5 at% 15N enrichment; short incubation (~50 h) to capture plant–microbe competition dynamics.
- Biomass and tissue processing: drying and weighing of shoots/roots; AM colonization assessment via staining and microscopy.
- Isotope analysis: IRMS for 13C/12C and 15N/14N ratios; precision better than ±0.2‰ (13C) and ±0.3‰ (15N).
- Microbial biomass assessment: fumigation-extraction method with CHCl3; calculation factors for C and N (0.35 for C, 0.54 for N).
- Soil nutrient analyses: extractable ammonia, nitrate, phosphate; Olsen phosphate methodology; KCl extraction for inorganic N.
- Data provenance: measurements linked to specific pots and blocks; lab facilities include Stable Isotope Facility (Merlewood) for isotope measurements.

## Data structure and access (GIS-relevant format)
- Dataset: 1049 — Microcosm nitrogen pulse P2133_MICROCOSM_N_PULSE.csv.
- Key fields (sampled per microcosm/pot):
  - POT_NUMBER: microcosm pot identifier.
  - GLYCENE_LABELLED: labelled glycine vs. control (Yes/No).
  - WATER_TREATMENT: watering regime (e.g., watered vs. drought).
  - BLOCK: block number (1–5) for randomized design.
  - Presence/absence indicators: ONYCH (Protaphorura armata), SCHEL (Scheloribates laevigatus), ISOT (Isotoma anglicana), MESA (Mesaphorura macrochaeta), PLATY (Platynothrus peltifer), PSEU (Pseudosinella alba), HYPO (Hypoaspis aculeifer), FOLS (Folsomia quadrioculata), PRED (predatory mite).
  - AM_RLC: percent root length colonised by AM fungi.
  - Biomass measurements: SHOOT_... and ROOT (g) for harvests at multiple dates; MBC (microbial biomass C), MBN (microbial biomass N).
  - Isotope-related: ROOT_D15N, ROOT_D13C; SHOOT_D15N, SHOOT_D13C; SOIL_D15N, etc.; PERCENT_SOIL_TOTAL_N.
  - Other: various other isotopic ratios and concentration metrics recorded in downloadable formats.
- Data quality: includes numeric range checks, formatting checks, and logical integrity checks.
- Licensing and caveats: data subject to QA procedures; not guaranteed for accuracy or fitness for a particular use; liability statements included.

## Quality assurance and limitations
- Verification steps performed at data entry (range, format, logical checks).
- NERC provides no warranty on data accuracy or fitness for purpose; users assume risk for analyses and decisions.

## References and supportive materials
- Related publications and data handbooks cited for methodology and background (e.g., Sourhope Field Data Handbook 2003; ecological and isotopic methodology references).
- Links to broader context on soil biodiversity, decomposition, and isotope techniques for further methodological context.

## GIS-oriented notes for data products
- Spatial indexing: pot numbers and block design provide a clear, discrete spatial grid within the Sourhope site layout; potential to map spatial patterns of AM colonization, microbial biomass, or isotope enrichment across microcosms.
- Temporal aspects: data capture after specific growth periods and pulse labelling offers snapshots suitable for temporal GIS analyses when combined with additional time-series data.
- Integration potential: compatible with GIS layers on soil properties, vegetation, and isotope tracing to visualize interactions between soil fauna diversity, microbial activity, and plant nutrient uptake.