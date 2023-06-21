# Monte-Carlo-Simulation-of-Latitudes-and-Longitudes
This project aims to estimate the land area of nations using a Monte Carlo simulation of latitudes and longitudes. The estimation is based on the shapefile data provided by the GADM (Global Administrative Areas) database.

# Requirements
Python 3.x
geopandas
shapely
numpy
scipy
matplotlib

# How to Use
1. Clone the repository or download the project files.
2. Install the required dependencies mentioned above.
3. Run the main() function in the script to start the program.
4. Enter the name of the country for which you want to estimate the land area when prompted.
5. The program will download the shapefile for the country (if not already downloaded) and extract it.
6. It will then calculate the estimated land area of the country using the Monte Carlo method.
7. The estimated land area will be displayed in square kilometers.
8. A plot showing the country's shape will be displayed.

Please note that the estimation accuracy may vary depending on the size and complexity of the country's shape. The Monte Carlo method provides reasonable estimates for small and medium-sized countries, while for very large countries, the spherical excess calculation is used.

# Important Functions
estimate_land_area(polygons) : This function estimates the land area of a GeoDataFrame of polygons using the Monte Carlo method. It calculates the direct area for small countries and samples random points within the country's bounds to estimate the area for larger countries.

calculate_polygon_spherical_excess(polygons) : This function calculates the spherical excess of a GeoDataFrame of polygons. It converts the polygons to the WGS84 coordinate system (EPSG:4326) and calculates the spherical excess for each polygon or subpolygon in the dataset.

main() : This function serves as the entry point of the program. It prompts the user to enter the name of a country, downloads and extracts the shapefile, calculates the estimated land area, and displays the results.

# Acknowledgments
This project utilizes the GADM shapefile data provided by the University of California, Davis.
The geopandas library is used for handling geospatial data and performing geometric operations.
The shapely library is used for geometry calculations.
The matplotlib library is used for visualization.
