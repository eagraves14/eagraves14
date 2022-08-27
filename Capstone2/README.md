# Predicting Employee Attrition

*By now everyone has seen a headline about the 'Great Resignation' - the significantly high employee attrition rates following the COVID-19 pandemic.  While the name may imply that the phenomenon is new and temporary, it is actually a continuation of a decade-long trend of increasing voluntary attrition (https://hbr.org/2022/03/the-great-resignation-didnt-start-with-the-pandemic).  Thus, HR teams will need to continue to contend with rising turnover among the myriad of other issues they are facing such as the rise of remote/hybrid work arrangements and the corresponding heightened fluidity in the talent market.*

*Companies are building and expanding their People Analytics teams to apply data science and advanced analytics to help meet these challenges.  In this project, I have used a public HR dataset containing anonymized information about ~1,500 employees at a company to develop a statistical model to predict employee attrition (https://data.world/aaizemberg/hr-employee-attrition).  The information includes fields such as role, department, educational background, compensation, demographic information, internal and external work history, responses to employee surveys (about, for example, engagement, work-life balance, etc.) and, of course, whether that employee voluntarily left.*

## The Data

The table below shows the fields available in the dataset, separated by category. The target feature is a binary label called Attrition.

![field_table](../reports/figures/Capstone2_fields_table.png)

(Certain other fields were also present but are omitted because they did not provide meaningful information)

The data was already clean and did not have missing values.

## Visualizing the Information

Many of the fields exhibited at least a slight correlation with attrition rate.  Below, we focus on some of the more prominent associations.

**Numerical variables:**

*Age*: Attrition is higher among younger people.  Note the maximum age in this dataset is 60 - this may have been done intentionally to minimize the presence of retirements in the data set.

![Age_table](../reports/figures/AgeByAttrition.png)

*Distance from home*: Attrition is higher among those who live farther from work.

![Distance_table](../reports/figures/DistanceByAttrition.png)

*Number of prior companies*: While not obvious from the graphic below, attrition rate is positively correlated with number of prior companies worked at, likely due at least in part to confounding factors (e.g., employee may be in a function or role that is prone to high turnover in general).

Note on the graph: the median number of companies worked for the Attrition group is 1, which is less than the median for the non-Attrition group. However, the tail is longer for the Attrition group, and the average is higher.

![Companies_table](../reports/figures/CompaniesByAttrition.png)

*Total working years*: Similar to the trend for age, attrition is higher among those with fewer total working years.

![WorkingYrs_table](../reports/figures/WorkingYrsByAttrition.png)

*Years with current manager*: The longer someone has the same manager, the less likely they are to leave.

![ManagerYrs_table](../reports/figures/ManagerYrsByAttrition.png)
