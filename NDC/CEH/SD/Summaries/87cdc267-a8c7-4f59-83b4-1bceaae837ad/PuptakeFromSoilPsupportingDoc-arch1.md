# Plant tissue 33 P (radio-isotope P) content from a 33 P tracer study to determine the uptake of P by seven different grassland plant species from three different P chemical forms in soil.

- What and aim
  - A study to measure uptake of 33P by seven grassland plant species from three different phosphorus (P) chemical forms in soil.
  - Objective: determine if co-occurring species show different P source preferences (niche differentiation in P use).

- Location and timing
  - Conducted at Arthur Willis Environment Centre, University of Sheffield, UK.
  - Year: 2010 for the experiment; plus plant survey data collected in Wardlow Hay Cop in 2011.

- Experimental design
  - Model plant communities grown in 1 L pots with limestone grassland soil.
  - Growth period: 30 weeks in a climate-controlled greenhouse (18°C day / 15°C night).
  - Three P sources labelled with 33P: orthophosphate, DNA, calcium phosphate.
  - Plant communities: monocultures for each species or a 7-species mix (Agrostis capillaris, Festuca ovina, Carex flacca, Carex caryophyllea, Lotus corniculatus, Plantago lanceolata, Rumex acetosa).
  - Seven replicates per P-source × plant-community combination.
  - 33P solutions injected at 10 points in soil to a depth of 5 cm with gradual withdrawal of the needle.
  - DNA and calcium phosphate prepared with 33P; orthophosphate purchased with 33P.

- Sampling and measurements
  - Six days after 33P injection, aboveground biomass harvested, sorted by species (in mixed communities), dried, and weighed.
  - 33P content measured by scintillation counting to determine uptake.
  - Plant survey data collected later in 2011 from Wardlow limestone grassland: 30 quadrats (50 cm × 50 cm) to capture species cover.

- Laboratory instrumentation and methods
  - Scintillation counting: Packard Tri-carb 3100TR (Perkin Elmer).
  - Sample preparation: dry biomass ground, acid-digested with concentrated sulphuric acid at 350°C for 10 minutes; cooled and treated with hydrogen peroxide; diluted to 10 mL; 1 mL added to 10 mL scintillant.
  - 33P content expressed as kilobecquerels per gram of plant shoot (KBq g⁻¹).

- Data structure and files
  - Four CSV data files:
    - PuptakeFromCalciumphosphate
    - PuptakeFromDNA
    - PuptakeFromOrthophosphate
    - WardlowLimestoneSpeciesCover2011
  - PuptakeFrom* files: 11 columns each
    - MixMono: Monoculture (Mono) or mixed community (Mix)
    - Species: Codes for the seven species
    - PotRep: Pot replicate number
    - LiveDead: Tissue status (live = L1/L2, dead = D)
    - DryWtg: Dry weight (g)
    - DPMperPot: Disintegrations per minute, decay-corrected
    - MBqperPot: Activity in MBq per pot (converted from DPM)
    - PotBiomassg: Total biomass in pot (live and dead)
    - TotalMBqPerPot: MBq activity of live+dead in the pot
    - %UptakePerPot: Percentage of injected 33P taken up by that species in that pot
    - %UptakePerG: Uptake as a percentage per gram dry weight
  - WardlowLimestoneSpeciesCover2011 file: 3 columns
    - Quadrat: Quadrat identifier (30 replicate quadrats)
    - SpecName: Species name code
    - PercCov: Percentage cover per quadrat (survey by eye; total can exceed 100%)

- Species and sample nomenclature
  - Species codes: ACA (Agrostis capillaris), FOF (Festuca ovina), CFC (Carex flacca), CCC (Carex caryophyllea), LCL (Lotus corniculatus), PL (Plantago lanceolata), RAR (Rumex acetosa).
  - Mix vs. Mono indicates whether tissue sample came from a mixed plant community or a monoculture.

- Data completeness and quality
  - Dataset is complete aside from a small number of missing data points due to sample contamination and subsequent removal from analysis.