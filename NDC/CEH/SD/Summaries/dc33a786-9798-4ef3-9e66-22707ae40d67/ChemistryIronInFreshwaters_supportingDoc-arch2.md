# IRONCHEMISTRYDATA1.csv through IRONCHEMISTRYDATA4.csv – Dataset Schema and Metadata

## Aim and Context
- Provides standardized, time-series environmental chemistry data to assess environmental health and policy performance.
- Data are gathered from established monitoring responsibilities, verified and quality assured, then transformed into clear outputs (reports, maps, charts).
- Datasets are stored and uploaded to appropriate data portals to enable broad access and reuse.

## Data Files and Key Variables

- IRONCHEMISTRYDATA1.csv
  - SampleSite: Name of site
  - SampleDate: Date sample was collected
  - pHfield: pH in the field
  - pHfinal: pH retested in the laboratory
  - DOC: dissolved organic carbon (mg dm-3)
  - Na, Mg, Ca, Cl, NO3, SO4: major ions (µeq dm-3 or µg dm-3 as specified)
  - alklinity: alkalinity (µeq dm-3)
  - total_Fe, total_Fe_II: total iron and iron(II) (µg dm-3)
  - filtered_Fe, filtered_Fe_II: filtered iron and iron(II) (µg dm-3)
  - total_monomeric_Al, total_acid_reactive_Al: aluminium species (µg dm-3)

- IRONCHEMISTRYDATA2.csv
  - SampleSite, SampleDate (as above)
  - 3_5kDa_dialysates_Fe, 3_5kDa_dialysates_Fe_II: iron species in 3–5 kDa dialysates (µg dm-3)
  - 3_5kDa_dialysates_DOC: dissolved organic carbon in dialysates (mg dm-3)
  - 3_5kDa_dialysates_monomeric_Al: monomeric aluminium in dialysates (µg dm-3)

- IRONCHEMISTRYDATA3.csv
  - SampleSite, SampleDate (as above)
  - 10kDa_dialysates: iron in 10 kDa dialysates (µg dm-3)
  - 10kDa_dialysates_Fe_II: iron(II) in dialysates (µg dm-3)
  - 10kDa_dialysates_DOC: DOC in dialysates (mg dm-3)
  - 10kDa_dialysates_monomeric_Al: monomeric aluminium in dialysates (µg dm-3)

- IRONCHEMISTRYDATA4.csv
  - SampleSite, SampleDate (as above)
  - 15kDa_dialysates_Fe, 15kDa_dialysates_Fe_II: iron species in 15 kDa dialysates (µg dm-3)
  - 15kDa_dialysates_DOC: DOC in dialysates (mg dm-3)
  - 15kDa_dialysates_monomeric_Al: monomeric aluminium in dialysates (µg dm-3)

- Notes (across files)
  - Not measured; measurement not performed; insufficient sample; result below limit of detection (often indicated with <)

## Location Metadata
- Spatial references include multiple sample locations with coordinates:
  - Pool X: Easting 370205.5597, Northing 529824.1031
  - Pool Y: Easting 370205.5597, Northing 529824.1031
  - Roudsea Wood: Easting 332979.168, Northing 482716.448
  - River Hodder: Easting 370305.7676, Northing 459018.444
  - Whitray Beck tributary: Easting 367808.519, Northing 461991.799
  - River Lune: Easting 352204.8281, Northing 464732.7131
  - River Ribble: Easting 357798.9523, Northing 430127.0969
  - Gais Gill: Easting 371690.217, Northing 501091.119
  - River Eden: Easting 378140.504, Northing 499217.841
  - Black Burn: Easting 370737.101, Northing 543491.876
  - River Tees: Easting 388601.996, Northing 528411.4836
  - Wad Hazel Sike: Easting 379402.9006, Northing 535119.8543

## Data Quality, Access, and Stewardship

- Data verification, quality assurance, cleaning, and transformation are performed to support reliable outputs.
- Outputs are stored in appropriate portals and shared in accessible formats (reports, maps, charts).
- A key challenge is increasing the value of datasets by integrating with related data and enabling access to underlying data for reuse.

## How This Supports Monitoring and Policy Evaluation

- Provides an auditable, standardized record of chemical parameters across sites and over time.
- Enables time-series analyses of pH, DOC, major ions, and metal/aluminium speciation in both bulk samples and dialysates.
- Supports comparisons against standards and assessments of environmental health, informing policy performance and management decisions.