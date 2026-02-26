# Supporting information for: Chemical and physical data of water and its evolution over incubation experiments for three headwater streams in the Conwy catchment, North Wales (2014)

## Overview
- Presents chemical and physical data from incubation experiments on stream water from three headwater streams in the Conwy catchment, North Wales, conducted in 2014.
- Experiments tested effects of different treatments: controlled light exposure, sterilization (Mercury (II) chloride poisoning), and nutrient enrichment (nitrogen and phosphorus).

## Study area and sampling
- Three headwater streams:
  - Nant y Brwyn (NyB) — peat catchment
  - Glasgwm (Glg) — forested catchment
  - Hiraethlyn (Hir) — improved grassland catchment
- Field sampling locations:
  - NyB: N 52 59 20.8, W 3 48 04.9
  - Glg: N 53 02 24.2, W 3 48 21.1
  - Hir: N 53 12 17.5, W 3 46 59.1
- Incubations conducted at Environmental Centre of Wales (ECW) laboratory, Bangor, UK.
- Sampling dates in 2014:
  - NyB: May 22 and August 1
  - Glg: June 27 and September 25
  - Hir: June 13 and September 2

## Experimental design and treatments
- Incubations used 300 ml water aliquots in amber bottles with a cooling bath and a Sun Test Box CPS+ to control light exposure.
- Treatments:
  - Light vs. dark
  - HgCl2 poisoning in some light-exposed samples
  - Nutrient enrichment: nitrate (N) and phosphate (P), and both (N+P)
- Experimental runs:
  - 12–16 subsamples per run, with 3–4 treatments replicated 4–3 times each
  - Incubation duration up to 5 days with daily sub-sampling
  - Filtration through 0.45 µm Whatman filters before analysis

## Analytical methods
- Major ions and pH/alkalinity:
  - Ion Chromatography (Dionex DX-120) for cations and anions
  - pH measurement and alkalinity titration (0.02 N H2SO4)
  - Conductivity (microS/cm)
- Carbon and nitrogen:
  - Total carbon (TC), dissolved organic carbon (DOC), and non-purgeable organic carbon (NPOC) measured with Thermalox TC/TN Analyser
  - Total nitrogen (TN) by thermal oxidation with ozonation and fluorescence detection
  - For OC, different methods used depending on IC concentration (NPOC vs. TC–TIC)
- Absorbance and indices:
  - Absorbance from 200–700 nm; specific indices: E2/E3, E4/E6
- Particulate organic carbon:
  - POC determined via filtration of samples and combustion of blank-purged filters
- Quality control:
  - Instrument calibration prior to runs
  - Regular control standards and blanks
  - Coefficient of variation (cv) checks; high cv leads to reanalysis
  - CEH Bangor data quality standard: only reliable data reported

## Data structure and coding
- Core dataset structure:
  - Sample code: site abbreviation + run number + sample id
  - date_of_sampling: initial samples correspond to day d0
  - sampled_stream: NyB, Glg, or Hir
  - Treatment: one of eight combinations of light/dark with HgCl2 and/or nutrient additions
  - EC_d0, pH_d0, Alk_d0, TC_d0, DOC_d0, Abs254_d0, E2E3_d0, E4E6_d0, TN_d0, Cl_d0, Br_d0, N-NO3_d0, P-PO4_d0, SO4_d0, Li_d0, Na_d0, NH4_d0, K_d0, Mg_d0, Ca_d0, POC_d0
  - Additional day-specific measurements for day 1–5 (suffix _d1 to _d5), including Irr (irradiance), EC, pH, Alk, TC, DOC, Abs254, E2E3, E4E6, and various nutrient/ion concentrations (N-NO3_d1…N-NO3_d5, P-PO4_d1…_d5, etc.)
  - Day 5 columns also include TN_d5, Cl_d5, Br_d5, Li_d5, Na_d5, NH4_d5, K_d5, Mg_d5, Ca_d5, POC_d5
- Temporal scope:
  - Day 0 (d0) initial measurements
  - Days 1–5 (d1–d5) follow-up measurements during incubation

## Data quality and provenance
- Analyses conducted by Ophelie Fovet (INRA, Rennes) and coordinated by Chris Evans (CEH Bangor).
- Data quality emphasized through calibration, replicates, and verification; only validated values reported when uncertainties were controlled.

## Access and licensing
- Data available through the NERC Environmental Information Data Centre.
- DOI and access details provided for licensing and use restrictions:
  - https://doi.org/10.5285/eeffacad-1f23-456a-aac0-1bda40958f75
- Supporting information includes dataset-specific metadata and descriptions of measurement methods.