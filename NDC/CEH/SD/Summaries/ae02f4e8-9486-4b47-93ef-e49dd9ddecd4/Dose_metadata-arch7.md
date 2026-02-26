A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Overview
- Metadata describing a reference-site study in the Chernobyl Exclusion Zone, focusing on radionuclide and stable element data and estimated dose rates to biota.
- Published by the NERC Environmental Information Data Centre; includes data files intended for GIS-based mapping and analysis.
- Data are organized to support spatial visualization of dose rates by radionuclide and by species, suitable for map-based data products and end-user exploration.

## Data files and structure
- Biota_external_dose.csv
- Biota_internal_dose.csv
- Biota_total_dose.csv
- Biota_total_dose_per_radionuclide.csv
- Common structure across files includes:
  - Radionuclide: Cs-137, Sr-90, Am-240, Pu-239, Pu-240 or Pu-238
  - Explanation: description of the radionuclide or species context
  - Units: microGy h-1 for External_Dose_Rate (and related dose-rate measures)
  - External_Dose_Rate_microGy_h-1: statistical data fields (Mean, Variance, 5th/95th Percentile, Median, Min, Max, 25th/75th Percentile)
  - The dataset provides dose-rate data both external and internal, and total dose, with total dose per radionuclide

## Radionuclides covered
- Cs-137
- Sr-90
- Am-241
- Pu-239
- Pu-240 or Pu-238
- Data include external dose-rate statistics (microGy/h) and, where applicable, internal and total dose considerations

## Biota (species groups) represented
- Pinus sylvestris (pine) - wood
- Agrostis gigantea (grass)
- Lumbricus terrestris (earthworm)
- Apodemus agrarius (mouse)
- Sorex araneus (shrew)
- Sorex minutus (shrew)
- Apodemus flavicollis (mouse)
- Microtus agrestris and Microtus spp. (mouse)
- Muscardinus avellanarius (doormouse)
- Myodes glareolus (vole)
- Bombina bombina (toad)
- Bufo bufo (toad)
- Pelobates fuscus (toad)
- Rana arvalis (frog)
- Bombus and Xylocopa spp. (bee)
- Additional species groups are indicated but not exhaustively listed in the metadata excerpt

## GIS-relevant aspects and potential uses
- Enables map-based visualization of dose rates by radionuclide and by species, supporting spatial risk assessment and stakeholder communication.
- Allows comparison of external, internal, and total dose components across species and radionuclides.
- Supports layering with other geospatial data (habitat, land cover, boundaries of the Chernobyl Exclusion Zone) for contextual analysis.

## Data quality, standards, and integration considerations
- Data are assembled from multiple sources and datasets, requiring careful harmonization of:
  - Data standards and units (e.g., consistently using microGy h-1)
  - Spatial resolution and geographic alignment across biota and radionuclide datasets
  - Data cleaning and transformation to enable reliable GIS visualization
- Large or complex datasets may need packaging into manageable chunks for GIS workflows
- Consistent metadata and documentation are essential to enable correct interpretation of the dose-rate statistics

## Provenance and access
- Source: A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates
- Publisher: NERC Environmental Information Data Centre
- DOI: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4
- Data are intended for use as map-ready or map-supporting data products, with detailed column explanations included in the file headings

## Practical notes for GIS specialists
- Plan for integrating these CSVs with GIS layers that represent location, habitat, and exposure context to maximize the value of map-based visuals.
- Verify units and statistical fields (mean, percentiles, min/max) during data ingestion to ensure accurate representation in maps and analyses.
- Engage with end users to validate which species and radionuclides are most relevant for visualization, and iteratively refine the mapping approach based on feedback.