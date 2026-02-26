# UnknownsSpringSummerMetabolomics.csv

## Overview
- Project: Uplands-N2O (Grant NE/M015351/1)
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Focus: Metabolomics of sheep urine
- Design: Seasonal comparison (spring vs summer 2016) on a semi-improved site
- Sample size: 5 sheep per season (n = 10 total)
- Data type: Peak intensity values for unidentified compounds from untargeted primary metabolism analysis

## Data and Methods
- Sample collection and handling:
  - Urine collected from sheep in spring and summer 2016
  - Syringe filtered (< 0.2 μm) and flash frozen; procedural blanks of ultra-pure water processed identically
  - Frozen samples stored at -80 °C and shipped on dry ice
- Analytical workflow:
  - Analysis performed at West Coast Metabolomics Center, UC Davis
  - Instrument: ALEX-CIS GC-TOF-MS (Gerstel Inc.)
  - Nature of data: Untargeted primary metabolism data; focus on unidentified compounds
- Data structure:
  - Data headers include:
    - Sample: indicates season and sheep ID
    - Season: spring or summer 2016
  - Remaining headers: numeric identifiers for unidentified compounds with corresponding peak intensities

## Potential Uses for Monitoring Frameworks
- Provides a concrete example of collecting and processing biological metabolomics data across seasons for environmental health monitoring
- Demonstrates capture of raw, unidentified metabolomic features that could serve as biomarkers after identification
- Highlights the importance of linkages between sample metadata (season, individual ID) and analytical outputs for interpretation and trend analysis

## Data Quality and Governance Considerations
- Processing steps explicitly stated: blank correction applied to data
- Data management points:
  - Data should be reused with full citation
  - Underlying data access and sharing policies are not detailed; sharing the dataset may hinge on metadata completeness and provenance
- Metadata and interpretability gaps:
  - Limited metadata beyond season and sheep ID; missing site-specific conditions, diet, weather, sampling times, and handling details
  - Unidentified metabolites reduce immediate biological interpretability and policy relevance

## Limitations and Gaps for Policy-Relevant Monitoring
- Small, single-site study with five samples per season; limited statistical power and generalizability
- Unidentified compounds require subsequent identification for meaningful environmental health interpretation
- Sparse metadata complicates cross-study comparisons and reproducibility
- No explicit data governance or open-data framework described beyond citation requirement

## Implications for Practice
- When building monitoring frameworks, ensure:
  - Comprehensive metadata to accompany omics data (site context, management practices, environmental conditions)
  - Clear paths from unidentified features to identified compounds for interpretability
  - Robust data governance for sharing, versioning, and provenance to support transparency and reuse
  - Consideration of sample size and multi-site design to enhance applicability for policy decisions