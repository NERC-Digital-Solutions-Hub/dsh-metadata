# Thames Microplastics Dataset from Sediments in Thames River Tributaries, UK

- This dataset documents microplastic particles extracted from river sediment across four sampling sites in three Thames tributaries (Leach, Lambourn, The Cut) collected in Aug–Sept 2014.
- Particles are categorized by size (1–2 mm and 2–4 mm), type (fragment, fibre, film), and color; a subsample was analyzed by Raman spectroscopy to determine composition.
- Site characteristics include estimated sewage effluent share and population-equivalent density upstream of wastewater treatment works, allowing examination of anthropogenic impact on microplastic abundance.

## Aim and Scope for Monitoring Frameworks

- Enables scrutiny of environmental health measures related to microplastics and their association with sewage inputs and population density.
- Supports decision-making on monitoring design, data collection, and reporting to inform policy and future assessments.
- Provides transparency on data sources, methods, and metadata to facilitate data reuse and governance.

## Data Collection and Monitoring Methodology

- Site selection criteria:
  - Based on average effluent presence (LF2000 model) and upstream population-equivalent density.
  - Four sites representing a gradient from low to high sewage input and anthropogenic pressure.
- Sampling design:
  - Four replicate sediment samples per site collected along a 3 m transect at 1 m spacing, from the riverbank surface to ~10 cm depth.
  - Sampling window aligned with seasonal low flow (Aug 28–Sept 3, 2014).
- Physical processing (three-step extraction):
  1) Visual inspection of sieved sediments (1–2 mm and 2–4 mm fractions) with specific plastic-identification criteria.
  2) Flotation using ZnCl2 solution (density ~1.7–1.8 g/cm3) to separate buoyant microplastics; subsequent filtration and drying.
  3) Final visual inspection of unfloated sediments to recover dense particles not captured by flotation.
- Contamination controls:
  - Controls processed with ZnCl2 solution to assess airborne/handling contamination.
  - Measures to minimize sample contamination during sorting and processing.

## Analytical Techniques

- Raman spectroscopy (20% subsampling):
  - Randomized particle selection across samples (grid-based coordinates).
  - Acquisition at 50x, 785 nm laser, 30 s per acquisition, spectral range 600–3200 cm−1.
  - Spectra matched against reference databases using BioRad KnowItAll Raman ID Expert, with corrections for baseline and intensity.
- Particle characterization (from Raman analysis):
  - Types: fragments, fibres, films (and occasionally glass as non-microplastic anthropogenic material).
  - Color categories recorded (e.g., red, blue, green, etc.).
  - Polymer identification including common polymers (PE, PP, PS, PVC, PET, Nylon, Polyester) and other or unidentifiable categories.
  - Pigments and other substances recorded where identified (e.g., Copper phthalocyanine, synthetic pigments).

## Data Format and Content

- ThamesMicroplastics_SamplingLocation.csv
  - Site_name, Grid_reference, Sewage_effluent_ (average percentage), Population_equivalent_density.
- ThamesMicroplastics_Number OfParticles.csv
  - Sample_ID, Replicate_number, Size_fraction (1–2 mm or 2–4 mm), Subsample_40_grams, Total_weight_grams, Fragment, Fibre, Film, Glass, Total_microplastics, Color columns, Polymer columns.
- ThamesMicroplastics_ParticleCharacteristics.csv
  - For 20% subsample analyzed by Raman: Sample_ID, Particle_ID, Color, Polymer (e.g., PE, PP, PS, PVC, PET, Nylon, Polyester, Other_polymer), Other_manmade, Natural_substance, Unidentifiable, and related categorical descriptors.
- Key notes:
  - Subsampling rule: 20% of total particles per sample (rounded to nearest 5 particles for practical counts).
  - Each row in ParticleCharacteristics.csv corresponds to a single particle identified by Raman.

## Data Quality, Metadata and Governance

- Metadata included to enable traceability: site name, exact grid reference, sampling replicate, size fraction, and replicate weights.
- Data processing chain documented (visual sorting, flotation, post-flotation inspection) to support reproducibility and evaluation of recovery efficiency.
- Public data sharing is integral to the approach, with underlying data and methods openly described to support transparency and governance.
- Quality assurance steps include contamination controls and cross-checks at multiple extraction steps, plus Raman validation for composition.

## Challenges and Considerations for Monitoring Frameworks

- Data gaps and completeness:
  - Large microplastics (1–4 mm) are targeted; smaller particles (<1 mm) are not accurately quantified, potentially underestimating total microplastic burden.
- Data access and interoperability:
  - Detailed metadata and consistent formatting are provided to facilitate integration with other datasets, though consolidation across programs may require standardization of variable definitions.
- Data governance:
  - Public sharing of datasets requires careful management of site-level and concentration data, including potential sensitivities around contamination controls and methodological specifics.
- Data transformation and interpretation:
  - Dense polymer mixtures and pigments require careful interpretation; linkage to sources and potential environmental pathways should be considered in policy contexts.

## References (Key Context)

- Horton et al., 2017; Claessens et al., 2013; Imhof et al., 2012; Nor & Obbard, 2014; Nuelle et al., 2014; Pottinger et al., 2013; Williams et al., 2009; Bowes et al., 2014; Kalpakjian & Schmid, 2008.