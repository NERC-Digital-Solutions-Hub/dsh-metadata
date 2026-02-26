SpringSummerMetabolomics.csv

## Overview
- Metabolomics dataset of sheep urine collected in spring and summer 2016 (n = 5 per season; total 10 samples) from a semi-improved site.
- Samples processed by syringe filtering (<0.2 μm), flash freezing, stored at -80°C, then shipped on dry ice to UC Davis for untargeted primary metabolism analysis.
- Analysis performed using ALEX-CIS GC-TOF-MS (Gerstel Inc.).
- Data represent peak intensity values for all identified compounds from the untargeted analysis.

## Data content and structure
- Data file contains peak intensity values for identified metabolites.
- Headers:
  - Sample: encodes season and sheep ID.
  - Season: spring or summer 2016.
  - Remaining headers: identified compounds with corresponding peak intensities as values.
- Procedural blanks of ultra-pure water were processed identically and used for blank correction.

## Data provenance and processing
- Data described in project: Uplands-N2O; Grant NE/M015351/1.
- Data cleaning steps include blank correction and standardisation to enable comparison across samples.
- Data collected and analyzed by a multi-author team (listed in the document).

## Reuse and citation
- If data are reused, ensure full citation of the original source.
- Authors: Karina A. Marsden et al.; includes multiple contributors.
- Aimed for broad data interoperability through explicit description of collection, processing, and analytical methods.

## Practical notes for use
- Suitable for comparing metabolite profiles between spring and summer in sheep urine.
- As untargeted data, expect a large number of features; downstream analyses may require feature filtering and normalization.
- Small sample size (n=5 per season) may limit statistical power; consider as exploratory data.