---
layout: archive
title: "Research Experience (Non-profit)"
permalink: /research/
author_profile: true
redirect_from:
  - /research
---

{% include base_path %}


# Flood Risk Assessment Using CHIRPS and Landsat Data in Sub-Basins

## 1. Introduction

Flooding poses a significant threat to many regions worldwide, including the Congo Basin. Effective flood risk management and mitigation require a comprehensive understanding of the factors contributing to flooding within specific sub-basins. This project utilizes a combination of CHIRPS (Climate Hazards Group InfraRed Precipitation with Station data) and Landsat data to analyze rainfall patterns and land cover changes to assess flood risk in various sub-basins.

By leveraging high-resolution precipitation data from CHIRPS and detailed land cover information from Landsat, the project aims to identify sub-basins most susceptible to flooding. This understanding is crucial for developing targeted strategies for flood risk reduction, including enhanced flood defenses, improved drainage infrastructure, and sustainable land management practices.

## 2. Background and Motivation

Flooding is a recurrent and devastating natural disaster that affects millions of people globally. Accurate flood risk assessment involves analyzing both climatic and land cover factors. CHIRPS provides high-resolution rainfall estimates, which are essential for identifying regions with significant precipitation. Landsat data offers detailed information on land use and land cover, which can be used to understand how these factors interact to influence flood risk.

In areas like the Congo Basin, where rainfall patterns and land cover changes significantly impact flood dynamics, integrating these datasets can provide valuable insights. For example, deforestation can increase runoff and reduce soil absorption, exacerbating flood risks. Therefore, understanding the relationship between rainfall and land cover is crucial for effective flood risk management.

## 3. Methodology

### 3.1 Data Collection

**CHIRPS Data:**
- CHIRPS provides high-resolution precipitation data, offering detailed insights into rainfall patterns over time.
- This dataset is used to identify regions within each sub-basin that experience significant precipitation, which is a key factor in flood risk.

**Landsat Data:**
- Landsat satellites offer detailed land cover and land use information.
- Key indices derived from Landsat data, such as the Normalized Difference Vegetation Index (NDVI) and soil moisture content, are used to assess vegetation cover and soil conditions.
- Changes in land cover, such as deforestation, are analyzed to understand their impact on flood risk.

### 3.2 Data Integration and Analysis

**Flood Risk Assessment:**
- Combining CHIRPS precipitation data with Landsat indices allows for a comprehensive analysis of flood risk.
- NDVI is used to assess vegetation health and cover, which influences soil absorption and runoff. Lower NDVI values indicate reduced vegetation cover, potentially increasing flood risk.
- Soil moisture content helps in understanding the soil's ability to absorb precipitation, with higher moisture levels indicating reduced capacity to handle additional rainfall.

**Sub-Basin Analysis:**
- The mean indices from Landsat data and CHIRPS precipitation data are used to evaluate flood risk across different sub-basins.
- Sub-basins with high precipitation and low vegetation cover are identified as more vulnerable to flooding.

### 3.3 Application of Findings

**Flood Mitigation Strategies:**
- The insights gained from the analysis are used to develop targeted flood mitigation strategies.
- Recommendations may include reinforcing flood defenses, improving drainage systems, and implementing sustainable land management practices to reduce flood risk.

**Resource Allocation:**
- Understanding the contribution of each sub-basin to overall flood risk enables more precise and effective allocation of resources for disaster preparedness and response.

## 4. Results and Discussion

The integration of CHIRPS and Landsat data provides a detailed understanding of flood risk within various sub-basins of the Congo Basin. By analyzing precipitation patterns and land cover changes, the project identifies sub-basins with the highest vulnerability to flooding. Key findings include:

- Sub-basins with significant precipitation and reduced vegetation cover are more susceptible to flooding.
- Changes in land cover, particularly deforestation, contribute to increased runoff and reduced soil absorption, exacerbating flood risks.

These findings highlight the importance of incorporating both climatic and land cover factors in flood risk assessments. The information gained is crucial for developing effective flood mitigation strategies and improving disaster preparedness.

## 5. Conclusion

This project successfully utilizes CHIRPS and Landsat data to assess flood risk in the Congo Basin. By analyzing rainfall patterns and land cover changes, the project identifies sub-basins most vulnerable to flooding and provides valuable insights for targeted flood risk management. The integration of high-resolution precipitation data with detailed land cover information enhances the accuracy of flood risk assessments, leading to more effective mitigation strategies and resource allocation.

Future work may focus on expanding the analysis to include additional factors such as topography and land use changes, as well as applying the methodology to other regions affected by flooding.

---

# Project Report: Detection of Deforestation Due to Roads, Logging, Industrial Agriculture, and Slash & Burn in the Congo Basin Using Sentinel-2 Data

## 1. Introduction

The Congo Basin, often described as the "lungs of Africa," is home to the second-largest tropical rainforest in the world. This crucial ecosystem plays a significant role in global climate regulation, carbon sequestration, and biodiversity support. However, it faces severe threats from deforestation driven by various factors including roads, logging, industrial agriculture, and slash-and-burn practices. Effective detection of deforestation due to these specific activities is essential for targeted conservation and management efforts.

