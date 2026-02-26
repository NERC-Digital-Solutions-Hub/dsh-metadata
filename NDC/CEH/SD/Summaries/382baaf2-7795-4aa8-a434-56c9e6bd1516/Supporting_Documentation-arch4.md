# Brief description of methods

## Overview
- Study of ozone effects on two plant species: Leontodon hispidus (Rough Hawkbit) and Succisa pratensis (Devil's-bit Scabious).
- Field experiment conducted in North Wales, UK (Abergwyngregyn), April 2016 onward.
- Plants arranged in 1 m square blocks within nine Free Air Ozone Enrichment (FAOE) rings (4 m diameter), using a Latin square design to alternate species.
- Ozone treatments: Low (mean ~24 ppb), Medium (mean ~40 ppb), High (mean ~57 ppb).
- Nitrogen treatment: 40 kg N ha-1 yr-1 added to one block in year 1; irrigation relied on natural precipitation.

## Experimental design and treatments
- Nine FAOE rings, each containing both species in alternating blocks.
- Ozone treatment assignments within rings: Low = A1, B2, C3; Medium = A3, B1, C2; High = A2, B3, C1.
- Soil: Orthic Podzol, pH 5.
- Measurements focused on growth and physiology: leaf ground cover, leaf litter, flowering, chlorophyll index, photosynthesis (Asat), and stomatal conductance (gs).

## Measurements and instruments
- Photosynthesis and stomatal conductance (Asat, gs) measured on healthy leaves with LI-COR 6400XT.
  - Mean chamber conditions: temperature 20°C, CO2 400 µmol mol-1, light 1500 µmol m-2 s-1, RH 60–80%, leaf VPD 0.8–1.2 kPa.
- Chlorophyll index measured on healthy leaves with Opti-Sciences CCM200.
- Flowering stems counted.
- Leaf cover assessed using 100-square grids overlaid on plant images; additional notes on damaged (PurpleCover) and frost-damaged leaves; October 2016 assessments; January 2017 frost damage.
- Litter weight: oven-dried litter (60°C) measured monthly from July 2016 to February 2017.

## Data files and metadata
- Five CSV data files:
  - Asat_gs.csv: Light-saturated photosynthesis (Asat) and stomatal conductance (gs).
  - Chlorophyll.csv: Chlorophyll index (Chl).
  - FlowerStems.csv: Number of flowering stems.
  - LeafCover.csv: Leaf ground cover; PurpleCover; FrostDamage.
  - WeightLitter.csv: Monthly litter weight (grams).
- Common columns across files:
  - Date or Month/Year; Ring (FAOE ring); Nitrogen (YES/NO); Ozone (Low/Medium/High); Species (Succisa or Leontodon).
- File-specific columns detail:
  - Asat_gs.csv: Asat (µmol CO2 m-2 s-1), gs (mmol H2O m-2 s-1).
  - Chlorophyll.csv: Chl (chlorophyll index).
  - FlowerStems.csv: No_FlowerStems (count).
  - LeafCover.csv: Cover (%), PurpleCover (%), FrostDamage (%).
  - WeightLitter.csv: Litter (grams).
- Data notes:
  - NA indicates missing measurement.
  - Leontodon showed no frost damage (NA in FrostDamage for that species).
  - Measurements conducted under standardized conditions as described above.

## Quality control and data validity
- Ozone levels calibrated with Thermo 49i analyser.
- LI-COR 6400XT pre-measurement checks for chamber temperature, light, pressure, flow rate; checks for CO2 and H2O; chamber leaks evaluated.
- Data graphically checked for outliers or unusual values.

## Summary for data governance and reuse
- Clear linkage between treatments (Ozone, Nitrogen) and measured plant responses across two species.
- Detailed, standardized metadata for each dataset to support discoverability, interpretation, and replication.
- Data are organized into five separate CSV files with explicit column headers and measurement units, enabling integration into broader data systems and cross-study comparisons.