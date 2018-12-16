# Food for thought


## Abstract
Food plays an essential role in our everyday life. However, we often underestimate its effect on our health and on the environment.
Just thinking at how worldwide [obesity has nearly tripled since 1975](http://www.who.int/news-room/fact-sheets/detail/obesity-and-overweight) or how [palm oil consumption affects deforestation](https://www.independent.co.uk/life-style/palm-oil-health-impact-environment-animals-deforestation-heart-a8505521.html) makes us wonder whether it is possible to change our eating habits to improve our's and world's life conditions. 

In order to move the first steps toward these changes, this projects has a double objective, pursued through the analysis of the [Open Food Facts](https://world.openfoodfacts.org/) database. 

 - **OUR FIRST IDEAS** 
 
 At the beginning of the project we wanted to:
 1. Give insights on food categories that potentially are dangerous for the environment, for example by considering the package type or the presence of palm oil in it.
 2. Investigate possible monopolistic situation in food industry e.g when one product category is only sold by some companies.
 3. Give nutritional scores for each product in various alimentation categories and we will assess the importance of some key nutrients (such as vitamins, cholesterol and others) in each product category.
 4. Create a food advisor that can help consumers choose the best product in a given category based on their nutritional data and their impact to the environment. 

 - **OUR FINAL PROJECT** 
 
 We had to reconsider our objectives after investigating the dataset (missing values, countries presence ect.). The final goals are:
1. Give insights on food categories regarding their nutrition content, impact on health (using a nutrition score called nutri-score) and their environmental impact (palm oil presence).
2. Provide a complete analysis of food brands in France. Each brand will be examined regarding the category of products it sells, if their are healthy or not and if they contain ingredient from palm oil. The analysis will focus on the 10 biggest french brands.
3. Create a food advisor that can help consumers choose the best product in a given category based on their nutritional data and their impact to the environment. 

## Dataset
The dataset used is: Open Food Facts (1.83 Gb).
The data can be downloaded in different formats, but we will choose the .csv or MongoDB dump format.

The data set is composed of different fields: we filter the one we are interested in like 'nutriments', 'ingredients_from_palm_oil_tag', 'countries_en', 'nutrition_grade_fr'. In particular, information about the creator of the dataset entry, the creation time will be discarded.

To handle the missing data, we will consider the 'state_tags' field that indicates which other fields are missing:
- we noticed that most of listed products are sold from either France or USA. 
- moreover, we observed that the nutritional score is present ONLY for french products.

At the end, we chose to restrict the analysis to France. 

## A list of internal milestones up until project milestone 2
| 05/11 - 11/11                                                                                                                                                                                                                                                                                                                                                    | 12/11 - 18/11                                                                                                                                                                                                                                                                                                                                                                                                                                  | 19/11 - 25/11                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Check how to open the file in MongoDB formats <br/> 2. Data exploration: analyzing and cleaning data <br/> 3. Check if there is a large number of missing values for fields of interest <br/> 4. General statistics for the field of interest <br/> (number of products sold in different country,  number of products containing relevant nutritinal information) | 1. Find a way to handle the missing data,  if this results to be compromising the objectives of the project (maybe using a complementary dataset). <br/> 2. List and plot for each products belonging in different categories, their nutritional value, their nutritional score and the owner company.<br/> 3. Visualize the products sold in France with all the caracterstics found in point 2. | 1. Define an index that summarizes the impact of each product on environemnt and health,  based on the variables found the previous week. <br/> 2. Analysis based on the insight on the actual data. <br/> 3. Build a website for the datastory.|

## Milestone 2

In the milestone 2 after reanalysing our dataset, we realized that there are a lot of missing/unknows and nan values, in fact we usually work with 40% of the total dataset.
In order to categorize all the different products, we decided to gather them according to the 'PNNS' group and we examined the associated nutrition values(proteins, sugars, fat, energy, carbohydrates and sodium quantity).
A PCA analysis has been performed, but unfortunately it didn't turn out with any discriminat features among the PNNS1 group division, so in order to be able to classify any products in a certain category further and deep analyis are needed.

On the other hand, we also took a look at how the different products were sold around countries. It turns out that around 85% of the products were sold in France and in the USA, so we decided to shrink our analysis on just these two countries.
Even more, we inspected the nutritional scores associated to those products and we realized that it was almost absent for the products sold in the USA, so just France was kept in the further analysis.

We also cleaned the brands features using a list of [food brands present in France](https://www.frenchclick.co.uk/t-Brands.aspx) and we looked at the distribution of the nutrition grades among the whole dataset.
Furthermore, we counted the nutrition grade occurences for each brand and we came up that most part of them use to sell 'junk ' food.

## Milestone 3

The final analysis pipeline is the following: 

1. _Food Categorization_: we explain how we define 9 food categories.
2. _Score category_ : we define how we can compute a score for each products regarding its nutritional score, the energy it represents, the presence of palm oil.
3. _Product Advisor_: choose the best product for your health giving a category ! 
4. _Nutrition values vs food categories in France_: we investigate the food categories w.r.t the nutritionnal scores of the products which belong to.
5. _Nutrition values vs brands in France_: we examine each french brands and see which one sell healthy / unhealthy products.
6. _Palm oil vs brands in France_: we investigate which brands in France sell the more products containing palm oil. 

The final data story can be found here: [_Food for Thought_](https://elisabettaaa.github.io/).

The distribution of the work between the team mates is the following:
 - Everybody did the preliminary analyis, the problem formulation, the cleaning of the dataset,  the datastory in html.
 - Elisabetta: 1. + 2. + 3.
 - Tom:        4. + 5. + 6.
 - Michael:    1. + 2. + 3.

Everybody will work on the presentation.
