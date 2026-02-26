# SUPPORTING DOCUMENTATION FOR 'Radiocarbon-dated charcoal datasets obtained from lake sediments from the Pantanal, Brazil'

## Overview
- Charcoal datasets derived from macroscopic charcoal fragments analyzed in radiocarbon-dated lake sediment cores from the Brazilian Pantanal.
- Core datasets include Laguna Mandior e (M1, M5), Laguna Mimoso, and Laguna Caceres with collection dates around 2001 and 2019.
- Geographic and core metadata provided in Table 1; radiocarbon dating details provided in Table 2.

## Data Contents and Structure
- Recorded values:
  - Concentration data: particles of charcoal >125 μm per cubic centimetre at each 1-cm depth horizon.
  - Depth value corresponds to the midpoint of the 1-cm sampling interval.
- Data files:
  - Each core has a separate .csv file.
  - Radiocarbon dates associated with each core are included as headers in the respective file, providing an age-depth context.
  - Radiocarbon dates are presented as uncalibrated conventional radiocarbon ages (BP).
- Sampling resolution:
  - 1-cm depth horizons for all cores; depths and horizons are explicitly linked to charcoal data.
- Data structure per core:
  - Laguna Mandior e M1: 3 radiocarbon dates; Laguna Mandior e M5: 3 radiocarbon dates; Laguna Mimoso: 2 dates; Laguna Caceres: 3 dates.
  - Age-depth profiles constructed from discrete horizons with full laboratory reporting for each date.

## Metadata and Provenance
- Table 1 (site data for each sedimentary record) includes:
  - Core identifiers, collection dates, coordinates, lake area, water depth, elevation, maximum core depth, sediment type, and collection method.
- Table 2 (radiocarbon dating details) includes:
  - Number of radiocarbon dates per core, date providers (Beta Analytic; UGAMS for Mimoso), units (Conventional Radiocarbon years BP), data structure (age-depth profiles), and note that full laboratory reporting is provided for each date.
- Radiocarbon dates include depth-correlated sample IDs, dating material, conventional ages, and, where available, d13C values.

## Methods and Quality Control
- Sample processing and deflocculation:
  - Sediments deflocculated using 7% sodium hexametaphosphate (LM and LC) or 10% potassium hydroxide (MIM).
  - Deflocculation performed at ~80°C for 30 minutes.
  - Residues washed and sieved at 125 μm and 250 μm.
- Analytical workflow:
  - 1-cm resolution counting conducted using a Bogorov tray.
  - Clay-rich sediments and organic-rich sediments processed with specific chemical protocols to ensure consistency.
  - Volume measured by water displacement.
- Quality control:
  - Standard laboratory procedures followed; lab ISO quality control details available via source laboratories.
  - Full laboratory reporting is provided for each radiocarbon date.

## Data Governance, Accessibility, and Use
- Data are organized to support reproducibility and age-depth modeling (1-cm horizon data with corresponding radiocarbon dates).
- Radiocarbon ages are uncalibrated; users should calibrate as needed for synthesis or comparison.
- Documentation includes explicit metadata for site, core, sampling, and dating methodologies to facilitate data discovery and interoperability.
- Licensing or reuse terms are not specified in the document; Data Stewards should confirm and attach appropriate usage licenses and update records as needed.

## Considerations for Data Stewards
- Interoperability:
  - Ensure consistent units (charcoal particles per cm3; 1-cm horizons) and consistent age reporting (uncalibrated BP) across cores.
  - Maintain clear links between Table 1 metadata, Table 2 radiocarbon dates, and per-core CSV data.
- Metadata completeness:
  - Preserve core collection methods, coordinates, lake characteristics, and depth information to support future re-use and age modeling.
- Updates and governance:
  - Consider documenting any subsequent updates, recalibrations, or additional radiocarbon dates as new data become available.
- Usage guidance:
  - Provide calibration guidance when integrating with other paleoenvironmental datasets.
  - Note that the dataset supports age-depth modeling of charcoal deposition but relies on uncalibrated radiocarbon ages; calibration should be applied for chronological synthesis.