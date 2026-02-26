# Description of the dataset

## Overview
- Water sampling dataset from Lake Akrotiri and its main inputs, collected July 2019 to November 2020.
- Covers eight monitoring sites around the lake, including input canals and a drainage pipe feeding Zakaki marsh.
- Part of the Darwin Initiative Plus project to monitor drivers of change in Akrotiri wetlands.

## Spatial context
- Lake Akrotiri (Limassol salt lake) located in the Sovereign Base Area of Akrotiri and Dhekelia (Cyprus).
- Eight sampling sites (Cyp1–Cyp8) with precise latitude/longitude provided for each site.
  - Cyp1: Northern Polemidia retention pond outlet (west of the casino)
  - Cyp2–Cyp4: Zakaki marsh area (north-east salt lake/outfalls)
  - Cyp5: Zakaki freshwater marsh drainage channel
  - Cyp6: Southern salt lake area
  - Cyp7: Fasouri freshwater marsh drainage channel
  - Cyp8: North-west salt lake near Fasouri marsh outfall
- The lake is an important wetland attracting migratory birds and experiences seasonal water level fluctuations.

## Field measurements and data collection
- July 2019: Field measurements by UKCEH using Myron L Ultrameter II and YSI DSS pro.
- After July 2019: Monitoring by Joint Services Health Unit (JSHU) with YSI DSS pro.
- Samples filtered on site through 0.45 µm Whatman WCN membrane filters.

## Monitoring and analytical information
- Laboratory analyses performed at UKCEH Wallingford for:
  - Phosphorus species: total phosphorus (TP), total dissolved phosphorus (TDP), soluble reactive phosphorus (SRP)
  - Silicate (dissolved silicon), ammonium
  - Chlorophyll a
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN)
  - Major dissolved anions ( fluoride, chloride, nitrite, nitrate, sulphate) and cations (via ICP-OES)
- pH measured with Radiometer PHM210; field instruments calibrated to NIST-traceable buffers.
- Chlorophyll determined spectrophotometrically; SRP via phosphomolybdenum blue method; TP/TDP via persulphate digestion and spectrophotometry.
- Dissolved oxygen, DO %, conductivity (and other field parameters) recorded in the field.
- Methods and instrumentation described with reference to established protocols (listed in References).

## Dataset format and parameters
- Key measured variables with definitions and units:
  - Suspended_solids: mg/L
  - Soluble_reactive_phosphorus: µg/L
  - Total_dissolved_phosphorus: µg/L
  - Total_phosphorus: µg/L
  - Dissolved_ammonium: mg/L
  - Dissolved_silicon: mg/L
  - Chlorophyll-a: µg/L
  - Dissolved_fluoride: mg/L
  - Dissolved_chloride: mg/L
  - Dissolved_nitrite: mg/L
  - Dissolved_nitrate: mg/L
  - Dissolved_sulphate: mg/L
  - Total_dissolved_nitrogen: mg/L
  - Dissolved_organic_carbon: mg/L
  - Field_pH: pH
  - Conductivity (and related measures): µS, ms/cm
  - Eh: mV
  - Temp: °C
  - DO_percentage: %
  - DO: mg/L
  - SPC, C: µS/cm and ms/cm
  - SAL-PSU: practical salinity units
- Some values missing due to equipment failure or access limitations.

## Quality assurance and data reliability
- Field staff are experienced; data checked for anomalous values.
- All analyses (except suspended solids) validated against Aquacheck QC standards (LGC Standards).
- SRP samples analyzed within 48 hours to minimize instability.

## Missing values and limitations
- Missing data caused by equipment failures, differing probe types, or access restrictions.
- Seasonal drying of the lake influences sampling opportunities and data continuity.
- Analytical notes: SRP stability considerations and methodological references provided.

## Practical implications for GIS work
- Spatially explicit: eight site coordinates enable mapping of nutrient and water quality gradients around the lake.
- Rich multi-parameter dataset suitable for map-based visualisation of spatial patterns (e.g., TP, SRP, nitrates, chlorophyll) and their relation to hydrological inputs.
- Metadata includes sampling period, methods, QA references, and analytical techniques, aiding reproducibility and integration with other GIS layers (wetlands, drainage channels, marshes).

## References
- Eisenreich et al. 1975; Leeks et al. 1997; Marker et al. 1980; Mullin & Riley 1955; Murphy & Riley 1962; Neal et al. 2000 (phosphorus and related analytical methods).