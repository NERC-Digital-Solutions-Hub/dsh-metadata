# DATA HEADER INFORMATION for Description_of_soil_profile.csv

## Overview
- Records soil profile pit descriptions collected during field sessions.
- Linked to Manual_1_Classical_Survey (page 13, section 2.3.3.2).
- Programme: ESPA; Project: P4GES.
- Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.

## Data schema (fields)
- Site_ID: P4GES site code. Type: Text String. Unit: (none)
- Horizon: Name of the soil horizon. Type: Text String. Unit: (none)
- depth_cm: Depth of the soil horizon. 0–10 means surface to 10 cm; 23–53 means sampled between 23 cm and 53 cm. Type: Numeric. Unit: cm
- color: Soil layer colour according to Munsell code. Type: Text String. Unit: (none)
- texture: Soil texture estimated in the field. Type: Categorical. Values: Clayey, Sandy, Sandy-Clayey, Silty-Clayey, Clay-sandy
- structure: Observed soil structure. Type: Categorical. Unit: (none)
- root_importance: Coverage percentage of roots observed in the soil layer. Type: Numeric. Unit: %
- porosity: Percentage of small porosity holes observed in the soil layer. Type: Numeric. Unit: %

Notes
- Blank cells and NA mean no data available.

## Data quality and standardisation for monitoring
- Data should be verified, quality assured, cleaned, and transformed as needed.
- Used to analyse environmental health by comparing descriptors against standards.
- Outputs are presented in clear formats (reports, maps, charts).
- Datasets should be stored and uploaded to the appropriate data portals.

## How this supports environmental monitoring
- Enables standardized documentation of soil profile properties over time.
- Facilitates comparisons across sites and depths to assess soil health trends.
- Can be integrated with other environmental datasets (e.g., land use, moisture) for broader health indicators.

## Governance, provenance, and access
- Clear provenance via field sessions; use of P4GES site codes.
- Acknowledgement requirements for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Data accessibility considerations align with goals to enable broader access to underlying data.

## Challenges and opportunities for analysts
- Increase value by combining soil profile data with related environmental datasets.
- Improve access to underlying data to support transparency and re-use.