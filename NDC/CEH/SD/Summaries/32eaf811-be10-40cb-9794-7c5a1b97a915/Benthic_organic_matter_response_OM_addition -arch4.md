# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Aim
- Assess how benthic organic matter (BOM) in Welsh upland rivers responds to the addition of leaf litter, using a BACI experimental framework.

## Experimental design
- Before-after-control-impact (BACI) design with:
  - Each stream divided into an upstream reference zone and a downstream experimental zone, separated by 20–50 m to ensure independence.
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013), both zones treated equally.
  - After period (T2): 57–62 days (Jan 2013 to Mar 2013) with leaf litter addition to the experimental zone.
- Leaf litter additions:
  - Proportional 1-tonne bags of oak, birch, and alder leaves added above the experimental zone.
  - Vegetation net bags also added to maintain minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - During T2, leaf packs degraded slowly, maintaining loose leaf litter; additional 630 kg (wet weight) added on 12 Feb and 5 Mar 2013 after storm-flows.
  
## Sampling regime
- Six random BOM samples collected per reach using a Surber net (0.1 m^2 area, 330 µm mesh, 10 cm depth).
- Five collection occasions: January, February, March, April, May 2013.
- Samples preserved on-site in 70% IMS; in the lab, macroinvertebrates separated and BOM processed.

## Collection and processing methods
- On-site: Surber net sampling as specified.
- Laboratory processing:
  - Rinse debris, separate macroinvertebrates, preserve in 70% IMS.
  - Rinse remaining material, retain on 1 mm sieve, dry to constant weight, record to 0.01 g.
  - Correct BOM for inorganic content by ashing a subset at 550°C for 5 h and applying ash-free conversion.
- Measurements:
  - Coarse and fine particulate organic matter (CPOM/FPOM) in grams.
- Calibration steps: None.
- Units: BOM stocks measured in grams.

## Data structure and metadata
- Data format: Flatbed CSV files.
- BOM data columns (10):
  - site_code: code of the sampling site
  - landuse: basin land-use
  - region: stream basin
  - time: before or after manipulation
  - month: collection month
  - reach: Experimental or Control site
  - replicate: replicate code
  - surber_area: area of the Surber sampler in m^2
  - cpom: coarse particulate organic matter (g)
  - fpom: fine particulate organic matter (g)

## Supporting documents and metadata
- DURESS_CU_site_description.csv: site description with 10 columns including
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment, etc.
- Survey campaigns referenced (WAWS Welsh Acid Water Survey, Plynlimon catchments, etc.) for context on data collection.

## Quality control and notes
- Calibration steps: None indicated.
- Quality control: Not explicitly described.
- Data discoverability: BOM data stored in CSV files with accompanying site description to aid interpretation; time frames and treatment conditions are clearly documented.