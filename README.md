# Election-analysis
# Overview of Project
My example client, Tom, and his manager, Seth, are counting votes for a Congressional district election in Colorado. The task at hand was to count the total number of votes that were cast and the number of votes for each candidates for an election audit. The next step would be to convert these candidate votes into percentages, and whichever candidate has the higher percentage of votes wins the Congressional district election. I was able to accomplish this for Tom and Seth through the modules for them to submit to the election commission, but they have requested that a similar Python code be run for the counties to complete their audit. 
## Purpose
The purpose of this Python project is to figure out the voter turnout per county, the percentage of votes from each county out of the total vote count and then the county with the highest turnout. 
# Results
As a result of the analysis, we were able to generate the total number of votes, the number of county votes dispered between Jefferson, Denver, and Arapahoe counties along with the percentages, which county had the largest turnout, the number of votes dispered between the 3 candidates, and the winner with percentage and voter count. 



* In order to find the total amount of votes cast for the Congressional election, the first step was to initialize a voter counter set at 0. It is set at 0 as this is the number the count needs to begin at every time the file is run. This is also put before the code where the file is actually opened to make sure the counter is established. Then, I initiated the increments to increase by 1 every time the file is run to print out all of the votes until there aren't any anymore.

* To figure out the number of votes cast from a specific county, I needed to run a decision statement once the file was open to access this data. I set the decision statement to see if the county presented matches any of the counties in the data. If the county does not match, then the code would add the county, but if it does match, it would either add the county for the first time it is mentioned or continue counting votes for that county. Here is a snippet of the code below to determine this: 

      # 4a: Write a decision statement that checks that the county does not match any existing county in the county list.
      if county_name not in county_options:

            # 4b: Add the existing county to the list of counties.
            county_options.append(county_name)

            # 4c: Begin tracking the county's vote count.
            county_votes[county_name] = 0
            
I also used a for loop to go through the county_votes dictionary to retrieve the values within the list, which would be the county_names. These values were then used to calculate the number of votes from the county. The number of votes attained were then put into a percentage formula in order to determine what percent of votes were from which county. 

* To find the county with the highest voter turnout, I used a decision statement to see the winning county and its vote count. I took the vote values from the previous paragraph and related that to the variable "largest_county_votes". Here is a snippet of the code I used to determine this: 

    if (votes > largest_county_votes): 
              largest_county_votes = votes
              largest_county = county_name

* A similar analysis was used for calculating the candidate voter results. To find the total amount of votes for a specific candidate, I ran a decision statement to see if the candidate_name was not in the list for candidate options. If the candidate name was not in the list, then I have the code add the candidate name into the data. If the candidate name was in the list, then I have the code add the name for the first time the name is mentioned or continue counting votes for that specific candidate. I then used a for lop to go through the candidate_votes dictionary to find the candidate names, which then allowed me to get the number of votes for that specific candidate. I put that into a percentage formula to find the percentages of voters each candidate received. 

* I used a similar process to determine which candidate won, what their percentage of votes was, and what the winning vote count was. In order to do this, I used an if statement to find both the winning count vs the votes and the winning percentage vs the vote percentage. I have a snippet of the code placed here: 

    if (votes > winning_count) and (vote_percentage > winning_percentage):
                winning_count = votes
                winning_candidate = candidate_name
                winning_percentage = vote_percentage

Here are the finalized results for the analysis:

![PyPoll Results.png](https://github.com/allysakarr/Election-analysis/blob/master/Images%20for%20PyPoll/PyPoll%20Results.png?raw=true).
