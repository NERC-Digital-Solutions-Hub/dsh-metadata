# Loch Leven long-term monitoring dataset

## Aim
- Provide a well-documented, up-to-date dataset from Loch Leven to support discovery, reuse, and governance.
- Ensure data are organized, traceable, and usable by others, with clear metadata, provenance, and processing history.
- Align with long-term monitoring goals under the UK-SCAPE WP7 LEVEN project, with data produced and quality-checked by NERC/CEH staff.

## Scope and Content
- Long-term monitoring dataset from Loch Leven, Scotland, started in 1968 and ongoing.
- Data collected as part of a sustained programme by multiple NERC institutions, most recently NERC/UK CEH.
- Output format: a single CSV file with comprehensive metadata columns covering sampling, site conditions, lake chemistry, and biota.
- Includes two main sites visited per sampling occasion (Reed Bower and Sluices), with Harbour (Site_H) referenced in site codes; three primary monitoring sites are Harbour (H), Reed Bower (RB), and Sluices/Outflow (L).
- Documented data types:
  - In situ measurements: conductivity, pH, temperature, Secchi depth (Secchi measured at Reed Bower).
  - Water sampling (field and laboratory analyses): soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP), chlorophyll a (chla), and related sub-samples.
  - Zooplankton: crustacean densities (e.g., Daphnia hyalina, Eudiaptomus gracilis, Cyclopidae, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, etc.) counted as individuals per litre.
  - Site metadata: river/harbour depth, wind direction and force, cloud cover, etc.
- Data notes:
  - Some measurements are site-specific (e.g., Secchi at Reed Bower) and some sampling occasions may miss one or both sites due to weather or resource constraints.
  - Zooplankton data include zero values (indicating absence at sampling resolution) and NA for missing values.

## Sampling regime and Sites
- Sampling cadence: generally fortnightly.
- Sampling sites per occasion: two main sites visited (Reed Bower and Sluices); Harbour referenced in site codes; site IDs include H (Harbour), RB (Reed Bower), and L (Sluices).
- Site coordinates (UK National Grid, epsg:27700):
  - Harbour (H): Easting 312251, Northing 701670
  - Reed Bower (RB / RB5): Easting 313568, Northing 701141
  - Sluices / Outflow (L / Sl8): Easting 317004, Northing 699380
- Access limitations: Reed Bower accessible only by boat; Sluices can be sampled by boat or from shore.

## Measurements and Analysis
- In situ measurements:
  - Conductivity (µS/cm), pH, temperature (°C) measured at each site.
  - Secchi depth (m) measured at Reed Bower.
- Field sampling:
  - Duplicate 2 L water samples per site; Reed Bower uses an integrated sampling tube; Sluices uses a bottle 10 cm below surface.
- Laboratory analyses:
  - SRP and TP (total phosphorus) via colorimetric methods; SRP by Murphy & Riley (1962) and TP via persulfate digestion per Wetzel & Likens (2000) with an added acidification step.
  - TSP (total soluble phosphorus) measured from filtered samples; chlorophyll a determined by filtering 400 mL and analyzing the filter.
  - Filter materials: Whatman GF/C filters.
  - Storage: filtered/unfiltered samples stored appropriately (refrigeration or freezing) as described.
- Weather data:
  - Cloud cover, wind direction, wind force recorded at Reed Bower when possible; wind force mapped to Beaufort scale with a reference table.
- Data sources and methods references:
  - Golterman, Clymo, Ohnstad (1978); Murphy & Riley (1962); Wetzel & Likens (2000); additional related Hydrobiologia literature and SNH reports.

## Data Processing and Quality Assurance
- Processing workflow:
  - An R-based import script processes raw data into the final database.
  - Wind force values like "4-5" use the first value.
  - Replicate probe values (conductivity, pH, DO) are validated using Median Absolute Deviation (MAD); values outside sensible ranges are handled accordingly.
  - pH values are converted to 10^pH for MAD calculation, then transformed back; final values are rounded (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
  - HQ4300 (inter-calibration) updates: column names updated to reflect HQ4300, while column order remains unchanged.
- Quality Assurance:
  - Automated checks plus manual review for data entry errors and out-of-range values.
  - Suspect values corrected where appropriate.
- Documentation and traceability:
  - All processing steps and calibration changes documented within the dataset description.
  - As of 2022, column names were slightly changed and two new zooplankton taxa were added; ongoing attention to data integrity and consistency.

## Data Format and Metadata
- Data storage: a single comma-separated values (CSV) file.
- Column semantics:
  - Columns describe determinands, site context, and units; including sampling date, week of year, site identifiers, water level, cloud cover, wind metrics, depth, Secchi depth, conductivity, temperature, dissolved oxygen (DO), pH, TP, SRP, TSP, chlorophyll a, and numerous zooplankton taxa densities.
  - Site-specific columns distinguish Harbour (H), Reed Bower (RB), and Sluices (L) measurements.
  - Units are explicitly stated per column (e.g., µS/cm, mg/L, °C, m, pH, etc.).
- Column reference:
  - Table 3 provides detailed column descriptions and mappings; Table 1 provides site codes and locations.
- Missing data:
  - Missing values are represented as NA.
- Documentation and references:
  - Detailed measurement methods, processing approach, and QA steps are described; key references for methods are cited.

## Data Access, Governance, and Maintenance
- Governance and stewardship focus:
  - Clear provenance: data collected by NERC/CEH staff; linked to UK-SCAPE WP7 LEVEN project.
  - Reproducibility: processing script in R with documented rules; QA steps codified.
  - Metadata richness: extensive column descriptions, site mappings, and measurement protocols to enable discovery and reuse.
- Maintenance and updates:
  - 2022 updates include minor column name changes for consistency and the addition of new zooplankton taxa.
  - Ongoing quality checks and validation to ensure data remain usable for current and future analyses.
- Data availability:
  - Dataset described as part of a long-term monitoring program; structured for integration into data portals and catalogues via standardized metadata and a consistent CSV format. Specific licensing or access terms are not stated in the document.

## Caveats and Considerations for Use
- Sampling gaps due to weather/resource constraints may create incomplete time series for certain sites or measurements.
- Harbour data are referenced but may not be consistently measured across all variables; rely on Table 3 and site mappings for exact coverage.
- Taxonomic resolution for zooplankton is generally species-level where possible, but preservation and condition may limit identification.
- Users should consult the 2022 updates and references for context on methodological changes and dataset evolution.