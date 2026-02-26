# Danum Valley Seedling Traits

- A comparative study of seedling traits in unlogged primary forest (Danum Valley Conservation Area, DVCA) and adjacent selectively logged forest (Ulu Segama Forest Reserve, USFR) in Sabah, Malaysia.
- Sampling occurred during a mast fruiting event and followed by trait measurements in Jan–Feb 2020.

## Study Context and Sites

- DVCA: 438 km2 of lowland dipterocarp forest and lower montane rainforest; high annual rainfall (~2305 mm) and mean temperature ~25.8°C.
- USFR: Adjacent logged region (1981–1993), with annual coupe-scale logging and a later Reduced Impact Logging trial in 1993.
- Forest management regimes:
  - Primary forest (DVCA) as reference.
  - Logged forest (USFR) with two regeneration regimes: Natural Regeneration and Active Restoration (tree planting and liana cutting).

## Sampling and Plots

- Seedling plots:
  - Primary forest: 87 plots within the Danum Valley 50 ha forest dynamics plot.
  - Logged forest: 96 plots (52 actively restored; 44 naturally regenerating) within INDFORSUS project plots.
- Seedlings sampled:
  - 399 individuals from 15 species (195 in primary; 204 in logged forests).
  - Most seedlings germinated during the mast event ~6 months before sampling.
- Plot inclusion and replication:
  - Samples drawn from 75 plots (46 primary; 26 logged).
  - In logged forests: 19 plots within actively restored areas; 7 in natural regeneration.
  - Some plots unusable due to high mortality or access issues.

## Trait Sampling and Measurement

- Traits measured per seedling: 14 traits including organ biomass, leaf and root metrics, and foliar nutrient content.
  - Biomass (total; dry mass after 50°C drying)
  - Root Length to Shoot Length (RL:SL)
  - Leaf Mass Fraction (LMF)
  - Root Mass Fraction (RMF)
  - Leaf Mass per Area (LMA)
  - Leaf Thickness
  - Leaf Force to Punch (LFP)
  - Leaf Area: Shoot Area (LA:SA)
  - Leaf Nitrogen (N leaf), Phosphorus (P leaf), Calcium (Ca leaf), Potassium (K leaf), Magnesium (Mg leaf)
  - Leaf Nitrogen to Phosphorus ratio (N:P)
  - Specific Maximum Root Length (SMRL)
- Sample collection and handling:
  - Seedlings collected outside seedling plots to enable continued monitoring.
  - Additional 10 seedlings per plot combined with three measured for foliar analyses.
  - When nearby seedlings were unavailable due to mortality, samples were taken ~20–40 m away for replication.
- Measurement methods:
  - LMF and RMF: dry mass proportions
  - LMA: dry leaf mass / leaf area (leaf area via scanning and ImageJ)
  - Leaf thickness: averaged over three leaves (via digital calipers)
  - LFP: measured with a digital force gauge
  - LA:SA: leaf area / shoot cross-sectional area (shoot area from shoot diameter)
  - Biomass: dried to constant weight at 50°C
  - Nutrients: foliar N, P via colorimetry; Ca, K, Mg via spectrometry after digestion
  - N:P: calculated from N and P concentrations

## Data Structure and Contents

- Data file: Danum_Valley_Seedling_Traits.csv
- Core fields and descriptions:
  - Date: sampling date; Forest: primary or logged; Management: Natural Regeneration or Active Restoration
  - Species, Family: taxonomic details
  - Seedling.Plot, Individual: plot and seedling identifiers
  - Biomass: total seedling biomass (g)
  - RL:SL: root length to shoot length ratio
  - LMF, RMF: leaf and root mass fractions
  - LMA: leaf mass per area
  - Leaf.Thickness: leaf thickness (mm)
  - LFP: leaf force to punch (N)
  - LA:SA: leaf area to shoot area ratio
  - Leaf.N, Leaf.P, Leaf.Ca, Leaf.K, Leaf.Mg: foliar concentrations (mg g-1)
  - Leaf.N:P: leaf N to P ratio
  - SMRL: Specific Maximum Root Length (mm g^-1)
- Data collection and processing notes:
  - Leaves sampled, dried, ground, and analyzed at Forest Research Centre, Sepilok
  - N and P determined colorimetrically; Ca, K, Mg by spectrometry
  - Leaves scanned for area; moisture content corrections applied

## Data Quality, Gaps, and Limitations

- Mortality and access issues limited sampling in some logged-forest plots; not all plots contributed seedlings.
- Sampling aimed to cover species representing >80% of seedlings on plots; some species sampled only in primary or only in logged forests.
- Datasets include a mix of actively restored and naturally regenerating plots within the logged forest, enabling comparisons of regeneration strategies.

## Relevance for Data Support Practice

- Illustrates end-to-end data workflow: site selection, plot-level sampling, cross-forest trait measurement, and structured data documentation.
- Provides a clear data dictionary and field definitions to facilitate data integration, quality assurance, and reuse.
- Demonstrates handling of mixed-management contexts and replication strategies to support robust comparative analyses.