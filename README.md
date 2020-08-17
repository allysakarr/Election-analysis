# Election-analysis
# Overview of Project
My example client, Tom, and his manager, Seth, are counting votes for a Congressional district election in Colorado. The task at hand was to count the total number of votes that were cast and the number of votes for each candidates for an election audit. The next step would be to convert these candidate votes into percentages, and whichever candidate has the higher percentage of votes wins the Congressional district election. I was able to accomplish this for Tom and Seth through the modules for them to submit to the election commission, but they have requested that a similar Python code be run for the counties to complete their audit. 
## Purpose
The purpose of this Python project is to figure out the voter turnout per county, the percentage of votes from each county out of the total vote count and then the county with the highest turnout. 
# Results
As a result of the analysis, we were able to generate the total number of votes, the number of county votes dispered between Jefferson, Denver, and Arapahoe counties along with the percentages, which county had the largest turnout, the number of votes dispered between the 3 candidates, and the winner with percentage and voter count. See the image below for the finalized version of the data analysis for Tom and Seth:



In order to find the total amount of votes cast for the Congressional election, the first step was to initialize a voter counter set at 0. It is set at 0 as this is the number the count needs to begin at every time the file is run. This is also put before the code where the file is actually opened to make sure the counter is established. Then, I initiated the increments to increase by 1 every time the file is run to print out all of the votes until there aren't any anymore.

