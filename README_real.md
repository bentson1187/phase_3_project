<img src='Images/Title.png' width=120%>

# Predicting Water Well Failures in Tanzania

# Overview

The Tanzanian Ministry of Water tracks vital information on water wells in its country to best ensure citizens are provided with a continual source of fresh water. A dataset housing this crucial information can be found [HERE](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/page/23/). 

I will be utilizing this dataset to train a classification model to accurately predict which water wells are not functional and also to gain insights into potential reasons for water well failures.

# Business Problem

It is undoubtedly obvious how crucial a consistent water supply is to every living thing in this world. Without it, life is not sustainable. A human can survive without food on average for about 1 to 2 months. However, a human can only survive 3 days without water! This time-frame without water can be shortened even further in climates which are extremely hot and humid. Tanzania, located on the east coast of Africa on the Indian Ocean, has parts of the country that are extremely hot and humid. The average high and low temperature in the most populous city of Dar es Salaam during the year is 86F and 70F, respectively. Dar es Salaam is located on the coast and has a average relative humidity of 70%. 

It is, therefore, extremely imperative to be able to supply a consistent source of fresh water for sustainment of human life in Tanzania. This begins with the evaluation of water wells in Tanzania with an emphasis on how reliability can be maximized to ensure a consistent supply of water is attainable. Unfortunately, our reliance on equipment (in this case a mechanical pump) means that 100% reliability can never be achieved. It is best to consider both reliability of the equipment and how quickly we can respond to an equipment failure and get it back to a running state. The response time to fixing a mechanical failure can be shortened with first predicting which water wells will fail. This key information can help maintenance organizations to ensure they have labor, tools and supplies ready to be mobilized in case of a failure. I will use machine learning to build a model to best predict water well failures in an attempt to understand what improvements can be made to factors such as funding, technology and maintenance operations.

# Data

The dataset has information on 59,400 water wells in Tanzania, for which only 55% are fully operational based on this dataset. Information on these water wells includes many important factors that impact their operability and will be explored in order to provide insight into how reliability, and therefore accessibility, can be maximized. I will clean and explore the data to best be utilized with a classification machine learning model to predict failure. Some of the important features are:
- Well Age
- Static Head
- Population around the well
- Well Location

<img src='Images/Feature_Importances.png' width=100%>

# Methods

Since a reliable source of water is so imperative to human survival, I believe the best model will prioritize determining which wells are not functioning even if that means that there are false positives. This is primarily due to the high cost of leaving a subset of the population without water for any given time. This approach will mean more money and time is spent on preventative maintenance ahead of the well failing, but should ensure the best reliability. In the context of a classification model, the model will be evaluated to maximize recall. Recall aims to maximize identifying true positives even if it means there will be false negatives. I specifically chose to use highly interpretable models in order to have a more clear understanding of which well features are helpful in making the classification choices.

# Results

The model analyzes how specific features of a home affect its value and uses this analysis to then determine a "best fit" prediction when trying to take in new home features and produce a new home value. Here is how the model classified each home feature with respect to how it influenced a homes value:

<img src='Images/Model Feature Influence.png' >

The feature which affects a home's value most positively is Total Home Square Feet. The grade of construction is also an important feature to predicting a home's value. The model utilizes the impact of the home features to give insights into rennovation opportunities.

## Rennovation Opportunity: Finish a 700 sqft Basement 

The model shows that having a basement negatively impacts a home's value. However, if a home has an unfinished basement with over 350 square feet then the extra square feet to the house may offset the negative affect of the basement. The median basement size for homes in this area is 700 square feet. If a homeowner would like to finish their basement which would add 700 square feet and use a high quality grade of construction, the predicted increase in a home's value is $81,000:

<img src='Images/Basement Rennovation.png'>

## Rennovation Opportunity: Add a Full Size Bathroom

The model shows that adding a bathroom positively impacts a home's value. If a homeowner were to add a full size bathroom (60 sqft) with high construction quality the model predicts an increase in a home's value of $43,200:

<img src='Images/Bathroom Rennovation.png'>

# Conclusions

For a homeowner looking to improve their home's value through rennovation, finishing a large basement or adding a full size bathroom will significantly improve a home's value. It is extremly important that the amount of additional square feet is large enough to offset costs and that the construction quality is high enough to last many years to come. Lastly, a few words of caution: The model suggests that adding an entire floor or adding a bedroom will most likely negatively impact a home's value unless the additional square feet is large enough to offset the negative impact and cost.

## **For More Information**

Please review our full analysis in my [Jupyter Notebook](https://github.com/bentson1187/dsc-phase-2-project/blob/231d7829a588150c9e801101b9ef99029747c3db/Bentson,%20Brian%20Phase%202%20Project.ipynb) or my [presentation](https://github.com/bentson1187/dsc-phase-2-project/blob/231d7829a588150c9e801101b9ef99029747c3db/Stakeholder%20Presentation.pptx).

For any additional questions, please contact **Brian Bentson, bentson.brian@gmail.com**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── Bentson,Brian Phase 2 Project.ipynb <- Narrative documentation of analysis in Jupyter notebook
├── Jupyter Notebook.pdf                <- PDF version of the analysis in Jupyter notebook
├── Microsoft Presentation.pdf          <- PDF version of project presentation
├── data                          <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```
