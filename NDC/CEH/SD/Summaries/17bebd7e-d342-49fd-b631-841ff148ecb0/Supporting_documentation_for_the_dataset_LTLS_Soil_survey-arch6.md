# Supporting documentation for the dataset Soil survey in England, Scotland and Wales carried out during 2013 and 2014, 2016, Toberman et al.

- Scope and purpose
  - Dataset from the LTLS Macronutrient Cycles project, covering soil survey results across England, Scotland and Wales conducted in 2013 and 2014 (with 2016 processing/documentation).
  - Aims to support analysis of long-term and large-scale carbon, nitrogen, and phosphorus interactions in UK soils, land, freshwater, and atmosphere.

- Sampling design and methods
  - At each site, soil cores were collected from a 100 x 100 m area.
  - A central line with regularly spaced points (11 m apart for 10 cores; 16 m for 6 cores) was used; individual coring sites were chosen at random distances from line points.
  - Core counts: typically 10 cores for semi-natural habitats; 6 or 10 cores for agricultural fields.
  - Depth sampling: top 20 cm sampled in some locations; additional 20 cm intervals sampled to reach 40 cm; in some cases the full 40 cm depth could not be reached.
  - Vegetation was removed prior to coring.

- Data structure and key tables (data model)
  - Locations_and_dates: sample_id, catchment (area where surface water converges), site_name, OS_Grid_ref, Easting, Northing, Latitude, Longitude, Altitude_metres, Sampling_date.
  - Bulk_density_data: BD_T (bulk density total), BD_P (bulk density particles <2 mm), BD_F (bulk density LOI-adjusted); units in g cm-3; includes measured dry weight and core volume.
  - Charcoal_and_coal_data: charcoal/coal content by mass (%), LOI, >2 mm fraction, muffle furnace measurements, and related fractions (Charcoal_frctn_of_LOI).
  - Radiocarbon_codes: SUERC radiocarbon facility code references for samples with radiocarbon data.
  - Site_vegetation_data: Habitat_type, Habitat_type_with_detail, Vegetation descriptions; includes catchment context.
  - Soil_chemistry_and_isotope_data: thickness_cm; sample layer designation (s = surface, d = deeper); BD_T, BD_P, BD_F (as above) with corresponding pH, N_% (nitrogen), C_% (carbon), P_tot_% (total phosphorus, both inorganic and organic components), delta13C, pMC (percent modern carbon), and related isotopic/elemental analyses. Methods include aqua regia digestion with ICP-OES, elemental analysis (Vario EL), and pH measurements.
  - P_tot_% and P_inorg_% vs P_org_%: breakouts for total phosphorus, inorganic phosphorus, and organic phosphorus; methods as above; some entries note < LOD (below detection limit).
  - Isotope data and radiocarbon context: delta13C, pMC, 14C_pMC values with corresponding methods and labs.
  - Soil_classifications_England_and_Wales: NSI classifications and related NSI_subgroup, NSI_brief; references to NSI classification data and survey information.
  - Soil_classifications_Scotland: Site_code, James Hutton Institute classifications, dominant soil map units, and 25k-scale mapping context.
  - Soil_cores_and_depth: Depth categories (shallow/deep), number of cores, mean_thickness_cm for cores, and related metadata.
  - Soil_texture_data: Clay and Silt fractions by mass, % clay, % silt; measurement method (Beckman Coulter LS200 laser granulometer); HOC flag indicating high organic content with no texture determination.

- Abbreviations and habitat types
  - Habitat_type abbreviations (e.g., AG = Acid grassland, Ar = Arable, C = Conifer plantation, CG = Calcareous grassland, H = Heathland, IG = Improved grassland, M = Montane, SP = Scots pine woodland, W = Broadleaved woodland, HOC = high organic content, etc.).
  - Abbreviations appear across data dictionaries to describe site and soil context.

- Key data quality notes and caveats
  - Depth sampling sometimes did not reach the planned 40 cm at all sites.
  - Data are organized across multiple related tables with cross-references via Sample_ID; users should join tables carefully to assemble complete records for samples.
  - Some fields denote not determined (ND) or below detection limits (< LOD).
  - Variable formats and units are specified per table (e.g., g cm-3 for bulk density, cm for thickness, % by mass for constituents).

- Potential uses for data support work
  - Build self-serve data products (dashboards, pivot tables) enabling exploration of soil physical properties (bulk density, depth distribution), chemistry (pH, C/N, P forms), and isotopic/isotopic proxy data.
  - Combine soil texture, chemical, and isotope data with site vegetation and classification metadata to analyze relationships between land use, soil types, and nutrient cycling.
  - Create data products for mapping or reporting on soil carbon storage, nutrient stocks, or depth-dependent properties across England, Scotland, and Wales.
  - Validate or enrich policy-relevant analyses for land management, agriculture, forestry, and habitat restoration with robust metadata and provenance.

- Provenance and context
  - Data are part of the NERC Macronutrient Cycles LTLS project, with documentation and data dictionaries detailing measurement methods, units, and table structures to facilitate use and integration with other LTLS datasets.