# Elter_light_2018-2019.txt

## Overview
- Weekly to monthly vertical profiles of underwater PAR (photosynthetically active radiation) collected from May 2018 to December 2019.
- Measurements taken at the deepest point of Elterwater inner basin.

## Location and Instrumentation
- Location coordinates: Lat 54.4287°, Long -3.0350°.
- Instrument: LI-COR LI-192 underwater quantum sensor (LI-COR, Lincoln, USA).

## Measurements and Frequency
- PAR measured at half-meter intervals from 0.5 to 6 meters depth.
- Frequency ranges from weekly to monthly within the data collection period.

## Data Structure
- Fields: Date (yyyy-mm-dd), Depth (m), Light (μmol s⁻¹ m⁻²).

## Data Quality and Processing
- Measurements were checked via visual inspection (quality assurance step).

## Potential Data Use and Products
- Build time-series of PAR by depth to study light penetration dynamics.
- Create vertical PAR profiles over time for visualization and analysis.
- Compare PAR patterns across depths and over seasons or weather events.

## Data Support Considerations for Reuse
- Handling irregular sampling: weekly to monthly cadence may require resampling or interpolation for uniform analyses.
- Data normalization: ensure units (Light) are consistently interpreted as μmol s⁻¹ m⁻².
- Metadata gaps to consider: calibration details, sensor aging, and any site-specific conditions are not specified.

## Suggested Data Support Actions
- Provide a reproducible read-in workflow (e.g., parse Date, Depth, Light; handle missing values).
- Offer example visualizations: (a) time series of Light at selected depths, (b) vertical light profiles at key dates.
- Provide derived metrics templates: daily/weekly PAR integrals or attenuation coefficients with depth.
- Include guidance on merging with additional environmental data if available (e.g., temperature, turbidity) to enrich analyses.