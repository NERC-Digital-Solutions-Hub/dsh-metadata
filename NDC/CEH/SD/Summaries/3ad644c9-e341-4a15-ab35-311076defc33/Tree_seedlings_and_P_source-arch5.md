# Study sites and focal species

## Overview
- Purpose: assess generality of findings across forest biomes by comparing shade-house responses of ECM- vs AM-associated species to different soil phosphorus (P) forms.
- Locations: Kabili-Sepilok Forest Reserve, Malaysia; Heishiding Nature Reserve, China.
- Experimental approach: shade-house experiments using germinated seedlings from eight focal tree species per site, exposed to five P treatments and two mycorrhizal types; measurement of growth, nutrient status, and mycorrhizal colonization.

## Study locations and environmental context
- Kabili-Sepilok, Malaysia
  - Remnant lowland tropical rainforest in Sabah; mean annual rainfall ~2975 mm; temperatures ~26.7–27.7 °C.
  - Overstorey ECM-dominated with limited phylogenetic diversity; understorey AM-dominated.
- Heishiding, China
  - Subtropical evergreen broad-leaved forest in Guangdong; mean annual temperature ~19.6 °C; ~1744 mm rainfall.
  - Similar ECM-dominated overstorey with diverse AM understorey.
- Both sites selected to compare ECM vs AM responses in different forest biomes.

## Experimental design
- Shade-house experiments conducted in two phases: Sepilok (Nov 2015–May 2016) and Heishiding (Sept 2015–Apr 2016).
- Seed material: fruits/seeds collected 2014–2015; surface-sterilised and germinated; seedlings transplanted after 3 months.
- Plant material: eight focal species per site; one seedling per pot; 12 blocks per site; 40 pots per block; total of 480 pots per site.
- Mycorrhizal status: ECM vs AM; root samples collected for colonization assessment.
- Exclusions: Canarium album at Heishiding removed due to low survival.

## Treatments
- Five phosphorus (P) treatments
  - Water (control)
  - Na3PO4 (inorganic P)
  - AMP (simple organic P)
  - Phytic acid (complex organic P)
  - Mixture (1/3 Na3PO4 + 1/3 AMP + 1/3 phytic acid)
- P addition: site-specific dosing based on background soil P
  - Heishiding: 0.24 mg P per g soil
  - Sepilok: 0.27 mg P per g soil
- Application: 10 mL solution per pot, monthly for 6 months
- Replication: 12 blocks per site; each block contains all treatments for all species (40 pots per block)

## Measurements and laboratory analyses
- Growth metrics: seedling height (cm) and total biomass (g) after 6 months; root biomass also recorded.
- Biomass normalization: TotalBiomassStandard = TotalBiomass divided by the maximum TotalBiomass observed for the species across all treatments.
- Nutrient analyses: total leaf N, P, K concentrations (Kjeldahl for N; ICP-OES after acid digestion for P and K); soil available P via Olsen method.
- Mycorrhizal colonization
  - AM: root segments stained; colonization assessed by gridline intersection method (200 intersections per seedling); colonization expressed as proportion of intersections with mycorrhizas.
  - ECM: live fine roots assessed under microscope; 30–50 root tips per seedling; colonization expressed as percentage of tips colonized.
- Sample handling: soil samples (50 g per pot) air-dried and sieved; roots cleaned and stored at 4 °C until analysis.

## Data structure and description of data fields
- Site (Column A): Sepilok, Malaysia or Heishiding, China.
- Block (Column B): 24 levels (1–12 Sepilok; 13–24 Heishiding) representing replicates of each treatment × species combination.
- Ptreatment (Column C): 5 levels; numeric codes 1–5 corresponding to the five P treatments (see D).
- P (Column D): Alphanumeric, combining Ptreatment with a descriptor: Water, Na3PO4, AMP, Phytic acid, Mixture.
- Species (Column E): Codes A–H for focal species.
- SpName (Column F): Binomial species name.
- MycorrhizalType (Column G): ECM or AM.
- Height (Column H): Seedling height in cm at end of experiment.
- TotalBiomass (Column I): Seedling total dry mass in g at end.
- TotalBiomassStandard (Column J): Biomass scaled to species maximum.
- RootBiomass (Column K): Seedling root dry mass in g at end.
- RootColonization (Column L): Proportion of AM root length or ECM root tips colonized; NA if not sampled.

## Data governance and stewardship considerations
- Data coding and consistency
  - Use of clear site, block, species, and treatment codes; ensure consistent mapping to descriptors (P forms) and species names.
- Metadata and provenance
  - Document collection dates, seed sources, soil collection sites, and environmental conditions per site; include climate context as part of metadata.
- Units and normalization
  - Maintain consistent units (cm for height, g for biomass); TotalBiomassStandard provides cross-species comparability.
- Quality control
  - Track instances of non-survival (e.g., Canarium album at Heishiding) and any treatment- or species-specific exclusions.
  - Standardize mycorrhizal assessment methods (gridline intersections for AM; root-tip counts for ECM) to reduce observer bias.
- Data storage and sharing
  - Store a complete data dictionary and codebook mapping codes A–H, 1–24, 1–5 to full descriptors.
  - Include methods for lab analyses (Kjeldahl, ICP-OES, Olsen P) to enable reproducibility.
  - Consider depositing the dataset with versioned release and clear licensing; provide data updates as experiments progress or are reanalyzed.