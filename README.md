# Analyzing customer spending behavior for an e-commerce business

Let's try analyzing customer behavior!

Things I have learned:

=> dbt technical:
- everytime I added a new column in seed, I need to do a full refresh (dbt seed --full-refresh) or it will cause an error
<img width="1412" height="204" alt="image" src="https://github.com/user-attachments/assets/5af34549-6a1e-45cd-8a6f-75bb7b6f831f" />

- don't forget to run dbt commands inside the dbt project or it will cause an error
- there are 3 stages in dbt:
  - staging
    in staging, we can clean up and prepare our data such as removing null values, casting columns data type, renaming columns, etc.
  - intermediate (not yet used here)
    this stage is used for complicated logic transformation, where multiple stagings are involved and the result of this intermediate will be reused by many marts
  - mart
    this is the analysis ready stage, the data is clean and the result can be acquired with minimal logic processes and joins
- there are 2 test types in dbt:
  - generic (built-in) tests
    there are 4 test:
    - unique
    - not_null
    - accepted_values
    - relationships
  - singular tests
    tests that can be customized as we needed
  - commonly used commands:
    - dbt run
    - dbt seed
    - dbt build
    - dbt debug
    - dbt test
