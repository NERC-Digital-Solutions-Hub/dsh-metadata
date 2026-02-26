# Brief description of the dataset

- This dataset documents microplastic particles extracted from sediments of four sampling sites across three Thames tributaries (the Leach, the Lambourn, and The Cut) in the UK, collected August–September 2014.
- Data are provided as counts by category (type, colour, and composition) and include site context, sample metadata, and a subsample with chemical composition identified by Raman spectroscopy.
- Researchers aim to relate microplastic abundance to anthropogenic impact by linking particle counts to site characteristics such as sewage effluent input and population density.

## Scope and sampling design

- Sampling sites chosen to represent a gradient of sewage input and upstream population served by sewage treatment works; four sites in total (two The Cut sites; one each for Leach and Lambourn).
- Four sediment replicates per site collected along a 3 m transect at 1 m intervals, surface sampled to about 10 cm depth.
- Samples processed into two size fractions: 1–2 mm and 2–4 mm.
- Seasonal low-flow period sampled (late Aug–early Sep 2014).

## Data collected and variables

- Three CSV data files:
  - ThamesMicroplastics_SamplingLocation.csv: site characteristics (Site_name, Grid_reference, Sewage_effluent_ average_percentage, Population_equivalent_density, etc.).
  - ThamesMicroplastics_Number OfParticles.csv: total microplastic particles per sample (per Sample_ID) and weight-related fields.
  - ThamesMicroplastics_ParticleCharacteristics.csv: detailed characteristics for a 20% subsample (particle-level data on type, colour, and Raman-identified polymer composition).
- Particle categories and characteristics:
  - Types: Fragment, Fibre, Film, plus separate Note for Glass (not a microplastic).
  - Colours recorded (e.g., Red, Yellow, Blue, Green, White, Beige, Grey, Purple, Black, Clear).
  - Polymers identified by Raman: PE, PP, PS, PVC, PET, Nylon, Polyester, Other_polymer, Copper_phthalocyanine/mortoperm_blue, Other_manmade, Natural_substance, Unidentifiable.
- Sample and processing metadata:
  - Sample_ID, Replicate_number, Size_fraction (1–2 mm or 2–4 mm), Subsample_40_grams indicator, Sorting_step, Total_weight_(grams).
  - Total_microplastics per sample (sum across fragments, fibres, films).

## Processing and analytical workflow

- Site selection and sampling context documented with LF2000 WQX-based estimates of effluent and upstream population density.
- Sample processing in three steps:
  - Step 1: Visual inspection of sieved sediments under a binocular microscope to identify potential microplastics using defined morphological criteria (with two additional criteria to avoid missing plastics). Particles must meet at least two of six qualitative cues (e.g., unnatural color, coating, shape, fiber integrity, shiny/glassy, flexible).
  - Step 2: Flotation in a dense ZnCl2 solution (1.7–1.8 g/mL) to separate buoyant plastics; repeated shaking and overflow collection to maximize recovery; float is filtered and dried for inspection.
  - Step 3: Final inspection of unfloated sediment to recover additional dense particles not captured in flotation.
- Contamination controls: three procedural blanks (ZnCl2 drawn through filters) processed to monitor airborne/handling contamination.
- Raman spectroscopy (chemical characterization):
  - 20% of particles sampled for Raman analysis; random selection within each sample.
  - Spectra acquired at 50x with a 785 nm laser; spectral range 600–3200 cm−1; analyses performed with KnowItAll Raman ID Expert to identify polymers and related pigments.
  - Raman results used to assign polymer identity and distinguish natural or unidentifiable particles.

## Data format and metadata

- File formats: three CSV files containing site metadata, particle counts, and particle-level Raman-characterized data.
- Key fields and their meanings:
  - Site_name, Grid_reference: site identity and exact location (British National Grid).
  - Sewage_effluent_(average_percentage), Population_equivalent_density: site-level context related to anthropogenic impact.
  - Sample_ID, Replicate_number: sample and replicate identifiers.
  - Size_fraction: 1–2 mm or 2–4 mm.
  - Subsample_40_grams: indicates whether the analysis used a subsample >40 g.
  - Sorting_step: extraction stage at which particles were obtained.
  - Total_weight_(grams): dry weight of the sediment sample analyzed.
  - Fragment, Fibre, Film, Glass: particle type classifications.
  - Total_microplastics: total microplastic count in the sample.
  - Colour columns: counts by color (Red, Yellow, Blue, Green, White, Beige, Grey, Purple, Black, Clear).
  - Polymer columns: Polymer identity as determined by Raman (PE, PP, PS, PVC, PET, Nylon, Polyester, Other_polymer, Copper_phthalocyanine/mortoperm_blue, Other_manmade, Natural_substance, Unidentifiable).
- Documented references support methods and interpretation (e.g., Horton et al. 2017; Claessens et al. 2013; Nor & Obbard 2014; and related methodological sources).

## Data provenance and references

- Methods draw on established procedures for microplastic extraction and identification in sediments, including:
  - Horton et al. (2017) for large microplastics in Thames tributaries.
  - Claessens et al. (2013); Imhof et al. (2012) for extraction approaches.
  - Nor & Obbard (2014) for visual identification criteria.
- Site context and broader Thames Basin references cited (Bowes et al. 2014; Williams et al. 2009; Pottinger et al. 2013; etc.).

## Data governance and stewardship considerations

- Data quality and usability:
  - Clear documentation of site selection rationale and sampling design enables reproducibility and meta-analysis relating microplastic abundance to effluent exposure and population density.
  - Multi-step extraction workflow with contamination controls enhances data trustworthiness; however, limitations remain:
    - Small particles <1 mm are not accurately detected with the described methods.
    - Only 20% of particles undergo chemical characterization, which may limit polymer-level inference for the full dataset.
- Metadata and interoperability:
  - Use of standard coordinate system (British National Grid) and explicit site descriptors supports integration with other Thames datasets.
  - Separator conventions (size fractions, replicate structure) and explicit column descriptions support data reuse in catalogues and portals.
- Data sharing and maintenance:
  - Dataset comprises three CSV files with machine-readable fields; suitable for deposition in data portals and institutional repositories.
  - Documentation links to established references, enabling users to understand methods, uncertainties, and potential biases.
- Practical challenges for Data Stewards:
  - Ensuring consistent interpretation of visual identification criteria across users and future re-analyses.
  - Maintaining alignment with evolving analytical standards (e.g., detection limits for <1 mm particles) and potential method updates.
  - Managing potential updates or additions to site-level data if extended sampling occurs.

## Practical takeaways for reuse

- The dataset is well-suited for analyses linking microplastic abundance to sewage inputs and population density in riverine sediments.
- Users should account for:
  - Size-range limitations (no reliable data for <1 mm).
  - Partial chemical characterization (only 20% of particles) when inferring polymer distributions.
  - Site-specific context (LF2000-based effluent estimates and upstream population served) to interpret abundance patterns.
- For governance, include metadata in data portals, note methodological limitations, and provide clear provenance to assist future data stewardship and integration with related Thames datasets.