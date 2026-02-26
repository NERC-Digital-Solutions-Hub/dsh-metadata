# Physical and chemical properties of wildfire ash collected from different ecosystems and burn severities across the globe, 2003-2021

## Overview
- Global dataset characterizing chemical and physical properties of wildfire ash collected from diverse ecosystems and burn severities between 2003 and 2021 (analyses through 2022).
- Aims to inform environmental health monitoring, policy scrutiny, and decision-making related to wildfire impacts.
- Two data files: ash_chemical_properties.csv (chemical characteristics) and ash_physical_properties.csv (physical characteristics).

## Data files and key variables
- Chemical characteristics (ash_chemical_properties.csv) include:
  - Metadata: country, site name, year, burn severity, material type, sample name.
  - Isotopic and elemental data: δ13C; total concentrations of C, CO3, N; major elements (P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, Cr, Co, Br, Sr); trace elements Hg, As, Cd.
  - Solutions/solutes: pH, electrical conductivity (EC), dissolved organic carbon (DOC), dissolved ions (NH4+, NO3−, Cl−, SO4^2−, F−, P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, B); Hg, As, Cd in dissolved form.
  - Additional indicators: UV (%T at 254 nm), %C and %N (elemental analysis), carbonates (CO3^2−).
- Physical characteristics (ash_physical_properties.csv) include:
  - Metadata: country, site name, year, burn severity, sample name.
  - Physical metrics: water retention at 33 kPa (WR_33kPa) and 1500 kPa (WR_1500kPa), bulk density (g cm−3), WDPT (water drop penetration time) classed outcomes (WDPT_1 to WDPT_10).

## Sampling scope and provenance
- Sampling sites include Madre del Agua (Tenerife, Spain); Thompson reservoir (Victoria, Australia); Higher Swineshaw reservoir (Manchester, UK); Mesa Fire (Idaho, USA).
- Coverage across multiple ecosystems and burn severities; data entries include site, year, and burn severity to enable cross-site comparisons.

## Analytical methods and standards
- Chemical analyses followed established methods:
  - Leachate-based and total analyses for multiple elements and compounds.
  - Digestion for total analysis per EPA 3051 (microwave-assisted acid digestion).
  - Leachate experiments modelled after Southern California wildfire methodologies.
  - Carbonates measured with Bernard Calcimeter (ISO 10693:1995 reference).
  - UV index measured at 254 nm; DOC via colorimetric method; P and PO4 via ascorbic acid method.
  - Cl−, NO3−, SO4− measured by liquid chromatography.
  - Elemental concentrations via atomic absorption spectroscopy (AAS) or emission spectroscopy; Hg via EPA 7473 thermal decomposition.
- Physical measurements include bulk density, water retention using pressure plates (33 kPa and 1500 kPa), particle density via pycnometer, WDPT for hydrophobicity.

## Data completeness, replication, and quality
- Chemical data: 296 ash samples; replication ranges from 2 to 20 per site and treatment (chemical characteristics).
- Physical data: 36 ash samples; 4 replicates per site and treatment.
- Completeness notes indicate some chemical parameters were not analysed for all samples; physical dataset reported as complete.
- Data governance considerations point to the need for transparent data sharing and metadata where applicable.

## Data governance, accessibility, and barriers
- Public sharing of underlying datasets is a consideration and can be a barrier for some datasets.
- Metadata quality and provenance are crucial for reuse and verification.
- Ensuring data are quality-assured, cleaned, transformed, and well-documented is essential for policy-relevant monitoring outputs.

## Relevance for monitoring and policy evaluation
- Provides concrete environmental health indicators for post-wildfire conditions, including:
  - Chemical leachates and dissolved constituents that influence soil and water quality.
  - Physical properties relevant to soil hydrology and ash behavior (water retention, density, hydrophobicity).
- Enables cross-regional comparisons of ash characteristics across burn severities, supporting risk assessment, remediation planning, and evidence-informed policy decisions.

## Practical considerations for monitoring frameworks
- Standardized metadata fields to capture site, year, burn severity, sample type, and replicates are essential for comparability.
- Data quality assurance and open data practices should be embedded at data origin to facilitate governance and sharing.
- When integrating into dashboards or reports, prioritize clearly described units, detection limits, and treatment of non-detects.

## References and standards cited
- EPA 3051 digestion protocol; ISO 10693:1995 for carbonate determination; Doerr (WDPT) for hydrophobicity standardization; Klute methods for water retention and particle density; Hue & Liu (1995) DOC method; Doerr (1998) hydrophobicity methodological context.