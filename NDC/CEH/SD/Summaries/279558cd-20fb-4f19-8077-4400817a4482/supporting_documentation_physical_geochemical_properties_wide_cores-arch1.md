# Physical and geochemical properties of saltmarsh soils produced from 33 wide diameter gouge cores spanning 19 UK saltmarshes collected between 2018-2021

## Overview
- Dataset describing physical and geochemical properties of saltmarsh soils from 33 wide-diameter gouge cores across 19 UK saltmarshes, collected 2018–2021.
- Primary aim: support calculation of organic carbon burial rates across UK saltmarsh ecosystems.

## Study design and locations
- Study sites: 19 UK saltmarshes distributed around the coastline (Scotland, Wales, England) to capture representative saltmarsh sediment types and organic carbon content.
- Core sampling: 33 gouge cores with 60 mm diameter.
- Core data collection: DGPS for precise site locations; cores described using Troels-Smith classification; samples frozen at -20°C until analysis.
- Depth sampling: Cores were sectioned into 1 cm intervals, yielding 1952 sediment sub-samples.

## Laboratory analyses
- Bulk density: Wet and dry bulk density measurements (g cm^-3).
- Organic carbon and nitrogen: Total organic carbon (OC) quantified with Elementar Soli TOC using a temperature-gradient method; nitrogen content measured concurrently.
- Stable isotopes: δ13C_org and δ15N determined via EA-IRMS after carbonate removal (acid fumigation) and drying; standard preparation involved tin and silver capsules with acid treatment as appropriate.
- Calibration and QA: TOC calibrations with CaCO3 and soil standards; isotope QA through repeat analyses of high OC sediment standard; laboratory equipment calibrated per University of St Andrews practices.

## Data structure and content
- Data resource: Physical_geochemical_properties_wide_cores.csv.
- Core and site identifiers: Core_ID, Saltmarsh, Marsh_type (Natural or Realigned), Marsh_zone (Low or High).
- Geographic and collection details: Nation (Scotland, Wales, England), Collection_year, Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Elevation_above_OD_m.
- Sub-sampling metadata: Sample_depth_cm, Mid_Point_depth_cm.
- Substrate and density: Substrate (Troels-Smith classification), Wet_bulk_density_g_cm3, Dry_bulk_density_g_cm3.
- Geochemical measurements: OC_perc, N_perc, CN, NC, d13C_per_mil, d15N_per_mil.
- Data formats: CSV; site coordinates provided as decimal degrees (WGS84) and/or grid coordinates (X/Y).

## Methods in brief
- Sampling protocol: 33 cores collected from 19 saltmarshes; cores described by Troels-Smith scheme; DGPS for site positions.
- Core processing: Sections cut to 1 cm; samples weighed before/after drying at 60°C for 72 hours for bulk density calculations.
- OC and isotopes: 50 mg per crucible for TOC analysis; 12 mg processed sediment allocated for OC and δ13C, while another 12 mg for N and δ15N; carbonate removal performed on carbonate-containing samples prior to isotope analysis.
- Calibration and quality control: TOC calibration with CaCO3 and standard references; isotope QA via high OC standard repeats.

## Uses and implications
- Enables estimation of organic carbon stocks and burial rates in UK saltmarsh ecosystems by integrating OC content, bulk density, and depth data across multiple sites.
- Facilitates cross-site comparisons of OC, N, CN/NC ratios, and stable isotopes in relation to marsh type, zone, and geography.
- Provides a standardized, mappable dataset suitable for statistical analyses, modeling, and meta-analyses of saltmarsh carbon dynamics.

## References and data provenance
- Key references for methods and standards include: Troels-Smith classification, DIN 19539, Harris et al. (acid fumigation), Dadey et al. (bulk density), Natali et al. (thermochimico references), Smeaton et al. (UK marine sediment carbon stocks).
- Data produced and curated under the Project: Carbon Storage in Intertidal Environments (C-SIDE); funding by NERC (NE/R010846/1).