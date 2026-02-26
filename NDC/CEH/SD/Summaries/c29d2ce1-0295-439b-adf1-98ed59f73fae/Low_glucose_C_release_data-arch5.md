# Time series of microbial carbon release from soil as carbon dioxide under different nitrogen and phosphorus treatments with a low glucose concentration added as a carbon source in the Conwy catchment, North Wales, UK (2015)

## Overview
- Study of soil microbial carbon mineralization to CO2 using 14C-glucose under different N and P treatment combinations in the Conwy catchment, North Wales, UK, 2015.
- Measurements obtained from 14CO2 evolved, captured in NaOH traps and quantified by liquid scintillation counting.
- Incubation conducted at 10°C to reflect mean annual temperature; traps emptied at multiple time points up to 6 weeks.
- Data described across several files: application data, raw time-series, and metadata for quality control and plot locations.

## Dataset content and structure
- Application data describes treatment combinations and sample counts:
  - Low concentration glucose (0.006 mM) with treatments: Control, N addition, P addition, and N&P addition.
  - Each treatment includes 42 samples; soil samples are 5 g (dry weight equivalent) per tube.
  - Depths considered across soil profile (topsoil 0–30 cm, midsoil 50–100 cm, subsoil 100–300 cm) with depth intervals detailed in the collection protocol.
- Time-series data (DPM counts) are tracked at numerous time points:
  - Time intervals: 0.5, 1, 2, 4, 6, 24, 48, 72, 96, 120, 144, 168, 192, 288, 336, 504, 672, 840, 1008 hours.
  - Columns labeled per time interval; empty cells indicate no data.
- Data collection and measurements:
  - Soil cores divided into depth intervals, sieved through 5 mm to remove stones/plants, ensuring sample homogeneity.
  - 5 g soil aliquots incubated with 14C-glucose; NaOH traps capture evolved 14CO2, then quantified with a Wallac 1404 counter.
  - 50 µl of 14C-glucose nutrient solution added per tube; NaOH traps replaced at the listed time points.
- Metadata and documentation:
  - Metadata for the Low_glucose_C_release_data.csv file (including column names and descriptions) provides data definitions and units.
  - Abbreviations used include HWMC (high molecular weight carbon), N (nitrogen), P (phosphorus).
  - Plot locations are referenced in Plot_locations.csv; descriptions of fields available in Plot_locations_metadata.rtf.
  - Quality control and reference data described in Low_glucose_C_release_data_metadata.csv.

## Data collection methods and scope
- Sampling and preparation:
  - Soil cores collected across multiple transects and cages; depths summarized as topsoil (0–30 cm), midsoil (50–100 cm), and subsoil (100–300 cm).
  - Sieve size (5 mm) chosen to minimize microbial community disturbance.
- Mineralization assay:
  - 5 g soil per tube; 14C-glucose added to surface; NaOH traps capture evolved CO2.
  - Incubation at 10°C with trap changes at specified intervals, then weekly up to 6 weeks.
- Provenance and documentation:
  - Plot locations recorded in Plot_locations.csv; description of fields in Plot_locations_metadata.rtf.
  - QC and reference data packaged in Low_glucose_C_release_data_metadata.csv.

## Data quality, governance, and usability
- Data stewardship considerations:
  - Metadata defines column names, units, and meanings; ensures consistency and interpretability across datasets.
  - Quality control documentation is provided to support data validation and reuse.
  - Clear indication that empty cells represent missing data.
- Standards and interoperability:
  - Use of standard file types (CSV, RTF) and explicit column descriptions facilitates reuse in data portals and analytics workflows.
  - Documentation of treatments, sampling depths, time-points, and units aids cross-study comparisons.
- Limitations and caveats:
  - Incubation conditions (10°C) are a controlled representation of soil processes; results reflect this specific experimental setup.
  - Data cover specific depths and time points as defined; missing data are indicated by blanks.
  - Plasma of 14C measurements relies on NaOH trapping efficiency and scintillation counting accuracy as per standard protocols.

## Access, reuse, and storage considerations
- Related materials available:
  - Low_glucose_C_release_data.csv with time-series DPM data.
  - Low_glucose_C_release_data_metadata.csv with column definitions and QC notes.
  - Plot_locations.csv and Plot_locations_metadata.rtf for spatial context.
- Sharing and update pathways:
  - Documentation supports discoverability and reuse by data users; governance guidance suggests ongoing updates and adherence to data standards.
- Availability considerations:
  - Described data and metadata are suitable for repository deposition and portal indexing; explicit embargo or access restrictions are not stated in the provided text.

## Key considerations for data stewards
- Ensure metadata completeness and consistency across related files (data, metadata, plot locations, and QC).
- Maintain clear provenance lineage from sampling to final DPM counts, including treatment definitions and depth-groupings.
- Clarify units, time-point labels, and handling of missing data to prevent misinterpretation during reuse.
- Provide user-friendly guidance on how to interpret depth groupings (topsoil, midsoil, subsoil) and how to map Transect/Row to plot locations.