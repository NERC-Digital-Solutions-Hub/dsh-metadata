# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose: documentation for a climate change manipulation site (drought and warming) at Clocaenog Forest, UK, providing protocols, data types, and processing details to support data use and analysis.

## Site and treatments

- Location: Clocaenog Forest, North East Wales (53°03'19''N, -03°27'55''W).
- Ecosystem: upland moorland dominated by Calluna vulgaris (heather); other species include Vaccinium myrtillus, Empetrum nigrum.
- Established: 1998; automated roof technology for drought and warming treatments.
- Plot design: 9 plots total (4 m x 5 m): 3 warming (W), 3 drought (D), 3 control (C). Arranged in 3 blocks.
- Treatments:
  - Drought: retractable polyethylene roof reduces rainfall on plots during growing seasons (May–Sept originally; since 2012, Apr–Oct). Rainfall reduction ~20% site-wide; some smaller rains excluded (~80% of rain removed within treatment).
  - Warming: retractable aluminium mesh curtains over plots, reflecting infrared radiation to reduce heat loss at night; activated after dusk (light threshold) and retracted during rain to limit rainfall exclusion (average annual rainfall reduction ~14%).
  - Wind exclusion: curtains prevented operation in high winds (>10 m/s) to avoid damage.
- Site-scale climate context: mean annual rainfall ~1411 mm; other site characteristics (soil: humo-ferric podzol; N deposition ~20–25 kg N ha^-1 yr^-1).

## Data collection and data types

- Data span and scope: comprehensive, multi-omics and environmental measurements collected across multiple years with varying methods over time.
- Data types (structured by category):
  - AWS meteorological data (on-site weather station)
    - Variables: air temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
    - Frequency/period: daily sensors; hourly averages; data from 1999–present.
    - Equipment/location: sensors mounted on a secured mast (4 m) after 2007.
  - Micro-meteorological plot data
    - Variables: soil and air temperature; soil moisture (gentle slope from surface to 10 cm); depth-specific soil temperature (5, 10, 20 cm); moisture via TDR (since 2008; earlier methods varied).
    - Frequency: minute-by-minute measurements; data logged as hourly (pre-2016) or half-hour averages (post-2016).
  - Rainfall data
    - Site-level rainfall: storage rain gauge (biweekly collection; 12.7 cm funnel; robustness against logger outages).
    - Rainfall chemistry: pH, NO3-, Cl-, SO4^2-, DOC, NH4+ (lab analyses; via ion chromatography and TOC).
  - Throughfall data (plot-level rainfall)
    - Method: plot-level rain collectors (diameter ~16.8 cm) with 3 replicates per plot; data biweekly.
    - Use: compute plot-level rainfall by adjusting site-level rainfall using percent reduction from throughfall data; data may be excluded if collection failed.
  - Water table depth
    - Method: permeable tubes to bedrock; manual biweekly readings (from 2009 onward); maximum measurable depths per plot provided.
  - Soil respiration
    - Method: three 20 cm diameter collars per plot; measurements using static chambers connected to IRGAs (CIRAS-2 and later LI-COR 8100-based systems).
    - Temporal coverage: 1999–2000 (CIRAS-2); 2001–2008 (CIRAS/Licor portable system); 2013–2014 (automated LI-COR 8100 with automated collars); results in mg CO2-C m^-2 h^-1.
  - Trace gases (CH4 and N2O)
    - Method: static chambers on the same collars as soil respiration; gas samples collected and analyzed via gas chromatography.
    - Sampling: multiple time points per campaign (0.25, 15, 30 minutes).
  - Net ecosystem exchange (NEE)
    - Year coverage: 2002–2004 and 2011; systems included CIRAS-2 and LI-COR 6400-based setups.
    - Processing: flux conversions to mg CO2-C m^-2 h^-1; biomass-based adjustments to account for plot-to-plot variation.
  - Photosynthesis
    - Ambient photosynthesis and response curves; two plant species (Calluna vulgaris; Vaccinium myrtillus) with leaf-area/biomass context.
    - Methods: CIRAS IRGA with PAR and Ci manipulations; several years (2001–2007) and multiple conditions (light response, A/Ci curves; fixed Ci/PAR in some years).
  - Vegetation survey data (plant biomass) – Pin Point
    - Method: pin-point, three quadrats per plot; 300 pins per plot; annual measurements (1998–2012, with gaps).
    - Conversion: pin hits converted to biomass using species-specific calibration factors; data adjusted for missing pins (scaling factor applied).
  - Canopy reflectance
    - Method: ground-based spectrometer (Ocean Optics S2000-FL) with NDVI680, NDVI570, PRI indices.
    - Timeframe: 2001–2004 (and some 2000–2004 measurements).
  - Vegetation phenology, annual growth and pathogen assessment
    - Species: C. vulgaris, V. myrtillus, E. nigrum; measurements include shoot elongation, budburst, leaf counts, flowering, and signs of herbivory/pathogen infection.
    - Timing: spring phenology and annual growth conducted across multiple years (1999–2009 window for growth metrics).
  - Vegetation chemistry
    - Determinants: C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates.
    - Material: green tissue and senesced litter; lab analyses.
  - Litterfall
    - Method: 12 litterfall collectors per plot; monthly collection (1999–2002); annual mean calculated and converted to g m^-2; carbon and nitrogen analyses on pooled year samples.
  - Root biomass
    - Methods span multiple years: soil cores (2003–2004; 5 cm x 15 cm), later cores with varied depths and WinRHIZO analysis (2011).
  - Soil microbial biomass
    - Method: chloroform fumigation-extraction (2000, 2001, 2012); DOC differences used with 0.45 KC correction to express microbial biomass carbon per g soil organic matter.
  - Nitrogen mineralisation
    - Method: paired cores; initial and final cores with 1 M KCl extraction; NH4+/NO3- analyses; rates derived from core comparisons (1998–2004).
  - SOM, SOC and bulk density
    - Derived from mineralisation cores; SOM and SOC percentages; conversion to g m^-2 using bulk density and core volume assumptions.
  - Soil solution and leachate chemistry
    - Lysimeters and tensioned soil water samplers (biweekly); pH, nitrate, chloride, sulfate, DOC; analysis by ion chromatography and TOC methods.

