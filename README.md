# Zomato-Insights
This project involves analyzing restaurant data from Zomato to extract insights such as ratings distribution, the impact of online ordering, and average costs for different dining types.Data cleaning and visualization techniques were employed using Python libraries like Pandas, Matplotlib, and Seaborn.

# Table of Contents
Installation
Dataset Overview
Data Cleaning
Analysis
Type of Restaurant
Ratings Distribution
Cost Analysis for Couples
Impact of Online Ordering
Conclusion
Installation
Clone this repository.


"git clone https://github.com/your-username/zomato-data-analysis.git"


Install the required Python libraries.

"pip install pandas matplotlib seaborn"

# Dataset Overview:-
The dataset used in this project contains information about 148 restaurants, including:

Name of the restaurant
Whether it supports online ordering
Availability of table booking
Restaurant rating
Number of votes
Approximate cost for two people
Type of restaurant (e.g., Buffet, Dining)

# Data Cleaning:-
The ratings were initially in a string format with a scale (4.1/5). A helper function controlRate() was used to convert the ratings into numeric format.
Missing or irrelevant data was checked, and unnecessary columns were removed.


# Analysis:-
Type of Restaurant
The data showed that most restaurants fall under the "Dining" category, while "Buffet" was less common.

"sns.countplot(x=dataframe['listed_in(type)'])
plt.xlabel("Type of restaurant")"


# Ratings Distribution:-
We explored the distribution of restaurant ratings. The majority of restaurants received ratings between 3.5 and 4.

"plt.hist(dataframe['rate'], bins=10)
plt.title("Ratings Distribution")
plt.show()"


# Cost Analysis for Couples:-
The data showed that couples typically prefer restaurants with an approximate cost of ₹300.

"sns.countplot(x=dataframe['approx_cost(for two people)'])"

# Impact of Online Ordering:-
We analyzed the impact of online ordering on ratings. Restaurants that supported online ordering generally had higher ratings.
A heatmap was created to visualize the relationship between restaurant type and online ordering.

"sns.heatmap(pivot_table, annot=True, cmap="YlGnBu", fmt='d')
plt.title("Heatmap: Online Orders vs Restaurant Type")"

# Conclusion:-
Dining restaurants primarily accept offline orders, while cafes tend to receive more online orders.The analysis also revealed that most restaurants fall within a moderate price range and tend to have ratings around 3.5 to 4.

