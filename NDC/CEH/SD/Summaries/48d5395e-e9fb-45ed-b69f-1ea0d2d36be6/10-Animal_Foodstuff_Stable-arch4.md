# Supporting documentation for 10-Animal_Foodstuff_Stable.csv

- Purpose: Acts as a data dictionary / metadata guide for the dataset of stable element concentrations in animal-derived foodstuff, enabling understanding, discovery, and reuse of the data.
- Scope: Defines the data structure, fields, units, and quality metadata for multiple elements measured in samples of foodstuff from animal sources.

## Data model and key fields

- Core identifiers and descriptors
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (foodstuff group).
  - Location: Location where the sample was collected.
  - Sample_Description: Part of the organism analyzed (e.g., portion analyzed).
  - Collection_Date: Date of sample collection (dd-mm-yyyy).
  - Sample_size: Amount analyzed (g fresh matter or mL for milk).

- Per-element measurements (for each element: Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th)
  - [Element]_mg/kg_fm: Concentration of the stable element on a fresh mass basis (or mg per L for milk where stated).
  - Unc_[Element]_mg/kg_fm: Combined uncertainty of the element concentration on a fresh mass basis.
  - Detection_Limit_[Element]_mg/kg_fm: Detection limit for the element on a fresh mass basis.
  - Notes: If a value is blank, it indicates the concentration was below the detection limit.
  - Units: Primarily mg/kg_fm (or mg/L for milk); some fields show variants or formatting inconsistencies in the text.

- Specific formatting notes
  - The Na field includes enumerated sub-parts describing concentration, units, and below-detection-limit status.
  - Several fields exhibit formatting irregularities in the documentation (e.g., inconsistent naming or line breaks), but the intended schema includes parallel triplets of concentration, uncertainty, and detection limit for each element.

## Metadata, quality and discoverability

- Emphasizes proper data formatting, complete metadata, data quality, and discoverability to support updates and reuse.
- Aims to verify data content and format, facilitating data sharing within and across networks.

## Usage and intended audience

- Designed to support data analysis, verification, and dissemination practices for data products used by analysts, policy colleagues, and broader data communities.
- Enables assessment of data availability, data quality, and suitability for analytical workflows, with clear indicators for when data points are below detection limits.

## Challenges addressed

- Provides structured metadata to manage multi-element measurements, detection limits, and measurement uncertainties.
- Addresses the need for consistent units (mg/kg_fm or mg/L for milk) and clear handling of values below detection limits to support reliable interpretation and integration with other data sources.