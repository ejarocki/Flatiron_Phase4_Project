# Phase4_Project
## Project Team:
 - [**Samira Chatrathi**](https://github.com/sgchatrathi)
 - [**Elijah Jarocki*](https://github.com/ejarocki)
 - [**Soo Ho (John) Park**](https://github.com/soohojp)

## Navigating the Repository
All data used in this project can be found in the file [`master_dataset_final.ipynb`](https://github.com/soohojp/Phase-1-Project-Best-Team-/blob/main/master_dataset.ipynb).
Each individual goal was coded separately by John for [Goal 1](https://github.com/soohojp/Phase-1-Project-Best-Team-/blob/main/Untitled%20copy.ipynb), Nick for [Goal 2](https://github.com/soohojp/Phase-1-Project-Best-Team-/blob/main/goal_2_nick_w.ipynb), and Ilene for [Goal 3](https://github.com/soohojp/Phase-1-Project-Best-Team-/blob/main/Data%20set%20cleaning%20-%20ilene.ipynb). These separate files were then joined into the [`master_dataset_final.ipynb`](https://github.com/soohojp/Phase-1-Project-Best-Team-/blob/main/master_dataset.ipynb). All images used in this README.md can be found in the [`pictures/`](https://github.com/soohojp/Phase-1-Project-Best-Team-/tree/main/pictures) folder seperated by who utilized them for which goal.

# Business Understanding and Stakeholder

In this project we work with Zillow Data from the years 1996 to 2018 to see which would be the best 5 zipcodes across the United States of America. Our definition of "best" is a zipcode that not only gives the best return on investment for the long term but is also stable. Our stakeholder is Berkshire Hathaway, the real estate conglomerate looking to expand to new markets all across the United States while also looking to see which locations will spearhead their real estate clients likelihood of the best return on investment. While the fluctuations of return on investment can be rather risky, we as a team prioritized stability as a means of long term return on investment.

# Data Understanding and Feature Engineering

We gathered data from the Zillow Dataset from April of 1996 to April of 2018. Since our definition of best relies heavily on Return on Investment we will need to feature engineer those columns into our dataset. We also decided as a team to create an expansion of locations accross America as the cultural prevelance of a conglomerate like Berkshire Hathaway calls for regional distinctions. We will feature engineer regions as well into our data frame. Finally, due to the housing bubble, where demand outweighs supply and leads to high pricing valuation that eventually pops and plummets the value of the home, we will be looking specifically within the years of 2009 to 2018.  

## Risk
Here we want to focus on the prices that have a coefficient of variance that is associated with a lower amount of risk.

## Regions


![All_forecast](time-series/photos/all_forecast.png)

# Conclusion
Through our data processing and engineering, we separated each zipcode into different regions, which are as follows: Northeast, Southeast, Midwest, Southwest, and West. Then, in our dataset, we created a new column called `ROI`, short for return on investment, by using the average sale price of 2009 as the initial purchase price and the average sale price of the last 12 months until April 2018 as the current price. With this new metric, we pinpointed which zipcodes within each region has the highest potential for investment returns. The five zipcodes with the highest `ROI` was located in Moroe, PA for the Northeast, Bolton, MS for the Southeast, North Liberty, IA for the Midwest, Fort Worth, TX for the Southwest, and finally Benton City, WA for the West. To ensure a risk averse investment strategy, our zipcodes were selected according to a coefficient of variation below the 60th percentile.

Subsequently, we applied the ARIMA and SARIMA models to forecast the future sale price of these zipcodes. Our forecasts suggest either a stabilization of price or a 9% to 63% increase in sale price in a span of 20 months. Such an increase signifies a `$5,000` up to `$110,000` increase in sale price. Considering the upward trend in sale price, investing in the zipcodes we’ve analyze can serve as potentially lucrative opportunities for our clients. Our strategy focused on risk averseness and diversification in different regions can minimize housing crashes or drastic fluctuations in price, while also securing the potential for rising real estate prices.
