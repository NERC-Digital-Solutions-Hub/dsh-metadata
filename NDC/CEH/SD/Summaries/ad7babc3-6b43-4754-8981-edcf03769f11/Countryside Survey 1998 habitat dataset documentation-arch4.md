# Broad Habitat Area Estimates by Land Class for Great Britain 1998

- National estimates of Broad Habitat stock for 1998 derived from the 2007 ITE Land Classification, with total area (000s ha) per Broad Habitat and Land Class, including 95% confidence intervals (lower and upper estimates). Freshwater habitats were analyzed with a different statistical model.
- The dataset is based on Countryside Survey fieldwork conducted mainly in 1998 (some sites in 1999), often referred to as Countryside Survey 2000.

## Data Contents and Formats

- CS1998_Broad_Habitat_Stock.csv
  - YEAR: Year of survey
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad Habitat description
  - LAND_CLASS_AREA: Total area of the Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha) (negative values to be treated as 0)
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)

- CS1998_stock.tif
  - 1 km pixel raster where each pixel band corresponds to a Broad Habitat class, providing the mean percentage habitat presence within each 1 km survey square for the sampled Land Class strata.
  - Band mappings indicate how Broad Habitat codes map to raster bands (e.g., Broad Habitat 1/2 mapping, and so on across bands 2–17).

- Spatial Reference
  - Pixel size: 1 km
  - Coordinate system: British National Grid (OSGB36), Transverse Mercator
  - Extent: Great Britain

## Methodology and Provenance

- Data produced from Countryside Survey 1998 field survey data (mainly 1998; some sites 1999) and linked to the 2007 ITE Land Classification for national estimates.
- Land Class and Broad Habitat classifications follow Bunce et al. (ITE Land Classification) with supporting definitions in Jackson (2000) and related literature.
- Freshwater habitats analyzed with a separate statistical approach from other habitats.
- Negative MEAN_ESTIMATE values are to be treated as zero.
- National estimates are provided per Land Class and Broad Habitat, with 95% confidence intervals (LOWER_ESTIMATE and UPPER_ESTIMATE).

## Data Quality, Usage Notes, and Governance

- All uses require acknowledgement of Countryside Survey data owned by NERC–Centre for Ecology & Hydrology.
- Data cover Great Britain and reflect 1998 field data and 2007 Land Classification mapping; considered historical baseline data.
- Metadata includes explicit notes on data origins, classification mappings, and statistical modeling differences for freshwater habitats.
- Potential considerations for data leaders:
  - Data lineage from field survey to final estimates and the Land Classification crosswalk.
  - Handling of negative MEAN_ESTIMATE values in analyses (set to zero).
  - Ensuring proper metadata availability for proper interpretation and recombination with other datasets.
  - Awareness of broader data governance context, including licensing and acknowledgment requirements.

## Access, Usage, and Licensing

- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey ©; All rights reserved.
- Use of the data should reference the Countryside Survey project and related publications (see references).

## References and Related Resources

- Carey et al. (2008) Countryside Survey: UK Results from 2007
- Scott (2007) CS Technical Report No. 4/07 – Statistical Report (generation of national estimates from 1 km survey squares)
- Bunce et al. (ITE Land Classification of Great Britain 2007)
- Jackson (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification
- Additional Countryside Survey project pages and methodological documents (as listed in the references)