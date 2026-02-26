# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Aim
- Investigate how adding leaf litter (organic matter) affects benthic organic matter (BOM) stocks in Welsh upland rivers.
- Use a BACI design to compare upstream reference sites with downstream experimental sites, focusing on coarse (CPOM) and fine (FPOM) particulate organic matter.

## Experimental design
- BACI framework: each stream has an upstream reference zone and a downstream experimental zone, separated by 20–50 m to ensure independence.
- Periods:
  - Before period (T1): 61–65 days, Nov 2012–Jan 2013; no manipulation; both zones treated identically.
  - After period (T2): 57–62 days, Jan–Mar 2013; experimental zone receives leaf litter addition.
- Leaf litter manipulation:
  - One-tonne bags of deciduous leaves (oak, birch, alder) distributed proportionally to experimental zone area.
  - Vegetable net bags maintain a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - Leaf packs reflect natural senescence; additional 630 kg (wet weight) of leaf litter added on 12 Feb 2013 and 5 Mar 2013 after storm events.
- Sampling framework:
  - Six random BOM samples per reach on five occasions (Jan–May 2013).

## Collection and processing methods
- Field collection: Surber net sampler (0.1 m^2, 330 μm mesh, 10 cm depth).
- On-site preservation in 70% IMS; transport to lab for processing.
- Laboratory processing:
  - Separate macroinvertebrates from debris; dry remaining material to constant weight.
  - Correct BOM for inorganic content via ash-free conversion using combustion at 550°C (subset) for 5 hours.
  - Weigh BOM to nearest 0.01 g; report as grams.
- Units: BOM stocks reported as grams (coarse and fine particulate organic matter).

## Calibration, QA, and data integrity
- Calibration steps: None listed.
- Quality control: None listed.
- Data handling notes: BOM samples are cross-checked against inorganic content; samples stored as flatbed CSVs with standardized fields.

## Data structure and content
- Data format: flatbed CSV files.
- Key BOM dataset columns (10 total):
  - site_code: code for sampling site
  - landuse: basin land-use
  - region: stream basin region
  - time: Before or After manipulation
  - month: sampling month (Jan–May 2013)
  - reach: Experimental or Control site
  - replicate: replicate code
  - surber_area: area of the surber sampler (m^2)
  - cpom: coarse particulate organic matter (grams)
  - fpom: fine particulate organic matter (grams)
- Supporting site descriptions: separate CSV with 10 fields (site_code, name, coordinates, grid, latitude, longitude, elevation, survey, catchment, etc.).

## Site information and context
- Site descriptions provide location coordinates (Eastings/Northings, latitude/longitude), elevation, grid references, and catchment context.
- Survey campaigns linked to Welsh Acid Water Survey (WAWS) and specific catchments such as Plynlimon and Llyn Brianne.

## Potential analyses and practical uses
- Compare BOM (CPOM and FPOM) before vs after leaf litter addition, between experimental and reference sites.
- Assess the magnitude and timing of BOM response to increased organic matter input, including responses after storm-related litter additions.
- Explore spatial variability across streams and link BOM stocks to land-use context and site descriptors.
- Use data to inform models of organic matter dynamics in upland streams and to improve understanding of how detrital inputs shape stream ecology.