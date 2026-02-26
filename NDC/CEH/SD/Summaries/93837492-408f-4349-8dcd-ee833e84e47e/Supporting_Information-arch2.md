# Brief description of the dataset

- Scope and purpose
  - Dataset on microplastic particles extracted from sediments of Thames River tributaries (UK).
  - Measures number of particles by category: type (fragment, fibre, film), colour, and composition (via Raman spectroscopy for a subsample).
  - Samples collected August–September 2014 from four sites across three rivers: Leach, Lambourn, and The Cut (two sites on The Cut).
  - Site characteristics include estimated average sewage effluent presence and population-equivalent density to relate microplastic abundance to anthropogenic impact.
  - Research conducted by the Centre for Ecology and Hydrology (CEH), UK.

- Sampling design
  - Four sampling sites representing gradients from low to high sewage influence.
  - Four replicate sediment samples per site collected along a 3 m transect (1 m spacing; parallel to the bank).
  - Sediment collected to about 10 cm depth; stored in 1 L jars.
  - Sampling windows: 28 August – 3 September 2014 (seasonal low flow).
  - Size fractions targeted for analysis: 1–2 mm and 2–4 mm (visible, easily quantifiable).

- Processing and analysis workflow
  - Three-step extraction to recover microplastics:
    1) Visual inspection of sieved sediments (binocular microscope) with specific particle criteria.
    2) Flotation in dense ZnCl2 solution (1.7–1.8 kg/L) to separate buoyant plastics; repeated shaking/overflow to maximize recovery; particles collected on 1.2 µm filters and dried.
    3) Final visual inspection of unfloated sediment post-flotation to detect plastics not recovered previously.
  - Contamination controls: three field-process blank controls using ZnCl2 solution filtered to assess airborne contamination.
  - Particle categorisation: fragments, fibres, films (plus notes on glass fragments as non-microplastics).

- Analytical chemistry (characterisation)
  - Raman spectroscopy performed on 20% of particles to determine polymer composition.
  - Randomized subsampling: particles chosen via grid/random coordinates to avoid bias; spectra acquired with a 785 nm laser; analyzed with BioRad KnowItAll Raman ID Expert software against a reference database.

- Datasets and formats
  - ThamesMicroplastics_SamplingLocation.csv: site characteristics (name, grid reference, average sewage effluent, population density, etc.).
  - ThamesMicroplastics_Number OfParticles.csv: total number of microplastic particles per sample; linked to site and sample weight; includes sample replication.
  - ThamesMicroplastics_ParticleCharacteristics.csv: subsample particle data (20% of total); includes particle type (fragment, fibre, film), colour, and Raman-identified polymer; also includes other descriptors (e.g., natural substances, unidentifiable).
  - Key variables and columns (highlights):
    - Site_name, Grid_reference, Sewage_effluent_(average_percentage), Population_equivalent_density
    - Sample_ID, Replicate_number, Size_fraction (1–2 mm or 2–4 mm), Subsample_40_grams, Sorting_step, Total_weight_grams
    - Fragment, Fibre, Film, Glass
    - Total_microplastics, Color columns (Red, Yellow, Blue, Green, White, Beige, Grey, Purple, Black, Clear)
    - Polymer columns (PE, PP, PS, PVC, PET, Nylon, Polyester, Other_polymer)
    - Other_polymers and pigments (e.g., Copper_phthalocyanine/mortoperm_blue, Other_manmade)
    - Natural_substance, Unidentifiable

- Context and references
  - Methodology aligned with Horton et al. (2017) and related microplastics extraction/verification literature.
  - Supporting references include Claessens et al. (2013), Imhof et al. (2012), Nor & Obbard (2014), Nuelle et al. (2014), Pottinger et al. (2013), Williams et al. (2009), and Bowes et al. (2014).