# Wind and strain data collected for 21 trees in Wytham Woods

## Overview
- Describes wind and tree strain data collected in Wytham Woods, southern England, from September 2015 to June 2016.
- Goals: extract resonant frequencies, estimate critical wind speeds for breakage, and test a finite element model of tree–wind dynamics.
- Metadata links to the Wytham Woods census via census IDs.

## Data collected and scope
- Strain data collected at 4 Hz using two strain gauges per tree, attached at 1.3 m height and oriented approximately perpendicular to each other.
- Six data loggers used; data availability is non-uniform due to battery and storage constraints.
- Data files are organized by tree sets with names like T1, T2_3, T4_7, etc., reflecting which trees are contained in each file.
- Wind data collected from the canopy walkway:
  - Winter: cup anemometer (Vector Instruments A100LK/5M).
  - Summer: Gill Sonic-1.
  - Time resolution varies between instruments.
- Local climate data and long-term wind data available from the Environmental Change Institute.

## Data structure and metadata
- First column in each data file: UTC datestamp.
- For each tree: two subsequent columns representing strain measurements, projected into Northward and Eastward directions.
- Strain values converted from millivolts (mV) to strain using calibration information in calibration.txt.
- Metadata includes census IDs to link trees to the Wytham Woods census dataset (tree_species_censusID.txt).

## Data processing, provenance, and documentation
- Matlab-based processing scripts and smaller, easier-to-use Matlab data files are available on GitHub: github.com/TobyDJackson/WindAndTrees_Wytham.
- A description of data processing steps, underlying assumptions, and sensitivities is provided on the same site.
- Processing provenance and methodologies facilitate reproducibility and auditing of data transformations.

## Access, sharing, and reuse
- Data and processing resources are openly hosted via GitHub for reuse and audit.
- Contact information provided for questions: tobydjackson@gmail.com.
- References to foundational literature are included to contextualize methods and data usage.

## Technical details and interoperability
- Data originate from multiple instruments and systems (strain gauges, loggers, wind sensors) with varying formats and time resolutions.
- File naming and structure support traceability of data to specific trees and logger deployments.
- Calibration, processing steps, and metadata are documented to support interoperability across analyses and datasets.

## Quality, limitations, and challenges (data stewardship considerations)
- Incomplete or uneven data coverage due to battery/storage constraints requiring multiple separate files per logger.
- Variability in data collection instruments and formats necessitates careful metadata management and standardization.
- Potential limitations in sharing datasets due to non-uniform data availability and instrument differences; mitigated by clear documentation, calibration data, and processing scripts.
- Ongoing need to align user needs with dataset contents (e.g., enabling researchers to link to census data and climate records).

## Governance and reuse implications for data stewards
- Ensure persistent linkage between strain data, tree census IDs, and external metadata (e.g., tree species, census, climate data).
- Maintain and version-calibrate metadata files (tree_species_censusID.txt, calibration.txt) to preserve data integrity.
- Preserve access to processing scripts and documentation to support reproducibility and transparency.
- Manage data provenance across multiple loggers and formats, documenting any data harmonization or transformations.
- Facilitate discoverability by providing clear data descriptions, unit definitions, and coordinate references (e.g., UTC timestamps, measurement directions).

## References
- Savill et al. (2010), Wytham Woods: Oxford’s Ecological Library.
- Butt et al. (2009), Long-term broadleaf monitoring plot at Wytham Woods.
- Moore et al. (2004), Inexpensive instrument to measure dynamic response of standing trees to wind loading.

## Contact
- Toby D. Jackson: tobydjackson@gmail.com
- GitHub: github.com/TobyDJackson/WindAndTrees_Wytham