# Quantum-geo-AI

Optimization problems on road networks
This research aims to bring a real-world geospatial applicationto the theory of quantum computation by converting a discrete problem  to  the  QUBO.

## Project 1- Exploring Quantum Computing Potentials in Solving a Combinatorial Optimization Problem to Minimize Exposure to Covid-19 During a City Journey

### Overview
1. Road Network Construction
      1. Export your specific area from [OSM](https://www.openstreetmap.org)
      2. Data Sanitization (import the shapefile of the road network to ArcGIS and convert it to GeoJSON format). For more details read this [instruction](https://pro.arcgis.com/en/pro-app/latest/tool-reference/conversion/features-to-json.htm)
      3. Construct road graph by using [Pandas](https://github.com/pandas-dev/pandas) and [NetworkX](https://networkx.org/documentation/latest/tutorial.html)
   
  ![Net](https://github.com/Amirhossein-Nourbakhsh/Quantum-geo-AI/blob/main/video/net.gif)
  ![Cluster](https://github.com/Amirhossein-Nourbakhsh/Quantum-geo-AI/blob/main/video/time.gif)
2. Trajectory data structure

|     id     |      datetime      |  lon | lat |
|----------|-------------|------|------|
| 1 |   02/01/2022 0:00 |  116.69171 |  39.85184 |
| 1 |   02/01/2022 0:10 |  116.69145 | 39.8571  |
| 2 |  02/01/2022 0:00  | 116.69183  |  39.8532 |
| 2 |   02/01/2022 0:10 |  116.69166 |  39.8545 |

   1. Import csv trj data to ArcGIS for GeoCoding data.
   2. Export to feature class
   3. Convert feature class to GeoJSON
   4. Convert GeoJSON to Data Frame by using [GeoPandas](https://github.com/geopandas/geopandas)
 
3. Find nearest node to each trajectory point
4. Find alternative shortest path
5. Construct Q matrix of QUBO problem
6. Run on [QBSolv](https://docs.ocean.dwavesys.com/projects/qbsolv/en/latest/)
7. Data visualization for final results

![Time](https://github.com/Amirhossein-Nourbakhsh/Quantum-geo-AI/blob/main/video/heatmap.gif)

## [Demo](https://amirhossein-nourbakhsh.github.io/Quantum-geo-AI/)
