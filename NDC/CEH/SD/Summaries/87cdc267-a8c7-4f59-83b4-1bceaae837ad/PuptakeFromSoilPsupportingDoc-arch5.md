# Plant tissue 33 P (radio-isotope P) content from a 33 P tracer study to determine the uptake of P by seven different grassland plant species from three different P chemical forms in soil

- Overview
  - What: Measurement of 33P uptake in aboveground plant tissue from a tracer study, assessing uptake from three P chemical forms (orthophosphate, DNA, calcium phosphate) across seven grassland species.
  - Where: Arthur Will is Environment Centre, University of Sheffield, UK.
  - When: Experiment conducted in 2010; plant survey data from Wardlow Limestone in 2011.
  - Why: To determine whether co-occurring plant species show niche differentiation in phosphorus (P) resource use.
  - Responsible: Gareth K Phoenix, University of Sheffield, UK.
  - Completeness: Dataset largely complete; a small number of data points are missing due to sample contamination and removal from analysis.

- Experimental design
  - Model plant communities grown in 1 L pots using natural limestone grassland soil.
  - Plants grown for ~30 weeks in a climate-controlled greenhouse (day/night 18°C/15°C).
  - Three 33P-labeled P sources prepared and added to soil to measure uptake.
  - Community types: monocultures and a seven-species mix (Agrostis capillaris, Festuca ovina, Carex flacca, Carex caryophyllea, Lotus corniculatus, Plantago lanceolata, Rumex acetosa).
  - Replication: seven replicates for each P-source x community combination.
  - 33P labeling: DNA labeled with 33P, calcium phosphate formed with 33P orthophosphate, orthophosphate purchased.
  - Application: 33P solutions (and calcium phosphate suspensions) injected at 10 points, depth 5 cm, while withdrawing needle to distribute P through soil profile.

- Sample collection and analysis
  - Harvest: Aboveground biomass collected six days after 33P injection, sorted by species for mixed communities.
  - Processing: Biomass dried, weighed, ground; ~50 mg digested with concentrated sulfuric acid, oxidized, and prepared for scintillation counting.
  - Measurement: 33P content determined by liquid scintillation counting; units expressed as KBq per gram of plant shoot.

- Laboratory instrumentation
  - Scintillation counting performed with Packard Tri-carb 3100TR (Perkin Elmer).
  - Sample prep includes acid digestion, oxidation, and scintillant-based counting.

- Analytical method and units
  - Biomass: dry weight per pot.
  - 33P measurement: DPM per pot (decays per minute, decay-corrected), converted to MBq per pot.
  - Uptake metrics: TotalMBqPerPot, %UptakePerPot, %UptakePerG (per gram dry weight).

- Data structure
  - Four CSV files: PuptakeFromCalciumphosphate, PuptakeFromDNA, PuptakeFromOrthophosphate, WardlowLimestoneSpeciesCover2011.
  - PuptakeFrom* sheets: 11 columns – MixMono, Species, PotRep, LiveDead, DryWtg, DPMperPot, MBqperPot, PotBiomassg, TotalMBqPerPot, %UptakePerPot, %UptakePerG.
  - WardlowLimestoneSpeciesCover2011: Quadrat, SpecName, PercCov.

- Variable names and coding
  - MixMono: Mono = monoculture samples; Mix = mixed-community samples.
  - Species: Codes for seven grassland species.
  - PotRep: Pot replicate number; in mixed communities, same PotRep indicates different species from the same pot; in monocultures, seven separate pots per species.
  - LiveDead: Live tissue samples (L1, L2) and dead tissue (D); limited to live tissue for most measurements.
  - DryWtg: Dry weight (g) per pot.
  - DPMperPot / MBqperPot: Activity measures with decay corrections.
  - PotBiomassg: Total biomass per pot (live and dead).
  - %UptakePerPot / %UptakePerG: Uptake efficiency per pot and per gram dry weight.

- Survey data
  - WardlowLimestoneSpeciesCover2011 provides quadrat-level plant cover data for the limestone grassland survey (30 quadrats, 50 cm x 50 cm), with SpecName and PercCov (percentage cover; totals may exceed 100% due to visual estimation).

- Data governance and reuse considerations for Data Stewards
  - Metadata needs: clear documentation of species codes, treatment groupings (monoculture vs mixed), experimental replicates, LiveDead distinctions, measurement units, and decay corrections.
  - Provenance: record labeling methods for 33P sources, synthesis details for DNA and calcium phosphate, injection protocol, and timing of harvest.
  - Data quality: note the contamination-related exclusions and how missing data were handled; maintain a data quality log.
  - Versioning and linkage: ensure consistent linking between PuptakeFrom* datasets and WardlowLimestoneSpeciesCover2011 for ecological interpretation.
  - Accessibility: specify storage locations and any access restrictions for the four CSV files.