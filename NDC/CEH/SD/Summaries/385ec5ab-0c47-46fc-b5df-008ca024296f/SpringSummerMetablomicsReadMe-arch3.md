# SpringSummerMetabolomics.csv

## Overview
- Project: Uplands-N2O
- Grant: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Data type: Metabolomics data from sheep urine
- Data description: Untargeted primary metabolism analysis results (peak intensities) from urine samples of sheep collected in spring and summer 2016 on a semi-improved site

## Data collection and processing
- Sampling design: 5 sheep sampled in spring and 5 in summer 2016 (n=10 total)
- Sample handling: Syringe-filtered (<0.2 μm) urine, flash-frozen; procedural blanks (ultra-pure water) processed similarly and blank-corrected
- Storage and transport: Frozen at -80 °C; shipped on dry ice to West Coast Metabolomics Center, UC Davis
- Analytical method: Untargeted primary metabolism analysis using ALEX-CIS GC-TOF-MS (Gerstel Inc.)
- Data quality steps: Blank correction performed; data intended for downstream metabolite identification and interpretation
- Data provenance: Project-related data described with explicit sample origins and processing steps

## Data content and structure
- Content: Peak intensity values for all identified compounds from the untargeted analysis
- Data headers:
  - Sample: Encodes season of collection and sheep ID
  - Season: Spring or Summer 2016
  - Other headers: Identified compounds; corresponding peak intensities beneath each
- Dataset scope: 10 samples (5 spring, 5 summer) from a semi-improved site; metabolite measurements presented as intensities

## Data access, reuse, and governance
- Citation requirement: If data are reused, must be fully cited
- Data sharing considerations: Underlying data and metadata exist within a structured CSV; broader data sharing and metadata completeness would influence reuse by others
- Governance cues: Documentation includes collection, processing, and analytical methods; provenance is explicit, aiding reproducibility and scrutiny

## Relevance to monitoring frameworks
- Demonstrates end-to-end data lifecycle relevant to environmental health monitoring: design, sample handling, quality control (blank corrections), analytical workflow, and clear data outputs (peak intensities)
- Reinforces needs identified for monitoring frameworks:
  - Clear metadata and provenance
  - Data quality assurance and transformation
  - Sharing and citation of data used in assessments
  - Transparency around analytical methods and instruments (GC-TOF-MS details)

## Considerations for implementation in monitoring
- Data scale and generalizability: Small sample size (n=10) limits broad policy conclusions; highlights need for scalable metadata standards and harmonized data formats
- Metadata sufficiency: Basic headers are present; additional metadata (units, compound identifications, calibration details, QC metrics) would enhance reuse
- Data interoperability: Consistent naming for samples and compounds supports integration with other datasets, provided standardized identifiers are used
- Barriers and opportunities: Public sharing of datasets may require careful governance and documentation to enable reuse while protecting sensitive information; robust metadata and provenance facilitate governance and decision-making in monitoring programs