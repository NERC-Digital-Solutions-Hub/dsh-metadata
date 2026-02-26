# Supporting documentation for Biota_CR.csv.

## Purpose and scope
- Describes the structure, meaning, and interpretation of the Biota_CR.csv dataset, which contains concentration ratios (CR) for stable elements in biota relative to soil.
- CR is calculated as CR = biota stable element concentration / soil stable element concentration.
- Data support environmental health monitoring and policy performance assessment, using RAP classifications from ICRP and standardized metadata.

## Data structure and key fields
- Sample_Code: unique sample identifier.
- RAP: sample type based on International Commission on Radiological Protection Reference Animals and Plants (RAPs).
- Sample_Description: additional description of the sample.
- Collection_Date: date of soil sample collection (format: dd month yyyy).
- Soil_used_for_CR_Calculations: identifies the soil sample(s) used to estimate the CR.
- Notes: notes on analyses or how samples were used to estimate whole-organism CR.

## Concentration ratio variables and detection limits
- Concentration ratio fields (unitless) exist for multiple elements, including I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
- Each element has a corresponding Detection_Limit_[Element] field, indicating the likely maximum CR value based on the quoted detection limit.
- For several elements, CR fields are blank when values are below detection limits, with the Detection_Limit fields providing guidance on the maximum plausible CR.
- Some elements (Cs, Ba, Tl) use multiple sub-columns (e.g., Cs, 1; Cs, 2; Cs, 3) to accommodate different reporting schemes or contexts; similar multi-column structures exist for Ba and Tl.
- For most elements, if the measurement is above detection limits, the CR is reported; if not, the CR value is not shown and the detection-limit-based value is provided instead.
- The Notes field documents any methodological specifics or how the whole-organism CR was estimated.

## Metadata, sampling, and RAP classification
- RAP (Reference Animals and Plants) classification is used to standardize sample types for comparability across datasets.
- Collection_Date uses a consistent date format to aid temporal analyses.
- The dataset architecture supports tracing back CR values to the originating soil sample(s) and biota, facilitating data provenance and reuse.

## Data quality, usage, and storage
- The documentation emphasizes verification, quality assurance, data cleaning, and transformation as part of meeting the aims of an environmental-monitoring analyst.
- Outputs derived from Biota_CR.csv are suitable for inclusion in reports, maps, and charts to monitor environmental health and policy performance over time.
- Proper storage and uploading of the resulting datasets to appropriate portals is considered a standard practice.

## Notes on interpretation and practical use
- CR values are unitless and, for animals, represent whole-organism concentration ratios.
- Non-detects are indicated by blank CR fields, with detection-limit values guiding interpretation of the maximum possible CR.
- The "Notes" column provides additional context on analyses or how whole-organism estimates were derived, aiding transparent interpretation.
- The standardized, richly annotated structure supports data integration with other monitoring datasets and facilitates broader data access for users beyond the original producers.