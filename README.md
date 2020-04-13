If you combine your problem statement, executive summary, data dictionary, and conclusions/recommendations, you have an amazing README.md file that quickly aligns your audience to the contents of your project. Don't forget to cite your data sources!

# Problem Statement

In this project, we examine the Ames Housing dataset and use linear regression models to predict the sale price of homes in Ames, Iowa. The dataset has over 70 columns and over 2,000 rows, each of which contains various attributes of a different home in Ames, Iowa. In addition, we participate in a Kaggle competition to compare our success to others'. 

I [am pretending that I] work for House Flippers International, a [fake] company that buys homes, fixes them up, and then sells them at a higher margin for profit. They are looking to expand to the Ames, Iowa market, and have tasked me with predicting the sale price of homes that they might potentially buy to flip and resell. In particular, they are curious as to how big of a factor location is when it comes to predicting price. They worry that if they flip a house in a poorly chosen location, it won't resell for a very high value. It is up to me to see just how big of an influence location has on sale price.



# Executive Summary

In this project, after initial expoloratory data analysis and cleanup were performed, 6 different linear regression models were created. From those six, three were chosen to be relevant to the problem. 

The first model (/code/1-linear-regression-location.ipynb) predicts price from columns of the dataset that are relevant to location. By "relevant to location," we mean aspects of a property that the home buyer cannot change (which neighborhood, how rural or metropolitan the area is, how sloped the land is, etc.). The second model (/code/2-linear-regression-no-location.ipynb) predicts price from columns of the dataset that are not relevant to location, i.e. everything about the home that the buyer can potentially change (i.e. quality of the kitchen, roofing material, number of bathrooms, etc.). The third model (/code/3-linear-regression-all-cols.ipynb) predicts price from all columns, both relevant to location and not. 

The classic phrase "location, location, location," which emphasizes what is most important when thinking of buying a home, may bring about the expectation that location is most relevant when it comes to predicting the sale price of a home. However, our findings demonstrate the contrary. We find that non-location aspects have a bigger affect on accurately predicting sale price, and that mdoeling based on both location and non-location information only does marginally better than predicting based on non-location information alone. 


# Data Dictionaries

The original data dictionary can be found at the following website: http://jse.amstat.org/v19n3/decock/DataDocumentation.txt. Each row of the dataset contains a record of various attributes of one home in Ames, Iowa. This dictionary describes the data in great detail, and in particular what types of attributes were recorded about each home. 

In the first model, the attributes used to predict sale price include: 
- MS Zoning
- Neighborhood
- Condition 1
- Condition 2
- Lot Frontage
- Lot Area
- Lot Shape
- Land Contour
- Lot Config
- Land Slope
- Utilities

In the second model, the attributes used to predict sale price were everything in the original dataframe not listed above. The third model was based on the entire dataset. 



# Conclusions and Recommendations

We conclude that location doesn't have such a big affect on the prediction of sale price as one might expect. In fact, the location-based model was off by plus or minus $54,000 (which is a lot considering the average house price is $181,000). The non-location-based model was only off by about $31,000, as was the model taking into account all attributes of the homes. All models performed better than our baseline model, the average house price, which was wrong by about $82,000 on average. 

This is actually good news for House Flippers International, because location is more out of the realm of a house flipper's control. The two attributes of a home that had the biggest impact on predicting sale price were exterior quality of the home, and the air conditioning. So, as long as the house flippers make sure the outside of the house looks really good and makes sure there is airconditioning, it shouldn't be too hard to predict what the house will sell for. 


