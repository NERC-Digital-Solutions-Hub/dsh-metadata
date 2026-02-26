# DATA HEADER information for Standing_dead_wood_carbon_stock.csv

## Purpose and scope
- Documents the carbon stock of standing dead wood.
- Associated programmes: ESPA (Environment and Sustainability Programme) and P4GES.
- DOI provided for the dataset: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data structure and key fields
- site_ID
  - Type/Source: Text string
  - Description: P4GES site code
- DBH
  - Description: Diameter of the dead wood trunk at 130 cm height
  - Type/Unit: Numeric; centimeters
- Diam_base
  - Description: Diameter of the trunk at 30 cm height
  - Type/Unit: Numeric; centimeters
- Diam_top
  - Description: Estimated diameter at the top of the trunk
  - Type/Unit: Numeric; centimeters
- Height
  - Description: Height of the standing dead wood
  - Type/Unit: Numeric; meters
- Volume
  - Description: Calculated volume of standing dead wood
  - Type/Unit: Numeric; cubic meters
  - Calculation: Volume = (1/3) * π * H * (r1^2 + r2^2 + r1*r2) where H is total height, r1 is base radius, r2 is top radius
- Category
  - Description: Wood density category
  - Type/Unit: Categorical; values S (sound), I (intermediate), R (rotten)
- Density
  - Description: Wood density
  - Type/Unit: Numeric; (unit not explicitly specified in header)
- Carbon_stock
  - Description: Carbon stock of standing dead wood
  - Type/Unit: Numeric
  - Unit: Megagrams per hectare (Mg·ha^-1) indicated, though a note mentions a possible unit inconsistency with milligrams per hectare
- Notes
  - Special note: "means no data available" used to indicate missing values

## Data quality, provenance, and stewardship
- Data are drawn from established sources and subjected to verification, quality assurance, cleaning, and transformation.
- Outputs are presented in clear formats (e.g., reports, maps, charts).
- Datasets are stored and uploaded to appropriate portals as part of data stewardship.

## Outputs and dissemination
- Outputs likely include environmental health indicators and policy-relevant metrics related to standing dead wood carbon.
- Data are prepared for downstream use, including integration with other monitoring datasets and broader analyses.

## Practical considerations for analysts
- Ensure consistent interpretation of units, especially the Carbon_stock unit (Mg·ha^-1) versus any potential ambiguity with mg/ha.
- Apply standardised methods for volume calculation and categorical coding to maintain comparability over time.
- Link with underlying data where possible to enhance transparency and enable broader data reuse.

## Challenges and opportunities for enhancing value
- Challenge: Increasing the value of the standing_dead_wood_carbon_stock dataset by integrating it with related environmental datasets.
- Challenge: Facilitating broader access to the underlying data used to generate final outputs.