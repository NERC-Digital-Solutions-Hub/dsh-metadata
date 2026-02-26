# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Overview
- Study uses a before-after-control-impact (BACI) design to test how benthic organic matter responds to added leaf litter in upland Welsh rivers.
- Each stream has an upstream reference (control) zone and a downstream experimental zone, separated by 20–50 m to ensure independence.
- Time framing:
  - Before period (T1): 61–65 days from Nov 2012 to Jan 2013; both zones untreated.
  - After period (T2): 57–62 days from Jan 2013 to Mar 2013; experimental zone receives leaf litter addition.
- Leaf litter addition:
  - One-tonne bags containing oak, birch, and alder leaves distributed proportionally to experimental zone area.
  - Vegetation nets maintained to keep a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - Additional leaf litter (630 kg wet weight per stream) added on Feb 12 and Mar 5, following storm events.
- Objective: determine how BOM stocks (coarse and fine particulate organic matter) respond to controlled organic matter enrichment.

## Experimental design and field setup
- Zones: upstream reference (control) and downstream experimental section per stream.
- Zone separation: 20–50 m between reference and experimental zones.
- Repetition: replicated across multiple streams with similar habitat structure (riffles, glides, pools) and land use.

## Sampling regime and collection methods
- Sampling method: Surber net sampler (0.1 m^2 area, 330 µm mesh, 10 cm depth).
- Sampling occasions: five monthly visits (January–May 2013).
- Sample handling: on-site preservation in 70% industrial methylated spirit (IMS); lab processing involved separating macroinvertebrates, drying, and weighing remaining material to 0.01 g.
- Inorganic correction: ash-free conversion applied by combusting a subset of samples at 550°C for 5 hours.

## Analytical methods and units
- Primary metrics: particulate organic matter stocks (coarse and fine POM).
- Units: grams (g) of cpom and fpom per sample.
- Data recording: BOM data weighed to nearest 0.01 g.

## Data structure and metadata
- Data files: flat CSV format.
- BOM dataset columns (10): site_code, landuse, region, time (Before/After), month, reach (Experimental/Control), replicate, surber_area, cpom, fpom.
- Supporting site metadata: DURESS_CU_site_description.csv with site_code, name, coordinates (Eastings/Northings), grid reference, latitude/longitude, elevation, survey campaign/catchment details.

## Quality control and calibration
- Calibration steps: none documented.
- Quality control: none documented.
- Ash-free correction implemented to adjust for inorganic content.

## Instrumentation
- Field: Surber net sampler (area 0.1 m^2; 330 µm mesh; 10 cm sampling depth).
- Laboratory: weight measurement using a weight-meter; sample preservation with IMS.

## Data management and accessibility
- Data organized for integration with broader monitoring datasets (structured CSV format; clear time and reach labeling).
- Site descriptions provided to enable geospatial context (coordinates, catchment information).
- Emphasis on standardised methods and clear metadata to facilitate reuse and potential data portal uploads.

## Relevance for environmental monitoring analysts
- Demonstrates a standardized BACI approach to evaluating how organic matter inputs affect benthic organic matter in streams.
- Provides explicit data structure (cpom and fpom) and temporal framing (Before/After) that supports trend analysis and policy-performance scrutiny over time.
- Metadata and site description files enhance data discoverability and integration with other environmental datasets, aligning with goals to increase dataset value and accessibility for downstream analysis.