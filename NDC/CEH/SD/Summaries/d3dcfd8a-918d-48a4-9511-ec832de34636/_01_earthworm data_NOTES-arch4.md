# Experimental Design/Sampling Regime

- Seven fields were sampled prior to conversion transects in April 2015, with follow-up sampling in April 2016 and April 2017.
- Temporal sampling extended to one arable field (BSSE) and one pasture field (SP), both long-term for the study.
- Additional temporal checks occurred in December 2015 (winter), July 2016 (summer), and October 2016 (autumn), yielding a sampling timeline from the April 2015 baseline to April 2017.
- At each sampling, earthworm and soil samples were collected from 8 locations per field: under the hedgerow and at the field-margin head of each 70 m transect, plus samples along 2, 4, 8, 16, 32, and 64 m from the hedge boundary.

## Field Sampling Design and Distances

- Sampling covered 8 positions per transect: hedge, margin, and 2/4/8/16/32/64 m within transects.
- Distance measurements are from the field hedge boundary, with hedge (H) and margin (M)指定 in the data files.
- A mix of treatment contexts existed (connected arable ley strip, unconnected arable strip with earthworm barrier, control land uses, no-till and conventional tillage strips) across different years/fields.

## Collection Methods / Fieldwork Instrumentation

- Earthworm sampling: soil blocks (18 x 18 x 15 cm) excavated at each distance; earthworms collected by hand-sorting.
- Deep-dwelling worms targeted by applying dilute allyl isothiocyanate (1.5 L of 0.1 g L-1 solution) into pits and allowing 30 minutes for collection.
- Earthworms stored in 80% ethanol; adults (with clitellum) identified using Sims & Gerard keys; juveniles classified into functional groups (epigeic, endogeic, or anecic).
- Biomass measured as abundant numbers of earthworms from December 2015 onward.
- Soil measurements: moisture (ML3 ThetaProbe) and temperature (Checktemp1) at 5 and 10 cm depths around the pits.
- Bulk density determined at 5 and 10 cm depths using steel rings; oven-dried at 105°C for 24 h.
- Samples returned to pits with positions recorded to avoid re-sampling the same spot.

## Data Files and Structure

- April2015_earthworm_Soil data.csv
  - 9 columns: Date, Field_name, SBH_code (XYZZ), Distance, Hedge/Margin indicators, Soil_Temp_10cm, soil_moisture_1-3, plus location-specific codes.
  - SBH_code encodes Field (X), Strip (Y), and Sample Location (ZZ); codes define fields (e.g., BSSE, BSSW, Hillside, Copse, etc.) and strip positions (Left, Central, Right).
  - April 2015 samples were from control land use (treatment strips not yet created).
- Dec2015_Earthworm_Soil data.csv
  - 10 columns: Date, SBH_code, Field_name, Strip, Distance, Hedge/Margin, Depth, Soil_temp_5cm/10cm, moisture_5cm/10cm, etc.
  - Depth codes: Mustard (P) or Topsoil (S); includes field treatment context for Strip.
- April2016_Earthworm_Soil data.csv, April2017_Earthworm_Soil data.csv, July2016_Earthworm_Soil data.csv, Oct2016_Earthworm_Soil data.csv
  - Each contains 15 columns: Date, SBH_code, plus Field (X), Strip (Y), ZZ (distance), Field_name, Strip, Distance, Depth, sample-type indicators, and multiple columns for soil moisture and temperature at different depths (5 cm and 10 cm) plus bulk density measurements.
- The EW_count files: April2015_EW_count.csv, April2016_EW_count.csv, April2017_EW_count.csv, Dec2015_EW_count.csv, July2016_EW_count.csv, Oct2016_EW_count.csv
  - Each contains 31 columns: Date, SBH_code, Field/Strip encodings, Depth, and 15 species/functional-group columns for earthworm counts or biomass.
  - The SBH_code encoding matches the above scheme (Field X, Strip Y, Distance ZZ).
  - Depth indicates Mustard (P) or Topsoil (S); Sample_type indicates abundance/count (A) or biomass (B).
  - Blank cells = no data available.

## Biological Data Content

- The datasets include earthworm counts or biomass by species and functional group.
- Species and functional groups included (examples):
  - Endogeic: various Allolobophora and Aporrectodea species (e.g., Allolobophora chlorotica; Aporrectodea caliginosa; Aporrectodea limicola; Aporrectodea longa; Aporrectodea rosea; Endogeic groups with names like END-Al-chl, END-Ad-esi, etc.).
  - Epigeic: species such as Dendrodrilus rubidus; Eisenia fetida; Lumbricus castaneus; Lumbricus festivus; Lumbricus rubellus; Lumbricus terrestris (with coded entries like EPI-Ds-rub, EPI-E-fet, etc.).
  - Anecic: species such as Lumbricus terrestris and other anecic taxa (e.g., ANE-Ap-noc, ANE-Ap-lon, ANE-L-ter).
- The dataset provides both functional-group classification and species-level identifications where available.
- Aims to capture spatial distribution (hedge/margin and distances across transects) and temporal changes across multiple years and field treatments.

## Metadata and Documentation

- Units and coding are documented within the data structure (dates, distances in meters, depths in cm, moisture in millivolts, temperatures in degrees Celsius, and bulk density in g cm-3).
- Data reference materials include taxonomic keys (Sims & Gerard, 1999) and methodological references (Zaborski 2003; Pelosi et al. 2008).
- Missing data are indicated by blank cells.

## Key Considerations for Data Management (Data Leaders Perspective)

- Longitudinal, multi-field, and multi-year design enables assessment of conversion effects, spatial patterns, and temporal dynamics in earthworm communities and soil properties.
- Standardized SBH_code encoding supports cross-file joins and consistent spatial referencing across years.
- The data include both abundance and biomass measurements, across species and functional groups, facilitating diverse ecological analyses.
- Data quality depends on consistent identification of species/groups, standardized sampling moments, and careful handling of missing data and treatment boundary changes.
- Metadata provides essential context for data discoverability, reuse, and integration with broader data communities (e.g., soil biology and agroecology datasets).