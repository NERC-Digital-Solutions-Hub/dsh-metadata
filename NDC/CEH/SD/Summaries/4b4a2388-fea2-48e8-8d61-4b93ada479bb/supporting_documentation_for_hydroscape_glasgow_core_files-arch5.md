# Headings used to record the stratigraphic data collected for each core

## Overview
- Describes the headings used to record stratigraphic data for each core.
- Data are organized as a matrix with columns (determinands) and rows representing contiguous core-depth intervals.
- Blanks indicate no measurement.
- Associated files are CSVs named with water body identification numbers (WBID) and project codes; file naming conveys lake/core location.

## Data Structure and Content
- Core slice identifier: Sub_ID (Internal UCL Amphora database unique ID).
- Depth information: Top_Depth_cm, Bottom_Depth_cm (distance to top/bottom of sliced core from sediment/water interface).
- Physical properties:
  - DW: Mass of sediment after drying at 105°C for 24 hours (percentage of dry weight).
  - LOI 550: Loss on ignition at 550°C (organic content percentage).
  - LOI 950: Loss on ignition at 950°C (carbonate content percentage).
  - wetd: Mass (g) of 1 cm³ of wet sediment.
- Radiometric dating:
  - Pb210_Total, Pb210_Total_err
  - Pb210_Supported, Pb210_Supported_err
  - Pb210_Unsupported, Pb210_Unsupported_err
  - Cum_Unsupported_Pb210, Cum_Unsupported_Pb210_err
  - Cs137, Cs137_err
  - Am241, Am241_err
- Age and accumulation metrics:
  - Date_AD
  - Age_yr, Age_yr_err (Constant Rate of Supply model)
  - SAR (Sediment dry mass accumulation rate)
  - SR, SR_err (Sedimentation rate)
- Mercury and geochemistry:
  - Hg µg/g (total mercury by atomic fluorescence)
  - XRF element concentrations: Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti%, V µg/g, Cr µg/g, Mn%, Fe%, Co µg/g, Ni µg/g, Cu µg/g, Zn µg/g, Ga µg/g, As µg/g, Br µg/g, Rb µg/g, Sr µg/g, Y µg/g, Nb µg/g, Ba µg/g, Pb µg/g
- Units and measurement context are provided in the descriptions; missing data are indicated by blanks.

## Metadata, Provenance and References
- Provenance: Sub_ID tied to the Internal UCL Amphora database.
- Method references:
  - Ref 1: Heiri, Lotter, Lemcke (2001) on loss on ignition methods for organic and carbonate content (reproducibility/comparability).
  - Ref 2: Appleby & Oldfield (1978) CRS model for calculating lead-210 dates with constant rate of supply.

## Data Quality, Processing and Governance
- Quality assurance: datasets should be quality checked, cleaned, and transformed before sharing.
- Standards: ensure accuracy, consistency, metadata completeness, and consistent data formats; align with user needs (publishing mindset for usability).
- Data availability and restrictions: identify disclosure risks, proprietary issues, and embargoes; manage updates and maintain versioning.

## Data Access, Sharing and Updates
- Upload and catalogue: datasets are uploaded to relevant portals and catalogued within data holdings; documentation of work performed on datasets may be prepared.
- Updates: systems should support ongoing updates and maintenance of data.

## Challenges for Data Stewards (as per archetype)
- Incomplete understanding of user needs and priorities.
- Timely acquisition of data from providers.
- Ensuring data creators meet standards (metadata, formats).
- Interoperability across many systems and formats.
- Handling large datasets and transferring large volumes.
- Dealing with outdated databases requiring bespoke, non-interoperable solutions.

## Associated Files
- 25855_doug_deep.csv
- 25866_bard_deep.csv
- 25866_bard_litt.csv
- 26001_possi_lit.csv
- 26145_hogg_deep.csv
- 26163_bish_deep.csv
- 26167_wode_deep.csv
- 26392_semp_deep.csv
- 26392_semp_int.csv
- 26392_semp_litt.csv
- 26535_libo_deep.csv