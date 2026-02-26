# Brief description of the dataset

- Microplastic particles extracted from sediments of Thames River tributaries (UK) with data on particle type, colour, and composition.
- Samples collected Aug–Sep 2014 from four sites across three rivers: Leach, Lambourn, and The Cut (two sites on The Cut).
- Sediments sorted into size fractions (1–2 mm and 2–4 mm), classified as fragments, fibres, or films; Raman spectroscopy used for composition on a 20% subsample.
- Site characteristics include estimated sewage effluent influence and upstream population density to explore anthropogenic impact on microplastic abundance.
- Study conducted by the Centre for Ecology and Hydrology, UK.

## Aim and scope

- Identify abundance and distribution of microplastics in river sediments.
- Relate microplastic counts to site-level indicators of human impact (effluent and population density).
- Characterize particle composition and polymer types to infer likely sources.
- Provide a dataset suitable for analysis of correlations, patterns, and potential predictive relationships.

## Sampling design

- Site selection based on two variables: average effluent presence (LF2000 model) and upstream population-equivalent density.
- Four sampling sites representing a gradient from low to high sewage input:
  - River Leach (low)
  - River Lambourn (low)
  - The Cut site 1 (intermediate, upstream of effluent)
  - The Cut site 2 (high sewage input, downstream of effluent)
- Sampling occurred during seasonal low-flow conditions (28 Aug–3 Sep 2014).
- At each site: four replicate sediment samples collected along a 3 m transect (1 m apart); surface ~10 cm depth; samples stored in 1 L jars.

## Laboratory processing and extraction

- Three-step extraction workflow to recover microplastics:
  - Step 1: Visual inspection of sieved sediments (fractions 24 mm and 1–2 mm) under a microscope to identify likely microplastics using a set of criteria (minimum two of: unusual color, coating, shape, fibre integrity, shine, flexibility).
  - Step 2: Flotation in dense ZnCl2 solution (1.7–1.8 kg/L) to separate buoyant plastics; filtration of floated material onto 1.2 µm filters; initial visual check.
  - Step 3: Visual inspection of unfloated sediment after flotation to catch dense particles not recovered in flotation; filtration and inspection.
- Contamination controls: three blank ZnCl2 controls processed to assess airborne/handling contamination.
- Size fractions retained for analysis: 1–2 mm and 2–4 mm.

## Particle analysis and Raman spectroscopy

- 20% of particles were selected for chemical characterization using Raman spectroscopy.
- Random sampling across samples to avoid bias (grid-based random coordinates).
- Spectra acquired with 785 nm laser, 30 s acquisition, two accumulations; range 600–3200 cm−1.
- Spectra compared against reference databases using BioRad KnowItAll Raman ID Expert; assignment to polymer types and pigments (e.g., PE, PP, PS, PVC, PET, Nylon, Polyester, Other polymer) or natural/unidentifiable materials.

## Data format and variables

Three CSV files comprise the dataset:
- ThamesMicroplastics_SamplingLocation.csv
  - Site_name, Description; Grid_reference; Sewage_effluent_(average_percentage); Population_equivalent_density
- ThamesMicroplastics_Number OfParticles.csv
  - Sample_ID; Replicate_number; Size_fraction (1–2 mm or 2–4 mm); Subsample_40_grams (whether subsample used); Total_microplastics; Total_weight_(grams)
  - Particle counts by category (Fragment, Fibre, Film; plus Glass)
- ThamesMicroplastics_ParticleCharacteristics.csv
  - For each analyzed particle (20% subsample): Sample_ID; Particle_ID; Fragment/Fibre/Film; Colour (colors: Red, Yellow, Blue, Green, White, Beige, Grey, Purple, Black, Clear); Polymer_Type (PE, PP, PS, PVC, PET, Nylon, Polyester, Other Polymer); Other_Pigments/Indicators; Natural_substance; Unidentifiable
- Additional columns describe:
  - Site_name, Description; Grid_reference
  - Replicate_number; Size_fraction; Subsample_40_grams
  - Sorting_step; Total_weight_(grams)

## Key methodological notes

- Size fractions chosen to reflect visible, analyzable particles and potential source implications.
- Visual criteria combined with supplementary features to distinguish microplastics from non-plastics.
- Raman spectroscopy provides composition data for a subsample to infer polymer types and potential sources.

## Quality control and limitations

- Contamination controls implemented via blank ZnCl2 filtrations.
- Raman subsampling is 20%, which provides broad composition insight but not complete polymer coverage.
- Temporal snapshot (one seasonal window in 2014) and limited number of sites (four total) constrain generalizability.
- Size detection limited to particles ≥1 mm due to methodological constraints.
- Some particles remain unidentifiable by Raman or may be misclassified despite verification steps.

## How this dataset supports analysis (Analysts perspective)

- Enables correlation analyses between microplastic abundance and anthropogenic pressure indicators (sewage effluent, population density).
- Allows examination of how particle type (fragment, fibre, film), size fraction, and color distributions vary with site characteristics.
- Facilitates investigation of polymer composition patterns and potential source attribution via Raman-identified polymers.
- Provides a structured, traceable data pipeline (site metadata, particle counts, and composition) suitable for model development and predictive analyses.

## References

- Bowes et al., 2014; Claessens et al., 2013; Horton et al., 2017; Imhof et al., 2012; Kalpakjian & Schmid, 2008; Nor & Obbard, 2014; Nuelle et al., 2014; Pottinger et al., 2013; Williams et al., 2009.