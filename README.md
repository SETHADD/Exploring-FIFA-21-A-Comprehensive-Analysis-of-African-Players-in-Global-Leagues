# Introduction
Kaggle is notorious for providing pure, clean datasets ready for analysis and model building.

This particular data is a very messy and raw dataset of EA Sorts hit FIFA series - FIFA21, which was scraped from sofifa.com.

The idea behind this data was definitely to learn a lot about data cleaning, but I took it up a notch to visualize the data of the African players in the data.

![alt text](https://github.com/SETHADD/Exploring-FIFA-21-A-Comprehensive-Analysis-of-African-Players-in-Global-Leagues/blob/main/FIFA-21-freezing.jpeg)

## Problem Statement
This was a data to learn about cleaning a messy data and the following were some of the problems with the data
 * Some of the columns had data types that made them difficult to work with eg. the height and weight columns were not in numerical forms
 * some of the columns had Remove unnecessary newline characters that needed to be trimmed.
 * 'Value', 'Wage' and "Release Clause' are string columns because they had M and K attached to some of the values.
 * Some columns have 'star' characters.Those columns had to be stripped of the stars and make the columns numerical etc.

## Skills Demonstrated
1. Before loading the data
 * Open the CSV file using Notepad.Click "File > Save As" and in the dialog window that appears I selected "ANSI" from the "Encoding" field before saving.This is to ensure that all non-English characters displays properly in Excel.
1b. The CSV file was loaded into Excel and the following was done.
 * Duplicates were checked and fortunately there were no duplicates.
 * Trim function was used to remove spaces before and after values in some columns.
 * Left function was used to extract the numbers from the skill moves and IR columns.
 * With If and Len functions, values in columns with 'K' and 'M' were multiplied by 1000 and 1000000 respectively.
 * unneccessary columns were deleted
 
2. The data was saved and imported to the SQL Server Management Studio to extract all the details of players from Africa.

![alt text](https://github.com/SETHADD/Exploring-FIFA-21-A-Comprehensive-Analysis-of-African-Players-in-Global-Leagues/blob/main/Extracting%20countries%20in%20SQL.png)

## Data Transformation
Both the clean data and the data on only African players were imported into Power Bi and the data was further transformed by removing some errors and further deleting some columns that were not visualized.
DAX (Calculate) was use to create a new measure of the total wages of Brazilian players.

## Modeling
A one-to-one relationship was setup between the two tables.
A table was created for all the New measures.
![alt text](https://github.com/SETHADD/Exploring-FIFA-21-A-Comprehensive-Analysis-of-African-Players-in-Global-Leagues/blob/main/Data%20model%20(power%20bi).png)

## Analysis and Viualization
Upon analysis, it was noticed that Brazil was the non-european country with the most weekly wages and as such compared theirs to that of Africa. Surprisinglty, All the African players combined made approximately $1 million less money than their brazilian counterparts even though Africa had more players.
Again, Nigeria and Senegal had the MOST players (129 each) but the financial value of the Senegalese players was $250,550 more than the Nigerians.

The visualization has;
 * The insights.
 * A Donut Chart of the preferred foot.
 * A map.
 * A bar chart of the sum of wages by country andd other important visuals.
 
![alt text](https://github.com/SETHADD/Exploring-FIFA-21-A-Comprehensive-Analysis-of-African-Players-in-Global-Leagues/blob/main/Power%20Bi%20Visuals.png)

## Conclusion and Recommendation

Africa indeed has great wealth of football talent just like Brazil but is not harnessing a lot money from the sale and most importantly the worth of the players.

As a recommendation, the Confederation of African Football (CAF) can contact the Brazilian Football Confederation to get insights on what they do differently and  turn teach their members to help Africa make the most of their talent.

