# Extent and tree species composition from a Scottish deciduous woodland survey, 1976-1979 Dataset Summary

- Purpose and scope
  - Census of deciduous woodlands in Scotland (including those with some admixture of conifers) to estimate extent and canopy species composition.
  - Aimed to determine distribution by species and regions, compare with 1947/1965 censuses, develop ecological classification, and map distribution of woodland types.
  - Geographic coverage: Scotland; time period: 1976–1979; data categories: woodland locations and canopy species percentage estimates.

- Survey design and methods
  - Initial step: map-based search of OS 7th Series 1:63,360 maps for woods >5 ha marked as deciduous; mixed stands included due to inability to estimate exact composition.
  - Ground-truthing: field surveys recorded canopy composition by visually estimating canopy percentages; checks ensured consistency between observers.
  - Key questions per wood: existence on map and canopy species percentages.
  - Survey teams: 1976 (926 woods, led by J.E.A. Proctor), 1977 (1913 woods, led by R.C. Munro), 1978–79 (completion), total 3744 woods.
  - Canopy assessment rules: only canopy-forming species recorded; understorey recorded only if part of canopy; open canopies and gaps handling (gaps >50% often led to deletion from records); exotics recorded separately; woods with >50% exotics typically deleted unless justified; conifer-broadleaf blocks treated as separate units.

- Data structure and contents
  - Data source: woodland survey results used to create a digital database; field data collected on paper summaries and computer printouts.
  - Main dataset: ScottishDecWoods_1976_79.csv with per-wood records including:
    - Identifiers and location: Site_Sheet, Number, Name, Easting, Northing, OS_GridRef, Area_ha.
    - Canopy percentages by species: Ash (AS), Beech (BE), Elm (EL), Exotics (EX), Sycamore (SY), Whitebeam (WH), Alder (AL), Birch (BI), Rowan (RO), Willow (WI), Aspen (AP), Scots Pine (SP), Hazel (HZ), Holly (HY), Oak (OA), Other (O), Cherry (CH), Lime (LI), Blackthorn (BL), Hawthorn (HA), Yew (YE), Poplar (PO), plus Total canopy percentage.
    - Metadata: Remarks, DEL_NOACCESS status (e.g., wood no longer exists, inaccessible, or lacking data); Total (count of canopy data).
  - Additional notes: grid reference chosen near centre of wood; name sourced from map or nearest feature; some data gaps acknowledged.

- Data quality, provenance, and rescue
  - Data quality: field procedures devised by J.E.A. Proctor; cross-checks between observers; comparisons with Nature Conservancy Council surveys in Dumfries and Galloway region; checks against basic data bank and map verifications.
  - Data rescue and digitisation: 2019–2024 data entry from original paper summaries and printouts; double-checked against final 1979 report; handwriting introduced potential site name errors; some discrepancies due to historic administrative boundaries or map revisions.
  - Verification: summaries compared with Bunce et al. (1979) and Parr (1981) where possible; major discrepancies identified and rectified.
  - Baseline considerations: OS maps served as a starting point but not a strict baseline due to uncertain revision histories (1954–1967).

- Data availability and usage notes
  - The dataset includes maps illustrating distribution by species (e.g., Hawthorn, Hazel, Oak, Rowan, etc.).
  - Main limitations: exclusion criteria and deletions mean some woodland types may be underrepresented; inconsistencies in inclusion of woods under 5 ha; some woods recently underplanted with conifers or undergoing felling may have been marked “delete.”
  - Intended uses: support ecological classification, analysis of woodland extent and composition, historical comparisons with earlier censuses, and informing landscape-scale forestry and conservation insights.

- Acknowledgements and references
  - Original survey management and analysis: Bunce, Munro, Parr, Procter (1970s)
  - Data entry and management (2019–2024): Wood, Dodd, Balmer, Walker, Draycott, Wright
  - Key references: Bunce et al. 1979; Parr 1981; Shaw & Bunce 1971 (National Woodlands Classification)