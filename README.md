Smart City Traffic Optimization: Bengaluru Congestion Hotspots Analysis -
This project analyzes traffic patterns in Bengaluru using a public dataset of daily traffic observations across major areas and junctions. 
The goal is to identify the most congested locations and provide actionable insights for smart city traffic management.

Live Interactive Dashboard  
(https://public.tableau.com/views/SmartCityTrafficOptimization/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

Project Motivation :
Bengaluru consistently ranks among the most congested cities in India and globally, with drivers losing significant time in traffic daily. 
While the city has begun rolling out the Bengaluru Adaptive Traffic Control System (BATCS) — an AI-driven signal optimization system —
prioritizing junctions for deployment is critical for maximum impact.

This analysis aims to:
- Pinpoint junctions with the highest traffic volume, lowest average speeds, and highest congestion levels
- Provide data-driven recommendations for where adaptive signal technology would deliver the greatest improvement

Dataset:
The analysis is based on the "Bangalore's Traffic Pulse" dataset (2024), containing approximately 8,936 daily records with the following key fields:
- Date
- Area Name (e.g., Koramangala, Hebbal, Indiranagar)
- Road/Intersection Name
- Traffic Volume (vehicles per day)
- Average Speed (km/h)
- Congestion Level (%)

A combined "Location" field was created by concatenating Area Name and Road/Intersection Name to uniquely identify each junction.

Key Findings:
The analysis revealed clear patterns:
- 'Koramangala' junctions (Sony World Junction and Sarjapur Road) consistently show the highest daily traffic volume (~41,000 vehicles) and lowest average speeds (~36 km/h).
- 'M.G. Road' (Trinity Circle and Anil Kumble Circle) and 'Indiranagar' (CMH Road, 100 Feet Road) follow closely in both volume and congestion.
- 'Hebbal Flyover' and 'Silk Board Junction' also appear regularly in the top lists, confirming their reputation as major bottlenecks.

These locations experience congestion levels as high as 94%, indicating near-constant gridlock during peak periods.

Methodology:
1. Data Cleaning
   Removed invalid records (zero speed, missing values) and created a unique location identifier.

2. Hotspot Identification  
   Ranked locations by three metrics:
   - Daily average traffic volume
   - Average speed (lowest = worst)
   - Congestion level percentage

3. Visualization 
   - Python (pandas, matplotlib) for initial exploration and static charts
   - Tableau Public for interactive dashboard with bar charts and filtering

4. Recommendation  
   - Prioritize deployment or expansion of the Bengaluru Adaptive Traffic Control System (BATCS) to the top 10-15 identified hotspots.
   - Early pilots have shown 20-33% reduction in delays at equipped junctions.

Repository Structure:
├── data/
│   └── raw_traffic_data.csv          #Original dataset
├── notebooks/
│   └── Smart_City_Analysis.ipynb     #Full analysis with code and comments
├── outputs/
│   ├── top_volume_hotspots.png
│   ├── lowest_speed_hotspots.png
│   └── bengaluru_traffic_hotspots_map.html (optional interactive map)
└── README.md

Tools Used:
- Python (pandas for data processing, matplotlib for charts)
- Jupyter Notebook in VS Code
- Tableau Public for interactive dashboard

Future Enhancements:
- Incorporate hourly data if available for peak-hour analysis
- Add geospatial visualization with latitude/longitude coordinates
- Compare pre- and post-BATCS performance at equipped junctions
------------------------------------------------------------------------------
Created by [ Sarveshwar Bhujade ] 
December 2025

