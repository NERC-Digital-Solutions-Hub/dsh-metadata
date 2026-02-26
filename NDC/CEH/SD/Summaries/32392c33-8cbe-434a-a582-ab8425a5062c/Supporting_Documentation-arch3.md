# Water quality data - work packages 3 and 5

## Overview
- Provides water quality measurements for work packages 3 and 5.
- Core data stored in Water_quality_data.csv; supporting metadata in Sampling_sites.csv and Determinand_list.csv.
- Methodology for particulates documented in Particulate_matter_method.rtf.
- Metadata is embedded within the data files; data quality, provenance, and usage rely on accompanying metadata.

## Data files and metadata
- Water_quality_data.csv: primary measurements with key identifiers and qualifiers.
- Sampling_sites.csv: site-level metadata (SiteName, SiteRef, Type, Sampling, Easting, Northing).
- Determinand_list.csv: definitions and details for each determinand (the other columns in Water_quality_data.csv).
- Particulate_matter_method.rtf: methodology information for analysis of certain particulates.

## Data content and column notes
- First five columns in Water_quality_data.csv:
  - SiteRef: unique site code; estuarine sites include BCN, TYC, DOL; others are freshwater.
  - SiteName: unique site name.
  - Trip: indicates field sampling occasion (single trip, autosampler, or multi-day sampling). Codes differentiate routine trips from intermediate dates.
  - Date: sampling date.
  - Time: sampling time.
- Determinand values: each has a qualifier (usually blank; sometimes < for below-detection).
- pH data issues:
  - Period of instrument failure led to incorrect pH values.
  - pHUncorrected column contains original values.
  - pH column contains a mix of correct and approximately corrected values; incorrect values flagged with an 'x' in the qualifier.
  - Approximate corrections for erroneous pH were made using alkalinity data.
- Missing data are shown as blank fields; zeros represent actual measured values.
- Additional column details are defined in Determinand_list.csv.

## Sampling context
- Site types include estuarine (e.g., BCN, TYC, DOL) and freshwater sites, with sampling influenced by tidal state (Fresh/Saline).
- Sampling approaches:
  - Spot sampling or Continuous sampling.
  - Trip records indicate field campaign timing; some samples collected via autosampler or manually over one or two days.
- Location data provided via Easting/Northing coordinates in national grid reference.

## Data quality, processing and transparency
- Metadata is distributed across Water_quality_data.csv, Sampling_sites.csv, and Determinand_list.csv; explicit column meanings are documented in Determinand_list.csv.
- Data issues to note:
  - Periods of instrument failure affecting pH measurements.
  - Some variables not measured in all samples.
  - Data may require transformation to standardize units and formats for integration (as indicated by the need to consult the Determinand_list.csv for column definitions).
- The Particulate_matter_method.rtf provides methodology context for relevant particulates.

## Governance, sharing and use in monitoring frameworks
- Data governance needs include:
  - Verifying data provenance and metadata completeness.
  - Ensuring data quality assurance, cleaning, transformation, and proper presentation (reports, charts, dashboards).
  - Sharing underlying data appropriately while managing access and openness.
- Potential barriers highlighted for monitoring frameworks:
  - Lack of data or data of insufficient standard.
  - Access delays or data silos within/between organizations.
  - Requirement to publicly share datasets can impede use of some data.
  - Inadequate metadata complicates verification of data suitability.
  - Data formats requiring transformation and challenges in communicating complex findings.
  - Establishing and maintaining data governance processes for storage, sharing, and updates.

## Practical implications for monitoring framework authors
- Use this dataset as a model for site-level time-series with accompanying site and determinand metadata.
- Pay attention to:
  - The distinction between raw (Uncorrected) and corrected data (pH, others) and the implications for interpretation.
  - The qualifiers on determinands and handling non-detects or below-threshold values.
  - The Trip field to contextualize sampling events and to align time-series analyses.
  - Site-type (Fresh vs Saline) and sampling type (Spot vs Continuous) to support stratified reporting and dashboards.
- Ensure comprehensive metadata when integrating datasets into monitoring frameworks, and address governance requirements to enable data sharing and reuse.