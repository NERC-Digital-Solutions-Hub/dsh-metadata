# Description of the Data and file structure

## Overview
- Source: Environment Agency macroinvertebrate abundance data, stored as a long-form dataset (year, month, day, site, sample, taxon, abundance) and provided as a single rds file accessible via R.
- Scope: Freshwater macroinvertebrate data across England from 2002–2019, collected mainly during March–May and September–November.
- Purpose: Data originally collected to understand water quality; later prepared for research use.

## Data structure and contents
- File format: A single rds file containing processed data pooled by family and broader taxonomic groupings.
- Key columns (examples): riverbasin, agency_area, waterbody, wfd_waterbody_id, site_id, full_easting, full_northing, season, year, month, day, Latitude, Longitude, sample_id, order_taxon, family_taxon, total_abundance, year_scaled, group.
- Metadata notes: Missing data coded as NA; coordinates are in geographic terms; units are discrete counts of individuals.

## Data collection and processing
- Source data: Extracted from the EA ecological monitoring database; three-minute kick-samples are the primary sampling method (≈99% of samples).
- Filtering criteria: Sites sampled for at least three years out of 18, with data available for both spring and autumn periods.
- Taxa included: Ephemeroptera, Plecoptera, Hemiptera, Megaloptera, Odonata, Coleoptera, Trichoptera, Turbellaria, Annelida, Crustacea, Diptera, Mollusca.
- Aggregation: Abundance counts summed at the family level within these taxa.
- Scale and reach: Final dataset (2002–2019) comprises 67,757 samples from 5,009 sites (out of 10,136); covers 2,774 waterbodies across ten river basins under the Water Framework Directive.
- Analysis tools: Data manipulated and analyzed with R during 2019–2022.
- Dataset bias: Nationally distributed but biased toward mid-to-lower perennial reaches, reflecting monitoring program aims rather than intrinsic biodiversity.

## Quality control and data quality
- QC history: In 2002, improved abundance estimation and QC procedures began; one in ten samples independently re-analyzed.
- Data span: Although related data exist from 1991, the usable scope is restricted to 2002–2019.

## Access, reuse, and provenance
- Public access: Data publicly available at https://environment.data.gov.uk/ecology-fish.
- Publication use: Cited in Powell et al. (2022) Global Change Biology article on river macroinvertebrate abundance trends.

## Provenance and lineage
- Derived from: EA Ecology and Fish Explorer Macroinvertebrate database.
- Processing: Data are filtered to three-minute kick-sample data, site-year selection criteria applied, taxa filtered, and counts aggregated to family level; overall dataset prepared for national-scale analysis (2002–2019).

## Considerations for Data Stewards
- Data governance: Ensure ongoing access and versioning of the single rds file; document lineage from EA sources to final dataset.
- Metadata and interoperability: Maintain comprehensive metadata for fields, units, and sampling methods; note potential biases due to site selection and seasonal coverage.
- Update and maintenance: Current dataset reflects 2002–2019; any future updates should align with the same structure and QC standards.
- Sharing constraints: Respect licensing and public access terms; provide clear provenance and usage citations.