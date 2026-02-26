# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

## Overview
- Describes a comprehensive dataset of dissolved constituents in water samples (e.g., Aluminium, Ammonium, Antimony, Arsenic, Barium, etc.) collected from environmental sites, with pre-concentration steps to improve detection limits.
- Data are organized around analyte-specific records including form, determinand, units, detection limits, start/end dates, location of analysis, analytical methods, QC qualifiers, filtration, and preservation details.
- Analyses are performed across multiple laboratories (Wallingford, Lancaster, Staylittle, Bangor, etc.) using a variety of analytical techniques (ICP-OES, ICP-MS, ion chromatography, colorimetry, AAS, TOC analysis, etc.).
- Sampling contexts include river, borehole, rainfall, cloud water, throughfall, and other inputs, spanning from the early 1980s to the mid-2000s.

## Data Model and Metadata
- Each analyte entry captures a consistent set of fields: Form, Determinand, Units, LQDC (low quantification detection continuum), Quote To, Start/End dates, Location of Analysis, Analytical Method QC Data Qualifier, Filtration, Preservation, and Method (with notes on preparation and concentration steps).
- Multiple sites and catchments are documented, enabling cross-site comparisons and integration.
- Data provenance indicates distinct laboratories and procedures, underpinning traceability and reproducibility.

## Data Quality, Provenance and Standards
- QC and data qualifier framework includes codes for evaluating accuracy and reliability (e.g., ISO 17025-related proficiency testing, interlaboratory schemes).
- Annotations note data quality states:
  - 11: Raw data at or below detection limit.
  - 12: Sensitivity issues due to method changes.
  - 13–17: Various cautions about data patterns, corrections, sampling times, and other caveats.
- Inter-lab QA references include Aquacheck LGC proficiency schemes and SRM materials, indicating formal quality assurance practices.

## Temporal and Spatial Scope
- Time coverage varies by analyte, with many entries spanning 1983–2007; some analytes have ongoing or contended end dates.
- Site codes and catchment contexts are provided, enabling area-based hydrological analyses.

## Hydrological Calculations and Conversions
- Provides explicit conversion between stream flow (cumecs) and area-weighted runoff (mm/15 min) using catchment areas for specific sites; formulas are given for both directions.
- Includes sample site names, catchment areas (sq. km), and conversion constants to support hydrological modeling.

## Sampling Timelines and Data Alignment
- Defines sampling times: grab samples for stream/borehole; time-integrated samples for rainfall-related inputs.
- Details on time-stamping emphasize that sampling times should be used to compute volume-weighted sampling times and year-mean sampling.
- Explains how volume-weighted time bases are derived, including handling of data gaps and AWS (automatic weather station) data.

## Implications for Data Leaders
- The dataset exemplifies a complex, multi-lab data ecosystem with long-running time series and heterogeneous analytical methods.
- Key governance needs:
  - Maintain a robust data dictionary and metadata standards to harmonize units, determinands, and methods across time and labs.
  - Implement clear data qualifiers and provenance tracking to document data quality and any corrections.
  - Establish cross-lab data integration practices, including method crosswalks when techniques change.
  - Ensure discoverability and accessibility of metadata (laboratories, QC procedures, preservation, filtration, and handling).
  - Manage change control and versioning to preserve historical context while enabling updates.
  - Foster communities of practice for data standards and interoperability across sites.

## Recommendations for Action
- Develop and publish a centralized data dictionary mapping determinands, units, and methods across all laboratories and time periods.
- Implement a cross-lab QC workflow that reconciles LQDCs, quotes, and QC qualifiers, with flagging for data requiring caution (e.g., qualifiers 11–13).
- Create data provenance trails for each analyte, including instrument specifics, prep methods, and archival notes.
- Standardize reporting formats and establish crosswalks for historical method changes to minimize inconsistencies in trend analyses.
- Ensure transparent documentation of sampling design, time-stamping rules, and volume-weighted calculations to support hydrological interpretation.

## Key Data Governance Questions
- How will method changes over time be reconciled to support consistent trend analyses?
- How should raw vs. processed data (as indicated by QC qualifiers) be treated in public data products?
- What standards will govern metadata completeness, unit harmonization, and cross-lab data integration for future expansions?
- How will data owners ensure discoverability and lineage, given multiple labs, sites, and long temporal coverage?