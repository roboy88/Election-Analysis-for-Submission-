# -*- coding: UTF-8 -*-
"""PyPoll Homework Challenge Solution."""
Initialize a county list, like the candidate_options list, that will hold the names of the counties.
Initialize a dictionary, like the candidate_votes dictionary, that will hold the county 
as the key and the votes cast for each county as the values.
# Add our dependencies.
from ast import Break
from cgi import print_directory
import csv
import os
from tkinter import X

# Add a variable to load a file from a path.
file_to_load = os.path.join("..", "Resources", "election_results.csv")
# Add a variable to save the file to a path.
file_to_save = os.path.join("analysis", "election_analysis.txt")

# Initialize a total vote counter.
total_votes = 369,711

county_votes:
Jefferson:10.5% (38,855)
Denver: 82.8% (306,055)
Arapahoe: 6.7%


# Candidate Options and candidate votes.
candidate_options = [candidate_results]
data = list()
print(data)
candidate_votes = {}
data = list()
print(data)
data = list()
print(data)

election_results

total_votes: 369,711
county_votes:
Jefferson: 10.5% (38,855
Denver:82.8% (306,055)
Arapahoe: 6.7% (24,801)

Largest County Tournout: Denver
Charles Casper Stockham:23.0% (85,213)

Diana DeGette: 73.8% (272,892)

Raymon Anthony Doane: 3.1% (11,606)

Winner: Diana DeGette
Winning Vote Count; 272,892
Winning winning_percentage; 73.8% 

# 1: Create a county list and county votes dictionary.
election_results.txt

Initialize an empty string, like winning_candidate, 
that will hold the county name for the county with the largest turnout.
Initialize a variable, like the winning_count variable, 
that will hold the number of votes of the county that had the largest turnout.
# Track the winning candidate, vote count and percentage
winning_candidate = "largest turnout"
winning_count = 0 ""
# votes with largest county turnout
winning_percentage = 0
Write a decision statement with a logical operator to check if 
the county name acquired in Step 3 is in the county list you created in Step 1.
# 2: Track the largest county and county voter turnout.
votes=["votes", "winning %percentage", "winning candidate"]
for x in total_votes:
    print_directory(X)
    if x == "winning %percentage":
        break




# Read the csv and convert it into a list of dictionaries
with open(file_to_load) as election_data:
    reader = csv.reader(election_data)

    # Read the header
    header = next(reader)

    # For each row in the CSV file.
    for row in reader:

        # Add to the total vote count
        total_votes = total_votes + 1

        # Get the candidate name from each row.
        candidate_name = row[2]

        # 3: Extract the county name from each row.


        # If the candidate does not match any existing candidate add it to
        # the candidate list
        if candidate_name not in candidate_options:

            # Add the candidate name to the candidate list.
            candidate_options.append(candidate_name)

            # And begin tracking that candidate's voter count.
            candidate_votes[candidate_name] = 0

        # Add a vote to that candidate's count
        candidate_votes[candidate_name] += 1

        # 4a: Write an if statement that checks that the
        # county does not match any existing county in the county list.


            # 4b: Add the existing county to the list of counties.


            # 4c: Begin tracking the county's vote count.


        # 5: Add a vote to that county's vote count.



# Save the results to our text file.
with open(file_to_save, "w") as txt_file:

    # Print the final vote count (to terminal)
    election_results = (
        f"\nElection Results\n"
        f"-------------------------\n"
        f"Total Votes: {total_votes:,}\n"
        f"-------------------------\n\n"
        f"County Votes:\n")
    print(election_results, end="")

    txt_file.write(election_results)

    # 6a: Write a for loop to get the county from the county dictionary.

        # 6b: Retrieve the county vote count.

        # 6c: Calculate the percentage of votes for the county.


         # 6d: Print the county results to the terminal.

         # 6e: Save the county votes to a text file.

         # 6f: Write an if statement to determine the winning county and get its vote count.


    # 7: Print the county with the largest turnout to the terminal.


    # 8: Save the county with the largest turnout to a text file.


    # Save the final candidate vote count to the text file.
    for candidate_name in candidate_votes:

        # Retrieve vote count and percentage
        votes = candidate_votes.get(candidate_name)
        vote_percentage = float(votes) / float(total_votes) * 100
        candidate_results = (
            f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")

        # Print each candidate's voter count and percentage to the
        # terminal.
        print(candidate_results)
        #  Save the candidate results to our text file.
        txt_file.write(candidate_results)

        # Determine winning vote count, winning percentage, and candidate.
        if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage

    # Print the winning candidate (to terminal)
    winning_candidate_summary = (
        f"-------------------------\n"
        f"Winner: {winning_candidate}\n"
        f"Winning Vote Count: {winning_count:,}\n"
        f"Winning Percentage: {winning_percentage:.1f}%\n"
        f"-------------------------\n")
    print(winning_candidate_summary)

    # Save the winning candidate's name to the text file
    txt_file.write(winning_candidate_summary)




# -*- coding: UTF-8 -*-
"""PyPoll Homework Challenge Solution."""

# Add our dependencies.
import csv
import os


#set the current directory
os.chdir("C:/Users/raney/OneDrive/Desktop/Analysis_Projects/Election_Analysis")
# Add a variable to load a file from a path.
file_to_load = os.path.join( "Resources", "election_results.csv")
# Add a variable to save the file to a path.
file_to_save = os.path.join("analysis", "election_results.txt")

# Initialize a total vote counter.
total_votes = 0

# Candidate Options and candidate votes.
candidate_options = []
candidate_votes = {}

# 1: Create a county list and county votes dictionary.
county_list = []
county_votes = {}


# Track the winning candidate, vote count and percentage
winning_candidate = ""
winning_count = 0
winning_percentage = 0

# 2: Track the largest county and county voter turnout.
largest_county = ""
county_voter_turnout = 0
winning_county_percentage = 0


# Read the csv and convert it into a list of dictionaries
with open(file_to_load) as election_data:
    reader = csv.reader(election_data)

    # Read the header
    header = next(reader)

    # For each row in the CSV file.
    for row in reader:

        # Add to the total vote count
        total_votes = total_votes + 1

        # Get the candidate name from each row.
        candidate_name = row[2]

        # 3: Extract the county name from each row.
        county_name  = row[1]


        # If the candidate does not match any existing candidate add it to
        # the candidate list
        if candidate_name not in candidate_options:

            # Add the candidate name to the candidate list.
            candidate_options.append(candidate_name)

            # And begin tracking that candidate's voter count.
            candidate_votes[candidate_name] = 0

        # Add a vote to that candidate's count
        candidate_votes[candidate_name] += 1

        # 4a: Write an if statement that checks that the
        # county does not match any existing county in the county list.
        if county_name not in county_list:            

            # 4b: Add the existing county to the list of counties.
            county_list.append(county_name)


            # 4c: Begin tracking the county's vote count.
            county_votes[county_name] = 0


        # 5: Add a vote to that county's vote count.
        county_votes[county_name] += 1



# Save the results to our text file.
with open(file_to_save, "w") as txt_file:

    # Print the final vote count (to terminal)
    election_results = (
        f"\nElection Results\n"
        f"-------------------------\n"
        f"Total Votes: {total_votes:,}\n"
        f"-------------------------\n\n"
        f"County Votes:\n")
    print(election_results, end="")

    txt_file.write(election_results)

    # 6a: Write a for loop to get the county from the county dictionary.

    for county_name in county_votes:

        # 6b: Retrieve the county vote count.
        votes = county_votes.get(county_name)

        # 6c: Calculate the percentage of votes for the county.

        vote_percentage = float(votes)/float(total_votes) * 100


        # 6d: Print the county results to the terminal.
        county_results = (f"{county_name}: {vote_percentage:.1f}% ({votes:,})\n")
        print(county_results, end="")

        # 6e: Save the county votes to a text file.
        txt_file.write(county_results)

        # 6f: Write an if statement to determine the winning county and get its vote count.
        if (votes > county_voter_turnout) and (vote_percentage > winning_county_percentage):
            county_voter_turnout = votes
            largest_county = county_name
            winning_county_percentage = vote_percentage


    # 7: Print the county with the largest turnout to the terminal.
    winning_county_summary = (
        f"\n-------------------------\n"
        f"Largest County Turnout: {largest_county}\n"                
        f"-------------------------\n")
    
    print(winning_county_summary)


    # 8: Save the county with the largest turnout to a text file.
    txt_file.write(winning_county_summary)

    # Save the final candidate vote count to the text file.
    for candidate_name in candidate_votes:

        # Retrieve vote count and percentage
        votes = candidate_votes.get(candidate_name)
        vote_percentage = float(votes) / float(total_votes) * 100
        candidate_results = (
            f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")

        # Print each candidate's voter count and percentage to the
        # terminal.
        print(candidate_results)
        #  Save the candidate results to our text file.
        txt_file.write(candidate_results)

        # Determine winning vote count, winning percentage, and candidate.
        if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage

    # Print the winning candidate (to terminal)
    winning_candidate_summary = (
        f"-------------------------\n"
        f"Winner: {winning_candidate}\n"
        f"Winning Vote Count: {winning_count:,}\n"
        f"Winning Percentage: {winning_percentage:.1f}%\n"
        f"-------------------------\n")
    print(winning_candidate_summary)

    # Save the winning candidate's name to the text file
    txt_file.write(winning_candidate_summary)

    The analysis of the election show that:

There were 369,711 votes cast in the election

County Votes breakdown:

Jefferson: 10.5% (38,855)
Denver: 82.8% (306,055)
Arapahoe: 6.7% (24,801)
County wuth largest number of votes: Denver

The candidates were:

Charles Casper Stockham
Diana DeGette
Raymon Anthony Doane
Candidate Votes breakdown:

Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
Diana DeGette received 73.8% of the vote and 272,892 number of votes.
Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
The winnner of the election was:

Diana DeGette, who received 73.8% of vote and 272,892 number of votes.