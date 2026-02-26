# DATA HEADER INFORMATION for Soil_carbon_stock.csv

## Overview
- Provides soil carbon stock importance and sensitivity to land management at depths 0-30 cm and 0-100 cm.
- Stocks are presented as either equivalent mass (SOC_Me_30, SOC_Me_100) or equivalent volume (SOC_Ve_30, SOC_Ve_100).
- Calculations are based on carbon content from a MIRS prediction model.
- Detailed calculations available in Manual_1_Classical_Survey.rtf, page 17, section 4.4.
- DOI and project context: ESPA Programme; Project P4GES (URLs provided).
- Acknowledgement required for the Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data structure and variables
- Site_id: P4GES site code; Variable Type = Text String; Unit unspecified.
- SOC_subplot: Subplot where the sample was collected; Variable Type = Categorical; values = S1, S2, S3, S4.
- SOC_Me_30: Soil carbon stock in equivalent mass at 30 cm; Variable Type = Numeric; Unit = Mg.ha-1.
- SOC_Me_100: Soil carbon stock in equivalent mass at 100 cm; Variable Type = Numeric; Unit = Mg.ha-1.
- SOC_Ve_30: Soil carbon stock in equivalent volume at 30 cm; Variable Type = Numeric; Unit = Mg.ha-1.
- SOC_Ve_100: Soil carbon stock in equivalent volume at 100 cm; Variable Type = Numeric; Unit = Mg.ha-1.

## Calculation and provenance
- All stock values are derived from carbon content predicted by the MIRS model.
- Full calculation details are documented in the referenced manual file.

## Usage notes and attribution
- Users can choose between mass-equivalent or volume-equivalent stocks and between depths (0–30 cm, 0–100 cm).
- Appropriate citation using the provided DOI and project information is required.
- Acknowledgement: Lab. des Radio Isotopes, Université d'Antananarivo for products derived from these data.