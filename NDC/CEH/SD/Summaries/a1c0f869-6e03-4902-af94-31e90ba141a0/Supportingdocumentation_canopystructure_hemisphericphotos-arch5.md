# Supporting documentation

## Overview
- Dataset comprises hemispherical photographs of canopy structure in 0.5 ha permanent sample plots, intended for leaf area index (LAI) estimation at the plot level.
- Context: Nordeste project in northeast Brazil (Caatinga biome) conducted by Brazilian and UK researchers to address decades of neglect in biodiversity and ecosystem-function research; LAI related to biomass, phenology, growth, water/nutrient use, carbon stocks, biodiversity, and ecosystem modelling.
- Photographs were taken between March 2017 and August 2019 to support LAI variation assessment across Caatinga plots.

## Dataset characteristics
- Sites and photos: 12 plots (sites) with about 36 files per site; 14 plots (sites) with about 50 files per site.
- Total: 1132 photos totaling 2607.8 MB.
- Image specifics: JPEGs captured with a Nikon D100 and Sigma 4.5 mm F2.8 fisheye lens; hemispherical imagery for canopy analysis under overcast conditions.
- Coverage: One photo at the intersection of four subplots for 12 plots; for other sites, one photo at the center of the subplot. Photos oriented with the camera top facing North at ~1 m height.
- Intended use: Processed photos provide representative plot-level LAI values (not sub-plot level).

## Collection and provenance
- Location context: Caatinga biome of Brazil; plots located across multiple sites with precise coordinates (latitude/longitude) and site metadata.
- Table 1 (Table not reproduced here) lists per-plot details: plot name, state, country, coordinates, number of photos, file size, and date.
- Data documentation includes notes on metadata irregularities and data provenance (e.g., MOR plots photographed on two different dates; JPEG dates may be incorrect).

## Metadata and identifiers
- Per-plot metadata fields include: plot code (e.g., BTI_01, CGR_01, MOR_01*), plot name, state, country, latitude, longitude, number of photos, size in MB, and date.
- Totals provided for the Caetité grouping (aggregated across all MOR/other plots), with total counts and aggregated sizes.
- Some entries contain anomalies (e.g., MOR plots showing two dates; certain date values and coordinates appear inconsistent or misformatted in the text).

## Data quality and limitations
- Image date metadata inconsistencies: jpg files have incorrect dates, with some photographs actually captured in 2017.
- Physical and logistical challenges noted: occasional camera trigger failures, adverse sky conditions leading to omitted images, and rejection of some images during processing.
- Processing caveat: photos provide a representative LAI for the whole plot, which may include canopy elements up to approximately 20 m from the camera, depending on vegetation height.
- Two MOR sites documented with two dates; some values and formatting in Table 1 show irregularities that may require verification.

## Usage considerations and sharing
- Purpose-built dataset intended for LAI estimation and canopy structure analysis across Caatinga plots; suitable for ecological and climate-related research.
- Metadata-rich structure supports data discovery, provenance tracking, and re-use by data users and software tools.
- No explicit licensing or access restrictions stated in the provided text; users should verify repository-level terms and any data-sharing requirements before distribution or reuse.

## Governance implications for Data Stewards
- Ensure metadata accuracy and consistency across all plots (verify coordinates, dates, and file counts).
- Standardize metadata fields (e.g., date formats, site naming) to improve interoperability and discoverability.
- Implement data quality checks to flag misdated JPEGs and inconsistent plot entries (e.g., MOR two-date entries).
- Document known data quality issues and processing notes (e.g., coverage limitations, potential LAI estimation caveats).
- Establish clear data provenance and update procedures, including how to handle late-arriving corrections or reprocessing of LAI estimates.
- Provide guidance on dataset maintenance, versioning, and any future additions or updates to LAI-derived products.