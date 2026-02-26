# SpringSummerMetabolomics.csv

## Overview
- Metabolomics dataset of sheep urine from spring and summer 2016 on a semi-improved site.
- Sample sizes: 5 sheep per season (n = 5 for spring, n = 5 for summer).
- Analysis: untargeted primary metabolism using GC-TOF-MS (ALEX-CIS) at the West Coast Metabolomics Center, UC Davis.
- Data processing: procedural blanks (ultra-pure water) were syringe filtered and blank-corrected; frozen samples stored at -80°C before shipping on dry ice.

## Data collection and processing
- Project: Uplands-N2O, Grant NE/M015351/1.
- Authors: Marsden, Lush, Holmberg, Whelan, King, Charteris, Cardenas, Jones, Chadwick, Wilson.
- Sample handling: urine samples collected in spring and summer 2016, syringe filtered (<0.2 μm), flash-frozen, and stored at -80°C prior to analysis.
- Instrumentation: ALEX-CIS GC-TOF-MS (Gerstel Inc.).
- Data type: peak intensity values for all identified compounds from the untargeted primary metabolism analysis.

## Data structure
- Header "Sample": encodes season and sheep ID.
- Header "Season": indicates the collection season (spring or summer 2016).
- Other headers: identified compounds from the primary metabolism analysis; values are the corresponding peak intensities under each header.

## Reuse and provenance
- Data description includes a citation reminder: if reused, ensure full citation.
- Grant number: NE/M015351/1.
- Authors listed for proper attribution.

## Potential uses and considerations
- Compare metabolite profiles between spring and summer to identify seasonal metabolomic differences.
- Identify season-specific metabolites and risk of confounding by site or year due to small sample size.
- Utilize as part of untargeted metabolomics workflows and integrate with other datasets (e.g., environmental or physiological data) to support broader analyses.

## Limitations
- Small sample size (n=5 per season) and single site/year limit generalizability.
- Data presents peak intensities rather than absolute concentrations.
- Identified status of all compounds is not specified; potential ambiguities in compound identification.
- Data are from one metabolomics platform and one laboratory, which may introduce batch effects or instrument-specific biases.