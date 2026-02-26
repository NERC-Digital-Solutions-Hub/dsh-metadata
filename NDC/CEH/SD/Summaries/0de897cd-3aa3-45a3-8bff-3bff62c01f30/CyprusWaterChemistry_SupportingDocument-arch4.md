# Description of the dataset

## Scope and purpose
- Water sampling dataset for Lake Akrotiri, Cyprus, from July 2019 to November 2020.
- Includes eight monitoring sites around the lake and input canals; part of the Darwin Initiative Plus project to understand drivers of change in the Akrotiri wetlands.
- Lake is a key eastern Mediterranean wetland with variable water levels and seasonal drying.

## Sampling locations
- Eight sites (Cyp1–Cyp8) with coordinates and site descriptions:
  - Cyp1: Northern Polemidia retention pond outlet west of the casino.
  - Cyp2–Cyp4: North east salt lake at Zakaki marsh outfalls (inland/furthest sampling points).
  - Cyp5: Zakaki freshwater marsh drainage channel (stormwater from western Limassol).
  - Cyp6: Southern salt lake (far from Zakaki/Fasouri inputs; edge runoff).
  - Cyp7: Fasouri freshwater marsh drainage channel (connected to Akrotiri aquifer when high).
  - Cyp8: North west salt lake (near Fasouri outfall and village storm drains).

## Field measurements and sampling timeline
- July 2019: Field measurements by UKCEH using MYRON L Ultrameter II and YSI DSS pro.
- Later samples: Collected by Joint Services Health Unit (JSHU) using YSI DSS pro.

## Monitoring and analytical methods
- Filtration: Field samples filtered immediately through a 0.45 μm membrane.
- Laboratory analyses (UKCEH Wallingford):
  - Phosphorus: Total phosphorus (TP), total dissolved phosphorus (TDP), and soluble reactive phosphorus (SRP) using acidified persulfate digestion and colorimetric methods.
  - Nutrients and pigments: Chlorophyll-a; dissolved organic carbon (DOC); total dissolved nitrogen (TDN).
  - Major dissolved constituents: Ammonium; dissolved reactive silicon; fluoride, chloride, nitrite, nitrate, sulphate.
  - Particulates: Suspended solids.
  - Cations/ions: Major cations by ICP-OES; anions by ion chromatography.
  - Field parameters: Conductivity, pH, oxidation-reduction potential (Eh), temperature, dissolved oxygen (DO) and DO saturation, SP C, and salinity (SAL-PSU).
- Instrumentation: pH measured with Radiometer PHM210; conductivity with Myron Ultrameter; additional field measurements with YSI DSS pro.

## Data structure and units
- Key variables with definitions and units (examples):
  - Suspended_solids: mg/L.
  - Soluble_reactive_phosphorus: μg/L.
  - Total_dissolved_phosphorus: μg/L.
  - Total_phosphorus: μg/L.
  - Dissolved_ammonium: mg/L.
  - Dissolved_silicon: mg/L.
  - Chlorophyll-a: μg/L.
  - Dissolved_fluoride, Dissolved_chloride, Dissolved_nitrite, Dissolved_nitrate, Dissolved_sulphate: mg/L.
  - Total_dissolved_nitrogen: mg/L.
  - Dissolved_organic_carbon: mg/L.
  - Field_pH: (dimensionless).
  - Conductivity (and related metrics): µS, SPC (µS/cm), C (ms/cm), SAL-PSU.
  - Temp: °C; DO_percentage: %; DO: mg/L; Eh: mV.
- Note: Total phosphorus includes both dissolved and acid-extractable particulate phosphorus; SRP is filterable reactive phosphorus.

## Missing data and quality assurance
- Some values missing due to equipment failure or access issues.
- Data collected by experienced field staff; checked for anomalous values.
- Analytical work (except suspended solids) performed alongside Aquacheck QC standards.

## Data provenance, limitations, and references
- Methods and analyses aligned with established literature:
  - Eisenreich et al. 1975; Leeks et al. 1997; Marker et al. 1980; Mullin & Riley 1955; Murphy & Riley 1962; Neal et al. 2000.
- Data provenance includes field measurement records, filtration steps, laboratory digestion and colorimetric analyses, and spectrophotometric quantifications.
- Dataset characterizes both field measurements and laboratory-derived concentrations across multiple parameters, enabling cross-site comparisons and long-term trend analyses.