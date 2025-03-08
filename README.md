# Hanson-Gary-Paniagua-Dolan-Project-3-
An overview of the project and its purpose
Our project was an exploration of global happiness data, and the factors that contributed to countries' happiness. We pulled together data from the CIA world factbook, World Happiness Report and Numbeo's Quality of Life Index. The goal was to examine the relationship between different variables and the Ladder Score, which represents happiness measured on a scale of one to ten. 

Instructions on how to use and interact with the project
We have loaded the raw data into a Postgres database using a data base diagram (ERD). This data can be downloaded into an excel for further manipulation. To view our analysis, you can open the attached python file. We have cleaned and merged the data sets into a single, large data frame. 
Additionally, we have added important features such as the ratio of health care value to life expectancy, and the ratio between purchasing power and cost of living. We have also provided a regional average for the ladder score of each country. Finally, we created a function that calculates the regional average and each country’s deviation from its regional average for any given variable in the data set.


The cleaned, final versions of the original csv can be found outside the resources folder; WHR, Population, and Gini. The Quality_of_Life CSV was not edited and can be found in the resources folder.

For this project, we used SQL: The data is structured so it was not necessary to work with NoSQL. The Postgres database adequately meets the requirements of this data set.

Entity Relationship Diagram or ERD: Our ERD is attached as a .png. The schema includes four tables: Population, Gini, QOL (Quality of life), and the WHR (World Happiness Report), which are all connected by country and year attributes. The tables use a mix of categorical (e.g., country names, regions) and numerical data (e.g., GDP, health scores, safety values), ensuring efficient querying and analysis.

Ethical Considerations: The data we used is not personalized, so there was little concern for the violation of any given person’s privacy. However, there is a risk that the data we have gathered may be used to make general policy claims. We have taken into consideration not to make any sweeping conclusions based on the data we’ve gathered here. There is a great deal of bias that can be involved when using one measure of happiness globally, and it is not wise to make sweeping generalizations without an understanding of the individual cultures involved.

Extra: GeoPandas Maps
Our team used GeoPandas, Seaborn, and Folium to create a set of maps to display our previously calculated Ladder Score, Individual Country Happiness Score, Regional Happiness Score, and Regional Happiness Deviation. The following steps were completed in order:

-GeoJSON file: We used a GeoJSON file containing characteristics such as country names and their corresponding region. A static blank world map was created. Next, the total number of unique country names was extracted from the GeoJSON file and sorted. A total of 177 countries were found.
-Main_merged.csv file: The csv was loaded and the total number of unique countries was extracted. 135 countries were found.
-Difference in datasets: In order to merge both datasets and create the maps, we calculated the different countries in each dataset. This led to a filtered dataframe of 126 countries that was then used to merge both datasets by region.
-World Map by Regional Indicator: Using Folium, we created a static map showing a color-coded map divided by the regions listed in our merged dataset. A total of 10 regions were found.
-Interactive_map: Using Folium and Seaborn, we then created an interactive map detailing the same color-coded regions from the step above. The Country Name, Regional Indicator, Happiness Score, Regional Happiness Score, and Happiness Score Deviation are shown as hover text per country.
-Interactive_heatmap: We created a heatmap using the steps above. The heatmap intensity was based on the Happiness Score.

The main “Hanson-Gary-Paniagua-Dolan-Project-3-“ repo contains the following:
“gitignore” me file
“Geopandas_FINAL.ipynb” file which contains our python code for the Geopandas map.
“transform.ipynb” file which contains our python code our project.
“Resources” folder which houses the following:
- 4 datasets used in our project: 1) “Gini_coefficient.csv”, 2) “Population.csv”, 3) “Quality_of_Life.csv”, and 4) “world-happiness-report.csv”.
-It also contains the following: 1) a “custom.geo.json” file which contains data for 177 countries, 2) a “main-merged.csv” which contains a clean and merged dataset of our project that was then used to create the Geopandas map, and 3) two html links to our “interactive_heatmap” and “interactive_map”.

Please note, we used in-class activities/notes, feedback from our professor/Tam and the following resources to complete the project:

References for the data source(s): A combination of feedback from our instructor/TA, in-class activities, and the following resources were used while working on our project.

Population data: https://www.cia.gov/the-world-factbook/about/archives/2021/field/population/country-comparison

Gini Coefficient data: https://www.cia.gov/the-world-factbook/field/gini-index-coefficient-distribution-of-family-income/country-comparison

Quality of Life Indexes: https://www.numbeo.com/quality-of-life/indices_explained.jsp

World Happiness Report FAQ: https://worldhappiness.report/faq/

Additional Resources
ChatGPT: https://chatgpt.com/
Example of Drought Heatmap: https://droughtmonitor.unl.edu/
GeoJSON file: https://geojson-maps.kyd.au/?utm_source=self&utm_medium=redirect
GeoJSON Overview: https://python-graph-gallery.com/map-read-geojson-with-python-geopandas/
GeoPandas Overview: https://geopandas.org/en/stable/docs/user_guide/io.html
Leaflet vs Folium Overview:
https://medium.com/@limeira.felipe94/choosing-the-right-mapping-library-leaflet-openlayers-vs-folium-and-geemap-bdbc92f701c4#:~:text=Leaflet%20and%20OpenLayers%20are%20ideal,integration%20with%20data%20analysis%20tools.
Pip install Folium: https://stackoverflow.com/questions/61818378/how-to-install-folium-for-python-3-7
Plotting with Folium: https://geopandas.org/en/stable/gallery/plotting_with_folium.html
Quality of Life Indexes: https://www.numbeo.com/quality-of-life/indices_explained.jsp
Reading GeoJSON files: https://www.youtube.com/watch?v=Kr658rFToOs&ab_channel=BugBytes
Seaborn Overview: https://www.geeksforgeeks.org/introduction-to-seaborn-python/#
World Happiness Report FAQ: https://worldhappiness.report/faq/


