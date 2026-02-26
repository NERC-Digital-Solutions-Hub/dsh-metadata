# Chemical and physical data of water and its evolution over incubation experiments for three headwater streams in the Conwy catchment, North Wales (2014)

## Overview
- Task 2 of Turf2Surf project produced chemical and physical data on stream water and its evolution during incubation experiments.
- Three headwater streams in the Conwy catchment, North Wales: Nant y Brwyn (NyB), Glasgwm (Glg), and Hiraethlyn (Hir).
- Incubations manipulated light exposure, sterilization (poisoning with HgCl2), and nutrient enrichment (nitrogen and phosphorus).

## Experimental setup and sampling
- Field sampling locations and times:
  - NyB: May 22 and August 1, 2014
  - Glg: June 27 and September 25, 2014
  - Hir: June 13 and September 2, 2014
- In-field collection:
  - Water sampled in mid-stream with 5 L bottles; additional 0.5 L for pH and alkalinity.
- Incubation in laboratory:
  - Conducted at Environmental Centre of Wales (ECW), Bangor.
  - Controlled light exposure using Sun Test Box CPS+; 6 phases of 999 minutes at 765 W/m2.
  - 12–16 subsamples per run; 300 mL per subsample placed in amber bottles.
  - Dark treatments shielded; some bottles poisoned with Mercury (II) chloride or enriched with nutrients (N as nitrate; P as phosphate).
  - Sampling: a subsample taken daily for analyses (d0 to d5); filtered (0.45 µm) sub-subsamples prepared for analysis.
- Treatments (per run):
  - Light or dark exposure
  - HgCl2 poisoning
  - Nutrient additions: nitrogen (N) and/or phosphorus (P)

## Measurements and analytical methods
- Major ions and pH/alkalinity:
  - Ion Chromatography (Dionex DX-120): cations with Ionpac CS12A; anions with Ionpac AS4A-SC.
  - pH and alkalinity measured by titration (0.02 N H2SO4) and conductivity via standard meters.
- Organic and inorganic carbon:
  - Total carbon (TC), non-purgeable organic carbon (NPOC), dissolved inorganic carbon (TIC) determined with a Thermalox TC/TN Analyser.
  - OC measured as NPOC for NyB (peat-dominated) and as TC − TIC for other streams.
  - Total nitrogen (TN) determined by thermal oxidation and downstream ozonation/fluorescence detection.
- Absorbance and indices:
  - Absorbance 200–700 nm (plate reader); data used to compute:
    - Absorbance at 254 nm (for DOC proxy)
    - E2/E3 ratio (absorbance 250/365 nm)
    - E4/E6 ratio (absorbance 465/665 nm)
- Particulate carbon:
  - POC via combustion of retained particulate organic matter on GF/C filters.
- Quality control:
  - Regular instrument calibration, control standards, and blanks.
  - Re-analysis when coefficient of variation exceeded acceptable thresholds (cv > 1); only validated values reported.

## Data structure and variables
- Data were organized per sample with coded identifiers:
  - Sample = station code (NyB, Glg, Hir) + run number (r1–r3) + amber bottle number (b01–b16)
  - d0 corresponds to initial sampling; d5 corresponds to end of run
- Core data columns (example for day 0):
  - EC_d0 (microS/cm), pH_d0, Alk_d0 (µeq/L)
  - TC_d0, DOC_d0, Abs254_d0 (1/m), E2E3_d0, E4E6_d0
  - TN_d0, Cl_d0, Br_d0, N-NO3_d0, P-PO4_d0, SO4_d0
  - Li_d0, Na_d0, NH4_d0, K_d0, Mg_d0, Ca_d0, POC_d0
- Day 1–5 measurements include Irr_d1–Irr_d5 (cumulated irradiance) and corresponding day-specific chemistry and absorbance data (TC_d1–TC_d5, DOC_d1–DOC_d5, etc.), plus EC_d5, pH_d5, Alk_d5, TN_d5, and other ions.
- Data description and column metadata provide details for each variable, including units and the day of measurement (d0–d5).

## Data quality, provenance, and storage
- Analyses conducted in CEH Bangor laboratory; instrument calibration and QA procedures documented.
- Data managed to ensure reliability; when doubt existed, analyses were repeated, and only validated values were retained.
- Storage conditions: samples stored in the dark at <5°C if delayed analysis.
- Documentation notes:
  - Sufficient metadata and coding scheme for traceability (station, run, bottle, day).
  - Clear description of analytical methods and quality controls.
- Data provenance:
  - Collected and analyzed by Ophelie Fovet (INRA, France) with coordination by Chris Evans (CEH Bangor, UK).
  - Supporting information and data accessibility provided via the NERC Environmental Information Data Centre.

## Access and licensing
- Data and detailed licensing information available at the following repository:
  - NERC Environmental Information Data Centre: https://doi.org/10.5285/eeffacad-1f23-456a-aac0-1bda40958f75

## Relevance for data use and integration
- Rich, multi-parameter time-series dataset enabling examination of how light exposure, sterilization, and nutrient additions influence carbon, nitrogen, and major ion chemistry in headwater streams.
- Structured data with explicit sampling, treatment, and day-by-day measurements facilitates cross-site comparisons (NyB, Glg, Hir) and integration with other ecological or hydrological datasets.
- Detailed metadata and QA/QA protocols support data reuse, replication, and the development of data products (dashboards, summaries, self-serve analyses) for broad audiences.