# Brief description of the dataset

- The dataset documents microplastic particles extracted from sediments of Thames basin tributaries in the UK. It records particle counts by category (type, colour, composition), with size classifications of 1-2 mm and 2-4 mm. A subset of particles was chemically characterized by Raman spectroscopy to determine composition. The study was conducted by the Centre for Ecology and Hydrology, UK.

## Purpose and scope

- To relate microplastic abundance to anthropogenic impact by linking particle counts to site characteristics (population density and sewage input).
- To provide data on particle type (fragment, fibre, film), colour, and polymer identity (via Raman) for sediments from river tributaries.

## Sampling design and sites

- Sites: four sediment sampling sites across three Thames tributaries — River Leach, River Lambourn, and The Cut (two sites on The Cut).
- Site selection criteria: represent gradients of sewage input and population equivalent density upstream of wastewater treatment works; sites chosen to cover low to high sewage influence.
- Sampling window: 28 August – 3 September 2014 (seasonal low-flow conditions).
- Replicates: at each site, four replicate sediment samples collected along a 3 m transect at 1 m intervals, with sampling depth ~10 cm and approximately 1 L per jar.
- Site-characteristic data collected: average effluent percentage (LF2000 model) and population equivalent density upstream of the treatment works.

## Sample processing and extraction methods

- Size separation: wet-sieved to obtain two fractions, 1-2 mm and 2-4 mm; samples oven-dried at 80°C and weighed.
- Extraction steps (three-step process):
  - Step 1: Visual inspection of entire sample with binocular microscope to identify microplastics using criteria (at least two of six features: unusual color, coating, irregular/unusual shape, intact fibrous form, shiny/glassy, flexible).
  - Step 2: Flotation using concentrated ZnCl2 (density 1.7–1.8 g/cm3); repeated shake and overflow to recover buoyant particles; floated particles filtered and dried for analysis.
  - Step 3: Final visual inspection of unfloated sediment post-flotation to ensure recovery of dense materials; filtered and inspected for microplastics.
- Contamination controls: three blank ZnCl2 controls processed to assess laboratory contamination.
- Particle sorting: identified and categorized as fragments, fibres, films (and noted glass fragments as non-microplastic).

## Analytical characterization

- Raman spectroscopy: 20% of particles per sample analyzed to determine chemical composition.
- Randomized selection: grid-based random coordinates used to select particles for Raman analysis.
- Instrument and settings: Raman spectroscopy (785 nm laser, 50x objective, 30 s acquisition, two accumulations, 600–3200 cm-1 range) with KnowItAll software for spectral matching.
- Data from Raman: polymer identities (e.g., PE, PP, PS, PVC, PET, Nylon, Polyester, Other polymer), pigments (e.g., copper phthalocyanine, other synthetic pigments), other materials, natural substances, and unidentifiable particles.

## Dataset structure and files

- ThamesMicroplastics_SamplingLocation.csv: site characteristics (name, grid reference, average sewage effluent percentage, population-equivalent density).
- ThamesMicroplastics_Number OfParticles.csv: total number of particles extracted per sample, linked to site characteristics and total dry weight; one row per sediment sample (Sample_ID).
- ThamesMicroplastics_ParticleCharacteristics.csv: characterisation of the 20% subsample analyzed by Raman spectroscopy, including particle type, colour, and polymer identity; one row per analyzed particle.
- Key fields include:
  - Site_name, Grid_reference, Sewage_effluent_(average_percentage), Population_equivalent_density
  - Sample_ID, Replicate_number, Size_fraction, Subsample_40_grams
  - Particles counts (Total_microplastics) and class breakdown (Fragment, Fibre, Film)
  - Polymer identity and colour data from Raman results
  - Additional fields describe the sorting step, total sample weight, and other metadata

## Data quality, governance, and usage notes

- Methodological basis: sampling and processing align with Horton et al. (2017) and related references; multi-step approach intended to maximize microplastic recovery without specialized equipment.
- Quality controls: contamination checks via blank ZnCl2 controls; randomization in Raman particle selection to prevent sampling bias.
- Coverage and limitations:
  - Observed particle sizes limited to 1-4 mm due to sieving and methodological constraints; no observations of plastic pellets reported.
  - Raman analysis covers a subset (20%) of particles, which informs composition but is not exhaustive for all particles.
  - Data describe relationships with sewage input and population density at sampling sites, enabling cross-site comparisons and system-level analyses.
- Potential uses for data leaders:
  - Integrate into broader data systems to assess data provenance, lineage, and quality controls.
  - Use site characteristics and particle data to model relationships between microplastic abundance/types and anthropogenic pressure.
  - Leverage structured CSV files for discoverability, metadata richness, and cross-network sharing.

## References

- Bowes, M.J. et al. (2014). Identifying priorities for nutrient mitigation using river concentration-flow relationships: The Thames basin, UK.
- Claessens, M. et al. (2013). New techniques for the detection of microplastics in sediments and field-collected organisms.
- Horton, A.A. et al. (2017). Large microplastic particles in sediments of tributaries of the River Thames, UK — Abundance, sources and methods for effective quantification.
- Imhof, H.K. et al. (2012). A novel, highly efficient method for the separation and quantification of plastic particles in sediments.
- Nor, N.H. & Obbard, J.P. (2014). Microplastics in Singapore's coastal mangrove ecosystems.
- Nuelle, M.T. et al. (2014). A new analytical approach for monitoring microplastics in marine sediments.
- Pottinger, T.G. et al. (2013). The stress response of sticklebacks downstream of wastewater treatment works.
- Williams, R. et al. (2009). National risk assessment for intersex in fish arising from steroid estrogens.