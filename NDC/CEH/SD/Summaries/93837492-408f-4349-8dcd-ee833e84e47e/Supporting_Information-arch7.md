# Brief description of the dataset

- Dataset on microplastic particles extracted from sediments of Thames River tributaries (UK) across four sampling sites in three rivers (Leach, Lambourn, The Cut) during Aug–Sep 2014.
- Particles are categorized by size (1–2 mm and 2–4 mm), type (fragment, fibre, film), and colour; a subsample (20%) is characterised chemically by Raman spectroscopy to determine polymer composition.
- Site characteristics include average sewage effluent percentage and population-equivalent density, enabling analysis of anthropogenic impact on microplastic abundance.
- Data are intended to support GIS-ready mapping and exploration of spatial patterns and drivers of microplastic presence.

## Sampling design and site information

- Four sampling sites representing a gradient of sewage input and population density:
  - River Leach (low), River Lambourn (low–moderate), The Cut site 1 (intermediate, upstream of effluent), The Cut site 2 (high, downstream of effluent).
- Sampling timeframe: 28 August – 3 September 2014 (seasonal low-flow conditions).
- At each site: four replicate sediment samples collected at 1 m intervals along a 3 m transect, surface sediment to ~10 cm depth, stored in 1 L jars.
- Site-level data captured for each site:
  - Grid reference, river name, Sewage_effluent_ (average %), Population_equivalent_density.
- Each sediment sample assigned a unique Sample_ID with a Replicate_number (four replicates per site).

## Processing and analysis workflow

- Three-part sample processing to extract microplastics:
  - Step 1: Visual inspection of sieved sediments (1–2 mm and 2–4 mm fractions) under binocular microscope; apply criteria to identify potential microplastics (requires meeting at least two of several visual/physical criteria).
  - Step 2: Flotation using a dense ZnCl2 solution (1.7–1.8 kg/L); centrifugation-like shaking and overflow to separate buoyant particles; floated particles collected on 1.2 µm filters and dried.
  - Step 3: Visual inspection of unfloated sediment post-flotation to recover any particles not captured by flotation; filtered and re-inspected.
- Contamination controls: three field-process controls (ZnCl2 solution filtered through identical filters) to assess airborne contamination.
- Particle identification and categorisation:
  - Particles classified as Fragment, Fibre, Film (and occasionally Glass as non-microplastic). Observations of plastic pellets were absent.
- Chemical characterisation (Raman spectroscopy):
  - 20% of total particles from each sample analysed randomly (using 785 nm laser, 30 s exposure, spectra 600–3200 cm⁻¹).
  - Spectra compared to reference library with BioRad KnowItAll Raman ID Expert; polymer types identified include PE, PP, PS, PVC, PET, Nylon, Polyester, Other_polymer, plus pigments and other substances.
- Fractions and storage:
  - Size fractions retained for analysis (1–2 mm and 2–4 mm); dry-weight measurements recorded; samples stored and protected from contamination.

## Dataset structure and fields

- ThamesMicroplastics_SamplingLocation.csv
  - Site_name, Description; Grid_reference; Sewage_effluent_; Population_equivalent_density.
- ThamesMicroplastics_Number OfParticles.csv
  - Sample_ID; Replicate_number; Size_fraction; Subsample_40_grams; Sorting_step; Total_weight_(grams); Total_microplastics; and counts by Fragment, Fibre, Film, Glass; Colour counts; Polymer counts (PE, PP, PS, PVC, PET, Nylon, Polyester, Other_polymer); Other_manmade pigments and substances; Natural_substance; Unidentifiable.
- ThamesMicroplastics_ParticleCharacteristics.csv
  - Particle-level data for the 20% subsample analysed by Raman: includes Particle_ID, Sample_ID, Site_name, Replicate_number, Size_fraction, Colour, Fragment/Fibre/Film status, Polymer (as identified by Raman), and other Raman-derived descriptors.

- Key field descriptions:
  - Sample_ID: unique identifier for each sediment sample.
  - Replicate_number: four replicate samples per site.
  - Size_fraction: 1–2 mm or 2–4 mm.
  - Subsample_40_grams: indicates whether a subsample >40 g was used.
  - Sorting_step: which step extracted the particle (visual, flotation, or post-flotation visual).
  - Total_weight_(grams): dry weight of the analysed sediment.
  - Fragment, Fibre, Film: microplastic category classifications.
  - Colour: observed colour categories (e.g., Red, Blue, Green, White, etc.).
  - Polymer columns: polymer type identified by Raman (e.g., PE, PP, PS, PVC, PET, Nylon, Polyester, Other_polymer).
  - Other_polymer, Other_manmade, Natural_substance, Unidentifiable: additional Raman-derived classifications.

## Potential GIS applications

- Map spatial distribution of microplastics across Thames tributaries and sites.
- Explore relationships between microplastic abundance and site characteristics (sewage effluent percentage, population density).
- Analyze distribution of particle types (fragments, fibres, films) and polymer types by location.
- Integrate with other Thames Initiative datasets for multi-criteria environmental analysis.
- Create visuals by size fraction, colour, and polymer composition to support policy and communication efforts.

## Quality, limitations and notes

- Size detection limits: small microplastics <1 mm not accurately determined; the analysis focused on 1–2 mm and 2–4 mm fractions.
- Visual identification criteria balance sensitivity and specificity to avoid false positives; Raman spectroscopy applied to a 20% subsample for chemical identification.
- Contamination controls implemented via field blanks to assess potential airborne contamination.
- Data context relies on methodology from Horton et al. (2017) and related references cited in the document.