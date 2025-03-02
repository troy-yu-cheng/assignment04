# **Intro2DS**: Assignment04 (Georgetown Spr 2025)

*Author: Troy Cheng, Caroline Atuhaire*

## Website URL

<https://troy-yu-cheng.github.io/assignment04/>        

## Data Set Description

The data we collect is from a publicly accessible data set of World Bank called [World Development Indicators](https://databank.worldbank.org/source/world-development-indicators). We are looking into the relationships of variables related to economic or education policy, conducting data analysis and visualization in [RStudio](https://posit.co/download/rstudio-desktop/).

[World Development Indicators (WDI)](https://datatopics.worldbank.org/world-development-indicators/) is the primary World Bank collection of development indicators, compiled from officially recognized international sources. It is a compilation of relevant, high-quality, and internationally comparable statistics about global development and the fight against poverty, presenting the most current and accurate global development data available, and includes national, regional and global estimates. The database contains 1,400 time series indicators for 217 economies and more than 40 country groups, with data for many indicators going back more than 50 years.

*Note: Even though Global Development Finance (GDF) is no longer listed in the WDI database name, all external debt and financial flows data continue to be included in WDI. The GDF publication has been renamed International Debt Statistics (IDS), and has its own separate database, as well.*

## Get Original Variables and Data Set

You can find detailed information (meta data) of our original variables in *0_OriginData_World_Development_Indicators.xlsx* file nested in the [data](https://github.com/troy-yu-cheng/assignment04/blob/main/data) folder.

The way how we selected original variables and download them from the world bank website is:

1. Open official data set of [World Development Indicators](https://databank.worldbank.org/source/world-development-indicators) published by [World Bank](https://www.worldbank.org/ext/en/home).
2. Click *Variables* tab on the top left, and set filter in five dimensions:
	- Database: select **World Development Indicators**.
	- Country: select **China**, **Uganda**, **United States**.
	- Series: open the filter tab on the top right of the console. Select *Growth Rates*, *Aggregate indicators*, and *Expenditure on GDP* in **Economic Policy & Debt** section. Scroll down and select all four boxes (*Efficiency*, *Inputs*, *Outcomes* and *Participation*) in **Education** section. Then scroll down to the bottom and select *Economic activity*, *Labor force structure*, and *Unemployment* in **Social Protection & Labor** section. Now you should see the amount of all available variables is 320 on the top right of the console. Then close the filter feature and select all 320 variables.
	- Time: select year 2001-2023. 23 variables in total.
	- Metadata Attributes: leave it as default (it should check all the boxes).
3. Download the data though the **Download options** tab on the top right of the whole page. Download the data as an Excel file. Also, download the Metadata though the same tab (you can set Metadata as Excel file though **Download options** → **Advanced options**). The Metadata for this project is saved as *2_Metadata_World_Development_Indicators.xlsx* in [data](https://github.com/troy-yu-cheng/assignment04/blob/main/data) folder.
4. Rename the file with any name you want on your local machine (here we do *0_OriginData_World_Development_Indicators.xlsx*).

## Transfer the Data Format and Clean Data

The first thing is to transfer the raw data into [tidy data](https://awunderground.github.io/data-science-for-public-policy2/02_tidyverse.html#tidy-data-1), which would make our data more manipulatable in RStudio. You can find how we did this in [index.qmd](https://github.com/troy-yu-cheng/assignment04/blob/main/index.qmd) (a [Quarto](https://awunderground.github.io/data-science-for-public-policy2/06_reproducible-research-with-quarto.html) document written in R markdown language), and the final out put file *1_world_bank_data_clean.xlsx* in the [data](https://github.com/troy-yu-cheng/assignment04/blob/main/data) folder.

Also, the raw data from the website have a lot of NAs (missing values). This causes many variables useless when conducting data analysis, because they don't have most of the values in their columns. We manually chose available variables which barely had NAs over year 2001-2023, and made a code book for them. You can find the codebook file *3_codebook_availabledata.xlsx*, which includes the variables' original long names and corresponding shorter names we created for them, in [data](https://github.com/troy-yu-cheng/assignment04/blob/main/data) folder. Then you can look up each variable's detailed information in metadata file *2_Metadata_World_Development_Indicators.xlsx*, which is also in [data](https://github.com/troy-yu-cheng/assignment04/blob/main/data) folder, searching by the variables' original names shown in *3_codebook_availabledata.xlsx*. You can reproduce these files following our code in [index.qmd](https://github.com/troy-yu-cheng/assignment04/blob/main/index.qmd).

Our final data file is *available_data.xlsx* in [data](https://github.com/troy-yu-cheng/assignment04/blob/main/data) folder. Feel free to open it first and get a sense of the data we're going to analyze.
