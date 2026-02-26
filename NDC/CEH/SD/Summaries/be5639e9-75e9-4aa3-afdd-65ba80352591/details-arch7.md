# Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone

## Overview
- A dataset of annotated soundscapes captured in the Chernobyl Exclusion Zone, Ukraine.
- Recording site: Buryakovka, abandoned village near deciduous and fruit trees; coordinates 51.382269, 29.924879 (WGS84).
- Equipment: Wildlife Acoustics SM3 Songmeter placed on an overgrown unpaved road near abandoned houses.

## Data contents
- Time period: 25 June 2015, a single continuous 12-hour recording from midday to midnight.
- Audio format: five stereo WAV files, 48 kHz sample rate.
- Annotations: five text files (same base name as audio files), annotations on channel 1; text files are tab-separated.
- Annotation format: columns include selections, begin time (s), end time (s), low freq (Hz), high freq (Hz), sound category 1, and additional information (e.g., notes on low-level vocalisations).
- Annotation channel: defined as channel one of two channels.
- Usability note: tags can be imported into Raven Pro for analysis.

## Data structure and provenance
- Annotations are produced by a single expert using Raven Pro.
- Spatial context is limited to one recording site; data describe temporal occurrences of vocalisations with frequency bounds.

## Temporal and spatial context
- Location context: recorded at a single site within the Chernobyl Exclusion Zone; habitat context includes deciduous trees and nearby abandoned houses.
- Temporal context: 2015-06-25, 12:00–24:00 (12 hours) local time.

## Access, licensing, and provenance
- Data centre: NERC Environmental Information Data Centre.
- Citation: Kendrick, P.; Barçante, L.; Beresford, N.A.; Gashchak, S.; Wood, M.D. (2018). Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone. NERC EIDC.
- DOI: 10.5285/be5639e9-75e9-4aa3afdd-65ba80352591
- Additional note: Tags are designed for import into Raven Pro.

## GIS relevance and usage guidance
- GIS application: map-based representation of vocalisation events at a known site; useful when integrated with habitat layers or additional spatial datasets.
- Data can be used to create time-enabled event layers from begin/end times and frequency ranges; potential to link vocalisation events with environmental variables.
- Practical considerations:
  - Only one geographic location is provided; spatial analyses will be limited to this site unless supplemented with additional BiVA data.
  - Annotation comes from a single expert; consider cross-validation with additional annotations for broader uncertainty assessment.
  - Data format compatibility: exportable to CSV/SHP-based workflows after processing begin/end times and frequency bands.

## Limitations and considerations
- Single recording site; limited spatial coverage.
- Annotations produced by one expert; potential for subjective bias.
- Only channel one annotations; stereo audio but analysis focuses on a single channel.
- Data coverage is constrained to a 12-hour window on a single day.

## Source reference
- Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone. Data access via NERC EIDC; DOI provided above.