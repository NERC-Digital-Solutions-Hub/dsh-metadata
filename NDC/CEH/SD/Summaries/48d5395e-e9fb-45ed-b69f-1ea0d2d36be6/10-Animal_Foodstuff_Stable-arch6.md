# Supporting documentation for 10-Animal_Foodstuff_Stable.csv

## Purpose
- Provides a data dictionary for the 10-Animal_Foodstuff_Stable.csv dataset.
- Documents how stable element concentrations in animal foodstuffs are recorded and interpreted.

## Data structure overview
- Each record includes:
  - Sample_Code: unique sample identifier.
  - Sample_Type: broad description of the sample group (foodstuff type).
  - Location: site where the sample was collected.
  - Sample_Description: part of the organism analyzed.
  - Collection_Date: date of collection (format: dd-mm-yyyy).
  - Sample_size: amount analyzed; units are g fresh matter for solids or mL for milk.
- For each element, the dataset captures concentration data along with quality metrics.

## Measured elements and related fields
- Elements included (with concentration, uncertainty, and detection limit fields):
  - Cs (stable cesium)
  - Sr (stable strontium)
  - K (stable potassium)
  - Na (stable sodium)
  - Ca (stable calcium)
  - Mg (stable magnesium)
  - P (stable phosphorus)
  - Pb (stable lead)
  - U (stable uranium)
  - Th (stable thorium)
- For each element, the typical fields are:
  - Element_mg/kg_fm or Element_mg/kg_fm (or mg/L for milk) for concentration on a fresh mass basis
  - Unc_Element_mg/kg_fm for the combined measurement uncertainty
  - Detection_Limit_Element_mg/kg_fm for the detection limit
- Some elements show multiple subfields (e.g., Na, Mg, and others listed with numbered subfields) reflecting data structure variations in the table.

## Measurements and units
- Solids (foodstuffs): concentration units are mg per kg fresh mass (mg/kg_fm).
- Milk: concentration units are mg per litre (mg/L).
- Sample_size units specify how the measurement relates to concentration (g fresh matter or mL for milk).

## Non-detects and data quality indicators
- Blank concentrations indicate that the measured concentration was below the detection limit.
- Uncertainty fields quantify the combined uncertainty of each concentration measurement.
- Detection limit fields indicate the threshold above which a concentration could be confidently measured.
- Some field names and formatting in the Na, Pb, U, and Th sections show irregular subfield numbering, but the intended interpretation remains consistent: non-detects are noted as blanks, with corresponding detection limits and uncertainties provided where available.

## Usage guidance for data interpretation
- Use Collection_Date to track temporal aspects of samples.
- Refer to Sample_Type and Sample_Description to understand the biological/source context of each sample.
- Interpret concentration values with their Unc fields to assess measurement precision.
- Treat blank concentration fields as non-detects, using the corresponding Detection_Limit to understand the reporting threshold.
- For milk samples, rely on mg/L units; for all other samples, mg/kg_fm units apply.