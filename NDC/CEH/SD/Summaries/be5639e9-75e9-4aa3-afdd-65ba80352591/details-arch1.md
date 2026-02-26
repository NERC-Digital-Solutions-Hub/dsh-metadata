# Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone

## Overview
- Audio captured in the abandoned village of Buryakovka, Chernobyl Exclusion Zone, Ukraine (coordinates: 51.38269, 29.924879).
- Recording date and duration: 25 June 2015, 12 hours from midday to midnight.
- Equipment: a single Wildlife Acoustics SM3 Songmeter mounted on an overgrown unpaved road near abandoned houses with deciduous trees.
- Recording setup: one continuous 12-hour file; stereo WAV files.

## Data content and format
- Files: five stereo WAV files, sampled at 48 kHz.
- Annotations: five corresponding text files, with the same base names as the WAV files.
- Annotation scope: annotations are made on channel 1 only.
- Annotation files format: tab-separated tables with columns including Begin Time (s), End Time (s), Low Freq (Hz), High Freq (Hz), Sound category 1, Additional information, Channel, View, and Selection/Description metadata.
- Additional notes: Text entries describe spectrogram view and other descriptive fields for each annotated segment.

## Annotation details
- Annotations created manually by a single expert using Raven Pro.
- Tags described in the text files can be imported into Raven Pro (link provided in the dataset).

## Provenance and access
- Citation: Kendrick, P.; Barçante, L.; Beresford, N.A.; Gashchak, S.; Wood, M.D. (2018). Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/be5639e9-75e9-4aa3afdd-65ba80352591

## Potential uses for analysts
- Enables study of bird vocalisation activity in a post-disaster/exclusion zone environment.
- Facilitates analyses of correlations between vocalisation characteristics (time, frequency range, duration) and environmental context.
- Data can support development and testing of predictive models for bird activity in restricted areas.
- Useful for cross-referencing with other datasets, given the explicit time stamps and frequency information.

## Considerations and limitations
- Only one annotator, and annotations are restricted to channel 1.
- Dataset comprises a single 12-hour recording from one location, which may limit generalizability.
- Data organization requires matching base names between WAV and corresponding annotation text files; careful handling needed to ensure correct pairing.
- Some fields rely on manual tagging and descriptive notes, which may vary in detail across segments.