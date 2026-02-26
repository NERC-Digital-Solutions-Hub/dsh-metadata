# DATA HEADER INFORMATION for Soil_carbon_stock.csv

## Overview
- Presents carbon stock importance and sensitivity to land management at two soil depths: 0-30 cm and 0-100 cm.
- Carbon stocks are provided as both equivalent mass and equivalent volume, calculated from carbon content via a MIRS prediction model.
- Detailed calculations are documented in Manual_1_Classical_Survey.rtf, page 17, section 4.4.

## Data structure and fields
- Site_id: P4GES site code; type Text String. Unit not specified.
- SOC_subplot: subplot where the sample was collected; categorical; values S1, S2, S3, S4.
- SOC_Me_30: soil carbon stock in equivalent mass at 30 cm depth; Numeric; unit Mg.ha-1.
- SOC_Me_100: soil carbon stock in equivalent mass at 100 cm depth; Numeric; unit Mg.ha-1.
- SOC_Ve_30: soil carbon stock in equivalent volume at 30 cm depth; Numeric; unit Mg.ha-1.
- SOC_Ve_100: soil carbon stock in equivalent volume at 100 cm depth; Numeric; unit Mg.ha-1.
- Notes: Field_material s_ressources are not populated in the header (empty in the provided data).

## Data provenance and references
- Programme: ESPA; Project: P4GES.
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data quality and usage notes
- Calculations rely on the MIRS prediction model for carbon content.
- Full calculation details available in Manual_1_Classical_Survey.rtf (section 4.4, page 17).
- Data are formatted for GIS use as map-ready carbon stock indicators (mass and volume equivalents) across depths and subplot locations.
- Be mindful of potential data gaps where certain fields or materials resources are not populated.