# Portugal Local Elections Data Analysis

Data on Portuguese Local Elections for "[Câmaras Municipais](https://en.wikipedia.org/wiki/C%C3%A2mara_municipal)" and some analysis. I aggregate data and process data from a number of sources and join them in one .csv file. 

## Analysis 

List of analysis done on this data. 

* [Portuguese Local Elections – Municipalities with more enrolled voters have a higher percentage of abstention](https://llcampos.wordpress.com/2017/04/12/portuguese-local-elections-municipalities-with-more-enrolled-voters-have-a-higher-percentage-of-abstention/)
* [Portuguese Local Elections – Ballot Order Effects](https://llcampos.wordpress.com/2017/04/21/ballot-order-effects-in-portuguese-local-elections/)

Fell free to pull request additions of other analyses. 

## Main Data File

The main data file is available [here](https://github.com/LLCampos/portugal-local-elections/blob/master/data/processed_data/elections_camaras_municipais_portugal.csv). Columns explanation:

### INE_ID
The ID given to the municipality by INE (Nacional Insitute of Statistics).

### year
Election year.

### concelho
Name of the municipality.

### enrolled
Number of people enrolled to vote.

### voters
Number of people who voted. 

### abstention_%
Percentage of people who were enrolled but didn't vote. Calculated as 100 - ((voters/enrolled) * 100).

### blank_votes
Number of blank votes. 

### null_votes
Number of null votes.

### party_initials
Letter by which the party is identified. 

### party_type
TODO 

### votes
Number of people who voted in the party.

### votes_%	
Percentage of people who voted in the party. Calculated as (votes / (voters - blank_votes - null_votes)) * 100

### number_mandates
Number of party representatives elected.

### candidate_name
Name of the main candidate of the party.

### gender
Gender of the main candidate of the party.

### position_ballot
Position of the party in the ballot (for example, 1 means that the party was the first one listed in the ballot).

### problems_ballot_order
If True, it means that there are problems with the data in **position_ballot** column. Description of the problem can be found [here](https://github.com/LLCampos/portugal-local-elections/blob/master/merging_data.ipynb).



 

## Data Sources:
* http://www.dados.gov.pt
* http://www.pordata.pt
