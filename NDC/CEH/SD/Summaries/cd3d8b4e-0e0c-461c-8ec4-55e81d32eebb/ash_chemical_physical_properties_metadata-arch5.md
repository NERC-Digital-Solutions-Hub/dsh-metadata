# Physical and chemical properties of wildfire ash collected from different ecosystems and burn severities across the globe, 2003-2021

## Overview
- A dataset describing chemical and physical properties of wildfire ash, comprising two CSV files: ash_chemical_properties.csv and ash_physical_properties.csv.
- Collected across global sites from 2003 to 2021; laboratory analyses conducted through 2022.
- Hosted and analyzed by Swansea University (UK); sampling locations include Madre del Agua (Tenerife, Spain), Thompson Reservoir (Victoria, Australia), Higher Swineshaw Reservoir (Manchester, UK), and Mesa Fire (Idaho, USA).
- Aimed to characterize wildfire ash chemistry and physics to inform environmental assessments.

## Data Content and Variables
- Chemical characteristics (ash_chemical_properties.csv):
  - Variables: Country, site name, year, burn severity, sample name, δ13C (‰), total concentrations of C, CO3, N; total concentrations (mg kg-1) of P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, Cr, Co, Br, Sr; dissolved concentrations (mg kg-1) of organic C (DOC), NH4+, NO3-, Cl-, SO4-, F-, P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, B; dissolved concentrations (µg kg-1) of Hg, As, Cd.
  - Isotopic and elemental indicators: δ13C, %C, %N, etc.
  - Other chemical metrics: pH, electrical conductivity (EC; µS cm-1), UV index (%T).
- Physical characteristics (ash_physical_properties.csv):
  - Variables: Country, site name, year, burn severity, sample name; WR_33kPa and WR_1500kPa (water retention at field capacity and wilting point); particle density (g cm-3); water drop penetration time (WDPT) class distribution (WDPT_1 to WDPT_10).
- Metadata and structure:
  - Features include sampling location details, year, burn severity, sample name, chemical and physical measurements.
  - Replicates: chemical analyses 2–20 replicates per site/treatment; physical analyses 4 replicates per site/treatment.
  - Completeness: chemical data is incomplete for some samples; physical dataset is complete.
  - Observations: 296 chemical ash samples; 36 physical ash samples.
  - Data management: intended for uploading to relevant data portals and catalogues; documentation of work performed may be included.

## Sampling and Analytical Methods
- Sampling provenance:
  - Global sites with country and site metadata; sample naming conventions capture site and burn context.
- Chemical analyses:
  - Leachate experiments for several dissolved constituents; digestion for total element analysis (EPA 3051 alternative) using microwave digestion.
  - Instrumentation: ICP-AES/AA for metals (e.g., As, Cd, Hg via appropriate methods); IC for Cl-, NO3-, SO4-; CHN for %C and %N.
  - Specific analyte methods labeled (e.g., Hg by EPA 7473; Na by AAS/AE; P&PO4 by colorimetric methods; UV index via colorimetric/UV measurements; DOC via oxidation method).
  - Carbonates quantified with Bernard Calcimeter (ISO 10693:1995).
- Physical analyses:
  - Bulk density (105°C drying), WR at 33 kPa and 1500 kPa via Richards pressure plates.
  - Particle density via pycnometer.
  - WDPT for water repellency (classifications WDPT_1 to WDPT_10), following Doerr’s protocol.
- Replication and controls:
  - Chemical: 2–20 replicates per site/treatment; physical: 4 replicates per site/treatment.
  - Controls: not applicable (NA) in this dataset.
- Method references:
  - Key sources include EPA 3051 (digestion), Doerr (WDPT), Klute (water retention methods), Blakes & Hartge (bulk density, particle density), ISO 10693 (calcimeter for carbonates), Hue & Liu (DOC method), and standard colorimetric/IC/AA techniques for various analytes.

## Data Management, Quality, and Completeness
- Completeness:
  - Chemical characteristics: some parameters not analysed for certain ash samples.
  - Physical characteristics: complete dataset.
- Data stewardship considerations:
  - Data are organized to enable portal deposition and cataloging; clear attribution to Swansea University and listed authors.
  - Documentation of methodologies supports reproducibility; explicit replication and sample-treatment metadata aids QA.

## Governance, Access, and Stewardship Implications
- Data stewardship focus:
  - Ensure standardized metadata schema (site, country, year, burn severity, sample name, replicates) and consistent units across chemical and physical datasets.
  - Maintain provenance and versioning, including the specific analytical methods and instrument models used.
  - Prepare data quality reports highlighting any incomplete parameters and the rationale.
  - Plan for dataset publication in data portals with clear licensing, DOI assignment, and dataset version control.
  - Implement an update workflow to incorporate new samples or re-analyses and document any embargoes or access restrictions.
  - Address interoperability challenges by aligning formats and ontologies to facilitate cross-dataset integration with other soil/ash datasets.
- Potential challenges to monitor:
  - Incomplete chemical data across some samples and the use of multiple analytical methods and instruments.
  - Large, multi-site dataset with diverse formats requiring careful harmonization.

## Usage and Significance
- Enables cross-ecosystem comparison of wildfire ash chemistry and physics across burn severities and geographic regions.
- Supports research on environmental impacts of wildfires, soil and water chemistry, hydrophobicity, and post-fire recovery processes.
- Provides a documented methodology suite and replicates framework that can guide similar future datasets.