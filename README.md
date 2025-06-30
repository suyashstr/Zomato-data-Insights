![Uploading image.png…]()

<h1 align="center" id="title">Zomato-Data-Insights</h1>
This project involves analyzing restaurant data from Zomato to extract insights such as ratings distribution, the impact of online ordering, and average costs for different dining types.Data cleaning and visualization techniques were employed using Python libraries like Pandas, Matplotlib, and Seaborn.

<h2>Table of Contents:-</h2>

Dataset Overview
Data Cleaning

Cost Analysis for Couples
Impact of Online Ordering
Conclusion
Installation
Clone this repository.

*  Installation
*  Dataset Overview
*  Data Cleaning
*  Analysis
*  Type of Restaurant
*  Ratings Distribution
*  Cost Analysis for Couples
*  Impact of Online Ordering
*  Conclusion
*  Clone this repository.

```
git clone https://github.com/your-username/zomato-data-analysis.git
```

Install the required Python libraries.

```
pip install pandas matplotlib seaborn
```

<h2>Dataset Overview:-</h2>
The dataset used in this project contains information about 148 restaurants, including:

Name of the restaurant
Whether it supports online ordering
Availability of table booking
Restaurant rating
Number of votes
Approximate cost for two people
Type of restaurant (e.g., Buffet, Dining)

<h2>Data Cleaning:-</h2> 
* The ratings were initially in a string format with a scale (4.1/5). A helper function controlRate() was used to convert the ratings into numeric format.<br>
* Missing or irrelevant data was checked, and unnecessary columns were removed.


<h2>Analysis:-</h2> 
Type of Restaurant
The data showed that most restaurants fall under the "Dining" category, while "Buffet" was less common.

```
sns.countplot(x=dataframe['listed_in(type)'])
plt.xlabel("Type of restaurant")
```

<h2>Ratings Distribution:-</h2>
We explored the distribution of restaurant ratings. The majority of restaurants received ratings between 3.5 and 4.

```
plt.hist(dataframe['rate'], bins=10)
plt.title("Ratings Distribution")
plt.show()
```

<h2>Cost Analysis for Couples:-</h2>
The data showed that couples typically prefer restaurants with an approximate cost of ₹300.

```
sns.countplot(x=dataframe['approx_cost(for two people)'])
```

<h2>Impact of Online Ordering:-</h2>
* We analyzed the impact of online ordering on ratings. Restaurants that supported online ordering generally had higher ratings.<br>
* A heatmap was created to visualize the relationship between restaurant type and online ordering.

```
sns.heatmap(pivot_table, annot=True, cmap="YlGnBu", fmt='d')
plt.title("Heatmap: Online Orders vs Restaurant Type")
```

<h2>Conclusion:-</h2>
Dining restaurants primarily accept offline orders, while cafes tend to receive more online orders.The analysis also revealed that most restaurants fall within a moderate price range and tend to have ratings around 3.5 to 4.

