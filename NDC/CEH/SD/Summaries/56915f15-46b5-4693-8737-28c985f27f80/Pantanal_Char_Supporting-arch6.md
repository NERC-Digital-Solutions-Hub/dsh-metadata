# SUPPORTING DOCUMENTATION FOR 'Radiocarbon-dated charcoal datasets obtained from lake sediments from the Pantanal, Brazil'

- This document describes charcoal datasets derived from macroscopic charcoal fragments in radiocarbon-dated lake sediment cores from the Pantanal, Brazil. Geographic and collection-generation data are summarized in Table 1.

## Data content and structure

- Core sites and data
  - Laguna Mandior e cores M1 and M5
  - Laguna Mimoso
  - Laguna Caceres
- For each record
  - Core collection date, coordinates, lake area, lake depth, elevation, and maximum sediment-core depth
  - Nature of sediments and collection method
- Charcoal data
  - Concentration data: particles >125 μm per cm3 at each 1-cm sediment horizon
  - Depth value represents the midpoint of the 1-cm interval
- Data files
  - Concentration data are stored as individual CSV files per core
  - Radiocarbon dates associated with each core are provided as headers within each CSV
  - Radiocarbon ages are uncalibrated conventional radiocarbon years BP

## Quality control and laboratory methods

- Standard laboratory procedures for preparation and counting of charcoal fragments
- Deflocculation and dispersion:
  - Clay-rich sediments: 7% sodium hexametaphosphate (Na6P6O18), 200 ml
  - Organic-rich sediments: 10% potassium hydroxide (KOH), 200 ml
  - Deflocculation performed at 80°C for 30 minutes
  - Organic residues washed and treated with 7% hydrogen peroxide for 24 hours
- Sieving and counting
  - Residues sieved at 125 μm and 250 μm
  - Counting performed under a low-powered microscope in a Bogorov tray
- Volume measurement by water displacement
- 1-cm residence sampling resolution

## Data structure and radiocarbon dating details

- Data structure
  - Each core’s concentration data in a separate CSV file
  - Radiocarbon dates for each core included as headers to create age-depth profiles
  - Data reported as sediments dated at discrete horizons (1-cm intervals)
- Radiocarbon dating table (Table 2)
  - Number of radiocarbon dates per core
  - Radiocarbon date provider (e.g., Beta Analytic, UGAMS)
  - Units: Conventional Radiocarbon years BP
  - Data structure: calibrated into an age-depth framework with full laboratory reporting
  - Includes documentation of quality control per laboratory (ISO details available from labs)

## Cores and representative dating details

- Laguna Caceres
  - Radiocarbon dates (uncalibrated): 1940 ± 30 BP at 41 cm; 1150 ± 30 BP at 21 cm; 260 ± 30 BP at 13 cm
  - d13C values provided for dated samples (e.g., -14.7, -11.1, -9.5 per mil)
- Laguna Mandior e core M1
  - 3 radiocarbon dates from Beta Analytic; conventional ages provided; used to create age-depth profile
  - Sample depths and IDs correspond to horizons used in charcoal data
- Laguna Mandior e core M5
  - 3 radiocarbon dates from Beta Analytic; conventional ages provided; age-depth profile
  - Sample depths correspond to horizon positions in charcoal data
- Laguna Mimoso
  - 2 radiocarbon dates (Beta Analytic and UGAMS); conventional ages provided
  - Sample depths correspond to horizon positions in charcoal data

## Data use and considerations for re-use

- Ages are uncalibrated radiocarbon (BP); calibrate as needed using a calibration curve
- Depth-resolution is 1 cm; charcoal concentration is reported as particles per cm3
- Data are organized per core in CSVs with radiocarbon dates embedded in headers for traceability
- Full laboratory reports and documentation are available via the listed date providers for each sample