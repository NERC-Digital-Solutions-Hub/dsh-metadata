# Plant tissue 33 P (radio-isotope P) content from a 33 P tracer study to determine the uptake of P by seven different grassland plant species from three different P chemical forms in soil

## Purpose and context
- Objective: Determine if co-occurring plant species differ in their uptake of phosphorus (P) from three different P sources, to assess potential niche differentiation in P resource use.
- Location: Arthur Willis Environment Centre, University of Sheffield, UK.
- Timeframe: Experimental work in 2010; plant survey data collected July–August 2011.
- Responsible researcher: Gareth K Phoenix, University of Sheffield.
- Completeness: Dataset is complete except for a small number of missing data points due to contaminated samples that were removed from analysis.

## Experimental design
- Plant communities: 1 L pots containing limestone grassland soil with either monocultures or a seven-species mix.
- Species included in the mix: Agrostis capillaris, Festuca ovina, Carex flacca, Carex caryophyllea, Lotus corniculatus, Plantago lanceolata, Rumex acetosa.
- Growth conditions: 30 weeks in a climate-controlled greenhouse (day/night 18°C/15°C).
- P sources: Three 33 P-labelled phosphorus sources synthesized for soil addition:
  - Orthophosphate
  - DNA (33 P-labelled nucleotides)
  - Calcium phosphate
- Replication: Seven replicates per P-source × plant-community combination.
- Application: 33 P solutions (or suspensions for calcium phosphate) injected at 10 points to a depth of 5 cm, with gradual withdrawal to ensure distribution.
- Post-treatment: After six days, aboveground biomass harvested and separated by species for mixed communities.

## Sample collection and analysis
- Biomass processing: Harvested, dried, and measured; 33 P content determined by scintillation counting.
- Unit of measurement: 33 P content expressed as KBq per gram of plant shoot.
- Sample preparation: Freeze-dried biomass ground and acid-digested; digestion followed by hydrogen peroxide oxidation; analysis by liquid scintillation counting.
- Instrumentation: Packard Tri-carb 3100TR scintillation counter (Perkin Elmer, Cambridge, UK).

## Data structure and variables
- Primary data files (four CSVs):
  - PuptakeFromCalciumphosphate
  - PuptakeFromDNA
  - PuptakeFromOrthophosphate
  - WardlowLimestoneSpeciesCover2011
- PuptakeFrom* files (11 columns each):
  - MixMono: Monoculture (Mono) or mixed community (Mix)
  - Species: Codes for species (ACA, FOF, CFC, CCC, LCL, PL, RAR)
  - PotRep: Pot replicate identifier
  - LiveDead: Tissue quality (L1, L2 for live; D for dead)
  - DryWtg: Dry weight (g)
  - DPMperPot: Disintegrations per minute, decay-corrected
  - MBqperPot: MBq activity per pot
  - PotBiomassg: Total in-pot biomass (g)
  - TotalMBqPerPot: MBq activity for live + dead material per pot
  - %UptakePerPot: Percentage of injected 33P taken up by the species in that pot
  - %UptakePerG: Uptake per gram dry weight
- WardlowLimestoneSpeciesCover2011 file (3 columns):
  - Quadrat: Quadrat identifier (30 replicates)
  - SpecName: Species code
  - PercCov: Estimated percent cover (by eye; totals may exceed 100%)

## Survey data context
- WardlowLimestoneSpeciesCover2011 provides additional community composition data across the sampled quadrats to contextualize P uptake within local species abundance and cover patterns.

## Data quality, provenance and completeness
- Completeness: Overall complete with a small number of missing data points due to contaminated samples removed from analysis.
- Data provenance: Experiment designed and executed to compare P source use among seven grassland species under controlled conditions; uptake metrics calculated from standardized scintillation counting workflow.

## How this dataset supports environmental monitoring and analysis
- Enables standardized assessment of how different plant species obtain nutrients from multiple P forms, informing models of P cycling and resource partitioning in grassland ecosystems.
- The standardized data structure (per species, pot, and P source) supports cross-site comparisons and integration with other monitoring datasets.
- Facilitates quality assurance by providing explicit definitions of each variable and consistent units (KBq, MBq, % uptake, g biomass).
- Supports data transparency and reuse by including both uptake data and accompanying vegetation cover context.