# Experimental Design/Sampling Regime

- Purpose and scope
  - Document describes a longitudinal, multi-field study of earthworms and soil properties to assess changes associated with land-use conversion.
  - Seven fields were sampled before conversion transects (April 2015) and re-sampled in April 2016 and April 2017; additional temporal sampling occurred in December 2015 (winter), July 2016 (summer), and October 2016 (autumn).
  - Temporal sampling indicates observed annual changes in these fields are representative of changes in the other study fields.
  - Sampling locations within each field included eight points: under a hedge, field-margin boundary, and distances of 2, 4, 8, 16, 32, and 64 meters from the field-margin boundary along transects.

- Experimental design and locations
  - Fields: Big Substation East (BSSE), Big Substation West (BSSW), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
  - Sampling framework used fixed transects with designated strip treatments (CAL, UAL, Ctrl, NTL-A, CTL_A) in certain fields; NB: April 2015 sampling used control land uses as strips were not yet created.

- Collection methods and instrumentation
  - Earthworm sampling: soil block (18 x 18 x 15 cm) excavated at each distance; diluted allyl isothiocyanate applied to enhance collection of deeper-dwelling worms; worms hand-sorted, stored in 80% ethanol.
  - Identification: adults with clitellum identified using Sims & Gerard keys; juveniles grouped into functional groups (epigeic, endogeic, anecic).
  - Biomass: measured for earthworms from December 2015 onward.
  - Soil measurements: soil moisture at 5 cm and 10 cm depths, soil temperature at 5 cm and 10 cm depths, recorded at multiple pit positions.
  - Bulk density: measured at 5 cm and 10 cm depths using standard rings; calculated from oven-dried samples.

- Variables and measurements
  - Earthworms: counts and biomass by species and functional group (Endogeic, Epigeic, Anecic).
  - Species list examples include Allolobophora chlorotica, Allolobophoridella eiseni, Aporrectodea caliginosa, Aporrectodea longa, Lumbricus terrestris, Lumbricus rubellus, Eisenia fetida, and others.
  - Soil properties: soil moisture (multiple depth readings), soil temperature (multiple depth readings), and bulk density (5 cm and 10 cm depths).
  - Sampling context: distance from hedge, hedge vs margin vs fixed distances (2, 4, 8, 16, 32, 64 m), and field/strip codes.

- Data structure and file organization
  - Files provided include:
    - April2015_earthworm_Soil data.csv (9 columns)
    - Dec2015_Earthworm_Soil data.csv (10 columns)
    - April2016_Earthworm_Soil data.csv (15 columns)
    - April2017_Earthworm_Soil data.csv (15 columns)
    - July2016_Earthworm_Soil data.csv (15 columns)
    - Oct2016_Earthworm_Soil data.csv (15 columns)
    - Earthworm_count CSV series: April2015_EW_count.csv, April2016_EW_count.csv, April2017_EW_count.csv, Dec2015_EW_count.csv, July2016_EW_count.csv, Oct2016_EW_count.csv (31 columns)
  - Common coding scheme across files:
    - Date: sampling date
    - SBH_code: field and distance code (X = field, Y = strip, ZZ = distance/location)
    - Field_name: full field name (BSSE, BSSW, Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field)
    - Strip: treatment type (CAL, UAL, Ctrl, NTL-A, CTL_A)
    - Distance: meters from hedge (H) or margin (M) indicated
    - Location codes for hedge (01) and margin (02) and distances (04, 05, 06, 07, 08, 09)
  - Depth and sensor columns vary by file version (e.g., soil_temp_10cm, soil_moisture_1/2/3, moisture_5cm_depth_1/2/3, etc.; later files include moisture_5 cm and 10 cm depth readings and bulk_density_5cm and bulk_density_15cm).

- Data content and format details
  - April2015_Earthworm_Soil data.csv: 9 columns; includes date, field, location code, sample location, distance, soil temperature and soil moisture readings.
  - Dec2015_Earthworm_Soil data.csv: 10 columns; adds field_name, strip, and extended location descriptors and multiple moisture/temperature readings.
  - April2016, April2017, July2016, Oct2016_Earthworm_Soil data.csv: 15 columns; expanded to include multiple depth measurements for temperature and moisture, plus field/strip metadata.
  - Earthworm_count files: 31 columns; comprehensive counts/biomass per species and functional group across dates, including all colonies and depth/location metadata.
  - Blank cells denote missing data.

- Earthworm functional groups and species
  - Functional groups defined: Endogeic (soil-living, horizontal burrowing), Epigeic (litter-living), Anecic (soil-living, deep vertical burrows).
  - Species represented include a wide range across groups, with codes like END-Al-chl (Allolobophora chlorotica), END-Ad-esi (Alloloboridella eiseni), END-Ap-cal (Aporrectodea caliginosa), ANE-Ap-noc (Aporrectodea caliginosa nocturna), END-Ap-lim (Aporrectodea limicola), ANE-Ap-lon (Aporrectodea longa), END-Ap-ros (Aporrectodea rosea), EPI-Ds-rub (Dendrodrilus rubidus), EPI-E-fet (Eisenia fetida), and many others including Lumbricus terrestris and Lumbricus rubellus.
  - Data include both abundance counts (A) and biomass (B) by species.

- Data quality, provenance, and usage notes
  - Emphasis on consistent sampling around hedges and field margins with transects to support comparative analyses across fields and treatment strips.
  - Data are suited for cross-file integration to analyze spatial and temporal trends in earthworm communities and soil properties in response to land-use changes.
  - Potential challenges for data usage include: patchy data gaps, multiple formats across years, and the need to align codes (field/strip/location) across datasets.
  - Documentation provides explicit mapping between codes and field/strip locations to enable data merging and reproducible analyses.

- References and background
  - Earthworms by Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008) referenced for methodology and identification keys.