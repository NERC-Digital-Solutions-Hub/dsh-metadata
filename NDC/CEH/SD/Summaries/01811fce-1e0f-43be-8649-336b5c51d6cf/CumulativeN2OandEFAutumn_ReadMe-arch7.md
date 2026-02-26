# ReadMe file for CumulativeN2OandEFAutumn.csv

## Purpose and scope
- Describes a dataset of cumulative N2O emissions and N2O-N emission factors (EF) from a field experiment.
- Focused on control (no urine), artificial sheep urine, and real sheep urine applications in a greenhouse gas measurement context.

## Location and experimental design
- Location: Humic gleysol in unimproved grazing land, Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation and coordinates: 556 m above sea level; 53°22'N, 3°95'W.
- Experimental design: Randomised block design.

## Treatments and application rates
- Treatments (as indicated in data headers): Control (no urine), ArtUrine (artificial sheep urine), Urine (real sheep urine).
- N application rates:
  - Artificial urine: 1120 kg N ha-1.
  - Nitrate and glucose treatment: 106 kg N ha-1 and 213 kg C ha-1 (note: described in text; dataset headers reflect the Control, ArtUrine, and Urine treatments).

## Data collection and computation
- Emissions measurement: Cumulative N2O emissions calculated for each chamber over 118 days.
- Calculation method: Area under the curve for each chamber, using trapezoidal integration starting from treatment application.
- Emission factors (EF): Percentage of total N applied that is released as N2O-N, corrected for the portion of chamber area not receiving treatment due to discrete urine patches.
- Data quality: Visual checks performed to identify errors.

## Data fields and units
- Treatment: Categorical, values include 'Control', 'ArtUrine', 'Urine'.
- Chamber: Numeric identifier for the chamber from which measurements were taken.
- Cum_N2O: Cumulative N2O emissions per chamber (units: micrograms N2O-N; timeframe: 118 days).
- EF: N2O-N emission factor (percent of total N applied).

## GIS relevance and applications
- Spatial analysis of emissions across plot chambers can be enabled by chamber-level data and precise location context.
- Suitable for creating map-based visualisations of emissions and EF by treatment and space, and for overlay with site features (topography, land use, etc.).
- Useful for evaluating spatial patterns and informing policy or stakeholder communication about agricultural N2O emissions.

## Considerations and limitations
- Data apply to a single unimproved grazing site in Snowdonia; generalisability to other soils or climates may be limited.
- N application methods include discrete patches, requiring correction (as noted) when calculating EF.
- Measurement covers 118 days; longer-term trends beyond this period are not reflected.

## Usage and attribution
- Authors must be acknowledged if data are reused or reproduced.