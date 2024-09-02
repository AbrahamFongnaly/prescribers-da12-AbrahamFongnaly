## Prescribers Database

For this exericse, we used the database derived from the [Medicare Part D Prescriber Public Use File](https://www.hhs.gov/guidance/document/medicare-provider-utilization-and-payment-data-part-d-prescriber-0). More information about the data is contained in the Methodology PDF file. See also the included entity-relationship diagram.

### Objective
The objective of this exercise is to explore and analyze the prescriber database to gain insights into prescription claims, drug costs, and specialties. Use joins, groupby, and orderby functions to answer specific questions and perform other tasks to understand trends and patterns in the data.

### Project Structure

**Prescriber Claims Analysis**
   
1. Top Prescriber by Claims:
  a. Identify which prescriber had the highest total number of claims across all drugs. Report the NPI and the total number of claims.
  b. For the top prescriber, provide additional details including the NPPES provider's first and last name, specialty description, and the total number of claims.
2. Specialty Analysis
  a. Determine which specialty had the highest total number of claims across all drugs.
  b. Identify which specialty had the highest total number of claims specifically for opioids.
  c. Challenge Question: Are there any specialties listed in the prescriber table that have no associated prescriptions in the prescription table?
  d. Difficult Bonus: Do not attempt until you have solved all other problems! For each specialty, calculate the percentage of total claims that are for opioids. Identify the specialties with a high percentage of opioid claims.
3. Drug Cost Analysis
  a. Find which drug (by generic name) had the highest total drug cost.
  b. Identify which drug (by generic name) had the highest total cost per day. Bonus: Round the cost per day to 2 decimal places.
4. Drug Classification
  a. For each drug in the drug table, categorize it into one of three types: 'opioid' if opioid_drug_flag is 'Y', 'antibiotic' if antibiotic_drug_flag is 'Y', and 'neither' otherwise. Hint: Use a CASE expression for this classification.
  b. Based on the classification from part a, compare the total spending on opioids versus antibiotics. Hint: Format the total costs as MONEY for easier comparison.
5. CBSA and Population Analysis
  a. Count how many CBSAs are located in Tennessee. Warning: The CBSA table contains information for all states, not just Tennessee.
  b. Identify which CBSA has the largest combined population and which has the smallest. Report the CBSA name and total population.
  c. Find the largest county (by population) not included in any CBSA. Report the county name and population.
6. Prescription Claims
  a. Find all rows in the prescription table where total_claims is at least 3000. Report the drug name and the total claim count.
  b. For the rows identified in part a, add a column indicating whether the drug is an opioid.
  c. Further enhance the results by adding another column that includes the prescriber’s first and last name associated with each row.
7. Pain Management Specialists
  a. Create a list of all NPI/drug_name combinations for pain management specialists (specialty_description = 'Pain Management') in Nashville (nppes_provider_city = 'NASHVILLE') for opioids (opioid_drug_flag = 'Y'). Warning: Double-check your query before running it.
  b. Report the number of claims per drug per prescriber. Ensure that all combinations are included, even if the prescriber had no claims. Report the NPI, drug name, and number of claims.
  c. Fill in any missing values for total_claim_count with 0. Hint: Use the COALESCE function to handle missing values.

This project was completed as part of an apprenticeship with Nashville Software School.
