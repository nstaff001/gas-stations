# An Analysis of Competitive Gasoline Markets

As a driver who needs to fuel up every now and then and as a consumer looking to maximize my utility, I have run into the following scenario many times:
one stretch of road with multiple gas stations on both sides that sees price variations upwards of 40 cents per gallon. I am always baffled that people choose
to go to that station charging the highest price for the same gallon of regular unleaded gasoline. Here's where my initial question spawned. "Why does there 
exist any price variation at all in small localized gasoline markets?" My hypothesis was that gas stations that cluster together have an influence on the prices
charged by their neighboring, competitive stations. More specifically, as the number of stations in an area increases, the gas price in that area decreases. 

To test this, I had to gather data on the gas prices in a designated city each day. I used the Selenium and Beautiful Soup packages in Python to webscrape the station 
names, prices, and addresses online. Additionally, I webscraped the wti crude oil price from a second site to act as a control for my study. Using the addresses
and a geocoding API, I calculated my variable of interest, the number of nearby gas stations within a half mile. This process involved converting the addresses 
into geocodes and then into latitudes and longitudes, which could be used to calculate distances between every pair. Similarly, as shown in the python notebook, 
you could use the same method to collect another variable for the distance from each gas station to the next closest one.

Finally, I imported the data into R and ran three panel regressions to analyze the effect of competition on gas prices. My results suggested that each additional firm
within a half mile radius lowers the predicted price per gallon by 2 cents holding brand and wti constant. The conclusion is that, on a small scale, increased firm 
competition lowers the equilibrium price for gasoline. Consumers see more benefit from the additional options as they can choose where they buy their gas, often at the 
station with lower prices. That being said, the magnitude of the decrease is not large, and certain brand names were shown to charge higher prices on average holding 
competition and wti constant. This phenomenon implies that there is an underlying belief among consumers that some brands of gasoline offer a higher quality product 
than others.

In the future, I would like to incorporate more control variables, collect data over a longer time period, and expand the scope of the study to many cities/regions. 
This will provide me with a more accurate picture of the mechanics within the gas market and potentially hint at consumer behavior in general. I am interested in two 
subjects: consumer behavior and spatial economics. This study catered to both interests as well as taught me how to webscrape, clean and merge datasets, and perform 
statistical analysis in R.

Edit: I have since added Tableau visualizations of the data collected in this project. The packaged workbook will include a sample of the data collected as well as three interactive maps illustrating the dynamics of competition in Fort Worth's gasoline market on May 6th, 2024. If you do not have access to Tableau Desktop, you can download Tableau Reader for free here: https://www.tableau.com/products/reader.
