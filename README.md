# Data Pipeline: Tarifas Aéreas Brasileiras

Este projeto consiste em uma pipeline de dados desenvolvida no **Azure Databricks** para o processamento e análise do histórico de tarifas aéreas no Brasil. O objetivo é transformar dados operacionais brutos em insights estratégicos sobre o comportamento de preços no setor de aviação.

## Arquitetura do Projeto

O projeto utiliza a **Arquitetura Medalhão (Medallion Architecture)** para garantir a governança e qualidade dos dados em cada etapa da jornada:

* **Camada Raw (Bronze):** Ingestão e armazenamento dos dados brutos em seu formato original.
* **Camada Trusted (Silver):** Etapa de limpeza, padronização de tipos, tratamento de valores nulos e filtragem utilizando **PySpark**.
* **Camada Business (Gold):** Tabelas agregadas e otimizadas para consumo de Business Intelligence, focadas em métricas de preço médio por trecho e sazonalidade.

## Stack Tecnológica

* **Linguagem:** Python (PySpark)
* **Ambiente:** Databricks (Community Edition)
* **Armazenamento:** Delta Lake / DBFS
* **Visualização:** Power BI
* **Versionamento:** Git / GitHub

## Visualização dos Resultados

Abaixo, a representação visual dos dados processados através da camada Business:

[Dashboard Preview]
https://github.com/tnovakED/tarifas-aereas-br/blob/main/Report-Tarifas.pdf

*(O detalhamento completo dos indicadores também pode ser consultado no arquivo disponível neste repositório, link acima)*

## Organização do Repositório

* `/raw`: Notebooks de ingestão inicial.
* `/trusted`: Processos de transformação e saneamento.
* `/business`: Agregações finais para KPIs de negócio.
* `Report-Tarifas.pdf`: Documento consolidado da análise.

---

**Desenvolvido por Tiago** *Foco em Engenharia de Dados e Análise de Business Inteligence da Aviação.*