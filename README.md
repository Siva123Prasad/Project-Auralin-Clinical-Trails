# Project-Auralin-Clinical-Trails
  Our goal in this project is to conclude whether a new oral insulin, Auralin, is effective or not.
  
  We will come to a conlusion once we thoroughly analyse the available data and compare the change in HbA1c of Auralin with the existing insulin variety name Novodra.

**Process**

First we will do some data detective work. The datasets that we have here have some obvious problems. Below are most of the problems they have, listed out. 

# Quality

**patients table**
Zip code is a float not a string
Zip code has four digits sometimes
Tim Neudorf height is 27 in instead of 72 in
Full state names sometimes, abbreviations other times
Dsvid Gustafsson
Missing demographic information (address - contact columns) (can't clean)
Erroneous datatypes (assigned sex, state, zip_code, and birthdate columns)
Multiple phone number formats
Default John Doe data
Multiple records for Jakobsen, Gersten, Taylor
kgs instead of lbs for Zaitseva weight

**treatments table**
Missing HbA1c changes
The letter 'u' in starting and ending doses for Auralin and Novodra
Lowercase given names and surnames
Missing records (280 instead of 350)
Erroneous datatypes (auralin and novodra columns)
Inaccurate HbA1c changes (leading 4s mistaken as 9s)
Nulls represented as dashes (-) in auralin and novodra columns
adverse_reactions table
Lowercase given names and surnames
# Tidiness
Contact column in patients table should be split into phone number and email
Three variables in two columns in treatments table (treatment, start dose and end dose)
Adverse reaction should be part of the treatments table
Given name and surname columns in patients table duplicated in treatments and adverse_reactions tables
