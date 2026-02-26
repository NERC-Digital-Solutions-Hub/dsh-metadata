# Supporting documentation for dataset: Saturated hydraulic conductivity, bulk density and soil organic carbon content from three paired upland woodland and grassland sites in northern England, July 2019-April 2021

## Overview
- Dataset measuring saturated hydraulic conductivity (Ksat), bulk density, and soil organic carbon (SOC) content from three paired upland woodland and grassland sites in northern England.
- Samples collected from the upper 50 cm of soil at random points; 60 total sample points (3 sites × 2 land uses × 10 points).
- Aimed to compare woodland and pastoral soils to infer potential impacts of upland tree planting for natural flood management.
- Sampling occurred between July 2019 and April 2021 (COVID-19 disruption noted); data processing occurred in subsequent months.
- Site coordinates provided for each location; work supported by Natural Environment Research Council’s NFM programme.

## Experimental design
- Sites (coded): JF (Jerusalem Farm, mature woodland), MW (Midgelden woods, ~15 years since planting), IF (Inchfield, newly planted <5 years).
- At each site, permanent grazed grassland (P) adjacent to woodland (T); both habitats sampled.
- Random sampling within woodland and grassland; edge exclusion: no samples within 20 m of woodland or grassland edge.
- Sampling plan: 10 points per habitat at each site, totaling 60 sample points.
- Depths: samples collected at depths corresponding to mid-points of 5, 10, 15, 25, 35, and 45 cm (depth intervals approximately 2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm, 32.5–37.5 cm, 42.5–47.5 cm).

## Data collection methods
- Bulk density rings (5.3 cm diameter) used to collect 5 cm long samples; depths sampled as described above.
- Samples stored at 4°C prior to laboratory processing.
- Saturated hydraulic conductivity measured with an Eijkelkamp 25-place permeameter; readings taken after saturation under a known hydraulic gradient.
- Bulk density determined gravimetrically via oven-drying at 105°C for 24 hours.
- Soil organic carbon content determined by loss on ignition at 450°C for 5 hours; assume 58% carbon in organic matter (conversion factor 0.58); users may convert back if needed.
- Ancillary context: a descriptive, visual soil interpretation recorded (e.g., texture notes).

## Quality control
- Permeameter procedures followed per Eijkelkamp manual; measurements conducted in School of Geography, University of Leeds.
- Mass accuracy: values recorded to two decimal places (grams).
- SOC: 10% of samples have random replicates; if replicate values are within 10%, the mean is used; if not, a third replicate is measured and the mean of all replicates used.

## Nature and units of recorded values
- Saturated hydraulic conductivity: metres per day (Ksat, m/day).
- Bulk density: grams per cubic centimetre (g/cm³).
- Soil organic carbon: percent of dry soil mass (% SOC; by default expressed as SOC%).
- Mid-point soil depth: centimetres (cm).

## Details of data structure
- Site: IF = Inchfield, MW = Midgelden, JF = Jerusalem Farm.
- Mid point depth: 5, 10, 15, 25, 35, 45 cm (representing 5 cm increments with corresponding mid-points).
- Trees/Pasture: T = woodland, P = grassland.
- Soil type: short descriptive terms.
- Bulk density: numeric, two decimals.
- Ksat: numeric.
- SOC %: numeric, two decimals.
- Mid point depth (cm): numeric (redundant column for clarity).

## Data considerations and limitations
- COVID-19 disruption affected sampling timeline (2019–2021).
- Some depths at certain sample points may be missing where shallow soils prevented sampling at all depths.
- Data reflect a comparative study of woodland versus pasture soils adjacent to upland sites; applicability may depend on local conditions and site history.

## Relevance for data stewardship and reuse
- Clearly labeled site codes, coordinates, habitats, and depth structure support discoverability and alignment with metadata standards.
- Documented methods, instruments, QA/QC procedures, and conversion factors support reproducibility and appropriate reuse.
- Users should reference the site-specific context (age of woodland, site pairings) and the intended comparative purpose (impacts of upland tree planting on hydraulic properties, density, and SOC).
- Suggested metadata enhancements for future stewardship: implement explicit date ranges for each sample, confirm exact GPS coordinates for all sampling points, and include full method references for the permeameter and SOC protocols used.