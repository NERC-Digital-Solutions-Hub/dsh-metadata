# Supporting documentation for 09-Animal_Foodstuff_Gamma_Spectrometry.csv

## Overview
- Dataset provides gamma spectrometry results for animal-derived foods, with sample metadata and radionuclide activity concentrations (Ra-226, Ra-228, Cs-137, K-40) on a fresh mass basis.
- Includes uncertainties and detection limits (ISO 11929) and notes on radioactive equilibrium where relevant.
- Fields cover sample identity, description, location, collection date, sample size, and measured values.

## Key fields (GIS-focused interpretation)
- Sample_Code: unique sample identifier.
- Sample_Type: general food-group description.
- Location: sampling location name (geocoding candidate for mapping).
- Collection_Date: date of sample collection (temporal mapping).
- Sample_Description: analyzed portion of the organism.
- Sample_size: amount analyzed (kg fresh matter or L for milk) for normalization in maps.
- Ra-226_Bq/kg_fm, Ra-228_Bq/kg_fm, Cs-137_Bq/kg_fm, K-40_Bq/kg_fm: activity concentrations (Bq per kg fresh mass or Bq per L for milk).
- Unc_Ra-226_Bq/kg_fm, Unc_Ra-228_Bq/kg_fm, Unc_Cs-137_Bq/kg_fm, Unc_K-40_Bq/kg_fm: uncertainties associated with the activity concentrations.
- Detection_Limit_Ra-226_Bq/kg_fm, Detection_Limit_Ra-228_Bq/kg_fm, Detection_Limit_Cs-137_Bq/kg_fm, Detection_Limit_K-40_Bq/kg_fm: detection limits per ISO 11929; blanks indicate non-detects.
- Notes on non-detects: where blank, concentration is below the detection limit.
- Equilibrium notes: Ra-226 in equilibrium with Pb-214 and Bi-214; Ra-228 in equilibrium with Ac-228.

## Spatial and temporal considerations
- Location enables geocoding for point or area-based mapping.
- Collection_Date enables temporal analysis and trend mapping.
- Units vary by sample type (kg fresh matter or L for milk); ensure consistent unit handling in GIS workflows.

## Data quality and standards
- Detection limits adhere to ISO 11929, supporting comparability across samples.
- Uncertainties provided for each measured concentration; useful for uncertainty visualization.
- Non-detects represented by blank fields; implement consistent handling in maps (e.g., suppression, censoring, or below-detection-symbols).
- Be mindful of occasional formatting inconsistencies in field names (e.g., spacing) when importing into GIS tools.

## How to use in GIS
- Geocode Location to create point datasets or join with regional shapefiles for choropleth/heatmaps.
- Visualize radionuclide concentrations by location and date; create multi-layer maps for different isotopes.
- Represent uncertainties and detection limits as separate layers or as error bars/patches on data points.
- Filter by Sample_Type or Collection_Date to focus on specific foods or timeframes.
- Treat non-detects appropriately to avoid misleading high-value representations.

## Practical integration tips
- Standardize field names and harmonize units during import.
- Preserve ISO 11929 detection limits and uncertainty fields for accurate interpretation.
- Maintain equilibrium-related notes for contextual analysis of Ra isotopes.

## Example use cases
- Map spatial distribution of Cs-137 and Ra isotopes in animal-derived foods across regions.
- Create time-series maps for a given location to show change in radionuclide levels.
- Compare activity concentrations across different sample types (e.g., milk vs. meat products) within the same region.