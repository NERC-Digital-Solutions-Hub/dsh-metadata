# Cumbrian Lakes plankton and fish data, used for turning points and early warnings analysis (1940 to 2013)

## Overview
- Datasets describing phyto- and zooplankton counts, chlorophyll concentration, and fish catch data from the Cumbrian Lakes (Blelham Tarn, Esthwaite Water, Windermere NBAS/SBAS).
- Time span: 1940 to 2013 (with varying coverage by dataset; specific ranges per data type).
- Origin: collected by the Freshwater Biological Association (FBA) and subsequently by CEH and its predecessor IFE since 1989.
- Use: data underpin Burthe et al. (2015); authors advised to be contacted directly before data reuse.

## Datasets and contents
- Windermere_fish_annual_catches.csv
  - Size: 23 KB; CSV format
  - Columns include: date, Year of sampling, site (NBAS/SBAS), Species (Arctic charr, perch, pike), variable (catch per unit effort with method), Catch (values).
- Cumbrian_Lakes_phyto_allsites.csv
  - Size: 2,505 KB; CSV format
  - Columns include: month, year, site (BLEL/ESTH/NBAS/SBAS), taxon (four-letter code), value (cells/colonies/filaments per ml), counter, chamber, form.
- Cumbrian_Lakes_zoo_allsites.csv
  - Size: 286 KB; CSV format
  - Columns include: month, year, site, variable (zooplankton counts), value (individuals per litre), confound.var.
- Cumbrian_Lakes_chl_allsites.csv
  - Size: 288 KB; CSV format
  - Columns include: date, month, year, site, variable (chlorophyll data code), value (mg m-3), confound.var.
  
## Sampling regime and collection methods
- Sampling frequency: weekly to biweekly at the deepest point of each lake.
- Collection methods:
  - Phytoplankton: Lugol-fixed samples collected with weighted plastic tube; counts via Lund chambers.
  - Chlorophyll: filtered through GF/C, extracted in methanol, spectrophotometric measurement.
  - Zooplankton: two sources; species-level net tows (Windermere NBAS) and aggregate filter counts from chlorophyll samples.
  - Fish (Arctic charr, perch, pike): CPUE estimates from angling, gill netting, and standardized trapping; long-term effort data used for annual CPUE calculations.
  
## Analytical methods and data processing
- Phytoplankton: microscopic enumeration; counts of dominant species summed to genus level to reduce analyst variability.
- Chlorophyll: standard spectrophotometric method (Talling 1974) on filtered samples.
- Zooplankton: species-level counts from net tows; aggregate crustacean counts from filter papers.
- Fish: annual mean CPUEs calculated by species, method, and basin; standardized nets and sampling protocols described across decades.
- Data used in analyses span multiple periods (e.g., phytoplankton 1978–2003/2005; chlorophyll 1964–2009; zooplankton 1964–2009; fish data from 1940–present).

## Provenance, rights and access
- Originators: Freshwater Biological Association (FBA); later CEH and predecessor IFE.
- Rights: Database Right / Copyright © NERC - CEH / Freshwater Biological Association.
- Access note: strongly recommended to contact data authors directly prior to reuse.

## Metadata, discoverability and documentation
- Sites and location data provided (Windermere NBAS/SBAS, Esthwaite Water, Blelham Tarn) with approximate grid references.
- Supplementary Table S1 referenced in Burthe et al. 2015 for full details.
- Documentation includes column definitions and data provenance, enabling cataloging and cross-dataset linking.

## Data quality assurance and governance
- QA decisions documented, e.g., aggregation of phytoplankton counts to genus level to harmonize across analysts.
- Longitudinal data spanning multiple decades with changes in methods; metadata explains counting chambers, analysts, and sampling details to support interoperability.
- Editorial notes emphasize cautious reuse and direct author engagement for data provenance verification.

## Storage, sharing and maintenance considerations
- Data stored as CSV files with explicit metadata for each column.
- File sizes vary (ranging from ~23 KB to ~2.5 MB), indicating a mix of concise and richer datasets.
- Stewardship needs: maintain provenance links to methods, ensure continued accessibility, and update metadata if datasets are rehosted or reformatted.

## Challenges and considerations for Data Stewards
- Incomplete picture of user needs and priorities may hinder discovery and reuse.
- Timely acquisition of data from ongoing or fragmented sources.
- Variation in data standards across different data creators and over long time spans.
- Interoperability across multiple systems and formats; large, potentially unwieldy datasets.
- Older databases and legacy methods may require bespoke, non-interoperable solutions.

## Contact and reuse guidance
- For re-use, practitioners should reach out to the original data authors to verify provenance and obtain any additional context or permissions.