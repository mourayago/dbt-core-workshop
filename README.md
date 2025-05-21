# dbt-core-workshop
Educational repository with the purpose of storing learning about dbt

## What is dbt?

dbt (data build tool) is an open-source tool that enables data analysts and engineers to transform data in their warehouse more effectively. It allows you to write modular SQL queries, manage dependencies between them, and version control your transformations using Git. With dbt, you can define your data models as code, test data quality, and generate documentation automatically, all following software engineering best practices. It integrates with modern data warehouses like BigQuery, Snowflake, Redshift, and others.

*by chatgpt*

## What are we going to do

1. First, let's clone the repository and use the Northwind database as an example.

We will use the repository created by the user [lvgalvao](https://github.com/lvgalvao/dbt-core-northwind-project) where we already have the bank to be used and the docker already with the tools that we will use in the project.

2. Repository cloned in */dbt-core-workshop/northwind-project*


`git clone git@github.com:lvgalvao/dbt-core-northwind-project.git
cd dbt-core-northwind-project`

- Docker files are stored at Docker Branch




## Study Notes

- Tudo que o dbt vai rodar fica dentro da pasta models, todos os scripts .sqp que irão criar as views e os reports.
    - dbt-core-workshop\northwind-project\dbt-core-northwind-project\northwind\models
    - Para saber um pouco mais sobre o que ele irá criar, ou seja, os scripts por trás que vão se comunicar com o banco, temos que ir na pasta target, onde lá teremos os scripts DDL's que irão rodar dentro do postgres depois do dbt-run

- Depois que fizemos a instalção das dependências utilizando o docker, entramos nele e na dependencia do dbt-core, clicamos nos três pntinhos para abrir o terminal de comando. Nele rodamos algumas coisas importantes como:
    - dbt debug -> para entender se está tudo o que com a instalação do dbt e com a comunicação com o banco.
    - dbt deps -> instala as dependencias faltantes do projeto
    - dbt run -> executa todos os scripts .sql na pasta models mencionada acima.

- Documentação fica dentro do manifest.json     
    - dbt-core-workshop\northwind-project\dbt-core-northwind-project\northwind\target\manifest.json