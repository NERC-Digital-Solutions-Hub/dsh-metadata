# Supporting information for: Chemical and physical data of water and its evolution over incubation experiments for three headwater streams in the Conwy catchment, North Wales (2014)

- The dataset provides chemical and physical water data and their evolution during incubation experiments across three headwater streams in the Conwy catchment, North Wales, collected in 2014.
- Part of Task 2, Work Package 4 of the Turf2Surf project; hosted and curated by CEH Bangor within the NERC Environmental Information Data Centre.

## Data scope and content

- Study sites:
  - Nant y Brwyn (NyB), peat catchment
  - Glasgwm (Glg)
  - Hiraethlyn (Hir)
- Treatments during incubations:
  - Light vs. dark exposure
  - HgCl2 poisoning
  - Nutrient additions: nitrogen (as nitrate), phosphorus (as phosphate), or both (N+P)
- Measured parameters (at initial day d0 and daily days d1–d5):
  - Major chemical species: total carbon (TC), dissolved organic carbon (DOC), particulate organic carbon (POC), total nitrogen (TN), various cations and anions (e.g., Cl, Br, N-NO3, P-PO4, SO4, Li, Na, NH4, K, Mg, Ca)
  - General water chemistry: pH, electrical conductivity (EC), alkalinity
  - Optical/trace metrics: absorbance (200–700 nm), E2/E3 and E4/E6 ratios
  - Additional metrics: OC/IC/TIC, NPOC, and related measurements
- Field and incubation setup:
  - Field sampling in streams using 5 L bottles; additional 0.5 L bottles for pH and alkalinity
  - Incubations conducted at Environmental Centre of Wales (ECW) lab, Bangor, using a Sun Test Box CPS+ to control light (6 phases; ~999 min per phase; ~765 W/m2)
  - Analyses performed at CEH lab in ECW
- Sampling timeline:
  - NyB: May 22 and Aug 1, 2014
  - Glg: Jun 27 and Sep 25, 2014
  - Hir: Jun 13 and Sep 2, 2014
- Laboratory procedures:
  - Ion chromatography (Dionex DX-120) for major ions; cations with Ionpac CS12A; anions with AS4A-SC
  - TC/TN analysis with a Thermalox TC/TN Analyser (oxidation, NDIR for CO2; NPOC via acidification and sparging)
  - POC via particulate matter combustion after filtration
  - pH and alkalinity via titration (0.02 N H2SO4); conductivity via standard meter
  - Absorbance measurements with a plate reader; specific indices computed (E2E3, E4E6)
- Sample handling and replication:
  - In each run, 12–16 subsamples per treatment with 3–4 treatments replicated 4–3 times
  - Daily subsampling for analytical measurements (0.45 μm filtered)
  - Initial and end-of-run measurements recorded (d0 and d5)

## Data structure and metadata

- Data structure:
  - Sample code: site abbreviation + run number + sample ID (NyB/Glg/Hir + r1–r3 + b01–b16)
  - date_of_sampling: day of stream sampling (d0 corresponds to initial sampling)
  - sampled_stream: NyB, Glg, or Hir
  - Treatment: listed as light/dark with optional +HgCl2, +N, +P, or +N+P
  - Day-specific columns for indices and concentrations (e.g., EC_d0, pH_d0, Alk_d0, TC_d0, DOC_d0, Abs254_d0, E2E3_d0, E4E6_d0, TN_d0, Cl_d0, N-NO3_d0, P-PO4_d0, etc.)
  - Day 1–5 variables include Irr_d1–Irr_d5 (cumulative irradiance) and corresponding chemical/optical measurements (TC_d1–TC_d5, DOC_d1–DOC_d5, Abs254_d1–Abs254_d5, E2E3_d1–E2E3_d5, E4E6_d1–E4E6_d5, EC_d5, pH_d5, Alk_d5, TN_d5, Cl_d5, N-NO3_d5, P-PO4_d5, SO4_d5, Li_d5, Na_d5, NH4_d5, K_d5, Mg_d5, Ca_d5, POC_d5)
- Data provenance and quality:
  - Analyses performed with instrument calibration in relevant ranges; use of control standards and blanks
  - Coefficients of variation (CV) monitored; analyses redone if CV too high; only validated data reported
  - Data quality aligned with Aquacheck International Testing scheme; data deemed reliable when validated
  - Storage of samples and data kept in dark, <5°C when not in use

## Access, licensing, and data management

- Access and licensing details available at the dataset’s DOI page:
  - https://doi.org/10.5285/eeffacad-1f23-456a-aac0-1bda40958f75
- Data are provided as supporting information to the main dataset and are intended for research use under the specified terms and licensing on the NERC Environmental Information Data Centre

## Relevance for data leadership and stewardship

- Demonstrates end-to-end data lifecycle: field collection, controlled incubation experiments, standardized laboratory analyses, and daily time-series data
- Rich metadata and explicit coding scheme for samples, runs, and days support reproducibility and discoverability
- Emphasizes data quality practices (calibration, controls, replication, CV monitoring) and clear criteria for validating reported values
- Provides a structured schema that can inform data governance, metadata standards, and cross-study integration in water chemistry and incubation experiments
- Data availability through a stable data centre with licensing information facilitates long-term stewardship and cross-institution collaboration