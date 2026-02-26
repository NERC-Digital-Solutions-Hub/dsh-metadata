# Brief description of the dataset

## Overview
- Dataset on microplastic particles extracted from sediments of Thames River tributaries (UK), collected Aug–Sep 2014.
- Four sampling sites across three rivers (Leach, Lambourn, The Cut; two sites on The Cut) chosen to span a gradient in sewage input and population density.
- Data are provided as counts of particles by category: type (fragment, fibre, film), colour, and composition (via Raman spectroscopy for a subsample).
- Size fractions analyzed: 1–2 mm and 2–4 mm.
- A subsample (20% of particles) was chemically characterized to determine polymer composition; site characteristics are included.

## Sampling design and site information
- Site selection based on average effluent percentage (LF2000 model) and upstream population-equivalent density.
- Four replicate sediment samples per site, collected along a 3 m transect at 1 m intervals; samples taken from the sediment surface to ~10 cm depth.
- Sampling window: 28 Aug–3 Sep 2014, under seasonal low-flow conditions.
- Sites include:
  - Leach (low sewage input, low density)
  - Lambourn (low-medium)
  - The Cut Site 1 (upstream of effluent outfall)
  - The Cut Site 2 (downstream of effluent outfall; high sewage input)

## Processing and extraction methodology
- Three-step extraction to maximize microplastic recovery without specialized equipment:
  1) Visual inspection of sieved sediments (size fractions 1–2 mm and 2–4 mm) using binocular microscope.
  2) Density separation using ZnCl2 solution (1.7–1.8 g/mL) to float plastics; repeated agitation and overflow collection; material retained on 1.2 μm filters.
  3) Final visual inspection of unfloated sediments post-flotation, with filtration to remove ZnCl2 residues.
- Pre-sieving to two size fractions (1–2 mm and 2–4 mm) prior to analysis; drying at 60–80°C to standardize weight and reduce contamination risk.
- Contamination controls: three blank ZnCl2 process controls analyzed for airborne/handling contamination.

## Particle identification and characterization
- Visual sorting criteria: microplastics identified if particles meet at least two of six features (e.g., unusual color, shiny/glassy, unnatural shape, etc.) to reduce misidentification of non-plastics.
- Particles categorized as:
  - Fragment
  - Fibre
  - Film
  - Glass (not a microplastic, but noted as anthropogenic waste)
- Post-processing analysis:
  - Raman spectroscopy performed on 20% of particles (randomly selected across samples) to determine polymer composition.
  - Raman setup: 785 nm laser, 50x magnification, 30 s acquisition, two accumulations, 600 l/mm grating, spectral range 600–3200 cm−1.
  - Software: BioRad KnowItAll Raman ID Expert; spectra compared to reference spectra to assign polymer type.
- Polymer types (as potential outputs): PE, PP, PS, PVC, PET, Nylon, Polyester, Other polymer; pigments and other manmade substances identified; natural substances or unidentifiable particles recorded.

## Data formats and dataset structure
- Three CSV files:
  - ThamesMicroplastics_SamplingLocation.csv: site-level characteristics (name, grid reference, average sewage effluent, population density).
  - ThamesMicroplastics_Number OfParticles.csv: total particle counts per sample, linked to site and replicate; includes sample weights and replicate info.
  - ThamesMicroplastics_ParticleCharacteristics.csv: details for 20% subsample analyzed by Raman; includes particle type, colour, and polymer identification.
- Key columns (examples):
  - Site_name, Grid_reference
  - Sewage_effluent_(average_percentage), Population_equivalent_density
  - Sample_ID, Replicate_number
  - Size_fraction (1–2 mm or 2–4 mm)
  - Subsample_40_grams (indicator whether particle came from subsample)
  - Sorting_step (the extraction step at which particles were recovered)
  - Total_weight_(grams)
  - Fragment, Fibre, Film, Glass (particle type classifications)
  - Total_microplastics
  - Colour columns (Red, Yellow, Blue, etc.)
  - Polymer columns (PE, PP, PS, PVC, PET, Nylon, Polyester, Other_polymer)
  - Other_manmade, Natural_substance, Unidentifiable

## Considerations for use and interpretation
- Composition data are based on a 20% subsample analyzed by Raman; apply appropriate scaling/uncertainty when inferring overall polymer distribution.
- Size restriction precludes analysis of microplastics smaller than 1 mm; results reflect 1–4 mm fractions only.
- Methodological steps (visual criteria, flotation efficiency) may influence recovery rates; a final step guards against missing dense or non-floating particles.
- Contamination controls are provided, but users should consider potential low-level laboratory/ambient contamination when interpreting very small counts.

## References
- Bowes et al. 2014; Claessens et al. 2013; Horton et al. 2017; Imhof et al. 2012; Kalpakjian & Schmid 2008; Nor & Obbard 2014; Nuelle et al. 2014; Pottinger et al. 2013; Williams et al. 2009.