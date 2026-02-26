# Macroinvertebrates of the Conwy catchment - taxon data.csv

## Overview
- Dataset describing macroinvertebrate communities (species level) in the Conwy catchment, Wales, UK.
- Covers three years of sampling: 2008–2010, with supporting habitat and geographic data.
- Aims to inform environmental health monitoring and policy evaluation by linking biotic data with site-level environmental variables.

## Data files and version
- Macroinvertebrates of the Conwy catchment - taxon data.csv (taxonomy and abundances)
- Macroinvertebrates of the Conwy catchment - environmental variables.csv (site-level physical and habitat variables)
- Macroinvertebrates of the Conwy catchment - supporting information.csv (site metadata and geography)
- Version control: 1.0 (date 28/06/16); author F. Edwards
- Contributors: sampling (Gearóid Webb, Peter Scarlett, John Davy-Bowker); lab analysis (Gearóid Webb, Helen Vincent, François Edwards); supporting information (Peter Scarlett, Gearóid Webb, François Edwards); planning/management (François Edwards, David Cooper)

## Sampling and methods
- Study area: tributary streams of the Conwy, Wales, UK.
- Timing: November 2008, 2009, 2010.
- Sampling protocol: 1 mm kick net following RIvPACS field protocol; samples processed in lab with 500 μm sieve.
- Taxonomic resolution: identification to the lowest possible taxonomic level, usually species.
- Data validation: cross-checking data printouts against laboratory sheets.
- Site variables recorded: depth, width, velocity, substrate cover, macrophyte cover.
- Taxon coding: valid taxon names and unique taxon codes per Davies & Edwards (2011).
- Environmental mapping: map variables derived using Intelligent River Network (Version 17).

## Data structure and metadata
- Taxon dataset columns:
  - Site code, Year, Sample date, Taxon code (per Davies & Edwards 2011), Taxon name, Life stage (L, P, A, U), Abundance in sample.
- Supporting information columns:
  - Site code, Site name, Easting, Northing, Grid reference, Distance from source (km), Altitude (m), Slope (m/km), Stream Strahler order, Upstream catchment area.
- Environmental variables dataset columns:
  - Site code, Year, Wetted width (m), Water depth (cm), Velocity (m/s), % cover of rock pavement, % cover of boulders/cobbles/pebble/gravel/sand/clay (four classes totaling 100%), % cover by macrophytes.
- Site codes: a key to site codes and corresponding site names is provided in the supporting information.

## Site metadata and attributes
- Supporting information includes detailed site-level data for multiple sites (names such as AFON CADNANT, AFON DDU UPPER, AFON LLEWESIG, etc.).
- For each site: coordinates (Easting/Northing/Grid ref), distance from source, altitude, slope, Strahler order, and upstream catchment area.
- Data constructs allow geographic traceability and context for habitat variables and macroinvertebrate communities.
- Sample identifiers defined by a unique combination of site code and project year.

## Data quality, governance and sharing
- Metadata-rich dataset enabling traceability and reproducibility.
- Taxon codes and valid scientific names facilitate interoperability with other RIvPACS-based datasets.
- Data quality steps include laboratory validation and cross-checking with field sheets; map variables derived from established methods.
- Public data sharing is considered within the governance framework, with underlying data and supporting information provided to enable reuse and verification.

## Relevance for monitoring policy and frameworks
- Provides baseline, site-specific macroinvertebrate community data linked to environmental drivers, suitable for ecological health assessment and monitoring policy evaluation.
- Adheres to RIvPACS methodology, enabling comparability with other riverine invertebrate monitoring programs.
- Rich metadata supports data governance, transparency, and evidence-based decision-making in environmental health monitoring.
- Identifies data collection and metadata requirements (e.g., taxon coding, site geolocation, habitat variables) relevant to planning future monitoring frameworks and addressing data gaps.