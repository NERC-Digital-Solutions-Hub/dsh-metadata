# Extensive_Intensive_Spatial_README.docx

## Project overview and authors
- Projects: Uplands-N O2 and Rothamsted Research, North Wyke, Farm Platform
- Grant numbers: NE/M015351/1, NE/M013847/1, NE/M013154/1, BBS/E/C/000J0100, BBS/E/C/000I0320, BBS/E/C/000I0330
- Authors: Alice F Charteris; Paul Harris; Karina A Marsden; Ian M Harris; Ziwei Guo; Deborah A Beaumont; Helena Taylor; Gianmarco Sanfratello; Davey L Jones; Sarah CM Johnson; Mick J Whelan; Nicholas Howden; Hadewij Sint; Dave R Chadwick; Laura M Cardenas

## Data description
- Single time-point spatial dataset covering site characteristics, soil parameters, and soil greenhouse gas (GHG) emissions for two sites: Extensive and Intensive
- Sample design:
  - Extensive site: 112 points on a 30 m × 30 m grid across 11.5 ha plus 3 random points (n = 115)
  - Intensive site: 78 points on a 15 m × 15 m grid plus 21 points on a 25 m × 25 m offset grid (n = 99) across 1.78 ha
- Geolocation: Field positions marked with GeoXT GPS (Extensive) or RTK surveying with Trimble GNSS (Intensive)
- Gas sampling: Air-tight static chambers; headspace samples collected at 0 and 60 min (Extensive) or 40 min (Intensive); two-point sampling used due to workload
- GHG measurements: N2O flux, CO2 flux, CH4 flux measured with a Perkin Elmer Clarus 580 GC (ECD for N2O; FID for CO2 and CH4)
- Soil sampling: Bulk density cores (Extensive: 0–5 cm; Intensive: 0–10 cm); soil samples stored at 4°C prior to analysis
- Soil measurements include: bulk density, water-filled pore space (WFPS), gravimetric moisture, organic matter, soil pH, extractable N forms (NO3–/NH4+), total soil C and N, C:N ratio
- Elevation, slope, and aspect derived from 1 m LiDAR data; Compound Topographic Index (CTI) derived from LiDAR

## Data headers and variables
- Site: Extensive or Intensive
- Sample_ID: Unique sample reference
- Grid: Grid size used
- Easting / Northing: Grid coordinates
- N2O_flux, CO2_flux, CH4_flux: Gas flux measurements
- Bulk_density: Soil bulk density (g cm-3)
- WFPS: Water-filled pore space (%)
- Soil_moisture: Gravimetric soil moisture (%)
- Organic_Matter: Soil organic matter (%)
- Soil_pH: Soil pH
- Soil_NO3N: Nitrate nitrogen concentration (mg NO3-N kg-1 soil DW)
- Soil_NH4N: Ammonium nitrogen concentration (mg NH4+-N kg-1 soil DW)
- Total_C / Total_N: Total soil carbon and nitrogen (%)
- CtoN: Carbon to nitrogen ratio
- Elevation, Slope, CTI: Topographic variables
- Aspect: Slope orientation (degrees)
- Veg_type/Org_Spread: Vegetation type (Extensive) or organic manure spread (Intensive)

## Methods and protocols
- Gas sampling timing and chamber setup designed to balance accuracy with volume of measurements
  - Extensive: headspace sampling at 0 and 60 min
  - Intensive: headspace sampling at ~40 min, ambient-equivalent initial concentrations
- Chamber types: Smaller cylindrical chambers (Extensive) vs larger cuboid chambers (Intensive)
- Gas analysis: GC with differentiation by detector (N2O via ECD; CO2 and CH4 via FID)
- Soil analyses: Standard soil science methods applied with site-specific depths and extraction solutions
  - Bulk density: oven-dried weight (105°C, 24 h) and sieving
  - Moisture and WFPS calculations using gravimetric moisture and porosity assumptions
  - Porosity: Site-specific particle density assumptions (Extensive: 1.4 g/cm3 organic + 2.65 g/cm3 mineral; Intensive: 2.65 g/cm3)
  - pH: Different preparation for Extentive (fresh soil in water) and Intensive (air-dried, ground, sieved in water)
  - Extractable N: 0.5 M K2SO4 (Extensive) and 2 M KCl (Intensive); NO3–/NO2– and NH4+ measured via colorimetric methods or discrete analyzers
  - NOx total oxidised nitrogen: inferred as NO3– via reduction of NO3– to NO2– and Griess reaction
- Organic carbon and nitrogen: Ext ensive by TruSpec analyzer; Intensive by Carlo Erba NA2000 elemental analyzer coupled to an isotope ratio mass spectrometer
- Topography and CTI: Derived from 1 m LiDAR and related methodologies
- Data quality and comparability notes:
  - Two-point headspace sampling leverages linearity in concentration increase
  - Daytime timing minimized for measurement variability

## Data management and governance
- Metadata considerations: Detailed methodological notes and dataset provenance included
- Data sharing: Underlying data intended for public sharing, with governance and transparency considerations
- Data harmonization: Site-specific differences acknowledged (Extensive vs Intensive) and documented to facilitate interpretation and potential cross-site comparisons

## References and methodologies cited
- Gas chamber and soil analysis standards and references include De Klein and Harvey (2012); Chadwick et al. (2014); Ball (1964); Ben-Dor and Banin (1989); Davies (1974); Jones and Willett (2006); Krom (1980); Searle (1984); Moore et al. (1991); Rowell (1994); Mulvaney (1996); MAFF (1986); and related LiDAR/geomorphometric sources (Evans et al. 2014; Ferraccioli et al. 2014).