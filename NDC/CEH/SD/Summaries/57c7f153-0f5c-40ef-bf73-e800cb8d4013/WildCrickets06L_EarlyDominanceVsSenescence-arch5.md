# WildCrickets06L_EarlyDominanceVsSenescence Description of content

## Overview
- Describes singing activity per sample and per individual male crickets.
- Includes whether an individual was high dominance (H) or low dominance (L) early in life, based on the population median.
- Aims to support analyses of dominance and potential senescence patterns.

## Variables and meanings
- EarlyDominance: classification of early-life dominance; values are H (high) or L (low).
- Year: year when the cricket was alive.
- ID: unique individual identifier.
- Temp: ambient temperature at the time of sampling (in °C).
- Age: age at sampling (in days).
- Sings: whether singing occurred at sampling (1 = yes, 0 = no).

## Data structure
- Per-sample and per-individual data are included, with a linkage between the EarlyDominance classification and the Sings measurement across sampling events.

## Data types and encoding
- EarlyDominance: categorical (H/L).
- Year: integer.
- ID: string or numeric identifier.
- Temp: numeric (°C).
- Age: numeric (days).
- Sings: binary integer (0/1).

## Metadata and standards
- Explicit units for Temp (°C) and Age (days).
- Clear definitions for H vs L (based on population median) and documentation of sampling protocol.
- Documentation of data collection methods, timing, and any data transformations.

## Data governance considerations
- Ensure consistent coding across records (H/L; 0/1 for Sings).
- Maintain data provenance, including who collected data and under what conditions.
- Implement quality checks for missing values, outliers, and unit consistency.
- Establish versioning and traceability for updates or reclassifications.

## Sharing and reuse considerations
- Provide comprehensive metadata to facilitate discovery and reuse.
- Clarify licensing and access rights for external users.