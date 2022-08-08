# bike-sharing-linear-regression

Ways to generate dummies:
1. df = pd.get_dummies(df, columns=['GenderClass','Embarked'], drop_first=True) # the duplicates are dropped automatically


2. dummy1 = pd.get_dummies(leads_data[["Lead Origin","What is your current occupation"]], drop_first=True)

# Adding Dummies to the main Dataframe.
leads_data = pd.concat([leads_data,dummy1], axis = 1)
cols_drop = ["Lead Origin", "Lead Source",  "What is your current occupation"]
leads_data.drop(cols_drop, axis = 1, inplace = True)
