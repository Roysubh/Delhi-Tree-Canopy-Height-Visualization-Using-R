# Delhi-Tree-Canopy-Height-Visualization-Using-R

Overview:
This project demonstrates how to analyze and visualize tree canopy height in New Delhi using high-resolution Canopy Height Model (CHM) data. 
Using R, we process geospatial data to create both static and interactive visualizations. 
The workflow combines spatial data processing, raster manipulation, and map rendering to showcase New Delhi's tree canopy height distribution.

Prerequisites:
Ensure you have R installed along with the following libraries:
pacman
sf
terra 
chmloader
maptiles
tidyterra
classInt
tidyverse
leaflet
htmlwidgets

Steps:
1. Install and Load Libraries
Start by installing the required libraries using pacman to streamline package management.

2. Define a Region of Interest (ROI)
Using New Delhi's coordinates (28.6139° N, 77.2090° E), define a 3 km buffer zone to limit the data extent for efficient processing.

3. Download Canopy Height Data
Use the chmloader package to download Canopy Height Model (CHM) data for the ROI. The CHM provides the height of the tree canopy in meters.

4. Process Canopy Height Data
Replace zero values with NA to ensure a clean visualization. Use the terra package for raster processing.

5. Add Street Map Tiles
Download street map tiles from OpenStreetMap using the maptiles package. These tiles provide a geographic context for the CHM data.

6. Create Static Map
Combine the CHM raster with street tiles to create a static map using ggplot2 and tidyterra. A gradient color palette represents varying tree heights across the region.

7. Generate Interactive Map
Use the leaflet package to create an interactive map that allows zooming, panning, and exploring canopy heights dynamically.

8. Export Outputs
Save the static map as a high-resolution PNG image and the interactive map as an HTML file for sharing.

Optional Features:
  Dynamic Zoom Level for Street Tiles
  Adjust the zoom level when fetching street tiles to balance resolution and area coverage.

  Regional Expansion:
  The workflow can be easily adapted for other regions by modifying the coordinates and buffer size.

Conclusion:
This project provides a robust workflow to visualize tree canopy height in urban areas. 
By leveraging R's spatial processing capabilities, we can create insightful maps for ecological analysis, urban planning, and more.

Additional Resources:
  OSM Data: "https://www.openstreetmap.org/#map=4/21.84/82.79"
  CHM Data: "https://github.com/TESS-Laboratory/chmloader"



