# Overview What: Plant tissue 33 P (radio-isotope P) content from a 33 P tracer study to determine the uptake of P by seven different grassland plant species from three different P chemical forms in soil.

- Purpose
  - Determine if co-occurring plant species differ in uptake of P from three 33P-labelled sources (orthophosphate, DNA, calcium phosphate) to assess niche differentiation in P resource use.
  - Data collected in 2010 at the University of Sheffield; dataset prepared by Gareth K Phoenix.

- Experimental design
  - Model plant communities grown in 1 L pots with natural limestone grassland soil.
  - 30-week greenhouse growth (day/night 18°C/15°C).
  - Three 33P-labelled P sources prepared for addition to soil.
  - Plant communities: monocultures or a 7-species mix (Agrostis capillaris, Festuca ovina, Carex flacca, Carex caryophyllea, Lotus corniculatus, Plantago lanceolata, Rumex acetosa).
  - Seven replicates per P-source × community combination.
  - 33P sources injected at 10 points per pot at 5 cm depth; post-injection monitoring occurred.
  - Field survey data collected in Wardlow Hay Cop, Peak District in July–August 2011.

- Sample collection and analysis
  - Harvested aboveground biomass six days after injection; sorted by species for mixed communities; weighed dry.
  - 33P content measured by liquid scintillation counting (Packard Tri-carb 3100TR).
  - Sample preparation: freeze-dry, grind, acid digest (conc. sulfuric acid, 350°C, 10 min), oxidant, dilute, mix with scintillant.
  - Output units: 33P content as KBq per gram dry weight; also MBq per pot, DPM per pot, total MBq per pot.
  - Data normalization: % uptake per pot and per gram dry weight.

- Data structure and contents
  - Four CSV data files:
    - PuptakeFromCalciumphosphate
    - PuptakeFromDNA
    - PuptakeFromOrthophosphate
    - WardlowLimestoneSpeciesCover2011
  - PuptakeFrom* files contain 11 columns:
    - MixMono: monoculture vs mixed-community sample
    - Species: coded species identifiers (Agrostis capillaris, Festuca ovina, Carex flacca, Carex caryophyllea, Lotus corniculatus, Plantago lanceolata, Rumex acetosa)
    - PotRep: pot replicate number (note: mixed communities: replicate numbers share pots across species; monocultures have seven separate replicate pots)
    - LiveDead: tissue vitality (L1, L2 for live; D for dead)
    - DryWtg: dry weight (g)
    - DPMperPot: disintegrations per minute (decay-corrected)
    - MBqperPot: MBq per pot
    - PotBiomassg: total biomass per pot (live + dead)
    - TotalMBqPerPot: MBq for live + dead in pot
    - %UptakePerPot: percentage of injected 33P taken up by the species in that pot
    - %UptakePerG: uptake as percentage per gram dry weight
  - WardlowLimestoneSpeciesCover2011 contains survey data:
    - Quadrat: 30 replicate 50 cm x 50 cm quadrats
    - SpecName: species name codes
    - PercCov: percentage cover per quadrat (eye-based, sums can exceed 100%)

- Data provenance and completeness
  - Complete dataset overall with a small number of missing data points due to contamination and removal from analysis.

- Additional context
  - Purpose of data: enable cross-species comparisons of P source preference and potential niche differentiation in P uptake among seven grassland species.
  - Instrumentation: scintillation counting (Packard Tri-carb 3100TR) for 33P activity.