This project employs Sentinel-2 satellite imagery to detect deforestation associated with roads, logging, industrial agriculture, and slash-and-burn practices. By analyzing multiple vegetation and land cover indices, including **NDVI**, **EVI**, **MSAVI**, **NDMI**, **NBR**, **NDBI**, and **NDWI**, we aim to identify and map areas affected by these activities.

## 2. Background and Motivation

The Congo Basin’s rainforest is vital for regulating the global climate and maintaining biodiversity. Deforestation caused by roads, logging, industrial agriculture, and slash-and-burn methods threatens these functions and contributes to climate change. Detecting and understanding the impact of these activities is crucial for effective conservation and sustainable management.

**Remote Sensing Techniques:**
- **Sentinel-2 Satellite Imagery:** Provides high-resolution images with various spectral bands, enabling detailed land cover analysis.
- **Vegetation and Land Cover Indices:** These indices help assess vegetation health, moisture content, burn severity, urban expansion, and water bodies.

## 3. Methodology

### 3.1 Data Collection

**Sentinel-2 Data:**
- High-resolution imagery with 13 spectral bands.
- Multi-temporal images used to derive various indices and detect deforestation.

### 3.2 Indices Calculation

**Vegetation and Land Cover Indices:**
- **NDVI:** \[(NIR - Red) / (NIR + Red)\]
  - Indicates vegetation health; decreases suggest deforestation.
  
- **EVI:** \[2.5 \times (NIR - Red) / (NIR + 6 \times Red - 7.5 \times Blue + 1)\]
  - Provides enhanced vegetation information in dense areas; lower values may indicate deforestation.
  
- **MSAVI:** \[(2 \times NIR + 1 - \sqrt{(2 \times NIR + 1)^2 - 8 \times (NIR - Red)}) / 2\]
  - Reduces soil background effects; useful in areas with sparse vegetation.
  
- **NDMI:** \[(NIR - SWIR) / (NIR + SWIR)\]
  - Assesses moisture content; changes can indicate land cover alterations.

- **NBR:** \[(NIR - SWIR) / (NIR + SWIR)\]
  - Evaluates burn severity and changes in vegetation cover due to fires.

- **NDBI:** \[(SWIR - NIR) / (SWIR + NIR)\]
  - Highlights built-up areas and urban expansion; relevant for detecting infrastructure.

- **NDWI:** \[(Green - NIR) / (Green + NIR)\]
  - Identifies water bodies and assesses moisture; useful for detecting changes related to slash-and-burn practices.

### 3.3 Detection of Deforestation

**Target Activities:**
- **Roads:** Identified by increased NDBI and changes in NDVI and EVI values.
- **Logging:** Detectable through significant decreases in NDVI, EVI, and MSAVI values.
- **Industrial Agriculture:** Revealed by changes in NDVI, MSAVI, and NDMI values, indicating land conversion.
- **Slash and Burn:** Identified by variations in NDWI and NBR, indicating recent burning and vegetation removal.

**Analysis:**
- Temporal changes in vegetation and land cover indices are analyzed to detect and map deforestation due to the target activities.
- Significant changes in indices provide insight into the impact of roads, logging, industrial agriculture, and slash-and-burn practices.

### 3.4 Application of Findings

**Conservation and Management:**
- Identified deforestation hotspots are mapped and analyzed to inform targeted conservation strategies.
- Recommendations may include enforcing anti-logging measures, controlling agricultural expansion, and addressing slash-and-burn practices.

**Policy and Resource Allocation:**
- Detection results support policy decisions and resource allocation for conservation and management.
- Monitoring outcomes guide interventions to mitigate deforestation and promote sustainable practices.

## 4. Results and Discussion

The analysis of Sentinel-2 imagery and various indices successfully detected and mapped deforestation associated with roads, logging, industrial agriculture, and slash-and-burn practices. Key findings include:

- **Roads:** Increased NDBI values and changes in NDVI and EVI identified regions impacted by road construction.
- **Logging:** Significant decreases in NDVI, EVI, and MSAVI highlighted areas affected by logging activities.
- **Industrial Agriculture:** Changes in NDVI, MSAVI, and NDMI indicated land conversion for agriculture.
- **Slash and Burn:** Variations in NDWI and NBR revealed areas affected by burning practices.

These insights emphasize the need for targeted conservation measures and timely policy interventions to address the impact of these activities on the Congo Basin’s rainforest.

## 5. Conclusion

This project effectively utilized Sentinel-2 data and multiple vegetation and land cover indices to detect deforestation due to roads, logging, industrial agriculture, and slash-and-burn practices in the Congo Basin. The comprehensive analysis provided valuable information for conservation and management efforts, highlighting the importance of continued monitoring and targeted interventions.

Future work may involve integrating additional datasets and refining analysis techniques to enhance detection capabilities and support broader conservation initiatives.

