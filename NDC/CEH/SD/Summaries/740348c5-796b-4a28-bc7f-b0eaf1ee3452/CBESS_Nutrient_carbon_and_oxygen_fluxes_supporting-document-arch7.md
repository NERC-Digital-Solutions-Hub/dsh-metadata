# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) nutrient exchange fluxes between sediment cores and overlying site water

- Purpose: Dataset of fluxes between sediment cores and overlying site water, focusing on oxygen and nutrient exchanges (O2, NPOC, NOx, Ammonia, Nitrite, Nitrate, NOx, Phosphate, Silicate) measured in sediment cores incubated in overlying seawater.

- Key variables observed: Oxygen, Non-Purgeable Organic Carbon (NPOC), Ammonia, Nitrite, Nitrate, NOx, Phosphate, Silicate; flux values reported as rates per unit area (µmol/m2/hour).

- Flux direction convention: Positive flux = from sediment into overlying water; Negative flux = from overlying water into sediment.

- Study sites and habitats:
  - Essex (UK): Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) representing saltmarsh and mudflat habitats with clay soils; coordinates provided for each site.
  - Morecambe Bay (UK): Cartmel Sands (CS), Warton Sands (WS) representing saltmarsh and mudflat habitats with sandy soils; coordinates provided for each site.
  - Habitat contrasts: Saltmarsh habitats with two soil types (clay in Essex, sandy in Morecambe Bay) and mudflat habitats with differing sediment textures (cohesive clays/mud/silt in Essex vs coarse/mobile sediments in Morecambe Bay).

- Timeframe: Field sampling campaign conducted in winter and summer 2013.

- Sampling design and methods:
  - 12 quadrats sampled per site; one sediment core per quadrat (8 cm diameter), with a 10 cm headspace above sediment surface.
  - Cores incubated in tanks of locally collected seawater under daylight-simulating lamps; experiments performed under light and dark conditions to capture light/dark fluxes.
  - Oxygen measurements via Winkler titration on water from both core water and headspace after incubation.
  - Nutrient measurements: Separate incubation with headspace water filtered (0.2 µm); nutrients measured by autoanalyzers after ~3 hours to derive fluxes.
  - Calibration and quality control: All measurement instruments calibrated with standards; measurements adjusted to flux per unit area; nitrate calculated from NOx and nitrite; data quality control performed; no anomalous data points removed.

- Data formats and structure:
  - Raw data: Nutrient and carbon concentrations stored as .txt files.
  - Processed data: Final dataset provided as .csv; calculations performed in Excel.
  - Data fields include: Season, Location (Morecambe Essex), Site (e.g., CS, WS, AH, FW, TM), Habitat (Mudflat, Saltmarsh), Quadrat Number, Scale (A–D with defined meter ranges), and numerous flux measurements for Light and Dark conditions (e.g., Light O2 flux, Dark O2 flux, Light NPOC flux, Dark NPOC flux, Light Phosphate flux, Dark Phosphate flux, Light Silicate flux, Dark Silicate flux, Light Ammonia flux, Dark Ammonia flux, Light Nitrite flux, Dark Nitrite flux, Light Nitrate flux, Dark Nitrate flux, Light NOx flux, Dark NOx flux).
  - Units: Fluxes expressed as micromol/m2/hour; concentration data converted to flux per unit area; nitrate values derived from NOx and nitrite values.
  - Special notes: NA values indicate missing measurements; scale nomenclature uses A=1 m, B=1–10 m, C=10–100 m, D=100–upper limit.

- Provenance and reference context:
  - Dataset described with methodology aligned to Thornton et al. (2007) for sediment-water inorganic nutrient exchange and nitrogen budgets in estuaries.
  - Staff responsible: Anne Cotton; with contributions from Graham Underwood, John Green, Terry McGenity, and Alex Dumbrell.

- Potential GIS applications:
  - Spatial mapping of sediment-water fluxes across multiple coastal habitats.
  - Comparative analysis of flux dynamics between Essex and Morecambe Bay sites.
  - Integration with environmental layers (habitat type, soil texture, inundation frequency) to explore drivers of nutrient exchange.