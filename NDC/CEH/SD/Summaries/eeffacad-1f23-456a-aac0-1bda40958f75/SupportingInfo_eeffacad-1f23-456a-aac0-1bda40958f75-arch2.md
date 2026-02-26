# Chemical and physical data of water and its evolution over incubation experiments for three headwater streams in the Conwy catchment, North Wales (2014)

## Overview
- Data from Task 2, Work Package 4 of the Turf2Surf project (NEC04596) on chemical and physical characteristics of stream water and their evolution during incubation experiments.
- Focused on three headwater streams in the Conwy catchment, North Wales, during 2014.
- Aimed at understanding how light exposure, sterilization, and nutrient enrichment affect water chemistry over time.

## Study sites and sampling
- Streams:
  - Nant y Brwyn (NyB; peat catchment)
  - Glasgwm (Glg; forested catchment)
  - Hiraethlyn (Hir; improved grassland catchment)
- Field sampling points: middle of streams using 5 L bottles; additional 0.5 L bottles for pH and alkalinity.
- Sampling dates in 2014:
  - NyB: May 22 and August 1
  - Glg: June 27 and September 25
  - Hir: June 13 and September 2
- On-site coordinates provided for each station; samples processed in the Environmental Centre of Wales (ECW) laboratory.

## Experimental design and treatments
- Incubations conducted in ECW Bangor laboratory with a Sun Test Box CPS+ to control light exposure.
- Treatments (8 total) combining light exposure with chemical additions:
  - Light or dark
  - HgCl2 poisoning (poisoning treatment)
  - Nutrient enrichment: nitrogen (N as nitrate) and/or phosphorus (P as phosphate)
- Incubation setup:
  - 12–16 subsamples per run, with 3–4 treatments replicated 4–3 times each.
  - Each subsample: 300 mL water in amber bottles, circulated between a cooling bath and vessels in the Sun Test Box.
  - Dark treatments covered; Sun box cycles through 6 phases of 999 minutes at 765 W/m2.

## Incubation logistics and coding
- Subsamples coded by station (NyB/Glg/Hir), run (r1–r3), amber bottle (b01–b16).
- Analyses taken at different times (beginning, end, or both) with day markers d0 (initial) and d5 (end).
- Daily subsamples taken for analyses using 0.45 μm filters; filtered subsamples coded by station/run/vessel/day (d0–d5).

## Analytical methods and instruments
- Major ions (anions and cations) measured by Ion Chromatography (Dionex DX-120):
  - Cations: Ionpac CS12A with 20 mM MSA as eluent
  - Anions: Ionpac AS4A-SC with NaHCO3/Na2CO3 eluents
- Carbon analyses (OC, IC, TC, NPOC, TIC, TN):
  - Thermalox TC/TN Analyser (680°C oxidation; CO2 detected by NDIR)
  - NPOC determined after acidification and sparging to remove inorganic carbon
  - TIC determined at lower furnace temperature with phosphoric acid catalyst
  - OC method chosen (NPOC for NyB; TC–TIC for others) depending on IC levels
- Particulate organic carbon (POC):
  - Filtration (GF/C 0.2 μm) of initial large volumes; combustion at 550°C; POC estimated from mass loss (assuming 50% carbon in organic matter)
- Dissolved and ancillary measurements:
  - pH and alkalinity by titration (0.02 N H2SO4)
  - Conductivity (µS/cm)
  - Absorbance spectra (200–700 nm) with 254 nm, E2/E3 (250/365 nm), and E4/E6 (465/665 nm) ratios
- Additional checks:
  - Calibration, controls, and blanks used; repeated analyses when data quality was in doubt
  - Coefficient of variation (cv) monitored; analyses redone if cv was too high (>1)

## Data structure and variables
- Structure focuses on per-sample entries with multi-day, multi-treatment data.
- Core fields include:
  - Sample Description: site + run + sample_id
  - Sampling date: date_of_sampling (d0 corresponds to initial sample)
  - Stream: NyB, Glg, Hir
  - Treatment: one of eight combinations (light/dark × HgCl2 poisoning ± N and/or P enrichment)
  - Day-specific measurements (example for day 0): EC_d0, pH_d0, Alk_d0, TC_d0, DOC_d0, Abs254_d0, E2E3_d0, E4E6_d0, TN_d0, Cl_d0, Br_d0, N-NO3_d0, P-PO4_d0, SO4_d0, Li_d0, Na_d0, NH4_d0, K_d0, Mg_d0, Ca_d0, POC_d0
  - Day 1–5 measurements include Irr_d1–Irr_d5 (cumulative irradiance), EC_d5, pH_d5, Alk_d5, TC_d5, DOC_d5, Abs254_d5, E2E3_d5, E4E6_d5, TN_d5, Cl_d5, Br_d5, N-NO3_d5, P-PO4_d5, SO4_d5, Li_d5, Na_d5, NH4_d5, K_d5, Mg_d5, Ca_d5, POC_d5
- The dataset provides a day-by-day view of how chemical and optical properties evolve under each treatment.

## Quality assurance and data reliability
- Instrument calibration performed prior to analyses.
- Use of control standards and blanks; results cross-validated with multiple injections when necessary.
- CEH Bangor adheres to Aquacheck International Testing scheme for data reliability; only validated values reported if uncertain.
- Replication within runs to ensure robustness; high variability prompted re-analysis.

## Data access and licensing
- Data and licensing details available via the NERC Environmental Information Data Centre:
  - DOI: https://doi.org/10.5285/eeffacad-1f23-456a-aac0-1bda40958f75
- Supporting information and metadata provide full methodological context and data structure definitions.