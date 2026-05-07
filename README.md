# Wildfire Monitoring and Vegetation–Thermal Dynamics Analysis in Southeastern Australia using VIIRS, Xee, and Google Earth Engine
## Overview

Wildfires are among the most destructive environmental hazards affecting ecosystems, biodiversity, infrastructure, and climate systems worldwide. Australia, particularly its southeastern regions, frequently experiences severe bushfire events driven by prolonged droughts, high temperatures, and dry vegetation conditions. Monitoring wildfire activity and associated environmental changes through satellite remote sensing provides critical insights for disaster management, ecological assessment, and climate resilience planning.

This project presents a Python-based geospatial workflow for wildfire monitoring and vegetation–thermal analysis over a bushfire-prone region in southeastern Australia using NASA VIIRS satellite products, Google Earth Engine (GEE), Xee, and xarray. The workflow integrates vegetation condition, fire activity, and land surface temperature into a unified analysis pipeline.

The analysis focuses on three major environmental indicators:
1. Normalized Difference Vegetation Index (NDVI) — used to monitor vegetation condition and stress
2. Fire Radiative Power (FRP) — used to detect and quantify active fire intensity
3. Land Surface Temperature (LST) — used to assess thermal anomalies and wildfire-related heating patterns

Satellite datasets were accessed directly from Google Earth Engine and converted into analysis-ready xarray datasets using the Xee backend. Spatial and temporal visualizations were then produced using matplotlib.

The workflow demonstrates how cloud-based Earth Observation platforms and Python geospatial libraries can be integrated for scalable wildfire monitoring and environmental analysis.

## Study Area
The study area covers a wildfire-prone region in southeastern Australia, particularly around East Gippsland and surrounding areas within Victoria and New South Wales. This region is known for recurring bushfire activity and was heavily affected during Australia’s Black Summer fire events.

## Objectives
- Monitor vegetation dynamics using NDVI
- Detect active wildfire hotspots using FRP
- Analyze land surface temperature variability
- Explore relationships between vegetation stress and wildfire activity
- Demonstrate Earth Engine–Xarray integration using Xee

## Datasets
1. VIIRS Surface Reflectance
- Dataset: NASA/VIIRS/002/VNP09GA
- Used for:
a. NDVI calculation
b. Vegetation monitoring

- Bands used:
I1 → Red band
I2 → Near Infrared (NIR) band
- Spatial Resolution: 500 m

2. VIIRS Active Fire Product
- Dataset: NASA/VIIRS/002/VNP14A1
- Used for:
a. Fire Radiative Power (FRP)
b. Active wildfire detection

- Band used: MaxFRP
- Spatial Resolution:1 km

3. VIIRS Land Surface Temperature Product
- Dataset: NASA/VIIRS/002/VNP21A1D
- Used for:
a. Surface thermal analysis
b. Heat anomaly detection

- Band used: LST_1KM
- Spatial Resolution:1 km

1. Temporal NDVI Dynamics over Southeastern Australia during the 2019–2020 Black Summer Bushfires
<img width="1541" height="2390" alt="image" src="https://github.com/user-attachments/assets/43f05863-1d3e-4213-a792-44b9f603609a" />

2. Maximum Fire Radiative Power (FRP) Composite showing Wildfire Hotspots in Southeastern Australia
<img width="596" height="455" alt="image" src="https://github.com/user-attachments/assets/59a34ae1-e0f4-4f9d-970c-6e2eebbb5db9" />

3. Temporal Land Surface Temperature (LST) Patterns associated with Wildfire Activity in Southeastern Australia
<img width="1558" height="2390" alt="image" src="https://github.com/user-attachments/assets/732d8bb9-aae6-4e15-a522-8bd1fb8b2282" />

## Results
The analysis highlights the strong interaction between vegetation condition, wildfire activity, and land surface temperature during the 2019–2020 Black Summer bushfires in southeastern Australia. NDVI maps reveal declining vegetation health and increasing vegetation stress over time, while the FRP composite identifies concentrated wildfire hotspots and intense fire activity across the region. LST maps show elevated surface temperatures in fire-affected areas, spatially aligning with major FRP hotspots. Together, the results demonstrate how active wildfires contribute to vegetation degradation and thermal anomalies, showcasing the effectiveness of integrating VIIRS NDVI, FRP, and LST datasets for regional-scale wildfire monitoring and environmental analysis.

## Notes
1. FRP data is sparse and only contains values where active fires are detected.
2. Maximum FRP composites provide better wildfire visualization than daily FRP time series.
3. VIIRS datasets provide near-daily global observations suitable for regional wildfire monitoring.
4. Using Xee enables efficient Earth Engine integration with Python multidimensional analysis workflows.

## Limitations
- Several limitations should be considered when interpreting the results:
- FRP products only detect active fire pixels and may miss small or short-duration fires.
- Cloud cover and atmospheric conditions can affect NDVI and thermal retrievals.
- LST represents surface temperature rather than near-surface air temperature.
- Spatial resolution of VIIRS products may not capture fine-scale fire behavior.
- Maximum composites summarize fire activity but do not preserve exact temporal progression.
- Wildfire dynamics are influenced by additional factors such as wind, humidity, fuel load, and topography, which were not explicitly included in this workflow.

## Potential Applications
1. Wildfire hotspot monitoring
2. Environmental hazard assessment
3. Vegetation stress analysis
4. Post-fire recovery studies
5. Climate and ecosystem monitoring
6. Disaster management support
