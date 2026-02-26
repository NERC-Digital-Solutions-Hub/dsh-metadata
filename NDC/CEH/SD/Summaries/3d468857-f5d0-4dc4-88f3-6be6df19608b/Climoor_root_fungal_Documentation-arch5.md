# Soil sampling

- A dataset detailing soil sampling, root extraction, measurement, and fungal colonisation assessments conducted on 1 April 2015 at a Calluna vulgaris site.
- Experimental design: three treatments (warming, drought, control) with multiple plots; three replicates per plot for each treatment.
- Sampling scope: soil cores (8 cm diameter) from 0-8 cm depth near Calluna vulgaris shrubs, stored at 4°C to minimise moisture loss.

## Methods and measurements

- Root extraction and cleaning
  - Cores cut into 1 cm subsections; roots of C. vulgaris isolated, cleaned to remove debris, and stored in deionised water at 4°C.
  - Larger roots (>1 mm) identified as C. vulgaris; fine roots verified by tracing to larger identifiable roots; necrotic roots discarded.
- Root measurements
  - Metrics such as root length, diameter, and number of root tips measured with WinRHIZO v3.2 on a flatbed scanner (300 dpi, 24-bit, 5 mm water layer).
  - Fine roots (≤1 mm) prioritized for microscopy; larger roots weighed after oven-drying at 70°C for 24 h.
- Fungal colonisation measurements
  - Processing included KOH treatment and vinegar-ink staining; microscopy used to identify ericoid mycorrhizal (ErM) colonisation by hyphal coils in cells.
  - Observations used a 40x magnification with a graticule for consistent scoring of ErM and presence of Dark Septate Endophytes (DSE).
- Quality control
  - Tested multiple KOH concentrations/durations to confirm consistency; example photographs used to standardise colonisation scoring; data checked for outliers and improbable values.

## Data structure and key fields

- Dataset size: 53 columns and 72 rows.
- Core identifiers
  - A: Entry = Unique ID; B: Plot; C: Depth (cm); D: Treatment (warming, control, drought); E onward: numerous measured variables.
- Measurement fields (selected groups)
  - WinRHIZO-derived metrics: AnalysedRegionArea_cm2, Length_cm2, SurfArea_cm2, AvgDiam_mm, LenPerVol_cm_m3, RootVol_cm3, Tips, DryWeightAll_g, DryWeight2mm_g; and multiple root length measurements (Length_Root1 to Length_Root5).
  - Root samples and structure: Data points for various root segments and depths.
- Colonisation and endophyte data
  - ErM_0_Root1 to ErM_0_Root5; ErM_0_1_Root1 to ErM_0_1_Root5; ErM_1_10_Root1 to ErM_1_10_Root5; ErM_10_50_Root1 to ErM_10_50_Root5; ErM_50_90_Root1 to ErM_50_90_Root5; ErM_90_100_Root1 to ErM_90_100_Root5 (counts of segments with varying ErM colonisation levels).
  - DSE_Root1 to DSE_Root5 (counts of segments with DSE).
- Data provenance and description
  - The dataset entries are described as unique combinations of plot and depth, with explicit unit and description fields for each column.

## Governance and usability considerations for Data Stewards

- The dataset provides comprehensive methodological metadata (sampling, processing, imaging, staining, and scoring procedures) essential for reproducibility and reuse.
- Clear treatment design and depth information support robust metadata and filtration in data portals.
- The rich per-root and per-segment colonisation data enhance scientific value but require careful data dictionaries and user guidance to avoid misinterpretation.

## Challenges and considerations

- The dataset contains a large number of derived and categorical fields (e.g., multiple ErM and DSE colonisation categories across several root segments and depths), which may complicate interoperability and require thorough metadata for reuse.
- Potential alignment with user needs: ensuring that the dataset’s extensive supplementary fields are discoverable and clearly documented for data users not involved in the original study.
- Handling of multiple data streams and formats (root measurements, microscopy observations, and imaging-derived metrics) necessitates consistent naming conventions and versioning for future updates.

## Implications for data sharing and stewardship

- To maximise discoverability and reuse, accompany the data with a detailed data dictionary, methodology notes, and a data lineage narrative.
- Include explicit units, data types, and acceptable value ranges, along with any embargo or usage restrictions.
- Consider publishing to a data portal with the dataset’s metadata, linking to protocols, QA checks, and any supporting raw images or scans.