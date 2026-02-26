# Description, Experimental Design and Collection

- This dataset contains glucosinolate concentrations from Brassica napus plants grown in FreeAir Diesel and Ozone Enrichment (FADOE) rings. Full FADOE configuration and quality control details are described in reference [1].
- Each sample is coded by Sample_ug_g-1_dw (Column A) and linked to a Ring (Column B). Rings were placed in a wheat field in 2018 (Field coordinates provided) and moved to an adjacent field in 2019.
- Experimental treatments (Column C): four pollutant conditions—diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON; natural air).
- Aphid inoculation: plants were inoculated at five weeks with 50 aphids, 10 aphids, or no aphids. Leaves analyzed came from three plants per sample, with aphids_present indicating presence (Yes) or absence.
- Sampling and replication: after harvest, leaves were freeze-dried and ground; up to three replicate samples were analyzed per ground sample (Column F indicates Replicate).
- Analytes and data structure: seven glucosinolates measured by LC-MS (Columns G–M) with aggregate metrics including Indole_GLS (Column N), Aliphatic_GLS (Column O), and Total_GLS (Column P).
  - Seven glucosinolates: Progoitrin, Glucoalyssin, Gluconapin, Glucobrassicanapin, Glucobrassicin, 4-methoxyglucobrassicin, and Neoglucobrassicin.
- Data collection and analysis methods:
  - Glucosinolates identified using LC-MS per protocol in reference [2].
  - Total concentrations reported as indolic, aliphatic, and combined totals.
- Provenance and quality control:
  - Full FADOE methodology, including quality control measures, documented in reference [1].
  - LC-MS protocol and postharvest glucosinolate considerations described in reference [2].
- Data context and usage:
  - Data enable analysis of how air pollutants and aphid treatment influence glucosinolate profiles across rings, treatments, and plant replicates, including season-to-season field moves (2018 to 2019).
- References:
  - [1] Ryalls et al. 2022. Anthropogenic air pollutants reduce insect-mediated pollination services. Environmental Pollution, 297, 118847.
  - [2] Jasper et al. 2020. Growth temperature influences postharvest glucosinolate concentrations and hydrolysis product formation in rocket salad. Postharvest Biology and Technology, 163, 111157.