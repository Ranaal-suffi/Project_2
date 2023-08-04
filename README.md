# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
I want to determine a relationship between the number of available bikes and the rating of a particular location.

## Process
### Collect data:
- Collect data from citybikes
- Collect the data from yelp lat and long from citybikes
- Collect the data from foursquares using the lat and long from citybikes
### Convert data into dataframe
- Convert all data to dataframe
### Study the results
- Isolate the columns that can be used for our statistics modeling, like the rating, the numbers of available bikes, etc.

## Results
### Initial Discovert
In the SNS pairplot result, shows that there is some relationship between how available bikes and the longititude/latitude as well as empty slots and longitutde/latitude.
This relationship was interesting to me so I calculate the correlation between different columns and I found that there was a positive correlation between free_slots and latitude but not longitude.
I found a negative correlation between available_bikes and longitude but not latitude. It was interesting because free_slots was only correlated with latitude and available_bikes was only correlated with longitude.

### Correlations
I wanted to see if this relationship was significant so I calculated the pearsonr for available_bikes and longitude and free_slots and latitude. Both were significant.
I thought there might be certain areas with higher ratings so I calculated the pearsonr for longitude and ratings and also found a significant correlation although it was positively weak based on the correlation table from earlier.

### Significance 
I completed a linear regression model for each of free_slots and latitude and available_bikes and longitde. Both suggested that the location explains the variance in the available_bikes and free_slots. From a business standpoint
this means that certain areas have more bikes than other areas in our sample.

I completed a multivariate linear regression model for rating and latitude + longitude. This model showed that 99% of the variance in rating was explained by the latitude and longitude. In other words, certain areas have restaurants
and bars that are higher rated than other areas, which means we can look into this some more.

### Conclusions
From above, there defiantly a relationship between the bike station location and number of bikes available. As well, rating and location, which may be a good place to start investigate more and look into change the bike stations location or increase number of the slots for each location or even help with bike company to make adjustment on the number of bikes the need to make available for each location

## Challenges 
- The amount of API calls wasted 24hrs because I ran out of credits
- Not having enough time to understand and study the data can give a wrong conclusion for the data

## Future Goals
Try to study the number of bikes for certain station at different time of the day and different day of the week which can be helpful to determine which time of the day or day of the week there are more demined on bikes. 
