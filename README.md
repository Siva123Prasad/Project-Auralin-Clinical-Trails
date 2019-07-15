# Project-Auralin-Clinical-Trails
  Our goal in this project is to conclude whether a new oral insulin, Auralin, is effective or not.
  
  We will come to a conlusion once we thoroughly analyse the available data and compare the change in HbA1c of Auralin with the existing insulin variety name Novodra.

**Process**

First we will do some data detective work. The datasets that we have here have some obvious problems. Below are most of the problems they have, listed out. 

# Quality

**patients table**
1. Zip code is a float not a string
2. Zip code has four digits sometimes
3. Tim Neudorf height is 27 in instead of 72 in
4. Full state names sometimes, abbreviations other times
5. Dsvid Gustafsson
6. Missing demographic information (address - contact columns) (can't clean)
7. Erroneous datatypes (assigned sex, state, zip_code, and birthdate columns)
8. Multiple phone number formats
9. Default John Doe data
10. Multiple records for Jakobsen, Gersten, Taylor
11. kgs instead of lbs for Zaitseva weight

**treatments table**
1. Missing HbA1c changes
2. The letter 'u' in starting and ending doses for Auralin and Novodra
3. Lowercase given names and surnames
4. Missing records (280 instead of 350)
5. Erroneous datatypes (auralin and novodra columns)
6. Inaccurate HbA1c changes (leading 4s mistaken as 9s)
7. Nulls represented as dashes (-) in auralin and novodra columns
8. adverse_reactions table
9. Lowercase given names and surnames

# Tidiness
1. Contact column in patients table should be split into phone number and email
2. Three variables in two columns in treatments table (treatment, start dose and end dose)
3. Adverse reaction should be part of the treatments table
4. Given name and surname columns in patients table duplicated in treatments and adverse_reactions tables


# Solution
Here, I have approached 3 facets of data analysis as below.
1. Dealing missing data
2. Eliminating some structural issues: Tidiness
3. Cleaning some content issues: Quality

Each will be dealt with in a separate .ipnyb file
