# DATA HEADER INFORMATION for Description_of_soil_profile.csv

## Overview
- Dataset records soil profile pit descriptions observed during field sessions.
- Associated program/project references: ESPA (Environmental Sample Programme) and P4GES.
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d’Antananarivo for products derived from these data.

## Dataset provenance and context
- Site_ID: P4GES site code; textual identifier.
- Horizon: Name of the soil horizon; textual.
- depth_cm: Depth of the soil horizon; numeric, in centimeters. Clarifies sampling depth (e.g., 0–10 cm means surface to 10 cm; 22–53 cm means 23 cm to 53 cm depth).
- color: Soil layer color using Munsell coding; textual.
- texture: Field-estimated soil texture; categorical (Clayey / Sandy / Sandy-Clayey / Silty-Clayey / Clay-sandy).
- structure: Observed soil structure; categorical.
- root_importance: Coverage percentage of roots in the soil layer; numeric (%).
- porosity: Percentage of small porosity holes in the soil layer; numeric (%).

## Data schema and units
- Site_ID: Text string; no unit.
- Horizon: Text string; no unit.
- depth_cm: Numeric; unit = cm.
- color: Text string; no unit.
- texture: Categorical; values as listed above.
- structure: Categorical; values as listed above.
- root_importance: Numeric; unit = %.
- porosity: Numeric; unit = %.

## Data quality and handling
- Missing data: Blank cells and NA indicate no available data.
- Metadata and data management considerations: Information implies reliance on field observations and potential need for consistent metadata from dataset originators.

## Reuse, governance, and implications for monitoring frameworks
- Data provenance and attribution are explicit; products derived require acknowledgement of the providing laboratory/institution.
- The dataset supports standardized capture of soil profile attributes, enabling comparability across sites for soil health monitoring.
- Practical considerations for monitoring: field-based measurements (horizon depth, color, texture, structure, root presence, porosity) feed into soil health indicators and trend analyses.

## Relevance for policy monitoring and decision-making
- Provides structured soil health indicators that can inform land management policies, agricultural support, and environmental health assessments.
- Highlights typical data challenges (metadata adequacy, data sharing considerations, and need for consistent data governance) that monitoring programmes must address to ensure data usefulness and transparency.