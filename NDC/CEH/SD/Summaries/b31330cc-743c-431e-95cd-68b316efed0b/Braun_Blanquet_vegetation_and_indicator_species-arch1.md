# DATA HEADER INFORMATION for Braun_Blanquet_vegetation_and_indicator species.csv

- Purpose: Records the percent cover of indicator species using the Braun-Blanquet scale.
- Data provenance and references:
  - DOI: https://doi.org/10.5285/b31330cc-743c-431e-95cd-68b316efed0b
  - Programme: ESPA; Project: P4GES
  - Acknowledgement required: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data
  - Related documentation: Manual 1_Classical_Survey
- Data context:
  - The dataset uses a site code (P4GES WP4 site code) as site_id
  - Indicates presence and characteristics of indicator species across sites
  - Includes taxonomic and vernacular names, family, life form, and abundance

## Key fields and data types

- site_id
  - Information: P4GES WP4 site code
  - Variable Type: Text String
  - Unit: .
  - Field materials/resource s: .
- Scientific_name
  - Information: Scientific name of the inventoried species
  - Variable Type: Text String
  - Unit: .
  - Field materials/resource s: botanist
- Local_name
  - Information: Vernacular/local name
  - Variable Type: Text String
  - Unit: .
  - Field materials/resource s: botanist
- Family
  - Information: Scientific family of the inventoried species
  - Variable Type: Text String
  - Unit: .
  - Field materials/resource s: botanist
- Life_form
  - Information: Life form category
  - Variable Type: Categorical
  - Unit ok: Fern/Shrub/ Herb/Grass/ Vine/Tree
  - Field materials/resource s: botanist
- Percent_cover
  - Information: Degree of dominance of the inventoried species
  - Variable Type: Numeric
  - Unit ok: %
  - Field materials/resource s: numeric scale
- Indicator_species
  - Information: Whether the species is a specific indicator of land use
  - Variable Type: Binomial
  - Unit ok: Yes/No
  - Field materials/resource s: NA
- B_B_scale
  - Information: Braun-Blanquet scale value category
  - Variable Type: Categorical
  - Unit ok: 0 Not present; 1 1-5% cover; 2 5-25% cover; 3 25-50% cover; 4 50-75% cover; 5 75-95% cover; 6 >95% cover
  - Field materials/resource s: 

## scale and measurement details

- The Braun-Blanquet scale categories (B_B_scale) map to percent cover ranges, enabling standardized comparisons of species abundance
- Percent_cover provides a direct numeric measure of dominance, aligned with the Braun-Blanquet categorization

## Data quality, access, and usage notes

- Data are designed to be trackable and citable via DOI, with clear provenance to ESPA/P4GES
- Metadata fields indicate source references (botanist) for taxonomic and vernacular information
- Documentation references (Manual 1_Classical_Survey) support methodological context
- Users should align analyses with the indicator_species flag to identify land-use indicators and consider Life_form when aggregating across habitats

## Practical considerations for analysts

- Use site_id to combine across sites for spatial analyses or site-level comparisons
- Leverage Scientific_name and Local_name for taxonomic crosswalks; ensure consistency with life-form categories
- Interpret Percent_cover alongside B_B_scale to assess both precise and categorical abundance
- Employ Indicator_species to filter for land-use indicator species in modeling or reporting
- Cite the DOI and project/program URLs; acknowledge the data source as required

## Citation and related resources

- DOI: https://doi.org/10.5285/b31330cc-743c-431e-95cd-68b316efed0b
- Programme: ESPA; Project: P4GES
- Related materials: Manual 1_Classical_Survey
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo for derived products