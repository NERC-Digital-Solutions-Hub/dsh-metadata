# Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone

## Overview
- Audio dataset captured in the abandoned village of Buryakovka, Chernobyl Exclusion Zone, Ukraine (WGS84 coordinates provided).
- Recording setup: a single Wildlife Acoustics SM3 Songmeter on an overgrown road near abandoned houses with deciduous/fruit trees.
- Recording period: 12 hours on 25/06/2015 (midday to midnight), continuous.
- Recording format: stereo WAV files, 48 kHz sampling rate.
- Annotation: performed manually by a single expert using Raven Pro.
- Data packaging: five WAV files accompanied by five text annotation files sharing the same base filenames; annotations exist only on channel one.

## Data collection and provenance
- Location and environmental context detailed (near abandoned houses, deciduous trees, fruit trees).
- Timeframe and equipment explicitly documented.
- Provenance captured via the NERC Environmental Information Data Centre; DOI provided for citation and access.

## Data structure and contents
- Audio: five stereo WAV files (48 kHz).
- Annotations: five corresponding text files with tab-separated tables (same base name as audio files).
- Channel alignment: annotations apply to channel one (of two).

## Annotations and formats
- Annotation content includes:
  - Begin Time (s) and End Time (s): vocalisation start/end.
  - Low Freq (Hz) and High Freq (Hz): frequency bounds.
  - Sound category: tags (e.g., Sound category 1).
  - Additional information: notes such as low-level vocalisations.
  - Selection/view metadata indicating spectrogram view and ordinal ordering.
- Text files use a tab-separated structure; headers indicate fields and repetition seen in the sample.
- Annotations are designed to be compatible with Raven Pro (tags can be imported into Raven Pro).

## Metadata, access, and reuse
- Access and citation: BiVA dataset available via the NERC Environmental Information Data Centre; DOI provided.
- Discoverability: five paired audio/annotation files with consistent naming for easy linking.
- Usage considerations:
  - Suitable for wildlife vocalisation analysis and methodological development.
  - Limitations include a single annotator, a single recording location, and potential gaps in metadata standardization across files.
  - Data integrity relies on explicit annotation timing and frequency bounds; metadata supports reuse and cross-study comparisons when aligned with similar datasets.

## Practical considerations for Data Leaders
- Emphasize clear provenance, standardized metadata, and compatibility with analysis tools (e.g., Raven Pro) to facilitate discovery and reuse.
- Recognize scope limitations (single site, single annotator) when planning cross-network analyses or data-integrated work.
- Ensure citation and access pathways (DOI, EIDC entry) are maintained to support governance and collaboration across data communities.