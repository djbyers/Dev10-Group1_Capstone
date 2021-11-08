# Group1_Capstone

Broadly speaking, this project aims to use a variety of and financial factors to forecast different measures of economic and societal well-being. Our data, drawn primarily from the World Bank database, draws upon different measures of government debt, tax revenue, stock value within an economy, inflation, and GDP, among others, to predict values such as poverty, unemployment, wealth disparity, life expectancy, and infant mortality rate.

Using an automated API call from the World Bank, we were able to collect data from every registered country from the years 1990-2020. The goal of our analysis is to be able to produce actionable results by building our models and visualizations to use the data from one country in one particular year to predict whichever dependent variable we choose for the following year in that country. For example, we will use GDP, central government debt, tax revenue, and total value of stocks traded in the United States in 2000 to predict the unemployment rate in the United States in 2001. With this goal in mind, by the end of our process, we should be able to create predictions on a global scale for how these socioeconomic dependent variables will end up at the end of 2021 using the 2020 data.

# Table of Contents
- DatabricksAndETL - This folder contains our Databricks Jupyter Notebooks and our ETL report.
- NapkinDrawingsAndFeedback - This folder contains our visualization and dashboard napkin drawings and the feedback we received about them.
- code - This folder contains the following sub-folders which all have code in them:
    - Preliminary Code - This code charts our early progress through the machine learning process. We did not directly use this code in the final implementation of our machine learning.
    -  Final Machine Learning - This code contains the Jupyer Notebooks we used to create our final machine learning models.
    -  Power BI Code - We used this code to create Power BI visualizations with Python.
- Project Specifications - This folder contains our initial exploratory questions, data platform diagrams, and project management plan.

# Indicator Glossary

The exact indicators we are pulling from the World Bank, their API call code, and their meanings are as follows (all definitions used are those provided by the World Bank):

CM.MKT.TRAD.GD.ZS - Stocks Traded, Total Value:

The value of shares traded is the total number of shares traded, both domestic and foreign, multiplied by their respective matching prices. Figures are single counted (only one side of the transaction is considered). Companies admitted to listing and admitted to trading are included in the data. Data are end of year values.

FP.CPI.TOTL.ZG – Consumer Price Index:
    
Inflation as measured by the consumer price index reflects the annual percentage change in the cost to the average consumer of acquiring a basket of goods and services that may be fixed or changed at specified intervals, such as yearly. The Laspeyres formula is generally used.

CM.MKT.TRNR - Stocks Traded, Turnover Ratio:

Turnover ratio is the value of domestic shares traded divided by their market capitalization. The value is annualized by multiplying the monthly average by 12.

GC.TAX.TOTL.GD.ZS – Tax revenue (% GDP):
    
Tax revenue refers to compulsory transfers to the central government for public purposes. Certain compulsory transfers such as fines, penalties, and most social security contributions are excluded. Refunds and corrections of erroneously collected tax revenue are treated as negative revenue.

NY.GDP.PCAP.CD - GDP per Capita:

GDP per capita is gross domestic product divided by midyear population. GDP is the sum of gross value added by all resident producers in the economy plus any product taxes and minus any subsidies not included in the value of the products. It is calculated without making deductions for depreciation of fabricated assets or for depletion and degradation of natural resources. Data are in current U.S. dollars.

GC.DOD.TOTL.GD.ZS - Central Government Debt (%of GDP):

Debt is the entire stock of direct government fixed-term contractual obligations to others outstanding on a particular date. It includes domestic and foreign liabilities such as currency and money deposits, securities other than shares, and loans. It is the gross amount of government liabilities reduced by the amount of equity and financial derivatives held by the government. Because debt is a stock rather than a flow, it is measured as of a given date, usually the last day of the fiscal year.

SI.POV.GINI – Gini Coefficient:

Gini index measures the extent to which the distribution of income (or, in some cases, consumption expenditure) among individuals or households within an economy deviates from a perfectly equal distribution. A Lorenz curve plots the cumulative percentages of total income received against the cumulative number of recipients, starting with the poorest individual or household. The Gini index measures the area between the Lorenz curve and a hypothetical line of absolute equality, expressed as a percentage of the maximum area under the line. Thus a Gini index of 0 represents perfect equality, while an index of 100 implies perfect inequality.

FM.LBL.BMNY.GD.ZS – Broad Money (% of GDP):

Broad money (IFS line 35L..ZK) is the sum of currency outside banks; demand deposits other than those of the central government; the time, savings, and foreign currency deposits of resident sectors other than the central government; bank and traveler’s checks; and other securities such as certificates of deposit and commercial paper.

FI.RES.TOTL.CD - Total Reserves:

Total reserves comprise holdings of monetary gold, special drawing rights, reserves of IMF members held by the IMF, and holdings of foreign exchange under the control of monetary authorities. The gold component of these reserves is valued at year-end (December 31) London prices. Data are in current U.S. dollars.

SM.POP.TOTL – Migrant Stock Population:

International migrant stock is the number of people born in a country other than that in which they live. It also includes refugees. The data used to estimate the international migrant stock at a particular time are obtained mainly from population censuses. The estimates are derived from the data on foreign-born population--people who have residence in one country but were born in another country. When data on the foreign-born population are not available, data on foreign population--that is, people who are citizens of a country other than the country in which they reside--are used as estimates. After the breakup of the Soviet Union in 1991 people living in one of the newly independent countries who were born in another were classified as international migrants. Estimates of migrant stock in the newly independent states from 1990 on are based on the 1989 census of the Soviet Union. For countries with information on the international migrant stock for at least two points in time, interpolation or extrapolation was used to estimate the international migrant stock on July 1 of the reference years. For countries with only one observation, estimates for the reference years were derived using rates of change in the migrant stock in the years preceding or following the single observation available. A model was used to estimate migrants for countries that had no data.

SI.DST.10TH.10 – Income Held By Top 10%:
    
Percentage share of income or consumption is the share that accrues to subgroups of population indicated by deciles or quintiles.

SI.DST.FRST.10 – Income Held By Bottom 10%:

Percentage share of income or consumption is the share that accrues to subgroups of population indicated by deciles or quintiles.

SI.POV.NAHC - Poverty Head Count:

National poverty headcount ratio is the percentage of the population living below the national poverty line(s). National estimates are based on population-weighted subgroup estimates from household surveys. For economies for which the data are from EU-SILC, the reported year is the income reference year, which is the year before the survey year.

SP.DYN.LE00.IN - Life Expectancy at Birth:

Life expectancy at birth indicates the number of years a newborn infant would live if prevailing patterns of mortality at the time of its birth were to stay the same throughout its life.

SP.DYN.IMRT.IN - Infant Mortality Rate:
    
Infant mortality rate is the number of infants dying before reaching one year of age, per 1,000 live births in a given year.

SL.UEM.TOTL.ZS - Total Unemployment:

Unemployment refers to the share of the labor force that is without work but available for and seeking employment.

NE.EXP.GNFS.ZS - Exports of Goods and Services (%of GDP):

Exports of goods and services represent the value of all goods and other market services provided to the rest of the world. They include the value of merchandise, freight, insurance, transport, travel, royalties, license fees, and other services, such as communication, construction, financial, information, business, personal, and government services. They exclude compensation of employees and investment income (formerly called factor services) and transfer payments.
    
