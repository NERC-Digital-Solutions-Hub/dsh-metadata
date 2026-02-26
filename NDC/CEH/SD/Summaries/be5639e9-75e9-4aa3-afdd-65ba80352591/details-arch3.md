# Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone

## Data Access and Citation
- Available through the NERC Environmental Information Data Centre (EIDC).
- Citation: Kendrick, P.; Barçante, L.; Beresford, N.A.; Gashchak, S.; Wood, M.D. (2018). Bird Vocalisation Activity (BiVA) database: annotated soundscapes from the Chernobyl Exclusion Zone. DOI: https://doi.org/10.5285/be5639e9-75e9-4aa3afdd-65ba80352591

## Data Description
- Location: Abandoned village of Buryakovka, Chernobyl Exclusion Zone, Ukraine (51.382269, 29.924879, WGS84).
- Field setup: A single Wildlife Acoustics SM3 Songmeter placed on an overgrown unpaved road near abandoned houses with deciduous/fruit trees.
- Recording: One continuous 12-hour recording from midday to midnight on 25/06/2015.
- Annotation: Performed by a single expert using Raven Pro.
- Output: Five stereo WAV files (48 kHz) and five corresponding text tag files; annotations apply to channel one.
- Data organization: Text files are tab-separated and contain metadata about selections, view from spectrogram, channel, begin/end times, frequency bounds, sound category tags, and additional information. Tags can be imported into Raven Pro.

## Data Content and Structure
- Raw data: Five WAV files (stereo) totaling 12 hours of audio from a single location.
- Annotations: Five corresponding text files with structured fields for time, frequency, and labeling (sound categories and additional notes).
- Reference tools: Annotations designed to interoperate with Raven Pro (tag import possible via provided text formats).

## Annotation Workflow and Tools
- Annotation performed by one expert.
- Tooling: Raven Pro used for labeling; text tags are aligned with respective WAV files.
- Accessibility of annotations: Text tag files link to their associated WAV files and can be used to reproduce or extend analyses in Raven Pro.

## Data Quality, Metadata, and Sharing
- Metadata explicit (location, date, equipment, sampling rate, channel assignment, and annotation specifics).
- Data formats are open (WAV audio and text-based annotations) to support reuse and interoperability.
- Annotations are confined to channel one of the stereo recordings.

## Practical Considerations for Monitoring Frameworks
- Demonstrates integration of raw environmental data with structured, machine-readable annotations.
- Highlights the importance of metadata completeness (location, date, equipment, sampling rate) for data reuse in monitoring programs.
- Shows a clear data governance pathway: dataset stored in a recognized data centre with a stable DOI, enabling citation and long-term accessibility.
- Illustrates potential workflow for policy-relevant environmental monitoring: single-site, expert-annotated acoustic data that can be used to develop and validate automated monitoring or biodiversity indicators.
- Example of data sharing and interoperability challenges mitigated by providing standardized annotation formats that are compatible with common analysis tools (e.g., Raven Pro).