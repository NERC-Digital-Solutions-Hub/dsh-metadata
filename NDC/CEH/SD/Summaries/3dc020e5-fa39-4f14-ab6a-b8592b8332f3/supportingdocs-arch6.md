# Physical, chemical and biological data from peatland ponds, Pennines, UK, 2012-2014

## Overview
- Dataset accompanying the analysis Beadle et al. Landscape-scale peatland rewetting benefits aquatic invertebrate communities (in press, Biological Conservation).
- Aims to quantify colonisation and changes in invertebrate communities in restored peatland ponds, and to relate ecological patterns to physico-chemical variables.
- Biological data: invertebrate abundances; physical/chemical data: multiple measurements including environmental conditions and water chemistry.
- Study area: peatland ponds in the Pennine hills, northern England; data cover 2012–2014.
- Completeness: dataset is complete; pH values for five samples were estimated from a statistical relationship due to a sensor failure.

## What data are included
- Four CSV files containing four linked data components:
  1) Chron_nat_inverts.csv — 82 columns; invertebrate abundances by pond (chronosequence, natural ponds denoted with n)
  2) MH_inverts.csv — 45 columns; invertebrate abundances by pond (Moor House chronosequence dataset subset)
  3) Chron_natural_physical_chemical.csv — 26 columns; pond metadata plus physico-chemical measurements (natural ponds)
  4) MH_physical_chemical.csv — 26 columns; pond metadata plus physico-chemical measurements (Moor House dataset)
- Key data topics:
  - Biological: macroinvertebrate taxa abundances (species level where possible; Chironomidae sub-sampling applied when totals >50)
  - Physical: location, coordinates, aspect, elevation, pond dimensions, volume
  - Chemical: dissolved oxygen, temperature, pH, total nitrogen, total phosphorus, dissolved organic carbon, dissolved Al/Fe/Si, etc.
- Pond coding: pond codes (e.g., MHC06 for Moor House chronosequence pond 06); natural ponds indicated with n prefix (e.g., nWFN01).

## Study sites and sampling design
- Study components:
  - Chronosequence at Moor House National Nature Reserve (six peatlands total in chronosequence)
  - Twenty naturally-formed ponds across four peatlands (sampling locations with landowner access)
- Sampling regime:
  - Two-monthly field visits from 04/2013 to 06/2014 (ages 4–18 months), with one snow-related gap (month 14)
  - On each visit: five ditches sampled; one pond per ditch randomly selected
  - Small ponds (≤3 m²) disturbed during sampling; ponds marked and resampling avoided on the same pond in a visit
  - For chronosequence: ten ponds sampled per site across two sampling years (06/2013 and 06/2014, different ponds)
- Total ponds: 105 across all sites
- Field data collected: geographic coordinates, elevation, aspect, pond dimensions (long/short axis, perimeter), depth measurements, estimated water volume, vegetation cover

## Field and laboratory methods
- Biological sampling:
  - Macroinvertebrates collected with a long-handled net (250-µm mesh)
  - 2 minutes of sampling across mesohabitats (open water, floating vegetation, littoral vegetation, bottom sediments) + 1 minute searching for surface dwellers
  - Specimens preserved in 70% methylated spirits; transported to lab
  - Sorting, identification to species where possible; Chironomidae >50 individuals sub-sampled (n=50)
  - Chironomids prepared via chemical steps (KOH digestion, acetic acid, ethanol) and mounted for identification
- Physical measurements:
  - Altitude and location via Garmin GPS; aspect from coordinates and OS Terrain50
  - Pond dimensions and volume measured on site; mean depth derived from extensive depth measurements
  - On-site water measurements: dissolved oxygen, water temperature, and pH using HACH HQ30d
  - pH sensor failure: missing values inferred from pH–Mg relationship (r = 0.81) across samples
- Chemical analyses (on-site filter and lab):
  - Water sample filtered (0.45 µm) for total nitrogen (TN), total phosphorus (TP), dissolved organic carbon (DOC), aluminum (Al), iron (Fe), silica (Si)
  - Instruments: Analytikjena multi N/C 2100, San++ Automated Continuous Flow Analyzer, Thermo Fisher iCAP7600 Duo ICP-OES
- Methodology references: full sampling methodology described in Beadle et al. (in press)

## Data structure and formats
- File 1: Chron_nat_inverts.csv
  - 82 columns; pond code as identifier; invertebrate taxa abundances per pool
- File 2: MH_inverts.csv
  - 45 columns; pond code as identifier; invertebrate taxa abundances per pool
- File 3: Chron_natural_physical_chemical.csv
  - 26 columns; pond code; site/location; sampling date; pond age; coordinates; pond dimensions; volume; temperature; DO; pH; dissolved solutes
- File 4: MH_physical_chemical.csv
  - 26 columns; analogous structure to File 3 with Moor House dataset specifics
- Data coding notes:
  - Site names and pond identifiers align across files
  - Units and measurement methods documented within the column descriptions (e.g., temp in deg C, DO in mg/L)

## Quality control and completeness
- Macroinvertebrate specimens verified by independent experts
- Calibration and standardization:
  - Temperature, DO, and pH sensors calibrated before each field visit
  - Lab equipment for solutes calibrated with standards
- Completeness:
  - Dataset reported as complete; five pH values estimated from a statistical relationship due to sensor failure
- Publication reference for full methodology and context: Beadle et al. (in press) Biological Conservation

## How to use
- Suitable for analyses of colonisation dynamics, restoration effects on invertebrate communities, and relationships between physico-chemical variables and ecological communities
- Data can support self-serve data exploration and dashboard-style analyses through the provided structured CSVs
- Potential caveats:
  - pH imputed values; consider uncertainty in these items
  - Naturally formed ponds have some missing or non-standard metadata (e.g., NA for restoration year) in certain entries
- Suggested citation: Beadle et al. (in press); use the dataset alongside the Biological Conservation study for full methodological context