
# Bike Sharing for Des Moines

## Overview

NYC has an excellent bike sharing service called Citibike. It's useful for daily commuters and tourists alike. After spending a few days in NYC as tourists where they have used the Citibike extensively, two tourists for Des Moines, Iowa decided to try launching something similar in their hometown. They have a potential investor to provide them the seed money.


### Resouces

- Data resource: 201908-citibike-tripdata.csv, citibike_new_tripdata.csv
- Tools: Tableau Public, Jupyter Notebook

### Purpose

The purpose of this analyses is to explore the NYC Citibike data through visualization in order to pursue investors to fund a bike sharing service in Des Moines, Iowa.

The visualizations as a story can be found at this [Link](https://public.tableau.com/app/profile/nusrat.jahan7803/viz/NYCCitibikeViz/NYCCitibikeViz)

## Results

### Transformation of tripduration variable

Using Pandas, created a dataframe from our data source and changed the datatype of the **tripduration** column to **Date and Time** format. Gender column categories were given descriptive names as **Male**, **Female** and **UNknown**.

![New tripduration Df](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/New_Tripduration.png)

### Biking Trend

The data show evidence that the current generation of people use bike more than previous generations.

![Biking trend](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Bike%20trend.png)


### User Breakdown

**81%** users of NYC Citibike are **Subscribers**. By gender, **65%** of users are **Male** and **25%** of them are **Female**.

![User Type](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/User%20type.png)

### Where do the trips originate from?
Most trips originate in **downtown Manhattan**, i.e., the business district. 

![Starting Locations](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Starting%20Locations.png)

### Where do they end?
Again, destinations of most trips are often the same stations as popular origins indicating **concentrated use** within certain areas.

![Ending Locations](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Ending%20Locations.png)

### How long do the trips last?
Most trips are short, **less than 10 minutes**. This pattern holds regardless of gender.

![Checkout Time by Users](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Checkout%20time%20for%20users.png)

#### Is there variation in trip duration by gender?
The pattern of trip durations where most of these are short holds regardless of gender.

![Checkout Times by Gender](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Checkout%20times%20by%20gender.png)

### Are some weekdays busier than others?
Most trips occur on weekdays at rush hours (**8-9am and 5-7pm**). Wednesdays are an exception. On weekends, most trips are taken between **10am and 5pm**.

![Trips by Weekdays per Hour](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Trips%20by%20Weekday%20per%20hour.png)

#### Is there any interplay between gender and user type, and weekdays and hours?
The pattern of use by weekday and hour holds regardless of gender. However, the pattern is due to Subscribers. For non-subscribers (Customers), not much variations can be seen by weekdays.

![Trips by Gender, Weekday and Hour](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Trips%20by%20Gender%2C%20Weekday%20and%20Hour.png)

However, there's a more pronounced difference in levels of use between weekdays rush hours and weekends daytime for Male users than Females.

![Usertype by gender and weekday](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Usertype%20by%20gender%20and%20weekday.png)

### Is the bikesharing load distributed evenly?
It's worth noting that a small proportion of bikes are used heavily compared to other ones. We could expect that these bikes will requires frequent maintenance and/or replacing.

![Bike Utilization](https://github.com/Nusratnimme/citibike-sharing/blob/main/Images/Bike%20Utilization.png)

## Summary

The findings indicate that NYC Citibike service is a very successful enterprise. It appears that most users use it for commute to work as is evident from the weekdays and hours of peak usage, and the locations of the busiest stations. The short duration of the trips also suggest commuting as opposed to tourism/sightseeing. Most users are subscribers. Probably due to bike usage being concentrated in the business disctrict areas, some bikes are used significantly more than the others and may need more frequent servicing.

The key takeaways for a potential bike sharing service in Des Moines would be that:
- the downtown area with offices should be better served;
- incentives should be created for users to subscribe.

### Further Analyses

- A map visualization could be created to show **most popular routes** by using frequencies of the unique start and end station pairs. This could suggest which areas of the town needs to have better biking infrastructure such as bike lanes with physical barriers, etc.
- As we know that some bikes tend to be used a lot more than the others, a map visualization could be created to show the destination stations of the heavily used bikes. This is to determine whether heavily used bikes end up concentrated into popular stations. If that's the case, efforts should be made to move them around to more evenly ditsribute the usage load.    
