# Overview

- What: Plant tissue 33 P (radio-isotope P) content from a tracer study to determine P uptake by seven grassland species from three P chemical forms in soil.
- Where: Arthur Willis Environment Centre, University of Sheffield, Sheffield, UK.
- When: Experimental work in 2010; plant survey data collected July–August 2011.
- How: Three 33 P sources (orthophosphate, DNA, calcium phosphate) injected into limestone grassland soil in pots containing monocultures or a seven-species mix; six days later, aboveground biomass harvested and 33 P uptake measured by scintillation counting.
- Why: To assess whether co-occurring species show different P-source preferences (niche differentiation in P uptake).
- Who responsible: Gareth K. Phoenix, University of Sheffield, UK.
- Completeness: Dataset is complete except for a small number of missing data points due to sample contamination and subsequent removal from analysis.

## Experimental design

- Model plant communities grown in 1 L pots with natural limestone grassland soil.
- Growth period: 30 weeks in a climate-controlled greenhouse (day/night 18°C/15°C).
- P sources: Three 33 P-labelled forms synthesized/obtained for injecting into soil; seven species used in mixes: Agrostis capillaris, Festuca ovina, Carex flacca, Carex caryophyllea, Lotus corniculatus, Plantago lanceolata, Rumex acetosa.
- Community types: Monocultures and a 7-species mixture.
- Replication: Seven replicates for each P-source × plant-community combination.
- Injection details: 33 P solutions (and calcium phosphate suspensions) injected at 10 points to 5 cm depth with gradual withdrawal to distribute P through the soil profile.
- Plant survey data collection: 30 quadrats (50 x 50 cm) in Wardlow Hay Cop (Field location) in July–Aug 2011 to characterize soil/plant context.

## Sample collection, analysis, and instrumentation

- Harvest: Aboveground biomass harvested six days after 33 P injection; separated by species for mixed communities; dried weights recorded.
- 33 P measurement: Biomass digested (sulphuric acid at 350°C, with peroxide cleanup), emulsifying scintillant added, and 33 P activity measured via liquid scintillation counting.
- Units: 33 P content expressed as KBq per gram of dry plant shoot.
- Instrumentation: Scintillation counting using Packard Tri-carb 3100TR (Perkin Elmer).

## Data structure and content

- Files: Four CSVs:
  - PuptakeFromCalciumphosphate
  - PuptakeFromDNA
  - PuptakeFromOrthophosphate
  - WardlowLimestoneSpeciesCover2011
- PuptakeFrom* files (11 columns each): 
  - MixMono: Monoculture (Mono) or mixed community (Mix)
  - Species: Species code (ACA, FOF, CFC, CCC, LCL, PL, RAR)
  - PotRep: Pot replicate number (careful with Monoculture vs Mix)
  - LiveDead: Tissue status (Live samples L1/L2; D for dead)
  - DryWtg: Dry weight per pot (g)
  - DPMperPot: Decay-corrected disintegrations per minute
  - MBqperPot: MBq per pot
  - PotBiomassg: Total biomass in pot (live + dead)
  - TotalMBqPerPot: MBq activity for live + dead per pot
  - %UptakePerPot: Share of injected 33P taken up by the species in that pot
  - %UptakePerG: Uptake per gram dry weight
- WardlowLimestoneSpeciesCover2011 file (3 columns):
  - Quadrat: Quadrat identifier (30 replicates)
  - SpecName: Species name code
  - PercCov: Percentage cover per quadrat (field survey; sum may exceed 100%)
- Species codes correspond to the seven grassland species listed above.

## Variable definitions and units

- 33 P uptake metrics:
  - DPMperPot and MBqperPot measure activity; totals can be converted to % uptake per pot or per gram dry weight.
  - %UptakePerPot and %UptakePerG indicate uptake efficiency relative to injected P, either per pot or per gram of tissue.
- Sampling details:
  - LiveDead differentiates tissue viability; duplicates typically exist for live tissue measurements.
- Survey data:
  - PercCov provides field-based species cover estimates per quadrat.

## Data quality, provenance, and notes

- Completeness: Largely complete; a small number of data points missing due to contamination and removal from analysis.
- Provenance: Data collected from controlled greenhouse experiment with explicit P sources and plant combinations; plant survey data collected in the field at Wardlow Hay Cop.
- Metadata and clarity: Extensive documentation of variable names, coding (MixMono, Species), and measurement procedures (digestion, scintillation counting) supports data discoverability and reuse.

## Relevance to data leadership and stewardship

- Data assets are organized into clearly named CSV files with well-defined variables and units, supporting discoverability and interoperability.
- Provenance and methodology are detailed, enabling reproducibility and proper data interpretation across teams or networks.
- The structure supports cross-referencing uptake results by P source, plant species, and community type, enabling comparative analyses and meta-studies.
- Emphasizes careful metadata capture (including replication, live/dead tissue status, and per-pot vs per-gram metrics) to facilitate correct aggregation and downstream analytics.
- Highlights data quality practices (decay correction, unit conversions) and traceability from laboratory methods to dataset variables.