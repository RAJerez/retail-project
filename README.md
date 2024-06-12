#### Una buena práctica es testear las task que voy agregando a mi dag
Paso 1: Acceder a la CLI de Airflow
    
    $ astro dev bash

Paso 2: Correr test

    $ airflow tasks test <dag> <task_id> <YYYY-mm-dd>

#### Para verificar la conexión de Soda a Bigquery:
    
    $ astro dev bash
    $ soda test-connection -d retail -c include/soda/configuration.yml

#### Corriendo el Quality Check
    
    $ astro dev bash
    $ soda scan -d retail -c include/soda/configuration.yml include/soda/checks/sources/raw_invoices.yml
    