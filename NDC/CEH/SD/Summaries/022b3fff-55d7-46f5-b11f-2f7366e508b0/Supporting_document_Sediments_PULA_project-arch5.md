# A brief description/overview of the data being described

- The PULA sediments characterization data folder comprises 14 files describing 7 sediment cores from the Notwane Reservoir.
- Core details:
  - Seven cores, with lengths ranging approximately 35–85 cm.
  - Locations provided as coordinates (latitude/longitude) and associated with the Notwane Dam.
  - Collection dates span 22-Nov-2017 and 19-Feb-2018.
- Data scope:
  - Two main data groups:
    - Grain size measurements for each core (7 spreadsheets: Core_*_Grain_size_details.csv).
    - Grain size averages and metals/organic matter data (7 spreadsheets: Core_*_Grain_size_avg_and_metals.csv).
  - Depths are recorded in cm from the sediment–water interface for each sample.

## Data contents

- Grain size details (Core_*_Grain_size_details.csv):
  - Depth-specific grain size metrics (Dv(10), Dv(50), Dv(90)) in µm.
  - Three measurements per interval plus average values.
- Averages and metals (Core_*_Grain_size_avg_and_metals.csv):
  - Column 1: Core sequential number.
  - Column 2: Depth (cm) from the sediment–water interface (0 cm).
  - Column 3: Average Dv(50) grain size (µm) for the interval.
  - Column 4: Organic Matter (OM) content (%).
  - Columns 5–9: Trace metal abundances (Fe, Cu, Pb, Cr, Zn) in µg kg-1.
  - Blanks indicate data below detection limits or data loss.

## Sampling and analytical methods

- Sampling technique:
  - Seven cores collected with a push corer (50 mm diameter) from shore or a small boat.
  - Cores stored at 4 °C for water retention, split, photographed, and sub-sampled for grain size and geochemical analyses.
- Analytical methods:
  - Grain size: Malvern Mastersizer 3000 laser diffraction (Values reported as Dv(50)).
  - Organic Matter: Loss on ignition (LOI) after calcination (calcination at 550 °C; pre-drying at 105 °C; muffle furnace protocol).
  - Metals: 95 sediment samples analyzed by Microwave Plasma-Atomic Emission Spectrometry (MP-AES) after digestion with 65% nitric acid; filtration to <0.45 µm; dilution to 50 mL.
- Quality metrics:
  - Reported average standard deviations (RSDs) for metals: Fe 1.81%, Zn 4.02%, Cu 1.43%, Cr 0.82%, Pb 1.72%.
  - Detection limits: Cr 0.8 µg kg-1, Fe 1.7 µg kg-1, Cu 0.5 µg kg-1, Zn 28 µg kg-1, Pb 2.5 µg kg-1.
  - Notes on data quality: blanks reflect values below detection limits or data loss.

## Data structure and metadata

- Dataset composition:
  - 14 files total; 7 cores represented.
  - Core location table (Table 1) provides sampling coordinates for each core.
- Grain size details (Core_*_Grain_size_details.csv):
  - Depth, Dv(10), Dv(50), Dv(90) for each of the three measurements; includes averages.
- Averages and metals (Core_*_Grain_size_avg_and_metals.csv):
  - Core number; depth; average Dv(50); OM (%); Fe, Cu, Pb, Cr, Zn (µg kg-1); blanks indicate below detection or missing data.
- Data limitations:
  - Some blank cells correspond to detection limits or data loss.
  - Data cover 2017–2018 collection dates; consider versioning or updates if re-analysis occurs.

## Data governance and stewarding considerations

- Metadata and provenance:
  - Ensure core IDs, depths, coordinates, collection dates, and measurement methods are consistently recorded and traceable.
  - Preserve instrument details (Malvern Mastersizer 3000, LOI protocol, MP-AES) and detection limits for reproducibility.
- Data quality and QA/QC:
  - Maintain RSD values and detection limits; document any deviations or reprocessing steps.
  - Note missing data and below-detection observations with explicit metadata fields.
- Data storage and sharing:
  - Upload and catalogue all 14 files with standardized naming conventions (as used: Core_*_Grain_size_details.csv and Core_*_Grain_size_avg_and_metals.csv).
  - Ensure linkage between core metadata (Table 1) and the corresponding grain size and metals datasets.
- Access considerations:
  - Confirm data access rights and any restrictions; align with disclosure and data-sharing policies; ensure appropriate licensing and attribution.
- Recommendations for ongoing stewardship:
  - Add persistent identifiers for cores and attach a standardized metadata record (e.g., methodology, QA/QC, and data lineage).
  - Include units, reference frames, and date formats consistently; provide a data dictionary to accompany CSVs.
  - Consider updating with any new analyses or reprocessing to keep the dataset current and discoverable.