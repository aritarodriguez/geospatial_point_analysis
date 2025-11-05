# geospatial_point_analysis
**
Overview**

This script demonstrates data ingestion, cleaning, geospatial validation, unsupervised clustering, and visualization using Python. The workflow validates whether geographic points fall within a polygon boundary (e.g., city limits) and applies DBSCAN clustering to identify spatial groupings.

**Key Steps**

Data Ingestion – Reads CSV or Excel data containing latitude and longitude coordinates.

Data Cleaning – Normalizes headers, coerces numeric and datetime types, and drops rows with missing coordinates.

Geospatial Conversion – Converts the dataset into a GeoDataFrame (EPSG:4326) for spatial operations.

Polygon Validation – Imports a KML boundary file (Guayaquil), unifies polygons, and flags each point as inside or outside.

Unsupervised Clustering – Applies DBSCAN (with haversine distance) to detect spatial clusters in latitude/longitude data.

Visualization – Generates static hexbin density plots and scatter plots of DBSCAN clusters using matplotlib.

Output – Exports validated points with flags to CSV and produces an interactive Folium map (map_validation.html).

**Libraries Used**

pandas, numpy, geopandas, matplotlib, sklearn, and folium

**Outputs**

points_with_flag.csv – Cleaned dataset with polygon inclusion and cluster labels

map_validation.html – Interactive map visualization

Console summary – Cluster counts, top cluster sizes, and validation statistics
