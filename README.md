# INDIAN BOX OFFICE CHALLENGE


## Problem Statement: 
The Indian Box Office dataset comprises detailed information on films for the last 10 years, including aspects such as film titles, release dates, lead
actors/actresses, industries, budgets, collections, verdicts, IMDb ratings, runtimes, OTT platforms, directors, languages, and genres. Participants are tasked with leveraging Power BI to analyse this dataset and derive meaningful insights that can inform decision-making within
the film industry.

## Dataset provided: 
Participants will be provided with a rich collection of datasets, each meticulously curated to facilitate a comprehensive analysis of the Indian Box Office landscape over the past decade. The datasets include:

#### • Boxoffice_fact.csv: 

This file encompasses granular details of box office collections,providing essential quantitative metrics for revenue analysis.
#### • Director_dim.csv: 
A dimensional dataset offering professional information about film directors, enabling participants to correlate directorial influence with box office success.
#### • Genere_dim.csv:
 This dataset categorizes movies into various genres, aiding in the examination of genre-specific trends and audience preferences.
#### • Language_dim.csv: 
Language-specific data allowing for nuanced insights into the performance of films across different linguistic demographics.

## Key Questions to Guide Your Analysis:
1) Identify KPI’s such as total films, total budget, etc. ..
2) Identify the top 10 films by worldwide collection.
3) Analyze the annual release patterns and determine the year with the highest number of releases.
4) Compare the first-day collections with overall worldwide collections to identify films with
disproportionate first-day success.

5) Evaluate genre performance based on average IMDb ratings.
6) Investigate the relationship between film budgets and their worldwide collections.
7) Determine the directors with the most box office hits based on the 'Verdict' column.
8) Examine language trends and identify the most successful languages in the past decade.
9) Analyze the success and popularity of films released on various OTT platforms.
10) Assess the impact of lead actors/actresses on the success of films by examining average IMDb ratings.
11) Compare the performance of different film industries and identify the industry that has produced the highest-grossing films.
12) Are there particular months or seasons where films tend to perform better at the box office?
13) Which lead actors/actresses have consistently high-performing films?
14) Does the runtime of a film correlate with its box office success or IMDb rating?

#### How I approached this project:

 • Importing CSV files to POWERBI DESKTOP through GET  DATA.

 • Before loading the dataset i have cleaned the data & starts DATA VALIDATION by looking in to view tab & checking the column profile,column quality,column distribution,show white space,monospaced to figure out the data redundancy,Replacing null & blank,Replacing special character in prefix,date format,data type transformation.
  
  #### Data Validation
   ----------------------------------------------------
  
  ![Data Validation](https://github.com/kalaishann/power-query-data-cleaning/blob/b97d28aca71a26afdf083d010238c0bc17e80516/Data%20Validation.png)

 #### Replacing Special character
  -----------------------------------------------------
 ![Replacing Special character](https://github.com/kalaishann/power-query-data-cleaning/blob/b9c4abb5a7633c4743bc262d8bbb2aa5d8fa0a1b/Replacing%20Values.png)

 #### Finding Blanks
 -----------------------------------------------------
 ![Finding Blanks](https://github.com/kalaishann/power-query-data-cleaning/blob/b9c4abb5a7633c4743bc262d8bbb2aa5d8fa0a1b/Replacing%20Blanks.png)

 ![Replacing blanks with Zero](https://github.com/kalaishann/power-query-data-cleaning/blob/b9c4abb5a7633c4743bc262d8bbb2aa5d8fa0a1b/Replacing%20blank%20with%20zero.png)

 #### Finding Duplicates 
 ------------------------------------------------------
  ![Data Redundancy](https://github.com/kalaishann/power-query-data-cleaning/blob/b9c4abb5a7633c4743bc262d8bbb2aa5d8fa0a1b/Removing%20White%20Space.png)

 ![2 Distinct value in to 1 unique value](https://github.com/kalaishann/power-query-data-cleaning/blob/b9c4abb5a7633c4743bc262d8bbb2aa5d8fa0a1b/2%20Distinct%20value%20in%20to%201%20unique%20value.png)

#### Using Trim to remove prefix & suffix space   
-------------------------------------------------------
  ![Trim](https://github.com/kalaishann/power-query-data-cleaning/blob/b9c4abb5a7633c4743bc262d8bbb2aa5d8fa0a1b/Using%20Trim%20to%20remove%20space%20in%20prefix%20and%20suffix.png)
 
 • In power view - I have created DATE MASTER TABLE with year,Quarter,Month Nmae,Days of the week for TIME INTELLIGENCE FUNCTION.

 #### Date Master Table
---------------------------------------------------

  ![ Date Master Table](https://github.com/kalaishann/power-query-data-cleaning/blob/333efd012bb9a03ec3c244ae52a9826962061e3c/Date%20Master%20Table.png)

• I have created KEY MEASURES TABLE to keep all new measures.
 - Total budget

        TOTAL BUDGET = SUM(Boxoffice_Fact[Budget in Crores])

 - WorldWide collection

        WORLD WIDE COLLECTION = SUM(Boxoffice_Fact[Worldwide Collection  in Crores])

 - First Day Collection
 
       FIRST DAY COLLECTION = SUM(Boxoffice_Fact[First Day Collection Worldwide  in Crores]) 

 - India Gross Collection
 
       INDIA GROSS COLLECTION = SUM(Boxoffice_Fact[India Gross Collection in Crores]) 

 - Average IMDB rating

        AVG IMDB RATING = AVERAGE(Boxoffice_Fact[IMDb Rating])

