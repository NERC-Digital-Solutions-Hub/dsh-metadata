# Danum_Valley_Seedling_Traits.csv

## Study site
- Located in the unlogged primary forest of Danum Valley Conservation Area (DVCA) and the adjacent selectively logged Ulu Segama Forest Reserve (USFR) in Sabah, Malaysia (approx. 4°58' N, 117°52' E).
- DVCA: 438 km2 of lowland dipterocarp forest and lower montane rainforest; mean annual rainfall ~2305 mm; mean daily temperature ~25.8°C.
- USFR region sampled was logged 1981–1993; annual logging coupes ~27 km2 with >60 cm DBH trees harvested; high variation in logging intensity; Reduced Impact Logging trial established in 1993; silvicultural interventions in some coupes to restore forest carbon stocks in part of the study area.

## Seedling plots
- Seedling plots of 1 m2 established within both forest types in Sep–Oct 2019 during a mast fruiting event.
- Primary (DVCA) forest: 87 seedling plots; Logged (USFR): 96 seedling plots (52 actively restored; 44 naturally regenerating).
- In 2020 Jan–Feb, seedling sampling occurred across plots; 75 plots were sampled (46 primary; 26 logged).
- For logged plots: some plots had high mortality or access difficulties; seedlings were collected from just outside the permanent seedling plots to support ongoing monitoring.
- Sampling included three seedlings per plot (maximum available if fewer than three) from areas outside plots; an additional ten seedlings per plot were collected and combined with the three for foliar nutrient analyses.
- In cases of poor availability near plots (high mortality or access issues), seedlings were sampled at ~20–40 m from the seedling plot to improve replication and trait estimates.
- Seedling plots cover both active restoration and natural regeneration contexts within the logged forest.

## Trait sampling and measurement
- Total of 399 seedlings measured, across 15 species: 195 from primary forest; 204 from logged forest.
- Seedling age is unknown; most germinated during mast fruiting approximately six months before sampling.
- Species representation: seven species sampled in both forest types (except Dryobalanops lanceolata, sampled only in logged forest due to lack of individuals in primary forest); several species unique to primary or logged forest.
- Traits measured (14 traits per seedling):
  - Biomass (total, g)
  - RL:SL (root length to shoot length ratio)
  - LMF (Leaf Mass Fraction)
  - RMF (Root Mass Fraction)
  - LMA (Leaf Mass per Area)
  - Leaf.Thickness (mm)
  - LFP (Leaf Force to Punch, N)
  - LA:SA (Leaf Area : Shoot Area)
  - Leaf.N (nitrogen, mg/g)
  - Leaf.P (phosphorus, mg/g)
  - Leaf.Ca (calcium, mg/g)
  - Leaf.K (potassium, mg/g)
  - Leaf.Mg (magnesium, mg/g)
  - Leaf.N:P (nitrogen to phosphorus ratio, unitless)
  - SMRL (Specific Maximum Root Length, mm per g)
- Sampling and processing steps:
  - Seedlings collected in morning; separated into above- and below-ground organs; kept moist during transport.
  - Longest root and shoot lengths measured; shoot diameter measured near the first branch; shoot cross-sectional area derived assuming circular shoots.
  - Leaf area estimated by scanning all leaves and analyzing with ImageJ (LeafArea).
  - Leaf thickness measured on up to three leaves; mean calculated.
  - LFP measured at three points per leaf using a digital force gauge; mean calculated.
  - Biomass components dried at 50°C to constant weight; leaves, shoots, and roots weighed to compute LMF and RMF; LMA calculated as dry leaf mass divided by leaf area.
  - LA:SA calculated from leaf area and shoot cross-sectional area.
  - Foliar nutrient analyses conducted at Forest Research Centre, Sepilok: leaves ground and digested; N and P via colorimetric analysis; Ca, K, Mg via spectrometry; moisture content determined for oven-dry corrections.
  - N:P calculated as leaf N divided by leaf P.

## Data structure and description of data fields
- File: Danum_Valley_Seedling_Traits.csv
- Key fields and descriptions:
  - Date: Date of seedling sampling.
  - Forest: Forest type – primary (unlogged) or logged.
  - Management: Regime – Natural Regeneration or Active Restoration.
  - Species: Scientific species name.
  - Family: Plant family.
  - Seedling.Plot: Identifier for the 1 m2 seedling plot.
  - Individual: Identifier for the seedling individual (up to three per plot).
  - Biomass: Total seedling biomass (g).
  - RL:SL: Root length to shoot length ratio (mm/mm).
  - LMF: Leaf Mass Fraction (g g^-1).
  - RMF: Root Mass Fraction (g g^-1).
  - LMA: Leaf Mass per Area (g m^-2).
  - Leaf.Thickness: Leaf thickness (mm).
  - LFP: Leaf Force to Punch (N).
  - LA:SA: Leaf area to shoot area (cm^2 mm^-2).
  - Leaf.N: Leaf nitrogen concentration (mg g^-1).
  - Leaf.P: Leaf phosphorus concentration (mg g^-1).
  - Leaf.Ca: Leaf calcium concentration (mg g^-1).
  - Leaf.K: Leaf potassium concentration (mg g^-1).
  - Leaf.Mg: Leaf magnesium concentration (mg g^-1).
  - Leaf.N:P: Leaf nitrogen to phosphorus ratio (g g^-1).
  - SMRL: Specific Maximum Root Length (mm g^-1).
- Units are provided where applicable; some fields are described via method notes (e.g., how LMA or LA:SA were computed).

## Notes on data use and GIS relevance
- The dataset provides plot- and individual-level trait data linked to forest type and management regime within a defined geographic region (DVCA and USFR, Sabah, Malaysia).
- Suitable for spatial analyses that compare trait variation across primary vs. logged/restored forests, and for integrating with other spatial layers (topography, canopy, soil, disturbance history) to examine drivers of trait variation.
- Data are rooted in physical plots (1 m2) and include concrete sampling dates, enabling temporal alignment with other datasets or repeat surveys.
- Some species and plots may be underrepresented due to mortality or access constraints; sampling outside plots introduces additional replication but should be accounted for in spatial analyses.