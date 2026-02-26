# Soil Biodiversity Thematic Programme: Sourhope Site Summary

## Overview
- Four years into the NERC Soil Biodiversity Thematic Programme, focused on intensive study of a large field experiment at Sourhope, Scottish Borders.
- Main foci: above-ground biomass production (productivity), plant species composition, and relative abundance (diversity) under controlled management.
- Five replicate blocks with six main plots per block, subdivided into ten sub-plots; data collected across multiple years (1998 baseline, 1999–2002 ongoing).

## Dataset scope and provenance
- Site: Rigg Foot Experimental Site, Sourhope; 5 blocks on a downslope gradient.
- Treatments: five plot-level management regimes (Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime) and Insecticide (formerly Biocide) plots; mowing conducted on the whole site.
- Data collected include:
  - Weather data from on-site Automatic Weather Station (1999–2002).
  - Above-ground biomass: annual biomass estimates from 0.5 m2 random cells within sub-plots, collected before each mowing (1999–2002).
  - Botanical data: baseline vegetation survey (1998) and repeated point analysis surveys (2000, 2001, 2002) using 0.5 m2 cells with 100-point grids; bryophyte identification enhanced in 2002.
  - Soil data: soil pH (5 cm depth) and soil moisture (theta probe; 2002 measurements) with ongoing collection since 1998.
  - Additional niche measurements: small-scale vegetation cover estimates, biomass by species, and bryophyte counts; extensive species lists (Appendix 3) and various survey outputs (Appendix 6–8).
- Data volume: over 11,621 soil samples collected since the start; 11621 soil samples documented in the report up to 2002.
- Data storage and access: full project-level details and datasets are available via the Soil Biodiversity website (and through the Centre for Ecology and Hydrology, Windermere Road).

## Methods and data collection practices
- Site management and treatments (annual cycle):
  - Monthly mowing to ~6 cm (May–September) site-wide.
  - Insecticide (Dursban 4 OPA) applied to Insecticide plots after mowing.
  - Spring fertilisation with nitrogen and/or lime on designated plots.
- Data collection specifics:
  - Above-ground biomass: harvests from random 0.5 m2 cells within sub-plots, drying to 80°C and weighing.
  - Baseline and annual botanical surveys using point quadrats (25 points baseline; 100-point method for 2000–2002 with 25 pinned points per 0.5 m2 cell).
  - Soil monitoring: pH measured on-site, with periodic soil moisture assessments; targeted sampling in July/August 2002 for moisture correlates with biomass.
  - Weather data: on-site measurements captured continuously since February 1999.
- Data analysis approaches:
  - Biomass data normalized to Control 1 for cross-year comparisons.
  - Biomass data log-transformed for ANOVA (split-plot Genstat 6) to assess treatment, year, and interaction effects.
  - Principal Component Analysis (PCA) applied to point analysis survey data (with yearly treatment-based rankings).
  - Shannon diversity indices calculated from point analyses to track diversity changes across treatments and years.
  - Functional grouping of plants (stress-tolerators S, competitive-stress-ruderals CSR/SR-CS-R) used to interpret community responses.

## Key findings (from the data)
- Mowing effects
  - Consistent decline in Agrostis capillaris and Agrostis vinealis across most treatments since 2000; possible site-level factor beyond treatment (e.g., mowing regime, disturbance pattern, climate).
  - Festuca rubra expansion, particularly in fertile plots (lime and/or nitrogen), associated with reduced disturbance and higher nutrients.
  - Widespread bryophyte expansion (mosses) across the site, correlated with a ~6 cm sward height maintenance and reduced grazing; more pronounced in unimproved plots.
  - Stress-tolerant species increased broadly, except in plots receiving nitrogen + lime where competitive-stress-ruderal groups expanded.
- Fertilisation effect
  - Nitrogen and/or lime additions increased above-ground productivity; plots with both nitrogen and lime showed the strongest productivity gains (though possible signs of plateau or stress at higher soil pH).
  - Soils treated with lime achieved pH near 7.0; higher lime input linked to drier micro-sites, potentially stress for moisture-sensitive species.
  - A positive relationship between soil pH and biomass exists on a site level; within combined N+L plots, the relationship can be negative due to altered moisture dynamics.
  - Nutrient-rich plots favored C-S-R (competitive-stress-ruderal) species; unimproved plots favored stress-tolerant species due to lower fertility.
