# What are data unit tests and why we need them

- Theodore Meynard from GetYourGuide

- Talk: https://2022.pycon.de/program/MPWLWP/

  

- What?
- Frameworks for Data unit testing
- In practice at GetYourGuide



## What?

- Data product = Code + Data
- Data product test = Code test + Data test



### How to do data unit testing?

- Verify some expectations. Check
  - Range and Mean
  - Missing values
  - Duplicates
  - no. of samples



## Frameworks

1. Great expectations
   1. Supports SQL, Pandas, Spark
   2. **Data profiling**: Gives a draft of expectations
   3. Data validation
   4. Data documentation
   5. Supports distibution and statitstical tests
2. Pandora
   1. Pandas and Spark
3. TFDV
   1. Tenserflow
4. SODA

