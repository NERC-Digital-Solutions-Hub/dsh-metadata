# Chemical and physical data of water and its evolution over incubation experiments for three headwater streams in the Conwy catchment, North Wales (2014)

- Overview
  - Part of Turf2Surf project (Task 2, work package 4) producing chemical and physical data on stream water and its evolution during 5-day incubation experiments under controlled treatments.

- Study sites and field sampling
  - Three headwater streams in the Conwy catchment:
    - Nant y Brwyn (NyB; peat catchment)
    - Glasgwm (Glg; forested catchment)
    - Hiraethlyn (Hir; improved grassland catchment)
  - Field sampling in 2014: NyB on May 22 and August 1; Glg on June 27 and Sept 25; Hir on June 13 and Sept 2.
  - Water collection: 5 L plastic bottles from the stream, plus 0.5 L for pH and alkalinity; samples transported to ECW (Bangor) for incubation.
  - Incubation started immediately after sampling; samples incubated at ECW laboratory with controlled light exposure.

- Experimental design and treatments
  - Incubations conducted in a Sun Test Box CPS+ at Bangor University to control light exposure.
  - Treatments included:
    - Light vs. dark
    - Mercury (II) chloride poisoning (HgCl2) in some light-exposed samples
    - Nutrient enrichment: nitrate (N) and phosphate (P), singly or in combination (N, P, N+P)
  - Each run included 12–16 subsamples across 3–4 treatments, with 4–3 replicates per treatment.
  - Incubation setup: 6 phases of 999 minutes at 765 W/m2; samples circulated between amber bottles and incubation vessels with daily sub-sampling (d0 to d5).

- Measured parameters and analytical methods
  - Chemical and physical variables measured:
    - Major cations and anions (ions) by Ion Chromatography
    - Major carbon species: Total Carbon (TC), Dissolved Organic Carbon (DOC), Non-Purgeable Organic Carbon (NPOC), Total Inorganic Carbon (TIC), Particulate Organic Carbon (POC)
    - Nitrogen: Total Nitrogen (TN), nitrate (NO3-), ammonium (NH4+)
    - pH, alkalinity, conductivity
    - Absorbance spectra: 200–700 nm; derived indices (E254, E2E3, E4E6)
  - Specifics:
    - OC/IC/TC measured by Thermalox TC/TN Analyser with NOx detection
    - DOC measured as NPOC or TC–TIC depending on sample IC content
    - POC: filtration (GF/C filters) and combustion to determine POM/POC
    - Ion concentrations and pH/alkalinity via standard titration and Ion Chromatography
    - Absorbance measured with a plate reader; corrections against Milli-Q blank
  - Quality control and calibration:
    - Instruments calibrated with relevant ranges; control standards and blanks used regularly
    - Reanalysis if coefficients of variation (CV) were too high; only validated values reported
    - CEH Bangor adheres to Aquacheck International Testing scheme; data considered reliable when validated

- Data structure and metadata
  - Data organization:
    - Sample code: station abbreviation + run number + sample ID
    - Day 0 (d0) values establish initial conditions; day 5 (d5) values show evolution
    - Fields include date_of_sampling, sampled_stream, treatment, and a broad suite of d0 and d5 variables
  - Key variables and their descriptions:
    - Field measurements at d0: EC_d0, pH_d0, Alk_d0, TC_d0, DOC_d0, Abs254_d0, E2E3_d0, E4E6_d0, TN_d0, Cl_d0, NO3_d0, PO4_d0, SO4_d0, Li_d0, Na_d0, NH4_d0, K_d0, Mg_d0, Ca_d0, POC_d0
    - Day-by-day measurements: Irr_d1–Irr_d5, TC_d1–TC_d5, DOC_d1–DOC_d5, Abs254_d1–Abs254_d5, E2E3_d1–E2E3_d5, E4E6_d1–E4E6_d5, plus EC_d5, pH_d5, Alk_d5, TN_d5, Cl_d5, NO3_d5, PO4_d5, SO4_d5, Li_d5, Na_d5, NH4_d5, K_d5, Mg_d5, Ca_d5, POC_d5
  - Documentation and provenance:
    - Data set prepared by Ophelie Fovet (INRA) and coordinated by Chris Evans (CEH Bangor)
    - Laboratory analyses conducted at ECW ( Bangor) and CEH laboratories
    - Supporting information and data centre references provided via DOIs

- Data quality, governance and accessibility
  - Data quality:
    - Extensive QA: calibrations, controls, blanks, replication, and cross-checks
    - Replication and controls used to ensure robustness; high CV triggers reanalysis
  - Data governance:
    - Data managed with standard laboratory QA processes; metadata accompanies the dataset
    - Source institutions and coordinators identified; dataset is part of a wider research data centre
  - Access and licensing:
    - Data and licensing details available at the NERC Environmental Information Data Centre via the provided DOI
    - Access to data and information on licensing restrictions available through the data centre link

- Relevance for monitoring frameworks
  - Provides a comprehensive, well-documented dataset of water chemistry and optical properties under controlled incubation conditions, useful for:
    - Testing and calibrating indicators of terrestrial-aquatic interactions
    - Evaluating responses of carbon, nitrogen, and ionic species to light exposure and nutrient inputs
    - Informing data governance, metadata requirements, and data sharing practices in monitoring frameworks
  - Demonstrates rigorous data collection, treatment controls, QA procedures, and transparent provenance, aligning with best practices for environmental monitoring datasets