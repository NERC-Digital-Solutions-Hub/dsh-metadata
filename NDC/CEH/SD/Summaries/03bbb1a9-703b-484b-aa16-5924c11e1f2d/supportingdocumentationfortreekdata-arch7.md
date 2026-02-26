# Saturated hydraulic conductivity, bulk density and soil organic carbon content from three paired upland woodland and grassland sites in northern England, July 2019-April 2021

## Overview
- Dataset measures three soil properties across three paired upland sites in northern England: saturated hydraulic conductivity (K), bulk density, and soil organic carbon content.
- Comparison between woodland (T) and adjacent grassland/pasture (P) to assess potential impacts of upland tree planting on soil properties.
- Sampling occurred July 2019–April 2021, with processing in subsequent months; COVID-19 disruptions affected timelines.
- Supported by the Natural Environment Research Council's NFM research programme.

## Experimental design
- Sites and codes:
  - JF = Jerusalem Farm (old mature deciduous woodland)
  - MW = Midgelden Woods (deciduous woodland ~15 years since planting)
  - IF = Inchfield (newly planted deciduous woodland, <5 years before sampling)
- Each site has adjacent permanent grazed grassland (P) and woodland (T); both land covers sampled.
- Sampling design: random sampling within woodland and grassland, with a 20 m buffer from edges; 10 sample points per land cover per site, totaling 60 sample points.
- Geographic coordinates:
  - JF: 53.7484, -1.9459
  - MW: 53.7089, -2.1553
  - IF: 53.7054, -2.1319

## Data collection methods
- Soil sampling at depths from the top 50 cm, using bulk density rings (5.3 cm diameter) to collect 5 cm long samples.
- Depths sampled (mid-point depths in cm): 5, 10, 15, 25, 35, 45 cm (corresponding to 2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm, 32.5–37.5 cm, 42.5–47.5 cm).
- K measurement: saturated hydraulic conductivity determined with an Eijkelkamp 25-place permeameter; readings taken after saturation with known hydraulic gradient.
- Bulk density: determined gravimetrically via oven drying at 105°C for 24 hours.
- Soil organic carbon: measured for the upper two depths using loss on ignition; assumed carbon content of soil organic matter is 58% (conversion factor 0.58).
- Descriptive soil interpretation provided (e.g., silt, sand, structured clay).

## Quality control
- K measurements: procedures followed per Eijkelkamp manual (School of Geography, University of Leeds).
- Bulk density: mass measured to two decimal places (g).
- Soil organic carbon: 10% of samples replicated; if replicate values within 10% of each other, mean used; otherwise a third replicate was measured and the mean of all replicates used.

## Nature and units of recorded values
- K: saturated hydraulic conductivity (metres per day, m/d)
- Bulk density: (grams per cubic centimetre, g/cm³)
- SOC: soil organic carbon content (% of dry soil mass)
- Depth: mid-point depth in centimetres (cm)

## Details of data structure
- Columns include:
  - Site: IF = Inchfield, MW = Midgelden, JF = Jerusalem Farm
  - Mid point depth: depth samples in 5 cm increments; reported as mid-point in cm
  - Trees/Pasture: T = woodland, P = grassland
  - Soil type: qualitative descriptor
  - Bulk density: numeric (two decimals)
  - K: numeric (m/d)
  - SOC %: numeric (two decimals)