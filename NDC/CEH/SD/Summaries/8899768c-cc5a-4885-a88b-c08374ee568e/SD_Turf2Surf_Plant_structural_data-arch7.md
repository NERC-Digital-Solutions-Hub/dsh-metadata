# Details of data structure for the dataset Plant structural measurements in North Wales and Northwest England (2013 and 2014) as detailed in the table Turf2Surf_Plant_structural_data.csv

- Scope
  - Describes the data structure for plant structural measurements (2013–2014) in North Wales and Northwest England, as referenced in Turf2Surf_Plant_structural_data.csv.
  - Related datasets share the first 9 columns to allow easy combination and integration with GIS data.

- Related datasets sharing the first 9 columns
  - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014)
  - Soil carbon data in the Conwy catchment in North Wales (2013 and 2014)
  - Soil physical, chemical and biological measurements in the Conwy catchment in North Wales (2013 and 2014)
  - Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014)

- Core identifiers and 9-column schema (Columns A–I)
  - Site Number: unique site identifier (as in Table 1 of the supporting docs)
  - Habitat: broad habitat category
  - Habitat Description: detailed habitat description
  - Site name: site designation
  - Ecosystem Component: plant, soil or roots
  - If Plant: plant species; otherwise NA
  - Plot: plot number (1–4)
  - Replicate: replicate number (used when measurements are not co-located with plots)
  - Soil depth interval: applicable to soil and root components

- Data quality, completeness and structure
  - Missing values indicated as NA (e.g., restricted soil depths, limited number of replicates, outliers)
  - Some sites sampled for non-plant data (soil, physiological) but not plant structural data; structure kept consistent to enable cross-dataset joins
  - NA also marks data not collected for a given site

- Variable naming conventions (interpretation guidance for GIS work)
  - Beginning of a variable name:
    - r = square-root transformed data
    - untransformed % cover otherwise
    - c1 = subordinate species excluded (1% threshold) in the plot
    - c = subordinate species included
  - End of a variable name:
    - db = trait values derived from published mean database values only
    - ob = observed/measured trait values for the two dominant species substituted for database means
  - Example: rc1LDMCob
    - r: square-root transformed cover
    - c1: subordinate species excluded
    - LDMC: Leaf Dry Matter Content
    - ob: measured traits for dominants included
  - This coding allows GIS users to understand whether a trait value is transformed, whether minor species were included, and whether values come from databases or direct measurements

- Trait values and calculations (conceptual overview for mapping)
  - Mean abundance-weighted trait values (x_jk) for SLA and LDMC are computed for each NPP plot j within site k
  - Trait values (τ_ijk) are based on either raw or square-root transformed cover for each species i in plot j at site k
  - Traits come from measured values for dominants or from published databases when dominants lack measurements
  - These calculations facilitate spatially explicit trait mapping at the plot level across sites

- Dataset layout and column details (22 additional columns; 155 rows)
  - The dataset includes 22 extra columns beyond the first 9, plus 155 rows
  - J: NPP (growth) – Unit: g dry biomass m^-2 yr^-1
  - K: lnNPP – Unit: g dry biomass m^-2 yr^-1
  - L: rcht – Unit: cm (square-root transformed canopy height)
  - M: rcht1 – Unit: cm (square-root transformed canopy height, subordinate excluded)
  - N: rBcov – Unit: % (square-root transformed bryophyte cover)
  - O: rBcov1 – Unit: % (square-root transformed bryophyte cover, subordinate excluded)
  - P: rc1LDMCdb – Unit: g dry mass g^-1 fresh mass (square-root transformed LDMC, subordinate excluded, database values only)
  - Q: rc1LDMCob – Unit: g dry mass g^-1 fresh mass (square-root transformed LDMC, subordinate excluded, measured dominants)
  - R: rc1SLAdb – Unit: mm^2 mg^-1 dry mass (SLA, database values only)
  - S: rc1SLAob – Unit: mm^2 mg^-1 dry mass (SLA, measured dominants)
  - T: rcLDMCdb – Unit: g dry mass g^-1 fresh mass (LDMC, database values only)
  - U: rcLDMCob – Unit: g dry mass g^-1 fresh mass (LDMC, measured dominants)
  - V: rcSLAdb – Unit: mm^2 mg^-1 dry mass (SLA, database values only)
  - W: rcSLAob – Unit: mm^2 mg^-1 dry mass (SLA, measured dominants)
  - X: c1LDMCdb – Unit: g dry mass g^-1 fresh mass (untransformed LDMC, subordinate excluded, database values only)
  - Y: c1LDMCob – Unit: g dry mass g^-1 fresh mass (untransformed LDMC, subordinate excluded, measured dominants)
  - Z: c1SLAdb – Unit: mm^2 mg^-1 dry mass (untransformed SLA, subordinate excluded, database values only)
  - AA: c1SLAob – Unit: mm^2 mg^-1 dry mass (untransformed SLA, subordinate excluded, measured dominants)
  - AB: cLDMCdb – Unit: g dry mass g^-1 fresh mass (untransformed LDMC, database values only)
  - AC: cLDMCob – Unit: g dry mass g^-1 fresh mass (untransformed LDMC, measured dominants)
  - AD: cSLAdb – Unit: mm^2 mg^-1 dry mass (untransformed SLA, database values only)
  - AE: cSLAob – Unit: mm^2 mg^-1 dry mass (untransformed SLA, measured dominants)
  - NA = measurements not performed for that site

- Practical GIS considerations
  - Use Site Number as the primary key to join this dataset with GIS layers (sites, plots, habitats)
  - Use the first 9 columns to link to spatial features and to align with other Turf2Surf datasets
  - Attach 22 additional trait columns to plots/sites for spatial analysis of productivity and functional traits
  - Be mindful of transformed vs. untransformed values when creating maps or performing comparisons
  - Account for missing data (NA) by using appropriate GIS handling (e.g., masked layers, gap filling, or documented exclusions)
  - Ensure temporal context (2013–2014 data) is preserved when creating time-series maps or comparing across years

- Notes and caveats for accurate interpretation
  - The data are structured to facilitate combining across related Turf2Surf datasets; ensure consistent joins on the 9 shared columns
  - Trait values may come from databases (db) or measured values (ob); interpret maps with awareness of data provenance
  - Some sites lack plant structural data but have other measurements; consult related datasets for a complete view

- Bottom line for GIS specialists
  - The document provides a cohesive, joinable data structure with clearly defined core fields, robust naming conventions for transformed and sourced trait data, and a rich set of derived trait variables suitable for map-based analysis of plant structure, biomass production, and leaf traits across sites in North Wales and Northwest England (2013–2014).