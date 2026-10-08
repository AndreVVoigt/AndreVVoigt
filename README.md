# André Voigt

Estudante de Engenharia da Computação no CIn/UFPE, com foco em Engenharia de Dados. Construo pipelines ponta a ponta em AWS, Azure e GCP, com arquitetura Medallion (Bronze/Silver/Gold), processamento distribuído e modelagem dimensional.

Membro da [LED | CIn - UFPE](https://www.linkedin.com/company/led-cin-ufpe/), a Liga de Engenharia de Dados do Centro de Informática.

## Stack

- **Linguagens:** Python, SQL
- **Processamento:** PySpark, Spark SQL, Polars, Pandas, DuckDB
- **Plataformas e armazenamento:** Databricks, Delta Lake, Unity Catalog, Parquet, PostgreSQL
- **Orquestração:** Apache Airflow, Databricks Jobs
- **Cloud:** AWS (S3, Lambda, EMR Serverless, Athena, ECR, IAM), Azure, GCP (Cloud Storage)
- **Ferramentas:** Docker, Git, Power BI, Looker Studio
- **Conceitos:** Data Lakehouse, Arquitetura Medallion, Modelagem Dimensional (Star Schema), ETL/ELT, Qualidade de Dados

## Certificações

- [Microsoft Certified: Azure Data Fundamentals (DP-900)](https://learn.microsoft.com/api/credentials/share/pt-br/AndreVoigt-2563/324319CA09255D65?sharingId=5051D8804E941A27) — Microsoft, agosto de 2026

## Projetos

### [NYC Taxi OLAP: DuckDB + AWS Lambda + S3](https://github.com/AndreVVoigt/olap-lambda-duckdb)
Engine analítica serverless sobre 308 milhões de corridas do táxi de Nova York (2019–2025), em Parquet particionado no S3 e consultada via AWS Lambda com DuckDB.
- Ingestão idempotente dos 84 meses em 3,1 min, sem falhas, com regras de qualidade explícitas (descartar, sinalizar ou manter).
- Agregação do lake inteiro reduzida de timeout (>60 s) para 5,7 s ao ajustar row groups do Parquet, que cortou as requisições ao S3 de ~2.550 para ~190.
- Custo de ~US$ 0,0002 por consulta. [Documentação](https://docs.page/AndreVVoigt/olap-lambda-duckdb)

**Stack:** Python, DuckDB, Parquet, AWS Lambda, S3, ECR, IAM, Docker

### [Data Lakehouse ANP: Preços de Combustíveis](https://github.com/AndreVVoigt/monitor-preco-combustiveis)
Pipeline Medallion no Databricks com a série histórica (2013–2026) e a ingestão semanal dos preços de combustíveis da ANP.
- Ingestão incremental via web scraping, com a carga histórica separada do job semanal para reduzir custo de computação.
- Tratamento de schema drift na fonte e Star Schema (fato + 3 dimensões) consumido no Power BI.

**Stack:** Databricks, Azure, PySpark, Spark SQL, Delta Lake, Unity Catalog, Power BI

### [Lakehouse E-commerce na AWS](https://github.com/AndreVVoigt/lakehouse_ecommerce)
Pipeline Bronze/Silver/Gold sobre eventos de e-commerce, com jobs Spark no EMR Serverless orquestrados pelo Airflow.
- Deduplicação por chave lógica, particionamento por data e agregações diárias (receita, ticket médio, usuários e sessões únicos).
- Camada Gold consultada no Athena via tabelas externas.

**Stack:** AWS (S3, EMR Serverless, Athena), Apache Spark, Apache Airflow, Docker, Python

### [Bike Data Lakehouse (Databricks)](https://github.com/AndreVVoigt/databricks_project1)
Lakehouse Medallion com governança no Unity Catalog, validação de qualidade em PySpark e Spark SQL e Star Schema na camada Gold, orquestrado com Databricks Jobs.

**Stack:** Databricks, PySpark, Spark SQL, Delta Lake, Unity Catalog

### [Pipeline Dengue: Sala de Situação (DATASUS)](https://github.com/AndreVVoigt/pipeline-dengue)
Pipeline sobre milhões de notificações de dengue do SINAN/DATASUS: Data Lake no Cloud Storage, transformação com Polars, carga no PostgreSQL e [dashboard geoespacial](https://lookerstudio.google.com/reporting/50adc11a-611b-452e-9957-15443d9927d1) no Looker Studio.

**Stack:** Python, Polars, GCP (Cloud Storage), PostgreSQL, Looker Studio

### [ETL Olist: Pipeline e Dashboard de Vendas](https://github.com/AndreVVoigt/projeto-etl-olist)
ETL dos dados públicos da Olist com Pandas, carga em PostgreSQL e [dashboard](https://lookerstudio.google.com/reporting/74848e0d-43a6-4637-bb43-b380ca1b9603) de indicadores de vendas.

**Stack:** Python, Pandas, SQLAlchemy, PostgreSQL, Looker Studio

## Contato

[LinkedIn](https://www.linkedin.com/in/andredovalevoigt)
