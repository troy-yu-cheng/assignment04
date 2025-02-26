# **Intro2DS**: Assignment04 (Georgetown Spr 2025)

*Author: Troy Cheng, Caroline Atuhaire*

## Data Set Description

The data we collect is from a publicly accessible data set of [World Bank called World Development Indicators](https://databank.worldbank.org/source/world-development-indicators). We are looking into the relationships of variables related to economic or education policy.

### Original Variables

You can find detailed information (meta data) of our original variables in *0_OriginData_World_Development_Indicators.xlsx* file nested in the [data](https://github.com/troy-yu-cheng/assignment04/blob/main/data) folder.

The way we selected original variables from the website is:

1. Open official data set of [World Development Indicators](https://databank.worldbank.org/source/world-development-indicators) published by [World Bank](https://www.worldbank.org/ext/en/home).
2. Click *Variables* tab on the top left, and set filter in five dimensions:
	- Database: select **World Development Indicators**.
	- Country: select **China**, **Uganda**, **United States**.
	- Series: open the filter tab on the top right of the console. Select *Growth Rates*, *Aggregate indicators*, and *Expenditure on GDP* in **Economic Policy & Debt** section. Scroll down and select all four boxes (*Efficiency*, *Inputs*, *Outcomes* and *Participation*) in **Education** section. Then scroll down to the bottom and select *Economic activity*, *Labor force structure*, and *Unemployment* in **Social Protection & Labor** section. Now you should see the amount of all available variables is 320 on the top right of the console. Then close the filter feature and select all 320 variables.
	- Time: select year 2001-2023. 23 variables in total.
	- Metadata Attributes: leave it as default (it should check all the boxes).
3. Download the data though the **Download options** tab on the top right of the whole page. Download the data as an Excel file. Also, download the Metadata though the same tab (you can set Metadata as Excel file though **Download options** → **Advanced options**).

