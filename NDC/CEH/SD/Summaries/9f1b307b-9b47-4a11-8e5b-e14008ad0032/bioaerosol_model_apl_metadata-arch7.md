# A brief description overview of the data being described

## Purpose and scope
- Import templates for dispersion modelling of Aspergillus fumigatus from outdoor composting sites across England (2008–2014).
- Model outputs hourly concentrations (where data exist) at postcode-weighted centroids.
- Postcode centroids within 4 km of open composting sites are modelled hourly.
- Intended to understand likely exposure near outdoor composting sites; produced within ADMS 5 (requires ADMS 5 to run).
- Collected by the Air Quality Management Resource Centre (UWE) and The Small Area Health Statistics Unit (Imperial College London).

## Data and model design
- Aim: first population exposure estimates near 217 operating large-scale outdoor composting facilities in England (2005–2014) using existing A. fumigatus modelling parameters.
- Model parameters are auto-generated when model files are uploaded.

## ADMS source parameters
- Source height: 3 m; pollutant exit velocity: 2.95 m/s; pollutant temperature: 29°C.
- Emissions from composting facilities treated as area sources.

## ADMS pollutant parameters
- PM2.5 used as a proxy for bioaerosol concentrations.
- Concentrations converted from CFU/m³ to g/m³ (1 CFU/m³ = 1 g/m³) due to model limitations.
- Time-varying emission factors (TVEF) capture daily/seasonal variability.
- Daily emissions: 9×10^6 g m⁻² s⁻¹ during operational periods (assumed 8:00–17:00, Mon–Fri).
- Dormant hours: 11×10^3 g m⁻² s⁻¹.
- Seasonal variation: monthly variations based on Defra composting tonnage, offset by one month.

## ADMS meteorological inputs
- Nine nearby meteorological stations used: Boulmer, Church Fenton, Coleshill, Crosby, Heathrow, Isle of Portland, Lyneham, Marham, Spadeadam.
- Data from nine stations via MIDAS SYNOP format (CEDA).
- Surface roughness: urban 1 m; rural 0.3 m (based on land use in ADMS).

## ADMS pollutant prediction area
- Concentrations modelled for residential postcodes (average ~12 households) within 4 km of a facility.
- Postcodes sourced as X, Y centroids from ONS; coordinates updated yearly (2005–2014).
- Duplicates removed; data imported into ArcMap 10.2; cropped to postcodes within 4 km of the 217 facilities.

## ADMS model outputs and data structure
- Outputs provided as short-term hourly sequences; yield daily A. fumigatus concentrations (g/m³) at each included postcode.
- To run: upload the appropriate model file (.APL) and execute.
- Data files (.APL) are named by the nearest meteorological station and must be uploaded into ADMS; input parameters auto-populated.

## Practical GIS considerations
- Data designed for a small-area epidemiological focus, enabling postcode-level exposure mapping.
- Requires aligning postcode centroids with facility locations, weather station footprints, and surface roughness settings for accurate spatial analysis.
- Yearly coordinate changes necessitate updating dataset georeferencing and ensuring consistent spatial joins across years.

## Collaboration and references
- Data collated by the Air Quality Management Resource Centre (UWE) and The Small Area Health Statistics Unit (Imperial College London).
- Key references include ADMS User Guide, dispersion-model parameter studies, SCAIL-Agriculture, and related bioaerosol emission literature.