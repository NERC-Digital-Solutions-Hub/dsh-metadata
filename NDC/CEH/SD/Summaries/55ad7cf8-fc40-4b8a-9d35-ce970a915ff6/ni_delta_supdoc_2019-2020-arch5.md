# EIDC Supporting information
Monthly atmospheric ammonia, acid gas, inorganic aerosols and base cation concentrations from Northern Ireland DELTA gas and aerosol monitoring network, 2019-2020

## Overview
- Dataset from Northern Ireland DELTA gas and aerosol monitoring network, 2019 and 2020.
- Measures monthly atmospheric concentrations of inorganic, water-soluble reactive gases and aerosols at 4 NI sites.
- Gases: NH3, HNO3, SO2. Aerosols: NH4+, NO3-, SO4 2-, Cl-, Na+, Ca2+, Mg2+.
- Jointly operated by AFBI and UKCEH; funded by DAERA, Northern Ireland.
- Data are produced to support testing atmospheric transport models and nitrogen/sulfur budgets; intended for use by researchers and policy/review bodies.

## Experimental design and monitoring aims
- DELTA® network expanded NI spatial coverage to study variability and seasonality of gas and aerosol components.
- Concurrent gas and aerosol measurements enable assessment of relationships between NH3, HNO3, SO2 and inorganic aerosol composition.
- Aims include delivering data suitable for model testing and annual budget estimation for reduced vs oxidised nitrogen and sulfur.

## Monitoring sites
- Four NI sites: Hillsborough (AFBI25), Ballynahone (AFBI26), UoU Coleraine (AFBI27), Sandholes (AFBI28).
- Site information provided, including start dates (2019), ongoing status, and approximate coordinates (reported to two decimal places for confidentiality).
- DELTA® method used at all sites with monthly sampling cycles and local operators managing sample exchange.

## UKCEH DELTA® method (sampling and analysis)
- Low-volume diffusion denuder system for long-term monitoring of NH3, HNO3, SO2, and associated aerosols.
- Sampling rate: 0.2–0.4 L min-1; volume recorded with gas meter to convert to concentrations (µg m-3).
- Monthly exposure cycles; samples exchanged by trained operators; samples collected on denuders and aerosol filters.
- Laboratory analysis of extracts:
  - Gases: HNO3, SO2 (IC), NH3 (SEAL-AA3).
  - Aerosols: NH4+, NO3-, SO4 2-, Cl-, Na+, Ca2+, Mg2+ (various methods: IC or ICP-OES; NH4+ also by SEAL-AA3).
- HONO is collected but not reported due to potential interference.
- Limits of detection (LOD) provided for each ion/compound (monthly exposure basis around 15 m3 sample volume).

## Data collected and units
- Concentrations expressed as µg m-3, calculated from measured species mass and sampled air volume.
- Major ions tracked in denuder extracts (NO3-, SO4 2-, NH4+) and in aerosol filter extracts (NO3-, Cl-, NH4+, Na+, Ca2+, Mg2+).
- Typical LODs for monthly data provided (e.g., NH4+ ~0.01 µg m-3; NO3- ~0.05 µg m-3; etc.).

## Data structure and contents
- Data organized as monthly values per site; each row represents one site per month.
- Key fields:
  - site_id, site_name, network_id (AFBI), parameter_id (gas or aerosol species with delta method), measurement_start/end dates and times, measurement value, unit (µg m-3), flags (Less_than, verification, data_capture, validity), EMEP_code, MONTH, YEAR, comments.
- Parameters include both gas-phase (e.g., delta_NH3_g, a_HNO3_g, a_SO2_g) and aerosol/particulate (e.g., a_NH4_p, a_NO3_p, a_Cl_p, a_Na_p, a_Ca_p, a_Mg_p).
- Data are accompanied by a flagging scheme to indicate detection limits, verification status, and data validity.
- Final ratified dataset is time-stamped and version-controlled.

## Quality control and data ratification process
- Three-stage QA workflow:
  - Stage 1: Automatic data checks in AAGA (Oracle database) with auto-flagging against EBAS data flags; includes date overlaps, exposure duration, flow rate checks, outlier rejection, and missing samples (-9999 placeholders).
  - Stage 2: Manual data review and flagging (ion balance checks, sampling malfunctions, outlier handling, data provenance issues).
  - Stage 3: Expert review by experienced air-quality scientists considering site context, trends, inter-site comparisons, and gas–aerosol relationships; final ratification with a locked, time-stamped output and a Ratified status.
- Output files produced contain calculated concentrations, data flags, and versioned documentation.

## Data flags and standards
- Flags conform to EBAS/EMEP standards and are harmonised with UK national networks (UK-AIR).
- Flags categorized into groups (Valid, Invalid, Missing) and subgroups for mechanical, chemical, extreme values, and data-originator decisions.
- Examples of flagged conditions:
  - Below/above detection limits, sample anomalies, instrument or filter issues, contamination, outliers, and sampling duration anomalies.
  - Specific flags cover issues like flow deviations, damaged filters, coating errors, and co-located instrument checks.
- Flags are used to communicate data quality and guide user interpretation and data integration.

## Data processing, provenance, and documentation
- Raw data and site records are stored in the AAGA Oracle-based system; calculations performed via a ShinyApp to derive concentrations.
- Ratified outputs are generated in a standard template, time-stamped, and versioned for traceability.
- References and standards cited include EN 17346 (diffusion samplers for NH3), methodological publications on DELTA®, and EBAS/NILU flag documentation.
- Data and flag guidance linked to:
  - AGANet (Acid Gas and Aerosol Network)
  - NAMN (National Ammonia Monitoring Network)
  - EBAS flag index

## Accessibility, governance, and usage
- Data governed by NI networks and national/international standards; designed for interoperability with other monitoring efforts and datasets.
- Includes documentation of methods, site specifics, LODs, QA procedures, and flag semantics to support data discovery, reuse, and audit trails.
- Data suitable for researchers, modelers, and policy assessment requiring standardized, quality-assured measurements of NH3, HNO3, SO2, and inorganic aerosol constituents.

## References and resources
- EN 17346: Ambient air – Standard method for NH3 diffusion samplers.
- Peer-reviewed DELTA® method documentation and related atmospheric chemistry studies.
- EBAS flags and guidance for data submission and quality assessment.