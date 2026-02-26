# ReadMe file for Biomass_N_and_CtoN.csv

## Overview
- ReadMe describing Biomass_N_and_CtoN.csv.
- Data derive from a field trial on greenhouse gas emissions from sheep urine patches applied to semi-improved upland grassland.
- Focus on above-ground biomass harvests collected within greenhouse gas chambers (chamber size 50 cm x 50 cm).

## Study context and location
- Location: orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales (270 m above sea level; 53°13'N, 4°0'W).
- Experimental treatments (n=4) include Control (no urine), ArtUrine (artificial sheep urine), and RealUrine (real sheep urine).
- Design: randomised block with spring and autumn applications in 2016.

## Experimental design and sampling
- Treatments applied in spring and autumn 2016.
- Biomass cuts taken four times following spring treatments and three times following autumn treatments.
- Biomass samples stored in paper bags; dried in an oven at 80 °C for 24 hours.
- Dried samples ground in a ball mill and analysed with a TruSpec® Analyzer (Leco) against certified reference materials.

## Data collection and quality checks
- Data visually checked for errors after analysis.
- Data headers in the CSV:
  - Sample_date: date of sampling
  - Plot_no: chamber number from which biomass samples were taken
  - Treatment: Control, ArtUrine, RealUrine
  - Season: Spring or Autumn corresponding to treatment
  - Biomass: above-ground biomass in g dry weight m-2
  - Foliar_N: nitrogen content of dried, ground biomass in %
  - Foliar_CtoN: carbon-to-nitrogen ratio of biomass samples

## Data fields and interpretation
- Biomass: indicates dry weight biomass per square meter.
- Foliar_N: nitrogen content percentage in biomass.
- Foliar_CtoN: carbon-to-nitrogen ratio in biomass.
- Data are tied to specific treatments, seasons, and chamber plots, enabling assessment of urine treatment effects on biomass composition.

## Data governance and usage notes
- Authors must be acknowledged if data are reused or reproduced.
- The dataset originates from a single field site and year (2016), which may affect generalizability.
- Metadata provided supports discoverability and reuse within data governance frameworks, with clear provenance, processing steps, and quality checks.

## Potential considerations for data stewards
- Ensure consistent interpretation of Treatment labels (Control, ArtUrine, RealUrine) across datasets.
- Maintain detailed provenance on sample processing (drying, grinding, analyzer) to support reproducibility.
- Consider adding additional contextual metadata (e.g., exact sampling intervals, plot coordinates, and full statistical design) if expanding to multi-site or multi-year datasets.
- Verify any updates or corrections to dates, sample IDs, or measurement units to preserve data integrity.