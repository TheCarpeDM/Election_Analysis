# Election_Analysis

## Overview of Election Audit

This week's task is to help Tom (and Seth) tabulate and audit Colorado's election results. Our goal was to determine who won the election, how many votes each candidate received, and what percentage of the votes each candidate received. We then added for further information the voter turnout for each county, the percentage of votes in each county, and the county with the highest turnout.

## Election Audit Results

### Main Results

* Total Votes: 369,711

### Candidate Results

* **Winner: Diana DeGette**
 * Votes: 272,892
 * Percentage: 73.8%

* 2nd Place: Charles Casper Stockham
 * Votes: 85,213
 * Percentage: 23.0%

* 3rd Place: Raymon Anthony Doane
 * Votes: 11,606
 * Percentage: 3.1%
 
### County Results

* **Largest Turnout: Denver**
 * Votes: 306,055
 * Percentage: 82.8%

* 2nd Largest Turnout: Jefferson
 * Votes: 38,855
 * Percentage: 10.5%

* 3rd Largest Turnout: Arapahoe
 * Votes: 24,801
 * Percentage: 6.7%

## Election Audit Summary

### For Use With Any Election

This script can be used for any state-level election as long as the results are provided in csv format like those in [this election](Resources/election_results.csv). It will handle any number of candidates and counties, and will provide the same data presented in the [output txt file](Analysis/election_analysis). 

### Possible Modifications

To name the text file with the appropriate state's name, you can change line 11 from:
> file_to_save = os.path.join("Analysis", "election_analysis.txt")

to

> file_to_save = os.path.join("Analysis", "state_election_analysis.txt")
where "state" is your state's name.

If your results use different columns for candidates' names and counties, (but are still in csv format), you can change lines 49 and 52 from:
> candidate_name = row[2]

and

> county_name = row[1]
 
to
 
> candidate_name = row[x]

and

> county_name = row[y]

where "x" is the column index (column number - 1) of the candidates' names and "y" is the column index of the county names.
