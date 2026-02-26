# Supporting documentation for the Cryptosporidium in Welsh upland water biota data (2012-2015)

- Scope and purpose
  - A sample survey aligned with the wider DURESS project to test for Cryptosporidium across Welsh upland water biota (2012–2015).
  - No treatments or replication in the sampling; controls were used in laboratory assays, not during field sampling.
  - Data aimed at characterising environmental presence of Cryptosporidium and supporting related analyses.

- Sampling and specimen types
  - Fish tissue sampling (gills and gut contents): 74 fish from 11 upland river sites (summer 2012) via electrofishing; 73 gut and 74 gill samples tested (16 salmon gills, 41 brown trout, 16 bullhead). Samples frozen at -20°C.
  - Fish faeces: live fish faecal sampling from 8 sites (summer 2013) by anaesthetising fish and collecting faeces during gut massage; 117 fish faecal samples frozen at -20°C.
  - Otter faeces: 41 ground samples collected around upland riparian zones (2013) with uncertain species origin; additional otter samples came from dead otters across England and Wales (2011–2015) for host-range exploration.
  - Aquatic invertebrate larvae (filter-feeders): 290 larvae from genera including Baetis, Rhithrogena, Leuctra, Hydropsyche, Simulium, Philopotamus, Plectrocnemia, Amphinemura collected June 2012 from Llyn Brianne catchment; stored in absolute ethanol.
  - Data files: Results_Biofilm_Fish_Mammals.csv and Results_Invertebrate_Larvae.csv; site metadata described in DURESS_CU_site_description.csv.

- Laboratory methods and quality controls
  - DNA extraction methods tailored to sample type:
    - Gills and gut contents: QIAamp DNA mini kit.
    - Fish and mammal faeces: QIAamp Fast DNA stool mini kit.
    - Aquatic larvae: Gentra Puregene DNA kit; larvae ground in liquid nitrogen with freeze-thaw cycle.
  - Molecular testing:
    - Primary screening: nested PCR targeting the small subunit rRNA (ssu rRNA) gene; positive amplicons sequenced for species identification.
    - Genotyping: gp60 locus sequencing on Cryptosporidium parvum and C. hominis positives.
    - Invertebrate larvae: real-time PCR targeting C. hominis with an internal control to check for inhibition.
  - Controls and accreditation:
    - Included positive and negative controls in all assays.
    - Positive controls included known positive DNA and samples seeded with C. hominis oocysts for extraction control.
    - Laboratory methods accredited at the Cryptosporidium Reference Unit; accreditation later moved to ISO15189.
    - DNA sequencing outsourced to Source Bioscience; subsequent analysis performed at CRU.

- Data structure and files
  - Results_Invertebrate_Larvae.csv
    - Sample_number: unique CRU identifier.
    - Sample_Description: type of invertebrate larva tested.
    - Number_of_larvae_pooled: number of larvae tested and, if seeded, the number seeded with C. hominis oocysts.
    - Site: sampling location (linked to DURESS_CU_site_description.csv).
    - n18S: nested ssu rRNA PCR result (Neg/Pos).
    - Ch_Ct_value: Ct value from C. hominis real-time PCR.
    - IC_Ct value: internal control Ct.
  - Results_Biofilm_Fish_Mammals.csv
    - Site: sampling site (linked to site description file).
    - Sample_group: general source (e.g., biofilm, fish, etc).
    - Host: source organism (e.g., trout); N/A where not applicable.
    - Sample_Type: nature of sample (biofilm, faeces, etc).
    - CRU_Ref: unique CRU sample identifier.
    - n18S_result: nested ssu rRNA PCR/sequencing result.
    - GP60: gp60 PCR result.
    - Sequencing: result of sequencing.
    - Note: where host source could not be unambiguously identified, a question mark is appended to the mammal name (e.g., Mink?).
  - Site descriptions: DURESS_CU_site_description.csv (supporting document) provides site-level metadata.

- Data context and interpretation
  - All data reflect a cross-sectional sampling snapshot across multiple host groups and environmental vectors to assess Cryptosporidium presence and diversity.
  - Some field sampling limitations noted:
    - No in-field replication.
    - Otter samples partly sourced from a broader pool not exclusively from the test catchments, affecting host-specific inference.
  - Data are structured to enable integration with broader environmental monitoring datasets and policy-relevant analyses.

- References
  - Alves et al. 2003; Hadfield et al. 2011; Jiang et al. 2005 (methods and genotyping references for Cryptosporidium).