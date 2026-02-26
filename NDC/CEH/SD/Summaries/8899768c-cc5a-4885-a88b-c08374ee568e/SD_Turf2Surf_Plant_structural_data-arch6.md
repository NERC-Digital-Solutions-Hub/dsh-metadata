# Details of data structure for the dataset

- Overview
  - Supplement to supporting documentation for Turf2Surf data series.
  - Datasets covered: plant structural measurements (North Wales and NW England, 2013–2014); aboveground/belowground biomass in Conwy catchment (2013–2014); soil carbon in Conwy (2013–2014); soil physical/chemical/biological in Conwy (2013–2014); plant physiological measurements in North Wales and NW England (2013, 2014, 2016).
  - All datasets share the first 9 columns to enable easy combination and cross-dataset analysis.
  - Some sites are sampled for only a subset of data types (e.g., soil or physiological data) and are linked via related datasets.

- Shared data structure (first 9 columns)
  - Column A: Site Number (as in Table 1 of the supporting documentation).
  - Columns B–C: Habitat and Habitat Description.
  - Column D: Site name.
  - Column E: Ecosystem Component (plant, soil, or roots).
  - Column F: If Component = Plant, plant species; otherwise NA.
  - Columns G–H: Plot number (1–4) and Replicate number (for dominant vs co-located measurements).
  - Column I: Soil depth interval (for soil and roots components).
  - Missing values indicated as NA; some sites not sampled for plant structural data but sampled for other data (linked via related datasets).
  - Structure kept consistent across files to facilitate combining.

- Variable naming and data provenance conventions
  - Prefix r: square-root transformed data (e.g., for percent cover).
  - c1: subordinate species excluded; c: subordinate species included.
  - Suffix db: trait values from database mean values only.
  - Suffix ob: measured trait values for dominants substituted for database means.
  - Example decoding: rc1LDMCob = square-root transformed LDMC, subordinate species excluded, measured traits for dominants included.

- NPP dataset details (22 additional columns, 155 rows)
  - J: NPP (Annual aboveground net primary production); Unit: g dry biomass m^-2 yr^-1.
  - K: lnNPP; Unit: g dry biomass m^-2 yr^-1; Description: natural log of NPP.
  - L: rcht; Unit: cm; Description: square-root transformed canopy height.
  - M: rcht1; Unit: cm; Description: square-root transformed canopy height, subordinate species excluded.
  - N: rBcov; Unit: % (0.5); Description: square-root transformed bryophyte cover.
  - O: rBcov1; Unit: % (0.5); Description: square-root transformed bryophyte cover, subordinate species excluded.
  - P: rc1LDMCdb; Unit: g dry mass g^-1 fresh mass; Description: square-root transformed LDMC, subordinate species excluded, database values only.
  - Q: rc1LDMCob; Unit: g dry mass g^-1 fresh mass; Description: square-root transformed LDMC, subordinate species excluded, measured dominants included.
  - R: rc1SLAdb; Unit: mm² mg⁻¹ dry mass; Description: square-root transformed SLA, subordinate species excluded, database values only.
  - S: rc1SLAob; Unit: mm² mg⁻¹ dry mass; Description: square-root transformed SLA, subordinate species excluded, measured dominants included.
  - T: rcLDMCdb; Unit: g dry mass g⁻1 fresh mass; Description: square-root transformed LDMC, database values only.
  - U: rcLDMCob; Unit: g dry mass g⁻1 fresh mass; Description: square-root transformed LDMC, measured dominants included.
  - V: rcSLAdb; Unit: mm² mg⁻¹ dry mass; Description: square-root transformed SLA, database values only.
  - W: rcSLAob; Unit: mm² mg⁻¹ dry mass; Description: square-root transformed SLA, measured dominants included.
  - X: c1LDMCdb; Unit: g dry mass g⁻1 fresh mass; Description: untransformed LDMC cover, subordinate species excluded, database values only.
  - Y: c1LDMCob; Unit: g dry mass g⁻1 fresh mass; Description: untransformed LDMC cover, subordinate species excluded, measured dominants included.
  - Z: c1SLAdb; Unit: mm² mg⁻¹ dry mass; Description: untransformed SLA cover, subordinate species excluded, database values only.
  - AA: c1SLAob; Unit: mm² mg⁻¹ dry mass; Description: untransformed SLA cover, subordinate species excluded, measured dominants included.
  - AB: cLDMCdb; Unit: g dry mass g⁻1 fresh mass; Description: untransformed cover, LDMC, database values only.
  - AC: cLDMCob; Unit: g dry mass g⁻1 fresh mass; Description: untransformed cover, LDMC, measured dominants included.
  - AD: cSLAdb; Unit: mm² mg⁻¹ dry mass; Description: untransformed cover, SLA, database values only.
  - AE: cSLAob; Unit: mm² mg⁻¹ dry mass; Description: untransformed cover, SLA, measured dominants included.
  - NA: not performed for that site.

- Practical notes for data use
  - Data are designed to be combined across plant, soil, and root datasets via the shared first 9 columns.
  - Be aware of transformations and data provenance when analyzing traits (db vs ob; r vs untransformed; c1 vs c).
  - NA indicators denote missing measurements; some sites may lack certain data types (e.g., plant structural data vs soil data).
  - The NPP-related columns include both transformed and untransformed forms and clearly distinguish whether values come from database means or dominants’ measured values.

- Related documentation
  - Supplementary to Turf2Surf WP2 supporting documentation (Turf2Surf_WP2_Supporting_documentation.rtf).