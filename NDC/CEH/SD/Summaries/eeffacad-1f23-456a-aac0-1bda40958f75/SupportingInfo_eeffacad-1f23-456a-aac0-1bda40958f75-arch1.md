# Chemical and physical data of water and its evolution over incubation experiments for three headwater streams in the Conwy catchment, North Wales (2014)

- Summary
  - Dataset from Turf2Surf project Task 2 (work package 4) documenting chemical and physical properties of stream water and their evolution during 5-day incubation experiments.
  - Three headwater streams in the Conwy catchment (NyB Nant y Brwyn, Glg Glasgwm, Hir Hiraethlyn) with controlled light exposure, sterilization, and nutrient enrichment (N and/or P) treatments.
  - Aims to enable analysis of treatment and site effects on carbon, nitrogen, major ions, pH, conductivity, absorbance, and related parameters over time.

- Experimental design and sampling
  - Sites and coordinates: NyB (peat), Glg (forested), Hir (improved grassland) in Conwy catchment; in-lab incubations at ECW Bangor using a Sun Test Box CPS+ for light control.
  - Incubation setup: 12–16 subsamples per run, 3–4 treatments replicated 3–4 times; 6 phases of illumination (each 999 minutes at 765 W/m2) over 5 days.
  - Treatments: dark vs light; light-exposed samples with HgCl2 poisoning; nutrient additions with nitrate (N) and phosphate (P) alone or combined (N+P).
  - Sampling timeline: field collection on specified dates in 2014 (NyB: May 22, Aug 1; Glg: Jun 27, Sep 25; Hir: Jun 13, Sep 2). Subsamples collected daily for analysis (d0 to d5).
  - Sample handling: 5 L field bottles for major sampling; 0.5 L glass bottles for pH/alkalinity; immediate lab processing with daily sub-sampling for analyses.

- Measurements and analytic methods
  - Carbon and nitrogen: Organic carbon (OC), total nitrogen (TN), dissolved organic carbon (DOC), particulate organic carbon (POC); total carbon (TC) and non-purgeable organic carbon (NPOC) with specific measurement protocols; TIC and related calculations for OC where IC varies by site.
  - Inorganic species and major ions: major anions and cations (e.g., Cl, Br, N-NO3, P-PO4, SO4, Li, Na, NH4, K, Mg, Ca) measured by Ion Chromatography (Dionex DX-120); cations with Ionpac CS12A; anions with AS4A-SC.
  - pH and alkalinity: measured by titration (0.02 N H2SO4) on Metrohm 888 Titrando; alkalinity reported in µeq/L; pH on day 0 and day 5.
  - Conductivity: measured with a Jenway 4320 meter.
  - UV-Visible absorbance: 200–700 nm; plate reader; calculations including absorbance at 254 nm (for DOC estimation), E2/E3 (250/365 nm), E4/E6 (465/665 nm), humification index.
  - Particulate organics: POC via filtration (GF/C 47 mm, 0.2 µm), combustion at 550°C, and mass difference; details on initial filtration and conditioning of filters.
  - Quality control and calibration: instruments calibrated with relevant ranges; control standards and blanks used; analyses repeated if necessary; CEH Bangor data quality practice follows Aquacheck; coefficient of variation (cv) used to assess reliability (cv > 1 triggers reanalysis); only validated values reported.
  - Storage and handling: samples stored in the dark at <5°C if needed; cross-run checks performed.

- Data structure and variables
  - Data organization: sample, description code = station abbreviation + run + bottle; day-based measurements with d0 (initial) through d5 (end of run).
  - Example variables (per day): Irr_d1, EC_d5, pH_d5, Alk_d5, TC_d1–d5, DOC_d1–d5, Abs254_d1–d5, E2E3_d1–d5, E4E6_d1–d5, TN_d5, Cl_d5, Br_d5, N-NO3_d5, P-PO4_d5, SO4_d5, Li_d5, Na_d5, NH4_d5, K_d5, Mg_d5, Ca_d5, POC_d5.
  - Initial day (d0) measurements include EC_d0, pH_d0, Alk_d0, TC_d0, DOC_d0, Abs254_d0, E2E3_d0, E4E6_d0, TN_d0, major ions (Cl_d0, Br_d0, N-NO3_d0, P-PO4_d0, SO4_d0, Li_d0, Na_d0, NH4_d0, K_d0, Mg_d0, Ca_d0), and POC_d0.
  - Sub-samples and daily measurements are codified by station (NyB, Glg, Hir), run (r1–r3), bottle (b01–b16), and day (d0–d5); daily filtered sub-subsamples similarly coded for measurements from the daily sampling.
  - Data description and variable naming conventions are documented to allow traceability of units and methods.

- Data quality, provenance, and access
  - Data provenance: collected by Ophelie Fovet (INRA SAS) and coordinated by Chris Evans (CEH Bangor); analyses performed at CEH Bangor in ECW laboratory.
  - Documentation: comprehensive supporting information and data structure definitions provided; calibrations and QA procedures described.
  - Access and licensing: data hosted in the NERC Environmental Information Data Centre; licensing and use restrictions described at the provided doi; data content stated as reliable when measurements are validated.
  - Data citation: dataset is part of the Turf2Surf project deliverables; related DOI and project identifiers provided for traceability.

- Potential uses for Analysts
  - Analyze treatment effects (light exposure, HgCl2 poisoning, nutrient enrichment) on carbon cycling (OC, TN, POC, DOC) across streams.
  - Compare site-specific responses (peat NyB vs. forest Glg vs. grassland Hir) to illumination and nutrient additions.
  - Examine temporal dynamics over the 5-day incubation (d0–d5) and relate to cumulative irradiance (Irr_d1–Irr_d5).
  - Explore relationships among major ions, pH, alkalinity, conductivity, and organic matter metrics under different treatments.
  - Build predictive models of water chemistry responses to environmental drivers using the well-documented QA procedures and metadata.