# Digestate_HF_and_NW_Production.csv

## Dataset overview
- Supplementary documentation detailing the data structure for the Digestate_HF_and_NW_Production.csv dataset.
- Contains 7 columns and 90 rows.
- Source: digestate wheat trial conducted in 2017 at two sites:
  - Henfaes Research Center (HF)
  - North Wyke research station (NW)
- Variables come from treatments involving digestate and nitrogen fertilization, with yields measured as whole-plant and grain yields, plus Thousand Grain Weight (TGW).

## Structure and content
- Columns:
  - Site: HF or NW
  - Plot: experimental plot number
  - Block: blocking factor (1–5) in the randomized block design
  - Treatment: coded as either digestate-based treatments or nitrogen fertilizer rates
    - Digestate treatments: C (zero N control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP)
    - Nitrogen fertilizer rates: N-75, N-150, N-225, N-300 (NH4NO3 at 75, 150, 225, 300 kg N ha-1 respectively)
  - Plant_yield: whole plant yield at 100% dry matter (Tonnes ha-1)
  - Grain_yield: grain yield at 100% dry matter (Tonnes ha-1)
  - TGW: Thousand Grain Weight at 100% dry matter (grams)
- All yield data are reported at 100% dry matter; NA indicates not assessed.

## Experimental design and context
- Trials involve wheat plants grown under various digestate treatments and nitrogen addition rates.
- Plot harvest areas differ by site and treatment category:
  - HF (Henfaes): 
    - Nitrogen addition rate plots: harvest area 1.2 m × 6.5 m
    - C, D, AD, DNI, ADNI plots: harvest area 1.2 m × 14 m
  - NW (North Wyke):
    - Nitrogen addition rate plots: harvest area 2 m × 4.5 m
    - C, D, AD, DNI, ADNI plots: harvest area 2 m × 9 m

## Metadata, provenance, and standards
- Dataset name: Digestate_HF_and_NW_Production.csv
- Supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Data originate from the 2017 digestate wheat trial conducted at HF and NW, involving collaboration between Henfaes Research Center, Bangor University, and Rothamsted Research.
- Clear coding for treatments ensures traceability between digestate-based treatments and conventional N fertilizer rates.
- Units are explicitly stated (tonnes ha-1 for yields, grams for TGW); all yields are 100% dry matter.

## Data quality considerations and limitations
- 90 observations across 7 columns; potential gaps indicated by NA values (not assessed).
- Consistency needed across sites for Treatment coding (digestate vs. nitrogen-rate categories) to ensure interoperable analyses.
- Some site-specific differences in plot dimensions may affect metadata interpretation and downstream harmonization with other datasets.
- The documentation provided is a supplement; ensure linkage to the primary supporting documentation for full methodological details.

## Governance, storage, and sharing guidance
- Store with explicit linkage to the dataset name Digestate_HF_and_NW_Production.csv and its supporting documentation.
- Maintain versioning and provenance to reflect updates or corrections to the treatment codes, site labels, or yield calculations.
- Ensure metadata includes:
  - Clear definitions for all treatment codes (C, D, AD, DNI, ADNI, N-75, N-150, N-225, N-300)
  - Site identifiers (HF, NW) and their full names
  - Measurement methods for yield and TGW if available
  - Dry-matter basis confirmation (100% DM) and any preprocessing steps
- Facilitate discoverability by including this dataset in relevant data portals with cross-references to the associated supporting documentation.