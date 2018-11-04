# Food for thought


# Abstract
Food plays an important role in our everyday life. 
However, we ofter underestimate its effect on our health and on the environment.
Just thinking at how worldwide obesity has nearly tripled since 1975 or how palm oil consumption affects deforestation makes us wonder whether it's possible to change our eating habits to improve our life condition. 
The project aims at giving insight on food categories that potentially are dangerous for the environment, for example by considering the packadge type or the presence of palm oil.
Moreover, we would like to give nutritional scores for each product of the each category and observe if there are companies that have the monopoly for different product categories.
At the end, based on the previuos analysis, the idea is to create a food advisor for each food categories in differet country.

# Research questions

Food for health

1)Which indicators should we use as nutritional score ?
2)Is less healthy food mostly sold in certain Country?
3)Are certain products made of the same ingredients?

Food for planet
1)Are certain food categories associated with high enviromental damage ?
2)Are there companies that have monopoly of certain products?
3)Are there country more 'enviromental friendly'?

# Dataset
The dataset used is: Open Food Facts(1.83 Gb).
We can download the data set in different formats, but we'll chose the csv or MongoDB dump format.

The data set is composed of different fields: we'll filter the one we are interested in like  'nutriments', 'ingredients_from_palm_oil_tag', 'countries_tag','nutrition_levels'.
To handle the missing data, we'll consider the 'state_tags' that indicates the other missing fields.
Moreover, we notice that most of listed products come from either France or USA.
Hence, this could compromise cross country analysis.

# A list of internal milestones up until project milestone 2

11/11/2018

1)Check how to open the File by MongoDB formats
2)Data exploration: analyzing and cleaning data
3)Check if there is a large number of missing values for fields of interest 
4)General statistics for the field of interest (number of products sold in different country, number of products containing relevant nutritinal information)


18/11/2018

1)Find a way to handle the missing data(maybe using a complementary dataset)
2)List and plot for each products belonging in different categories, their nutritional value, their packadge and their nutritional score and the owner company.
3)For each country(if it's reasonable) visualize the products with all the caracterstics found in point 2).

25/11/2018

1)Define an index that summerizes the impact of each product on environemnt and health, based on the variables found the previous week.
2)Analysis based on the insight on the actual data. 
3)Update the Readme file.


# Questions for TAa
1)Is it possible to use the MongoDB as dataset? is it feasible to import it on Sparks or Pandas?
2)Is it reasonable to search for country differences even if there are discrepancies in the number of products per country?
3)Are the goals of our project broad enough? Are the reasearch questions detailed enough or should we limited in just part of them?

