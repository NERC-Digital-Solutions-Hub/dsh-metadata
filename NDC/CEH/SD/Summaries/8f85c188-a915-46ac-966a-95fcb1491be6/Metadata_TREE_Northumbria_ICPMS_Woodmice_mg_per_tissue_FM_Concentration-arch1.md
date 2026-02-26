# TREE_Northumbria_ICPMS_Woodmice_mg_per_tissue_FM_Concentration

- Purpose and scope
  - Metadata/dictionary for a dataset detailing concentrations of multiple elements in Northumbria wood mice tissues using ICPMS.
  - Concentrations are reported as milligrams per total tissue fresh mass (mg per tissue FM).
  - Includes sampling metadata (Latin and common species names, sampling site, date collected), UKCEH sampling codes and descriptions, and tissue sampled.

- Key fields and units
  - Taxonomy and sample identifiers: Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description.
  - Tissue information: Tissue description (name of wood mouse tissue sampled).
  - Concentration fields: I_mg_per_tissue_FM (iodine), Li_mg_per_tissue_FM (lithium), Na_mg_per_tissue_FM (sodium), Al_mg_per_tissue_FM (aluminium), P_mg_per_tissue_FM (phosphorus), K_mg_per_tissue_FM (potassium), Ca_mg_per_tissue_FM (calcium), Ti_mg_per_tissue_FM (titanium), V_mg_per_tissue_FM (vanadium), Cr_mg_per_tissue_FM (chromium), Mn_mg_per_tissue_FM (manganese), Fe_mg_per_tissue_FM (iron), Co_mg_per_tissue_FM (cobalt), Ni_mg_per_tissue_FM (nickel), Cu_mg_per_tissue_FM (copper), Zn_mg_per_tissue_FM (zinc), As_mg_per_tissue_FM (arsenic), Se_mg_per_tissue_FM (selenium), Rb_mg_per_tissue_FM (rubidium), Sr_mg_per_tissue_FM (strontium), Mo_mg_per_tissue_FM (molybdenum), Ag_mg_per_tissue_FM (silver), Cd_mg_per_tissue_FM (cadmium), Cs_mg_per_tissue_FM (cesium), Tl_mg_per_tissue_FM (thallium), Pb_mg_per_tissue_FM (lead), U_mg_per_tissue_FM (uranium).
  - Special notes on markers: Columns may contain <I, <Al, <V, <Cr, <Ni, <Mo, <Pb, <Ba markers indicating concentration values reported as “less than” a threshold.
  - Thyroid-specific data: Some elements have associated thyroid concentrations (e.g., Rb_thyroid, Sr_thyroid, Mo_thyroid, Ag_thyroid, Pb_thyroid, U_thyroid), with many entries noted as “No data collected for woodmice thyroid.”
  - Data completeness notes: Several entries indicate “No data collected” for particular tissues (e.g., Hind Leg Bone, woodmice liver for certain samples) or for specific thyroid measurements.

- Data availability and gaps
  - Some tissues/samples lack data entirely (e.g., Hind Leg Bone and woodmice 8 liver).
  - Thyroid data are largely missing for many elements.
  - Detection-limit indicators (<) are present in multiple concentration columns.

- Provenance and structure
  - Sample codes and descriptions are linked to UK Centre for Ecology & Hydrology (UKCEH) processes.
  - Data are organized by site, date, tissue, and a broad panel of elemental concentrations measured per total tissue fresh mass.

- How this data supports analysis
  - Enables correlation of element concentrations with site, species, and tissue type.
  - Supports cross-element comparisons within and across tissues, with explicit units and data quality notes.
  - Requires careful handling of missing data and censored (<) values, and careful interpretation where thyroid data or specific tissues are absent.