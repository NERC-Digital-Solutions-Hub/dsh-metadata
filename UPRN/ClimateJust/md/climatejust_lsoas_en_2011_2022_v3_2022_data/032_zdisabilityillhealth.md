### Comparative illness and disability ratio (Z-Score)

**Description:**
This field (also referred to as `ZDisabilityIllHealth` in the spatial dataset) represents the standardized Z-score for the comparative illness and disability ratio within a given Lower Super Output Area (LSOA). It measures how the local prevalence of long-term illness and disability in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a highly versatile indicator used across multiple dimensions of the socio-spatial climate vulnerability index, as poor health and disability affect a community's vulnerability in several different ways:

1.  **Sensitivity (Health Domain):** High proportions of people with illnesses indicate a higher level of underlying biophysical susceptibility to the impacts of extreme weather. The experience of a flood or heatwave can worsen pre-existing medical conditions, either as an immediate one-off shock or by accelerating an adverse health trajectory. Furthermore, extreme events can restrict a person's access to vital medicines (due to loss or emergency evacuations) and can cause power losses that prevent the use of complex, home-based healthcare systems, such as home dialysis.
2.  **Inability to Respond & Recover (Mobility Domain):** High rates of illness and disability also serve as a proxy for limited physical mobility. Limited mobility creates significant practical challenges when a community needs to take immediate action during a flood or heatwave, and hinders their long-term recovery. Individuals with disabilities require a significantly higher amount of resources, assistance, and planning to safely evacuate and reach the same level of post-event well-being as those without disabilities.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher comparative illness and disability ratio than the national average, indicating higher relative vulnerability.
*   **Values around 0** indicate that the ratio is approximately average for England.
*   **Negative values** signify a lower illness and disability ratio than the national average, indicating lower relative vulnerability.

To help map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD). Specifically, it utilizes the "Comparative Illness and Disability Ratio" indicator from the Health Deprivation and Disability Domain, which is originally sourced from the Department for Work and Pensions. It carries a weight of 0.143 within the "Sensitivity" dimension's Health domain, and a weight of 0.200 within the "Mobility" domains of both the "Inability to Respond" and "Inability to Recover" indices.