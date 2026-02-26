# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Purpose and data scope
- Provides metadata for two datasets describing radionuclide and stable element data, and estimated dose rates from a reference site in the Chernobyl Exclusion Zone.
- Data are archived in the NERC Environmental Information Data Centre (with a DOI for persistent access).
- Datasets cover biota and soil samples collected from the site, including location, timing, and concentration measurements.

## Datasets and key fields
- Biota_radionuclide_data.csv
  - Sample identifiers: Chornobyl_Center_ID; sample is linked to a biota Latin/Common name.
  - Temporal and spatial data: Date_biota_sampled (dd/mm/yyyy); Latitude and Longitude in WGS84.
  - Biological metadata: Age_of_biota, Sex_of_biota, Fresh_mass_of_biota_in_grams, Individuals_in_sample.
  - Radionuclide measurements (fresh mass basis): Cs-137_Bq_per_kg_FM, Sr-90_Bq_per_kg_FM, Am-241_Bq_per_kg_FM, Pu-239/240_Bq_per_kg_FM, Pu-238_Bq_per_kg_FM.
  - Derived/relational metrics: Cs-137_CR, Sr-90_CR, Am-241_CR, Pu_CR (concentration ratios).
  - Notes on units and applicability are provided; many fields show n/a where data are not available.

- Soil_radionuclide_data.csv
  - Sample/site metadata: N (laboratory sample identifier), GP_Point (sampling site), Latitude_WGS84, Longitude_WGS84, Date_Soil_sampled.
  - Dose-rate measurements: Dose_rate_microSv_per_hour_measurement_1 through 10 (ambient site measurements).
  - Soil mass data: Dry_mass_of_soil_in_grams.
  - Radionuclide activity (per dry mass or per sample): Cs-137_Soil_Bq_per_sample_DM, Am-241_Soil_Bq_per_sample_DM, Sr-90_Soil_Bq_per_sample_DM, Pu-239/240_Soil_Bq_per_sample_DM, Pu-238_Soil_Bq_per_sample_DM, and corresponding Cs-137_Soil_Bq_kg_DM, Sr-90_Soil_Bq_kg_DM, Am-241_Soil_Bq_kg_DM, Pu-239/240_Soil_Bq_kg_DM, Pu-238_Soil_Bq_kg_DM.
  - Uncertainty indicators: error_..._Bq_per_Sample_DM_P and similar P values (e.g., 0.95) indicating confidence intervals.
  - Notes indicate which fields are 95% confidence intervals and where data may be missing or not applicable.

## Metadata quality and standards
- Thorough, field-level documentation for each column, including:
  - Clear explanations and units (e.g., Bq per kg fresh mass, Bq per sample dry mass, µSv/h for dose rates).
  - Geographic coordinates using the World Geodetic System 84 (WGS84).
  - Time formats specified (dd/mm/yyyy) and sample identifiers tied to sampling events.
  - Explicit uncertainty reporting for several soil measurements.
- Data housed in a formal data centre (NERC Data Centre) with a DOI, enabling citation, versioning, and discoverability.
- Some fields are marked as not available (n/a) or have formatting inconsistencies, signaling opportunities for data cleaning and harmonization.

## Access, governance, and reuse considerations
- Location within a recognized environmental data centre supports governance, provenance, and long-term stewardship.
- DOI linkage enhances traceability and reuse across projects and networks.
- Structure supports cross-linking between biota and soil data, enabling integrated analyses and product development.

## Relevance to Data Leaders' aims
- Systems thinking: two linked datasets (biota and soil) with aligned metadata facilitate an end-to-end view of radionuclide dynamics and dose rates.
- User needs and co-ownership: rich metadata supports reuse by policy colleagues and researchers; clear identifiers and location data support collaboration and cross-network sharing.
- Data availability and gaps: documentation highlights data coverage (sample types, measurement types) and gaps (n/a fields), aiding prioritization of data collection or curation efforts.
- Data quality and lifecycle: explicit units, measurement types, and uncertainties support proper data quality assessment, transformation, and updates.
- Community and standards: centralized repository with standardized units and coordinates; potential for broader community use and harmonization with other environmental datasets.

## Practical implications for data strategy and decision-making
- Maintain and enforce consistent data standards across biota and soil datasets (units, time formats, coordinate systems).
- Act on missing values and ensure comprehensive uncertainty reporting where possible to improve reliability of downstream analyses.
- Leverage the DOI and data centre for governance, access controls, versioning, and collaboration with external partners.
- Consider integrating these datasets with additional reference-site data to strengthen cross-site comparisons and dose-rate modelling.