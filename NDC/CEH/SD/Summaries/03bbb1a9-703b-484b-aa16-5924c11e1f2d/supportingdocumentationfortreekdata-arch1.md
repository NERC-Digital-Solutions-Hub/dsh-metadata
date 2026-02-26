# Saturated hydraulic conductivity, bulk density and soil organic carbon content from three paired upland woodland and grassland sites in northern England, July 2019-April 2021

## Aim and scope
- Describes measurements of saturated hydraulic conductivity (Ksat), bulk density (BD), and soil organic carbon content (SOC) from three paired upland woodland and grassland sites in northern England.
- Focuses on comparing woodland vs. pasture soil properties to assess potential impacts of upland tree planting as part of natural flood management.
- Samples collected from the upper 50 cm of the soil profile; data collected between July 2019 and April 2021 (COVID-19 disruptions noted).

## Experimental design
- Three sites with codes: JF (Jerusalem Farm, mature woodland), MW (Midgelden woods, ~15 years since planting), IF (Inchfield, newly planted <5 years).
- Each site has adjacent permanent grazed grassland (P) and woodland (T); both habitats sampled.
- 10 sample points per habitat per site, totaling 60 sample points.
- Random sampling within woodland and grassland; no samples within 20 m of habitat edges.

## Data collection and processing methods
- Bulk density: soil rings (5.3 cm diameter) extracted to 5 cm length; depths sampled at 2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm, 32.5–37.5 cm, 42.5–47.5 cm (dataset mid-points: 5, 10, 15, 25, 35, 45 cm).
- Saturated hydraulic conductivity (Ksat): measured with an Eijkelkamp 25-place permeameter; samples saturated in bulk density rings, readings taken at a known hydraulic gradient.
- SOC: measured by loss on ignition at 450 °C for 5 hours on the upper two depths; carbon factor 0.58 applied to convert organic matter to carbon; SOC expressed as percent of dry soil mass.
- Sample storage: stored at 4 °C before laboratory processing; processing occurred in subsequent months.
- Descriptive soil context: qualitative notes on soil type (silt, sand, structured clay) accompany measurements.

## Quality control
- Instrument-specific procedures followed per the Eijkelkamp manual for each measurement.
- BD mass determined to two decimal places.
- SOC: random replicates for 10% of samples; if replicate values within 10% of each other, mean used; if not, a third replicate used and mean calculated.

## Nature, units, and data structure
- Recorded variables and units:
  - Ksat: metres per day (m/day)
  - BD: grams per cubic centimetre (g/cm³)
  - SOC: percent (%)
  - Mid-point depth: centimetres (cm)
- Categorical identifiers:
  - Site: IF = Inchfield, MW = Midgelden, JF = Jerusalem Farm
  - Trees/Pasture: T = woodland, P = grassland
  - Soil type: descriptive terms
- Data columns (structure):
  - Site, Mid point depth, Trees/Pasture, Soil type, Bulk density, Ksat, SOC %, (and mid-point depth in cm)
  
## Context, usage, and limitations
- Purpose: enable comparisons of soil hydraulic properties and carbon content between woodland and pasture, informing understanding of upland tree planting and flood management implications.
- Depth coverage: measurements across multiple depths with some data gaps where shallow soils prevented sampling at all depths.
- COVID-19 impact noted as a factor delaying sample processing.
- Data are organized with clear metadata and units to support cross-site analyses, trend identification with depth, and potential integration with other datasets.

## Potential analyses and applications for analysts
- Compare Ksat, BD, and SOC between woodland and pasture across sites and depths to identify patterns related to tree planting age and land cover.
- Assess relationships between BD and SOC and between SOC and Ksat within and across sites.
- Model how soil properties vary with depth and how woodland maturation stage influences soil hydraulic properties.
- Integrate with flood management models to evaluate potential effects of upland afforestation on soil infiltration and storage characteristics.