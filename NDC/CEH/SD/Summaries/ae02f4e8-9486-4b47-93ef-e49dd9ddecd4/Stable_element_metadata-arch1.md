# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

- Purpose and scope
  - A dataset describing a reference site in the Chernobyl Exclusion Zone with radionuclide and stable element concentrations in biota, plus estimated dose rates.
  - Distributed via the NERC Environmental Information Data Centre (with DOI).

- Data files included
  - Concentration_ratios.csv
    - Metadata and concentration-ratio data for radionuclides/elements in biota.
    - Key fields: Sampling_date (dd/mm/yyyy), ICRP_RAP (ICRP Reference Animals and Plants), Latin_Name, Common_Name, Code (Chornobyl Center sample ID), GP_Point (sampling site), Sex, Fresh_sample_mass_kg, Tissue, sample, and per-element CRs.
    - Per-element entries include <Li, Li_CR, <Be, Be_CR, <Na, Na_CR, <Mg, Mg_CR, <Al, Al_CR, etc. up to many elements including U, Pu, Cs, Sr, Cd, Mn, Fe, Zn, Se, V, Cr, Ni, Cu, Pb, Tl, U, U, U, U, with CR defined as fresh mass concentration in biota divided by dry mass concentration in soil.
    - Data notes: non-detects and censoring explained via LOD-based estimation; if tissue contributions above 10% of body burden from below-LOD tissues, whole-body value reported as “less than”; otherwise approximations used (<10.. markers).
  - Stable_element_concentrations.csv
    - Metadata and concentration data for stable elements in biota (and soil as applicable).
    - Key fields: Sampling_date, ICRP_RAP, Latitude, Longitude, GP_point, Sex, Sample_or_tissue_type, wholebody_mass_kg, sample, and per-element measurements.
    - Per-element entries include <(Element) (LOD handling), and (Element)_mg_kg_FM (milligrams per kilogram fresh mass) and (Element)_mg_kg_DM (milligrams per kilogram dry mass) representing activity concentration in biota per mg fresh mass and per mg dry mass in soil, respectively.
    - Elements covered follow the same general pattern as radionuclide elements, with repeated blocks for each stable element (e.g., Li, Na, Mg, Al, K, Ca, V, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Cd, Cs, Ba, Tl, U, U, etc.), including latitude/longitude and tissue-level mass information.

- Key definitions and units
  - ICRP_RAP: International Commission on Radiological Protection reference animals and plants.
  - Fresh_sample_mass_kg: mass of the biota sample in kilograms (fresh weight).
  - (Element)_mg_kg_FM: concentration in biota per mg of fresh mass (stable elements).
  - (Element)_mg_kg_DM: concentration in soil per mg of dry mass (stable elements).
  - CR (Concentration Ratio): ratio of fresh mass activity concentration in biota to dry mass activity concentration in soil (for radionuclide elements).
  - Li_CR, Na_CR, Mg_CR, etc.: the concentration ratios for each element; the corresponding _CR values are unitless.
  - <Element: denotes a value reported as below the detection limit (LOD) for that element in the tissue.

- Sampling and spatial/temporal metadata
  - Sampling_date format: dd/mm/yyyy.
  - Latitude/Longitude in WGS84 coordinates (stable element file).
  - GP_Point/GP_point: sampling site identifier in the Chornobyl Centre dataset.
  - Whole body and tissue-level data include sample counts and mass information to enable body-burden and tissue-specific analyses.

- Data quality, processing, and interpretation notes
  - Non-detect handling: LOD-based estimation used to approximate total element content in a tissue; if contributions from below-LOD tissues exceed 10% of the body burden, the whole-body concentration is reported as "<" (less than); if contributions are below 10%, approximations are used and flagged with <10..
  - Repeated element blocks: the dataset provides extensive per-element CRs and concentrations; not all elements are present for every tissue or sample.
  - Data provenance: metadata accompany concentration values, enabling traceability to sampling sites and individual samples.

- Intended uses and limitations
  - Enables analyses of correlations between radionuclide/stable-element concentrations and dose estimates for biota in the Chernobyl Exclusion Zone.
  - Suitable for ecological risk assessment, dose-rate modelling, and cross-sample comparisons, with careful attention to scale, detection limits, and metadata context.

- Access and citation
  - Source: NERC Environmental Information Data Centre
  - DOI: https://doi.org/10.5285/ae02f4e89486-4b47-93ef-e49dd9ddecd4
  - Data are organized into two primary CSVs (Concentration_ratios.csv and Stable_element_concentrations.csv) with detailed field definitions and notes for interpretation.