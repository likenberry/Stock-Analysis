# Stock Analysis with VBA

## Overview of Project

This project was created to as a way to analyze the results from a bunch of different stocks to look at the returns of these stocks over a course of time. While this analysis could have been done only using Microsoft Excel, this project was accomplished using Visual Basics for Applications (VBA). VBA is programming language that can be used inside of Microsoft Excel. VBA is a way of streamlining complex analyses by writing operatable commands which can fill out Excel spreadsheets. This analysis is looking at 11 specific stocks over the course of 2017 and 2018.

### Purpose

The purpose of this project was to create an analysis of the returns of stocks over the course of two years. This analysis allows a perspective buyer to see how well certains stocks did over the course of the two years to consider if investing is a good idea. This was done by writing a VBA script to loop over all of the data and return the desired results from the specific stocks in question. A timer was added as a way to know how long this analysis would take and conditional formatting was added to show which stocks had positive returns and which stocks had negative returns. A button was added to make the analysis interactive and allowing anyone to complete the analysis without having to understand how to run the code behind the button. Finally, the original VBA script was refactored or editted to make it adaptable to run with data from the entire stock market in less time.

## Results

The final VBA script written for this project was able to ask for the user's input for what year they would like to run an analysis on, either 2017, or 2018, output conditionally formatted results to show which stocks had a positive or negative return and a popup window with how long it took the script to run at the push of a button. In order to find the last row of data for the VBA script to run through a little research had to be done on Stackoverflow.com, this research returned a formula for finding the last row of data in a spreadsheet. This is the formula: RowCount = Cells(Rows.Count, "A").End(xlUp).Row. "RowCount" is the name of the variable used for this formula and "A" is the column that the formula is counting through.
![Outcomes of 2017 Stock Analysis](https://github.com/likenberry/Stock-Analysis/blob/main/Resources/VBA_2017_Stocks.png) 
As seen in the image above, most of the stocks in 2017 had positive returns except "TERP". "DQ" had the largest returns with the value of "DQ" increasing by almost 200%.
![Outcomes of 2018 Stock Analysis](https://github.com/likenberry/Stock-Analysis/blob/main/Resources/VBA_2018_Stocks.png) 
As seen in the results from the analysis of 2018, most of the stocks had negative returns except for "ENPH" which had a return of a little over 80% and "RUN" which had a return of 84%. The "Total Daily Volume" for all of the stocks changed between the two years. 
![Timer of 2017 Stocks Analysis](https://github.com/likenberry/Stock-Analysis/blob/main/Resources/VBA_2017_RunTime.png) 
This is the amount of time that it took the script to complete the analysis of 2017. 
![Refactored Timer of 2017 Stocks](https://github.com/likenberry/Stock-Analysis/blob/main/Resources/VBA_Challenge_2017.png) 
Here is the run time for the refactored code for 2017. This shows that the refactored code had a much faster run time than the original code. 
![Timer of 2018 Stocks Analysis](https://github.com/likenberry/Stock-Analysis/blob/main/Resources/VBA_2018_RunTime.png) 
This is the run time for the Stocks Analysis from 2018. 
![Refactored Timer of 2018 Stocks](https://github.com/likenberry/Stock-Analysis/blob/main/Resources/VBA_Challenge_2018.png) 
After the code was refactored, the run time for 2018 Stock Analysis was also less than in the original script.

## Summary

To refactor the original VBA script so that it could be used to analyze the entire stock market instead of only a couple of stocks, the script was refactored to only run through all of the data a single time. Three arrays were initialized to hold the output data. Nested for loops were used to set tickers to zero and check all of the rows for the data in question and increase the count of the ticker. The output worksheet was formatted to hold all of the variables with conditional formatting for the outcomes of the returns based on colors.

### Advantages of Refactoring

One of the advantages of refactoring code include streamlining code so that it can accomplish its program is a shorter amount of time for time sensitve analyses. Refactoring code can also make it less case specific so that it can be used in multiple sitautions. In this project, the refactored VBA code was created to shorten the run time of the analysis and make it adaptable to run on more stocks than in the original script. For the year 2017, the original script took longer to run than for the refactored script. The results were the same for the original and refactored script for 2018, with the refactored script running much faster than the original script. This means that refactoring the script did in fact make the script run faster which was the intended purpose.

### Disadvantages of Recfactoring

One of the disadvantages of refactoring code is that there is no guarentee that refacoring code will make the analysis take less time or make the code more efficient at performing the initial goal. This means that time could have been put into trying to improve the code without actually improving the performance of the code. Whenever functioning code is editted, there is the risk that the edits will cause errors in the code and time will have to be put in to debugging the script. Refactoring this code did take some time to debug and adapt but it did run faster after the refactoring.
