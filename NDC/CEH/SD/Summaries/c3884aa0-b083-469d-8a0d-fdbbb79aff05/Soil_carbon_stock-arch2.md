# DATA HEADER INFORMATION for Soil_carbon_stock.csv

## Overview
- Dataset on soil carbon stock importance and sensitivity to land management at two depths: 0-30 cm and 0-100 cm.
- Carbon stocks are provided in two representations: equivalent mass (SOC_Me_30, SOC_Me_100) and equivalent volume (SOC_Ve_30, SOC_Ve_100).
- Calculations derived from carbon content predicted by a MIRS model.
- Detailed calculation methodology available in Manual_1_Classical_Survey.rtf, page 17, section 4.4.
- Associated with ESPA programme and P4GES project; DOI provided; acknowledgement required for outputs derived from these data.

## Data Content and Variables
- Site_id: P4GES site code; Type: Text; Unit: not applicable; purpose: identify site.
- SOC_subplot: subplot where the sample was collected; Type: Categorical; Values: S1, S2, S3, S4.
- SOC_Me_30: soil carbon stock at 30 cm depth (mass equivalent); Type: Numeric; Unit: Mg.ha-1.
- SOC_Me_100: soil carbon stock at 100 cm depth (mass equivalent); Type: Numeric; Unit: Mg.ha-1.
- SOC_Ve_30: soil carbon stock at 30 cm depth (volume equivalent); Type: Numeric; Unit: Mg.ha-1.
- SOC_Ve_100: soil carbon stock at 100 cm depth (volume equivalent); Type: Numeric; Unit: Mg.ha-1.
- Note: There are references to field_materials_resources metadata in the header text; primary identifiers are Site_id and SOC_subplot.

## Calculation Source and Documentation
- Carbon content used to derive stocks comes from the MIRS prediction model.
- Full calculation details are documented in Manual_1_Classical_Survey.rtf (section 4.4).

## Provenance, Access, and Usage
- Programme: ESPA; Project: P4GES.
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Data handling notes: designed for standardized analysis and consistent reporting of environmental health indicators; aligned with typical monitoring workflows.

## Data Quality and Management
- Data are expected to undergo verification, quality assurance, cleaning, and transformation following established data handling practices.
- Outputs are prepared in clear formats (e.g., reports, maps, charts) and datasets are stored/uploaded to appropriate data portals.

## Practical Considerations for Analysts
- The dataset supports temporal and spatial monitoring of soil carbon stocks across depth horizons and two stock representations (mass and volume equivalents).
- Enables cross-site comparisons and integration with other environmental datasets to enhance monitoring value.
- Access to underlying data and metadata should be maintained to support reproducibility and policy evaluation.