- Insecticide effect
  - Plant diversity patterns with insecticide treatment align with some prior studies suggesting herbivory can affect plant communities, but direct causality to diversity is uncertain without detailed herbivory controls.
  - Trends show potential increases in diversity for some palatable species when herbivory pressure is altered, though broad conclusions require cautious interpretation.
- Trampling effect
  - First year of C2 (likely trampling-intensive) data show marked reductions in productivity, possibly due to trampling during 13CO2 labelling activities.
- Community structure and functional groups
  - By 2002, significant treatment effects on the relative abundance of functional groups (S, CSR, SR/CSR) across plots.
  - Nitrogen+Lime plots dominated by CSR-related species; unimproved plots dominated by S-type species; lime-only and insecticide plots showed varied responses.
- Temporal patterns and data notes
  - Biomass generally increased from 1999 baseline across treatments, despite a drop in 2002 relative to 2001.
  - Some block- and slope-position effects observed in productivity, with lower biomass on certain blocks.
  - A weather-related data gap occurred in 2002 due to a station malfunction (July–November data affected); remaining data used from substituted nearby stations for missing periods.
- Diversity and species composition
  - Point analysis shows a shift in species dominance across treatments (e.g., Festuca rubra and Poa pratensis more abundant in fertilised plots; Agrostis spp. decline; bryophyte frequency rising over years).
  - Shannon diversity indices reveal treatment-associated shifts from baseline, with notable drop in 2002 in nitrogen+lime plots.

## Data governance implications for Data Stewards
- Data lineage and metadata
  - Maintain clear documentation of site layout, treatment allocations, mowing schedules, and year-by-year changes to protocols.
  - Capture 0.5 m2 cell-level locations, sub-plot designations, and plot-level vs. site-level treatments to ensure reproducibility and traceability.
- Data quality and processing
  - Preserve raw biomass weights and computed/normalized values (e.g., biomass relative to Control 1, log transformations for analyses).
  - Record data processing steps (e.g., LS/ANOVA, PCA, Shannon indices) and any data corrections due to equipment issues (e.g., 2002 weather station gaps).
- Data availability and access
  - Ensure datasets (weather, biomass, point analyses, soil pH/moisture, bryophyte lists) are discoverable via the Soil Biodiversity portal.
  - Include data dictionaries and appendices (e.g., species lists, Appendix 3) to enable reuse by other researchers and program groups.
- Data update and maintenance
  - Track updates from ongoing Phase II projects (including 13CO2 pulse experiments and trace gas measurements) and ensure integration with historical data.
  - Note any embargoes or access restrictions and provide contact points (project PIs, CEH) for data requests.
- Data interoperability and standards
  - Align dataset naming, units, and measurement methods (e.g., biomass in g m-2, pH in H2O, moisture as theta) to facilitate cross-site comparisons.
  - Preserve functional-group classifications (S, CSR, SR/CSR) and maintain a consistent interpretation framework across years.
- Risk and gaps management
  - Document known data gaps (e.g., 2002 weather data loss) and the chosen substitutions or proxies; maintain flags for data quality and completeness.
  - Record potential confounding factors (e.g., trampling, mowing regime) to support transparent interpretation of results.

## Practical recommendations for Data Stewards
- Develop a comprehensive data schema and metadata template that captures:
  - Site, block, plot, sub-plot, and cell identifiers; treatment assignments and dates; mowing dates and heights; fertiliser rates; insecticide applications.
  - Measurement methods, instruments, units, and calibration notes; sampling dates; and data processing steps.
- Create data quality flags and provenance trails to capture:
  - Anomalies (e.g., 2002 weather data gaps), data corrections, and rationale for any imputations or substitutions.
- Ensure long-term data preservation and access:
  - Maintain version-controlled data releases; provide stable DOIs for datasets; update the central portal with new yearly data and appendices.
- Support reproducibility and reuse:
  - Provide example analyses or code snippets (e.g., how biomass was normalized or how PCA was performed) to accelerate re-use by other researchers.
- Foster discoverability:
  - Include cross-linking between datasets (biomass, soil, bryophytes, species lists) and the published analyses; maintain a clear data glossary and taxonomy references.

## Endnotes
- The Sourhope site provides a rich, multi-year dataset linking management practices to above-ground productivity, plant community structure, soil chemistry, and bryophyte dynamics.
- This dataset offers insights into how mowing, fertilisation, and insecticide treatment interact with soil pH, moisture, and disturbance regimes to shape plant functional groups and overall diversity.
- For access and detailed data descriptions, refer to the Soil Biodiversity website and CEH contact points referenced in the report.