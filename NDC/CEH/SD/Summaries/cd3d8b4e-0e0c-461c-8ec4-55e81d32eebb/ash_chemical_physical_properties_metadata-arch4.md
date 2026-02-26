# Physical and chemical properties of wildfire ash collected from different ecosystems and burn severities across the globe, 2003-2021

## Overview
- Global dataset characterizing wildfire ash chemical and physical properties from 2003–2021; analyses conducted 2003–2022.
- Two CSV data files: ash_chemical_properties.csv (chemical characteristics) and ash_physical_properties.csv (physical characteristics).
- Analyses conducted by Swansea University (UK) and collaborators; sampling locations include multiple international sites.

## Data files and what they contain
- Chemical characteristics (ash_chemical_properties.csv)
  - Variables include: country, site name, year, burn severity, sample name, δ13C; total C, CO3, N; total mg/kg concentrations of P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, Cr, Co, Br, Sr; total Hg, As, Cd; pH, electrical conductivity (EC), UV %T; dissolved concentrations (DOC, NH4+, NO3−, Cl−, SO4−, F−, P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, B); dissolved Hg, As, Cd.
  - Notes: some chemical parameters not analysed for certain samples.
- Physical characteristics (ash_physical_properties.csv)
  - Variables include: country, site name, year, burn severity, sample name, WR_33kPa, WR_1500kPa, particle density (g cm−3), WDPT classes (water drop penetration time categories).

## Sampling, replication, and sites
- Sites (sampling locations identifiable via Country field):
  - Madre del Agua (Tenerife, Spain)
  - Thompson reservoir (Victoria, Australia)
  - Higher Swineshaw reservoir (Manchester, UK)
  - Mesa Fire (Idaho, USA)
  - Analyses at Swansea University (UK)
- Temporal coverage: ash samples collected 2003–2021; chemical and physical analyses conducted 2003–2022.
- Replication:
  - Chemical characteristics: 2–20 replicates per site and treatment.
  - Physical characteristics: 4 replicates per site and treatment.
- Burn severities represented: extreme, high, moderate, and low.

## Variables and measurements
- Chemical data cover major and trace elements, carbon content, carbonate, pH, EC, UV transmittance, and a broad suite of dissolved species (DOC, inorganic anions/cations, trace metals).
- Isotopic and chemical indicators included: δ13C, C, N, CO3, and heavy metals (Hg, As, Cd, etc.).
- Physical data cover soil/ash properties affecting hydrology and infiltration: water retention at field capacity (33 kPa) and wilting point (1500 kPa), particle density, and WDPT hydrophobicity categories.

## Methodology and analytical procedures
- Digestion for total analysis: EPA 3051-alternative microwave digestion (0.25 g ash with acids, 200°C, ~45 min).
- Leachate experiments: 4 g ash in 100 mL DI water, shaking, settling, filtration; sub-samples prepared for various analyses.
- Carbonates: Bernard Calcimeter (ISO 10693:1995) with CaCO3 standards.
- UV index: colorimetric measurement at 254 nm.
- DOC: dichromate digestion with colorimetric read at 590 nm.
- P and PO4: acid-ascorbic method with calibration.
- Major ions (Cl−, NO3−, SO4−): liquid chromatography (Dionex 4500i).
- Carbon and nitrogen: elemental analysis (LECO CHN).
- Trace elements (As, Ca, Br, Mg, Al, Cd, Co, Cr, Cu, Fe, Mn, Ni, Pb, Sr, Zn): leachate and total digestion with atomic absorption/emission techniques (AAS/AES) per instrument specifications.
- Mercury: EPA 7473 thermal decomposition with AAS (DMA-80 system).
- Replication and quality control details summarized in the methodology.

## Completeness and limitations
- Completeness:
  - Chemical dataset: 296 ash samples.
  - Physical dataset: 36 ash samples.
- Limitations:
  - Some chemical parameters not measured for certain samples.
  - No periodic update mechanism indicated (static dataset).

## Data provenance and governance
- Data origin: Swansea University and collaborators; sampling across diverse ecosystems and burn severities.
- Documentation includes detailed methodological steps, instrument types, and calibration approaches.
- Metadata-rich dataset supports discoverability, cross-study comparability, and potential integration with other data networks.

## Implications and uses for Data Leaders
- Data strategy and governance
  - Assess cross-site comparability and harmonize units, detection limits, and metadata standards.
  - Implement clear data provenance, versioning, and access controls for broad collaboration.
- Data quality and stewardship
  - Identify data gaps (granularity, missing parameters) and plan harmonized collection or imputation strategies.
  - Ensure metadata completeness (site, year, burn severity, sampling methods) to enable reuse.
- Data collaboration and networked value
  - Use as a starting point for cross-network synthesis on wildfire ash composition and hydrophobicity effects on post-fire processes.
  - Align with broader datasets to support policy, environmental risk assessment, and land management decisions.
- Actionable next steps for data managers
  - Define a metadata schema and controlled vocabularies for site, burn severity, and sampling context.
  - Establish data quality checks and lineage documentation; create a data-access plan or license if needed.
  - Plan for periodic updates or extensions to cover additional sites or newer burn events.