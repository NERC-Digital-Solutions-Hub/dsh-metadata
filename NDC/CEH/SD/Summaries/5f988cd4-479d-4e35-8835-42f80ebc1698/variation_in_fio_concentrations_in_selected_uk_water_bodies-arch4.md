# Disease_distribution_data_UK_standing_waters.csv

## Purpose and context
- Investigates the spatial distribution of fecal indicator organisms (FIOs) in standing waterbodies and the drivers behind their presence.
- Focuses on UK Hydroscapes with contrasting landcover to understand how landscape influences FIOs.
- Aims to inform water quality, ecology, and potential human health implications for recreational users.

## Study areas and sampling scope
- Three Hydroscapes: Greater Glasgow (urban), Norfolk (agricultural), Cumbria (upland/pastoral).
- In each Hydroscape, 18 water bodies sampled to cover a gradient of size, productivity, hydrological connectivity, and ecological quality.
- Sampling occurred in Spring, Summer, and Autumn across 2016 or 2017.
- Time of day standardized: samples collected 3 hours after sunrise to align with UAV exposure studies.

## Sampling methodology and laboratory analysis
- Water bodies sampled at three spatially dispersed locations per lake (≈100 m apart); shallow water (<0.5 m) sampled by wading.
- At each location, three subsamples were collected (≈5 m apart) for a total of nine samples per water body per visit.
- Total samples: 1,278 unique samples across all water bodies and seasons.
- E. coli measurement:
  - Water collected ~30 cm below surface into sterile bottles (approx. 100 ml total volume used for each filtration run, with additional 10 ml and 1 ml volumes).
  - Samples stored at 4°C and processed within 6 hours of collection.
  - Filtration through 0.45-µm membranes onto MLGA agar; incubated at 37°C; colonies counted after 24 hours.
  - Results reported as colony forming units (CFU) per 100 ml.
- Additional measurements: heterotrophs (Hetero) CFU per 100 ml.

## Data structure and metadata
- Appendix describes field names for Disease_distribution_data_UK_standing_waters.csv:
  - Hydroscape: landscape category (Greater Glasgow, Cumbria, Norfolk)
  - season: spring, summer, autumn
  - site: focal water body name
  - sample: spatial sample code (1–3)
  - rep: sub-sample label (a–c)
  - Ecoli: E. coli concentration (CFU per 100 ml)
  - Hetero: heterotrophs concentration (CFU per 100 ml)

## Data lifecycle and governance (implications for Data Leaders)
- Longitudinal design across multiple seasons and diverse landscapes supports understanding drivers and patterns in FIO distribution.
- Well-defined sampling protocol and timing enhances comparability across sites and seasons.
- Metadata is explicitly structured, facilitating discoverability and re-use of the dataset.
- Large, multi-site, multi-season dataset offers opportunities for cross-site analysis, benchmarking, and informing water quality management.
- Clear documentation in the appendix aids data stewardship, interoperability, and potential integration with other datasets.

## Considerations and potential use cases
- Suitable for analyses of spatial drivers of FIO contamination and the impact of landcover types on water quality.
- Useful for informing public health risk assessments related to recreational water use.
- Can support policy discussions on monitoring programs and data standardization across regions.
- The dataset structure supports replication, meta-analyses, and integration with environmental variables (e.g., hydrology, land use) for broader ecological studies.