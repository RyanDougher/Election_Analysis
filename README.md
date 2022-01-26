# An Analysis of Election Results

## Overview of Project

### Purpose

After receiving election data in the form of a CSV file, the purpose of this analysis was to determine the winner using Python. Once the winner was determined, I completed the audit by providing data on voter turnout for each county, the percentage of votes from each county, and the county with the highest turnout. This all was printed and saved to a .txt file, where the results were easily readable.

## Election Audit Results

-How many votes were cast in this congressional election?
  -369,711 total votes.
  
-Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
  -Jefferson: 10.5% (38,855)
  -Denver: 82.8% (306,055)
  -Arapahoe: 6.7% (24,801)
  
-Which county had the largest number of votes?
  -Denver with 306,055 votes.

-Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
  -Charles Casper Stockham: 23.0% (85,213)
  -Diana DeGette: 73.8% (272,892)
  -Raymon Anthony Doane: 3.1% (11,606)

-Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
  -Winner: Diana DeGette
  -Winning Vote Count: 272,892
  -Winning Percentage: 73.8%

## Election Audit Summary

The purpose of using Python for this election analysis is that this script can be used to retrieve the results of any election, with slight modification. First, the data must be in a .csv file with three columns: Ballot ID, County, and Candidate, in that order. The first modification needed is that the path to load the new .csv file will need to be updated.

  # Add a variable to load a file from a path.
  file_to_load = os.path.join("Resources","election_results.csv")
  # Add a variable to save the file to a path.
  file_to_save = os.path.join("analysis", "election_analysis.txt")
  
 Unless the data is in the same exact format as the one used for this analysis, the next modification will be needed when getting the candidate name and county name from the data. If the data for this are in different rows, that will need to be specified on this code:
 
  # Get the candidate name from each row.
  candidate_name = row[2]
  # 3: Extract the county name from each row.
  county_name = row[1]
  
  With these minor modifications, this code can be used with other election datasets.
