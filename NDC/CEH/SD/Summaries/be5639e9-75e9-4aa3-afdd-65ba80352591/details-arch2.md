# Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone

## Overview
- A dataset of annotated bird vocalisations collected from the Chernobyl Exclusion Zone, Ukraine.
- Recording date: 25 June 2015; duration: 12 hours (from midday to midnight).
- Location: abandoned village of Buryakovka, with coordinates 51.382269, 29.924879 (WGS84); environment includes deciduous and fruit trees.
- Recording instrument: Wildlife Acoustics SM3 Songmeter on an unpaved road near abandoned houses.
- Data format: five stereo WAV files (48 kHz sampling); five accompanying text annotation files (same base names), with annotations on channel 1.
- Annotations: manually created by a single expert using Raven Pro.

## Data structure and contents
- File pairing: each WAV file has a corresponding tab-separated text file containing annotations.
- Annotation fields (examples of columns): selection number, view/spectrogram reference, channel (annotations on channel one of two), begin time (s), end time (s), low freq (Hz), high freq (Hz), sound category 1 (tags), additional information (notes such as low-level vocalisations).
- Annotations focus on channel one; text files provide the timing, frequency bounds, and tagging details for each vocalisation event.
- Purpose: supports identification and characterization of vocalisations within the recorded soundscape.

## Data access and usage
- Data source: Bird Vocalisation Activity (BiVA) database, published in the NERC Environmental Information Data Centre.
- Data citation: Kendrick, P.; Barçante, L.; Beresford, N.A.; Gashchak, S.; Wood, M.D. (2018). Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone. NERC EIDC. DOI: https://doi.org/10.5285/be5639e9-75e9-4aa3-afdd-65ba80352591
- Access and reuse: datasets are stored and accessible via the NERC EIDC; notes indicate compatibility with Raven Pro (annotations can be imported for analysis).

## Technical details relevant to monitoring analysts
- Standardized data format and metadata: time-stamped vocalisation events with frequency ranges, enabling consistent health indicators across time.
- Interoperability: annotations are Raven Pro-compatible, facilitating integration with existing acoustic monitoring workflows.
- Reproducibility: single expert annotation provides a clear, traceable methodology for this recording; potential need for cross-validation if used for extensive monitoring programs.
- Temporal and spatial context: single-day snapshot from a specific location within the Chernobyl Exclusion Zone; useful as a baseline when combined with additional datasets.

## Relevance for environmental monitoring
- Demonstrates how acoustic data can be captured, annotated, and stored in a standardized format for long-term environmental health assessment.
- Supports cross-dataset comparisons when integrated with other monitoring data (e.g., biodiversity surveys, habitat data).
- Highlights the importance of data accessibility and interoperability to enable broader data reuse and policy scrutiny.