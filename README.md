#### A good practice is to test the tasks I am adding to my DAG
Step 1: Access the Airflow CLI
    
    $ astro dev bash

Step 2: Run the test

    $ airflow tasks test <dag> <task_id> <YYYY-mm-dd>

#### To verify the Soda connection to BigQuery:
    
    $ astro dev bash
    $ soda test-connection -d retail -c include/soda/configuration.yml

#### Running the Quality Check
    
    $ astro dev bash
    $ source soda_venv/bin/activate
    $ soda scan -d retail -c include/soda/configuration.yml include/soda/checks/sources/raw_invoices.yml


#### Running dbt models

    $ astro dev bash
    $ source dbt_venv/bin/activate
    $ cd dbt
    $ dbt deps
    $ dbt run --profiles-dir /usr/local/airflow/dbt/