## Data processing, units, and methodology notes

- Data processing common themes:
  - Multiple measurement systems over time; unit conversions provided for Rs and NEE to convert raw measurements to mg CO2-C m^-2 h^-1.
  - Biomass adjustments: flux measurements adjusted for plot biomass using above-ground biomass data from vegetation surveys.
  - Throughfall adjustments: plot-level rainfall inferred from site rainfall using percent changes from throughfall data; data gaps handled by exclusion or infill with year-wide averages.
- Data structure and documentation:
  - Data tables referenced with file names (e.g., SD_*.rtf, CSVs) and accompanying methodological notes.
  - Legacy data notes: some data processing steps not always documented consistently; best-practice documentation may be incomplete for older datasets.
- Data accessibility:
  - Not all data are stored within a single portal (EIDC); contact CEH Bangor (Sabine Reinsch, Bridget Emmett) for access and details.

## Data quality, gaps, and challenges

- Data gaps and continuity:
  - Long time span with evolving measurement technologies; some measurements have intermittent coverage or methodological changes.
  - Throughfall and rainfall data require careful treatment when collectors fail or data are missing.
- Access and discoverability:
  - Some datasets reside outside centralized portals; discovery relies on contacting data custodians.
- Local scale and integration challenges (per Analysts perspective):
  - Data exist at plot-level (treatment replication across 3 blocks) enabling correlations between climate treatments and ecosystem responses.
  - Datasets span abiotic (climate, soil moisture, chemistry) and biotic (vegetation biomass, litter, respiration, trace gas fluxes) domains, suitable for cross-domain modelling but require careful harmonisation due to varied sampling frequencies and units.
- IT and data processing caveats:
  - Legacy data may lack complete processing documentation; conversions rely on stated factors and ideal gas-based calculations for gas fluxes.
  - Some datasets were processed with different equipment over time (e.g., CIRAS vs. LI-COR) requiring explicit unit conversions.

## Summary of accessibility and contact

- Primary data access may require liaison with CEH Bangor and project contacts.
- For data questions or to obtain datasets, contact:
  - Sabine Reinsch (sabrei@ceh.ac.uk)
  - Bridget Emmett (bae@ceh.ac.uk)
- Appendix materials: site and plot layout; grid references; plot codes for quadrats and measurement areas (useful for data geography and spatial analyses).

## Key takeaways for data-driven analysis

- Rich, multi-year, multi-variable dataset across abiotic and biotic aspects with plot-level replication for drought, warming, and control treatments.
- Data suitable for identifying correlations between climate manipulations and ecosystem responses (soil respiration, NEE, CH4/N2O fluxes, plant biomass changes, litter inputs, soil chemistry, etc.) and for building predictive models.
- Important cautions:
  - Heterogeneous data collection methods over time; ensure consistent unit conversions and account for methodological changes when combining datasets.
  - Throughfall-derived treatment rainfall requires careful adjustment and may yield occasional incomplete replication.
  - Legacy data may require reconstruction or verification of processing steps beyond what is documented.
- Data documented comprehensively by category, with explicit treatment descriptions, measurement protocols, and conversion factors where applicable.