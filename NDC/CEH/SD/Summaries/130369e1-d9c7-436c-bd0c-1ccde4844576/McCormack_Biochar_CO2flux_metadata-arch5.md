# Mesocosm CO2 Flux Dataset

- The dataset records CO2 flux measurements from mesocosms with multiple experimental factors, including biochar presence, crop treatment, and soil texture, across time and space within an enclosure.
- Measurements are taken under light and dark conditions using an infrared gas analyzer (IRGA), with a derived photosynthetic rate calculated from the difference between light and dark fluxes.

## Key Variables and Meaning

- Pot_number: unique identifier for each individual mesocosm.
- Block (biochar): indicates presence (+) or absence of 2% biochar (w/w) in soil.
- Crop_type: treatment type—Barley, Ryegrass, or Unvegetated.
- Soil_texture: soil texture category—SC (sandy clay), SZL (sandy silt loam), or CL (clay loam).
- Month: calendar month of sampling (1=Jan, 2=Feb, …).
- Year: year of sampling.
- Day_of_year: numerical day of year (1–365) for the sampling date.
- Block (spatial): spatial block within the enclosure; in a fully factorial design, one replicate per treatment combination across four spatial blocks.
- Light_flux: CO2 flux rate during light exposure (g CO2 m-2 h-1); positive = net efflux, negative = net uptake.
- Dark_flux: CO2 flux rate during dark exposure (g CO2 m-2 h-1); positive = net efflux, negative = net uptake.
- Photosynthes: photosynthetic rate within the mesocosm (g CO2 m-2 h-1), derived by subtracting dark_flux from light_flux.
- Note: '.' indicates a missing sample.

## Data Quality and Standards Considerations

- Missing data: '.' used for no sample; standardize missing value coding across the dataset.
- Units and method: specify units (g CO2 m-2 h-1) and measurement method (IRGA) in metadata; ensure consistency across records.
- Derived vs raw data: Photosynthes is a derived variable; clearly document the calculation method and ensure availability of raw light_flux and dark_flux for reproducibility.
- Time representation: Month/Year/Day_of_year encoding could be consolidated into a standard date field (e.g., sampling_date) to improve interoperability across systems.
- Naming consistency: there are two separate fields named Block (biochar presence and spatial block); rename to reduce ambiguity (e.g., Biochar_Presence and Spatial_Block) and clearly document both concepts in the metadata.

## Data Governance and Stewardship Recommendations

- Data dictionary and metadata: provide a comprehensive data dictionary, a README, and clear provenance detailing experimental design (fully factorial layout, four spatial blocks).
- Standard vocabularies: adopt controlled vocabularies for Crop_type and Soil_texture to facilitate cross-dataset discovery and interoperability.
- Data quality assurance: implement QA steps to validate units, value ranges (e.g., plausible flux values), and consistency between light_flux, dark_flux, and Photosynthes.
- Versioning and lineage: track dataset versions, documents any preprocessing or transformations, and record data updates or corrections.
- Discovery and sharing: prepare the dataset for portal/catalogue submission with machine-readable metadata, data access notes, and potential embargo information if applicable.
- Data retention and governance: specify policies for keeping raw data vs. processed derivatives, and outline procedures for updating or retracting data as needed.

## Practical Next Steps for Data Stewards

- Audit variable names for clarity and rename duplicates (e.g., separate Biochar_Presence and Spatial_Block).
- Validate data types, enforce consistent encodings for categorical fields, and standardize missing-value conventions.
- Create and attach a detailed metadata package (data dictionary, samplingDate field, measurement methods, and unit definitions).
- Ensure reproducible derivations (document Photosynthes calculation) and provide both raw and derived data where possible.
- Establish data sharing plan: update data portals/catalogues with discoverable metadata, and define access conditions and update routines.