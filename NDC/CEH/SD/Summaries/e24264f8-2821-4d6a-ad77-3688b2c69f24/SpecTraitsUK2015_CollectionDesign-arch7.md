# Field site and sampling

- Spatial context
  - Location: Mickleham, Surrey, UK; latitude 51°16'N, longitude 0°19'W (approximately 51.2667, -0.3167).
  - Sites reflect two soil types: deep alluvial soils (river Mole banks) and shallow chalk soils on a steep south-facing escarpment.
  - Soils and chemistry: chalk soil is alkaline (pH 7.9 ± 1.0; n = 10) with rendzina characteristics; alluvial soil near neutral (pH 6.7 ± 0.2; n = 10) with loamy texture; phosphorus more available in neutral soils, while alkaline chalk reduces phosphorus availability.
  - Implications for data: soil depth and composition influence nutrient availability and plant traits; geospatial context supports mapping of soil-type–trait relationships.

- Field sampling design
  - 66 trees sampled across six species; six species common to both sites: Acer campestre (field maple), Acer pseudoplatanus (sycamore), Corylus avellana (hazel), Crataegus monogyna (hawthorn), Fraxinus excelsior (ash), Sambucus nigra (elder).
  - For each tree: two fully sunlit branches collected, stored in a cool box, and transported to the lab within two hours.
  - Leaves and leaf disks: from each branch, ten mature leaves selected; three samples of 15 leaf disks cored with a 6 mm corer, wrapped in foil, frozen for later chemical analyses.
  - Morphometrics: leaf area measured from fixed-height photographs against a white background (ImageJ); leaves weighed fresh, dried at 70°C for ≥72 h to obtain dry mass; Leaf Mass per Area (LMA) calculated as dry mass per fresh leaf area; leaf water content computed as (fresh weight − dry weight) / fresh weight.
  - Data scope: 22 additional leaf chemical traits measured on the leaf disk samples.

- Data types and GIS relevance
  - Per-tree/per-branch identifiers, leaf-level metrics (LMA, leaf water content), and a suite of chemical traits (elemental concentrations, carbon fractions, pigments, PSII metrics, phenolics).
  - Spectral data and chemistry can be linked to spatial attributes (soil type, site coordinates) for GIS-based analyses and map-based data products.

- Leaf and canopy spectroscopy
  - Sampled: 10 leaves per branch were laid on a matt black surface for spectral measurements.
  - Instrument and range: FieldSpec 4 (Analytical Spectral Devices) measuring reflectance from 400–2500 nm.
  - Method: contact probe pressed to leaf surface with abaxial side toward the probe; calibration against Spectralon white reference every 5 samples; 10 measurements per branch averaged for analyses.
  - Data use: spectral reflectance data across visible to shortwave infrared bands for canopy/leaf trait inference.

- Chemical assays (methods overview)
  - Elemental concentrations (B, Ca, K, Mg, Mn, P, Si, Fe, Zn): ashed samples digested in nitric acid; analysis by ICP-MS.
  - Nitrogen and carbon: measured with elemental analyzer linked to isotope ratio MS to obtain N, C concentrations and stable isotopes.
  - Carbon fractions: hemicellulose, cellulose, lignin, and soluble carbon determined by sequential acid digestion (Van Soest method) using an Ankom fiber analyzer; reported on an ash-free dry mass basis.
  - Photosynthetic pigments: chlorophyll a, chlorophyll b, anthocyanins, and total carotenoids measured spectrophotometrically from leaf extracts; wavelengths used include 470, 649, 665 nm (Chl a, Chl b, carotenoids) and 530/650 nm for anthocyanins; calculations follow published equations (adjusted for chlorophyll contamination as needed).
  - PSII efficiency: maximum PSII fluorescence (Fv/Fm) derived from measurements of Fm and Fo with a PAM fluorometer.
  - Total phenolics: determined colorimetrically via Folin-Ciocalteau method (absorbance at 760 nm; tannic acid equivalents; blank with water).

- Implications for GIS-derived data products
  - Rich, multi-scalar dataset linking field-site coordinates, soil context, tree-level and leaf-level traits, spectral signatures, and chemical compositions.
  - Enables creation of map layers for site-specific trait distributions, soil–trait interactions, and spectral indices across two contrasting soil types and species assemblages.