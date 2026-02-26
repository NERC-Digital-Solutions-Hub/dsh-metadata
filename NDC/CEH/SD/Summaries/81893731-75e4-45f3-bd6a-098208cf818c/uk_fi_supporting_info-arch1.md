# Collection of water samples

- Study scope
  - Fieldwork conducted in autumn (September–November) across 2018–2020.
  - Collaboration with the Faroese Geological Survey (Jarðfeingi); sampling in the Faroe Islands at sites with high organic soil content.
  - Study sites span England, Scotland, Wales, Northern Ireland, and the Faroe Islands.
  - Water samples collected from various water body types within catchments (pools, headwaters, streams, inlets, reservoirs, lakes, outlets) and from multiple locations within each catchment under access constraints.

- Sampling and site measurements
  - In situ site variables: pH, conductivity, dissolved oxygen, water temperature; ambient air temperature, pressure, humidity.
  - Grab water sampling: 50 mL per site, filtered in the field through a 0.45 µm syringe filter; samples kept cold (cold bag in the field, cold box during transit) and stored at 4 °C in the lab.
  - Laboratory analyses on filtered water: dissolved inorganic and organic carbon, absorbance at eight wavelengths, dissolved nutrients, cations, metals, and anions.

- Organic matter collection and analysis
  - At roughly one-third of sites, additional large-volume water samples collected to extract particulate organic matter (POM) by filtration (0.7 µm), then concentrated to ~100 mL.
  - Concentrated samples evaporated to dryness; residue contains colloidal and dissolved organic matter (DOM).
  - DOM and POM analyzed for elemental composition using an Elementar Vario MICRO cube (total C, N, H, O; inorganic carbon removed via acid pretreatment).
  - Derived metrics for DOM/POM include Cox (carbon oxidation state), OR (oxidative ratio), DBE/C, C/N, H/C, O/C, and prop C (proportion of total C that is organic).

- Quality assurance and quality control (QA/QC)
  - Laboratory QA: 10% of samples replicated; instruments calibrated at start and checked throughout.
  - Data QA: replicate data compared; if consistent within 95%, averaged; if not, re-analysis performed.
  - Derived CHNO metrics restricted based on physical properties after calculation.

- Datasets and contents
  - UK_FI_Water_Chemistry (N = 448)
    - Site identifiers and environmental context: site code, sampling location details.
    - In situ environmental conditions: air temperature, humidity, air pressure, bank temperature (10 cm soil probe), water temperature.
    - Site water chemistry: pH, electrical conductivity (EC), dissolved oxygen (DO).
    - Laboratory water chemistry: DOC, SUVA254, E4/E6, DON, Prop_DON, DOP, Prop_DOP, and concentrations of Ca, K, Mg, Na, Al, Mn, Fe, Pb, Cd, Co, Cu, Ni, Zn, Li (all in mg L^-1 or µg L^-1 as specified).
  - UK_FI_DOM_CHNO
    - Dissolved organic matter (DOM) elemental content: N, C, H, O, Org. C (%).
    - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C, prop C.
  - UK_FI_POM_CHNO
    - Particulate organic matter (POM) elemental content: N, C, H, O, Org. C (%).
    - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C, prop C.
  - UK_FI_SITES
    - Site metadata and classifications: Type of surface water (e.g., lakes, headwaters, inlets, reservoirs, streams, pools), primary land use (e.g., cutting/peat extraction, felled forestry, grazing, moorland, plantation, renewable energy, restored, shooting, woodland), primary vegetation cover (from CEH Land Cover maps), catchment area (km^2, via DEM models and QGIS).
    - Location context: country (England, Scotland, Wales, Northern Ireland, Faroe Islands); anonymity provisions for certain locations (reservoirs).

- Data accessibility and provenance
  - Datasets include site codes, timing, and environmental as well as chemical measurements to enable correlation and modelling.
  - Metadata and derived metrics accompany primary measurements to support reproducibility and downstream analysis.