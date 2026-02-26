# UplandLowlandMetabolomics.csv

## Overview
- Dataset describing metabolomic profiles of sheep urine from autumn collections at two pasture site types: semi-improved and improved.
- Study design includes 8 samples in total (4 from semi-improved, 4 from improved pasture).
- Data derived from untargeted primary metabolism analysis using GC-TOF-MS.

## Experimental design and samples
- Samples: urine from sheep collected in autumn.
- Sites: semi-improved pasture and improved pasture.
- Replicates: 4 samples per site type (n = 4 per site).
- Sample handling: syringe filtration (< 0.2 μm), flash freezing; procedural blanks of ultra-pure water filtered and blank-corrected.
- Storage and transport: frozen at -80 °C, shipped on dry ice to the West Coast Metabolomics Center, UC Davis.

## Data collection and processing
- Analytical platform: ALEX-CIS GC-TOF-MS (Gerstel Inc., Linthicum, MD) for untargeted primary metabolism analysis.
- Data processing: peak intensity values recorded for all identified compounds; blanks corrected prior to data export.

## Data structure and variables
- Sample: combines sheep ID and site of urine collection.
- Site: categorical variable indicating semi-improved or improved pasture.
- Compounds: subsequent columns represent identified metabolites with their corresponding peak intensity values.

## Potential analyses and use cases
- Compare metabolite profiles between semi-improved and improved pasture sites.
- Identify metabolites with significant intensity differences between site types.
- Apply multivariate analyses (e.g., PCA, PLS-DA) to explore group separation and potential biomarkers.
- Integrate with other datasets to link metabolite changes to environmental or management variables.

## Provenance and usage notes
- Project: Uplands-N2O; Grant NE/M015351/1.
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick.
- Data reuse: If data are reused, ensure full citation.

## Limitations and considerations
- Small sample size (4 per site) may limit statistical power.
- Metadata details beyond Sample and Site are limited; no explicit normalization or scaling steps described.
- Untargeted nature means not all detected peaks may be identified or consistently annotated across samples.
- Blanks were corrected, but additional quality control or batch effects are not detailed.