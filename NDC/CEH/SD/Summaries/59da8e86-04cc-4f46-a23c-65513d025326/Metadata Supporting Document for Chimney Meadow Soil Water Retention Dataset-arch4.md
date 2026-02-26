# Objective To determine soil characteristics within the top metre of soil to relate to soil moisture and Electrical Resistivity Tomography measurements

## Overview
- Single-site soil characterization at Church Field, Chimney Meadow NNR, to relate soil properties to moisture and ERT measurements.
- Sampling targeted the soil region along the ERT transect with a pit located 13.75 m from the transect north end and offset 1.0 m west.

## Experimental design and sampling regime
- Representative sampling of the local soil type for the ERT experiment.
- Depth increments of 10 cm up to 1.0 m, with two samples collected at each depth from a level, horizontal cut in the soil pit.
- End caps used to preserve samples during transport.
- Field coordinates of transect endpoints and soil pit provided (OSGB grid references).

## Fieldwork and laboratory instrumentation
- Sampling using stainless steel rings (100 mm deep, 99 mm I.D.) to maintain sample volume (769.77 cm3).
- Four laboratory stages to impose suction and measure water content:
  - Stage 1: Sand bath with suction pF 0 to pF 2.0 (0 to -100 hPa) via sand transmission.
  - Stage 2: Sand/kaolin box for suction pF 2.0 to pF 2.7 (-100 hPa to -500 hPa) via kaolin-sand medium.
  - Stage 3: 5 bar pressure plate extractor.
  - Stage 4: 15 bar pressure plate extractor.

## Calibration steps and values
- Suction applied via dedicated equipment; ambient pressure offset corrections applied.
- Pressure vessels calibrated with certified standards; 15 bar plates use a single regulator, 5 bar plates use dual regulators.
- Soil moisture content determined by weighing a fixed soil volume at each suction step.

## Analytical methods
- Samples equilibrated in water baths to saturation, then progressively dried under controlled suctions.
- Equilibrium judged when daily weight difference < 0.1 g.
- Water-release (retention) curves constructed for each depth.
- Found two clay-dominated soil types interleaved (not in fixed horizons), indicating historical deposition changes in the Thames floodplain.

## Nature and units of recorded values
- Recorded values include:
  - Total weight (soil + water + ring)
  - Soil weight (total – ring)
  - Water weight (total – ring – dry soil)
  - MVF (moisture volume fraction) = water weight / volume of soil sample
- All weights in grams; CSV format for data storage.

## Converting between water potential units
- Units covered: MPa, kPa, Bar, pF.
- Key conversions:
  - 1 bar = 100 kPa; 1 MPa = 1000 kPa
  - -1.0 MPa = -10 bar
  - pF = log10( suction in cm of water ); 1 MPa ≈ 10200 cm water
  - Upper plant-available limit ≈ -0.033 MPa (pF 2.53); permanent wilting point ≈ -1.5 MPa (pF 4.18)
- Notes on converting to pF, including handling of negative signs in logarithms.

## Quality Control
- Recognition procedures followed; two sample sets per depth to detect procedural anomalies by cross-comparison.
- Anomalies identified by plotting both results together to spot inconsistencies.

## Format of stored data
- Data stored as comma-separated values (.csv).

## Soil type and context
- Church Field sits on a clay lens overlying sands and gravels.
- A and B horizons generally uniform to 1.1 m; mapping suggests a Kelmscott-type loamy soil with groundwater influence and flood risk, though local maps show a clay substrate in the Thames Valley with surrounding sand and gravel.

## Photographs
- Explanatory images available via the CEH Image Catalogue; linked to CEH SCWAFL project.

## References
- Blake & Hartge (1986); Klute (1986); Eijkelkamp equipment manuals (2005); Soil Moisture Equipment Corporation manuals (2002).