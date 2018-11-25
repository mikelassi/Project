# Food for thought


## Abstract
Food plays an essential role in our everyday life. However, we often underestimate its effect on our health and on the environment.
Just thinking at how worldwide [obesity has nearly tripled since 1975](http://www.who.int/news-room/fact-sheets/detail/obesity-and-overweight) or how [palm oil consumption affects deforestation](https://www.independent.co.uk/life-style/palm-oil-health-impact-environment-animals-deforestation-heart-a8505521.html) makes us wonder whether it is possible to change our eating habits to improve our's and world's life conditions. 

In order to move the first steps toward these changes, this projects has a double objective, pursued through the analysis of the [Open Food Facts](https://world.openfoodfacts.org/) database. First, it aims at giving insights on food categories that potentially are dangerous for the environment, for example by considering the package type or the presence of palm oil in it. The effect of possible monopolistic phenomena in food industry will also be analysed. Moreover, we will give nutritional scores for each product in various alimentation categories and we will assess the importance of some key nutrients (such as vitamins, cholesterol and others) in each product category.
Finally, based on the previuos analysis, the idea is to create a food advisor that can help consumers choose the best product in a given category based on their nutritional data and their impact to the environment. 

## Research questions

### Food for health

1. Which indicators should be used as nutritional score?
2. Is less healthy food mostly sold in certain countries?
3. Are certain products made of the same ingredients?

### Food for the planet
1. Are certain food categories associated with high environmental damage?
2. Are there companies that have monopoly of certain products?
3. Are there countries that are more 'enviromental friendly'?

## Dataset
The dataset used is: Open Food Facts (1.83 Gb).
The data can be downloaded in different formats, but we will choose the .csv or MongoDB dump format.

The data set is composed of different fields: we'll filter the one we are interested in like 'nutriments', 'ingredients_from_palm_oil_tag', 'countries_tag','nutrition_levels'. In particular, information about the creator of the dataset entry, the creation time will be discarded.
To handle the missing data, we'll consider the 'state_tags' field that indicates which other fields are missing.
Moreover, we notice that most of listed products come from either France or USA. Hence, since this could compromise cross country analysis, we will either extend the dataset or avoid considering absolute counts of products.

## A list of internal milestones up until project milestone 2
| 05/11 - 11/11                                                                                                                                                                                                                                                                                                                                                    | 12/11 - 18/11                                                                                                                                                                                                                                                                                                                                                                                                                                  | 19/11 - 25/11                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Check how to open the file in MongoDB formats <br/> 2. Data exploration: analyzing and cleaning data <br/> 3. Check if there is a large number of missing values for fields of interest <br/> 4. General statistics for the field of interest <br/> (number of products sold in different country,  number of products containing relevant nutritinal information) | 1. Find a way to handle the missing data,  if this results to be compromising the objectives of the project (maybe using a complementary dataset). <br/> 2. List and plot for each products belonging in different categories,  their nutritional value, their package type, their nutritional score and the owner company.<br/> 3. For each country (if it's reasonable) visualize the products  with all the caracterstics found in point 2. | 1. Define an index that summarizes the impact of each product on environemnt and health,  based on the variables found the previous week. <br/> 2. Analysis based on the insight on the actual data. <br/> 3. Update the Readme file. |


## Questions for TAs

1. Is it possible to use the MongoDB as dataset? Is it feasible to import it on Spark or Pandas?
2. Is it reasonable to search for country differences even if there are discrepancies in the number of products per country?
3. Are the goals of our project broad enough? Are the research questions detailed enough?


## Milestone 2

In the milestone 2 after reanalysing our dataset, we realized that there are a lot of missing/unknows and nan values, in fact we usually work with 40% of the total dataset.
In order to categorize all the different products, we decided to gather them according to the 'PNNS' group and we examined the associated nutrition values(proteins, sugars, fat, energy, carbohydrates and sodium quantity).
A PCA analysis has been performed, but unfortunately it didn't turn out with any discriminat features among the PNNS1 group division, so in order to be able to classify any products in a certain category further and deep analyis are needed.

On the other hand, we also took a look at how the different products were sold around countries. It turns out that around 85% of the products were sold in France and in the USA, so we decided to shrink our analysis on just these two countries.
Even more, we inspected the nutritional scores associated to those products and we realized that it was almost absent for the products sold in the USA, so just France was kept in the further analysis.
We also cleaned the brands features using a list of [food brands present in France](https://www.frenchclick.co.uk/t-Brands.aspx) and we looked at the distribution of the nutrition grades among the whole dataset.
Furthermore, we counted the nutrition grade occurences for each brand and we came up that most part of them use to sell 'junk ' food.
