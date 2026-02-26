# Dataset: Small rodent dynamics at Lathkill Dale SSSI, Derbys, 1971-2005

## Overview
- Long-term dataset (1971–2005) of population sampling for bank voles (Myodes glareolus) and wood mice (Apodemus sylvaticus) in a Derbyshire ash woodland.
- Includes annual/seasonal ash fruit-fall and a measure of winter severity; incorporates a 4-year experiment with supplementary ash fruit.
- Aims to explain between-year variation in reproductive and population growth using a state-space modelling approach; fruit-addition experiments aid interpretation.

## Data collected and variables
- Population data from live-trapping (catch-mark-release) on a 0.45 ha grid (90 Longworth traps; two 24-hour trapping periods per session, approximately every 6 months).
- Species: bank vole and wood mouse; adults and juveniles tracked (May/June and Nov/Dec periods).
- Environmental drivers:
  - Ash fruit-fall: annual dry-weight edible seed (g m^-2), split into Sept–Dec and Dec–Mar/Apr sub-totals.
  - Winter severity: mean minimum daily temperature Dec–Mar.
- Experimental manipulation:
  - Supplementary ash fruit introduced in two winters (1981–82, 1984–85) on an adjacent grid to compare against control.
- Outputs:
  - Population indices from marked adults; model-validated population estimates; juvenile counts; dates of collections.
- Data granularity:
  - Separate datasets for control vs experimental areas and for each species, with clearly defined temporal and sampling fields.

## Modelling and findings
- State-space modelling links demographic rates to environmental drivers (fruit-fall, winter severity) and density dependence.
- Key findings:
  - September–March fruit-fall strongly drives bank vole spring reproduction and growth; weaker but present influence on wood mice.
  - Winter severity affects bank vole winter growth and wood mouse spring growth; no winter breeding detected for either species.
  - Fruit-fall effects can persist for a year or more; density dependence significantly shapes both winter and summer growth.
  - Ash-fruit addition experiments confirmed the influence of autumn fruit availability on bank vole winter growth.
  - Overall, results show species-specific responses and notable delayed demographic effects.

## Location and collection regime
- Location: Lathkill Dale, Derbyshire, UK; primary study area 0.45 ha with ash-dominated woodland.
- Experimental area: ~150 m from control; similarly conditioned habitat.
- Data collection regime:
  - 1971–2005: six-monthly trapping (December–March and May–June) across 24-hour periods.
  - Environment and disturbance data collected in parallel (e.g., temperature, fruit-fall measurements).

## Data files and structure
- Data files (CSV) cover both species and both study areas, with explicit column structures:
  - Apodemus (wood mice):
    - FlowerdewApodemusData041212csv.csv: long-term environmental and population data (1971–2005).
    - FlowerdewApodemusExData040613Controlcsv.csv: control-area data (1981–1985).
    - FlowerdewApodemusExData040613Experimentalcsv.csv: experimental-area data (1981–1985).
  - Myodes (bank voles):
    - FlowerdewMyodesData291112csv.csv: long-term population and environmental data (1971–2005).
    - FlowerdewMyodesExData040613Controlcsv.csv: control-area data (1981–1985).
    - FlowerdewMyodesExData040613Experimentalcsv.csv.csv: experimental-area data (1981–1985).
- Each file includes detailed columns for year of collection, dates, counts (adults/juveniles), trapping periods, density indices, population estimates, temperature, and fruit-fall subtitles.

## Data quality, documentation, and governance
- Rich metadata accompanying each dataset (clear column headers, units, sampling methods, and trapping regime).
- Explicit description of experimental design (control vs experimental plots; ash-fruit addition protocol).
- Provenance documented: authors, affiliations, and contact details; dataset lineage preserved.
- Data are suitable for re-analysis, time-series modelling, and comparative studies on masting, climate effects, and small mammal demography.

## Access, sharing, and reuse
- Data provided as structured CSVs with thorough documentation, enabling reuse for modelling and meta-analyses.
- Suitable for investigations into long-term population dynamics, environmental drivers, and the impact of resource pulses.
- Usage should acknowledge original authors; consider contacting corresponding author for clarifications or additional metadata.

## Potential limitations and stewardship notes
- Multi-decade span may involve methodological changes; ensure consistent interpretation of trap effort, density indices, and population estimates.
- Occasional years with negligible fruit-fall or incomplete data; account for gaps in analysis.
- Plan for long-term preservation, keep metadata synchronized with any data portal migrations, and maintain explicit links to the experimental design.

## Practical guidance for Data Stewards
- Ensure discoverability and interoperability in data portals via a standardized metadata schema (including variables for fruit-fall, winter severity, and density indices).
- Maintain data dictionaries with units (e.g., g m^-2 for ash seed, degrees Celsius for temperature) and clearly define density indices vs. model-based population estimates.
- Preserve the clear separation between control and experimental datasets and document the exact fruit-addition protocol and timing.
- Provide clear provenance, licensing, and citation information; include instructions for replicating the state-space analysis or applying similar models to the data.
- Facilitate long-term storage, periodic updates, and provenance tracking to support future re-use and integration with other long-term ecological datasets.