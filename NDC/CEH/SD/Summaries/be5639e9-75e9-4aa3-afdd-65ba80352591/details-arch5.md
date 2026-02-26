# Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone

## Overview
- Audio captured in the Chernobyl Exclusion Zone, Ukraine, at the abandoned village of Buryakovka.
- Recording: a single 12-hour continuous session on 25/06/2015 (midday to midnight).
- Location coordinates: 51.382269, 29.924879 (WGS84).
- Equipment: Wildlife Acoustics SM3 Songmeter placed on an overgrown unpaved road near abandoned houses.
- Annotated by a single expert using Raven Pro (attention to the single-annotator context for interpretation and reproducibility).

## Data contents
- Five stereo WAV files, sampled at 48 kHz.
- Five corresponding text annotation files with the same base names as the WAV files.
- Annotations are on channel 1 only.

## Annotation and metadata structure
- Text annotation files are tab-separated and describe per-annotation entries, including:
  - Selection number (order)
  - View (spectrogram view)
  - Channel (annotations on channel one of two)
  - Begin Time (s)
  - End Time (s)
  - Low Freq (Hz)
  - High Freq (Hz)
  - Sound category 1
  - Additional information
- Annotations can be imported into Raven Pro, facilitating reuse and analysis.

## Provenance, access, and citation
- Data repository: NERC Environmental Information Data Centre.
- Citation: Kendrick, P.; Barçante, L.; Beresford, N.A.; Gashchak, S.; Wood, M.D. (2018). Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone. DOI: https://doi.org/10.5285/be5639e9-75e9-4aa3afdd-65ba80352591

## Stewardship and reuse considerations
- Clear linkage between audio data (WAV) and annotations (text files) supports discoverability and reuse.
- Metadata includes precise timing, frequency ranges, and spectrogram view, aiding interoperability with standard acoustic analysis workflows.
- Single annotator context should be considered when comparing with multi-annotator datasets; potential for annotation variability.
- Use of Raven Pro compatibility enhances accessibility for researchers aiming to reproduce or extend analyses.