# UnknownsSpringSummerMetabolomics.csv

## Overview
- Metabolomics dataset describing sheep urine from a Uplands-N2O project (grant NE/M015351/1).
- Study includes spring and summer collections from 2016, with 5 sheep per season (n=10 total).
- Data comprise peak intensity values for unidentified compounds from untargeted primary metabolism analysis.

## Data collection and processing
- Sample handling: urine collected from sheep on a semi-improved site, with syringe filtering (<0.2 μm) and flash freezing.
- Procedural blanks: ultra-pure water blanks processed identically and blank corrected.
- Storage and shipping: samples stored at -80 °C, shipped on dry ice to the West Coast Metabolomics Center at UC Davis.
- Analysis method: untargeted primary metabolism analysis using ALEX-CIS GC-TOF-MS (Gerstel Inc., Linthicum, MD).

## Data content and structure
- Data headers:
  - Sample: encodes season of collection and sheep ID.
  - Season: spring or summer 2016.
  - Other headers: numerical identity values for unidentified compounds; values correspond to peak intensities.
- The dataset contains peak intensity values for unidentified metabolic features.

## Provenance and usage notes
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick.
- Grant and citation: If data are reused, ensure full citation.
- Purpose: supports untargeted metabolomics interpretation; identification of compounds not yet annotated.

## Reuse considerations for data leadership
- Data governance and discoverability: dataset is CSV with explicit headers; clear linkage between sample metadata (season, sheep) and feature intensities.
- Data quality and limitations: small sample size (n=10) and unidentified features; blank correction applied; interpretation requires annotation of unidentified compounds.
- Metadata completeness: headers include season, sample identifiers, and compound feature columns; provenance and processing steps are described.
- Collaboration and interoperability: suitable for integration with other metabolomics datasets, but alignment requires consistent feature naming and potential reannotation.

## Key takeaways
- The dataset provides untargeted metabolomic profiles of sheep urine across two seasons, with rigorous blank correction and standardized GC-TOF-MS analysis.
- Useful for cross-season metabolomic comparisons of unidentified features, and as a basis for annotating unknown metabolites within a broader network or community of practice.