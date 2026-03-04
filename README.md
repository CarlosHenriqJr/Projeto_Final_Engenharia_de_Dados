# Projeto Final Engenharia de Dados - Painel COVID-19

## Visão Geral do Projeto

Este projeto é um trabalho final da disciplina de Engenharia de Dados da Semantix Academy, focado na criação de um pipeline de processamento de dados para a Campanha Nacional de Vacinação contra a COVID-19. O objetivo principal é demonstrar a capacidade de ingestão, processamento, otimização e visualização de grandes volumes de dados utilizando tecnologias do ecossistema Big Data, como Apache Spark, Apache Hive e Apache Kafka.

## Tecnologias Utilizadas

*   **Apache Spark:** Utilizado para processamento de dados em larga escala, transformações ETL e criação de visualizações.
*   **Apache Hive:** Para armazenamento de dados estruturados em formato de tabelas, com otimização via particionamento.
*   **HDFS (Hadoop Distributed File System):** Sistema de arquivos distribuído para armazenamento de dados brutos e processados.
*   **Apache Kafka:** Para publicação de dados processados em um tópico, permitindo consumo em tempo real.
*   **Jupyter Notebook:** Ambiente interativo para desenvolvimento e execução do pipeline de dados.

## Arquitetura e Fluxo de Dados

O projeto segue um fluxo de dados que envolve as seguintes etapas:

1.  **Ingestão de Dados:** Os dados brutos da Campanha Nacional de Vacinação contra a COVID-19 são carregados para o HDFS.
2.  **Processamento com Spark:** O Apache Spark é utilizado para ler os dados do HDFS, realizar transformações necessárias e criar diferentes visualizações dos dados.
3.  **Otimização e Armazenamento:**
    *   Os dados são otimizados e armazenados em uma tabela Hive particionada por município.
    *   Uma visualização é salva como tabela Hive.
    *   Outra visualização é salva em formato Parquet com compressão Snappy.
4.  **Publicação de Dados:** Uma visualização final é publicada em um tópico do Apache Kafka para consumo em tempo real.

## Objetivos do Projeto

Os seguintes objetivos foram propostos para o projeto, com seu status de conclusão:

*   ✅ Enviar os dados para o HDFS
*   ✅ Otimizar todos os dados do HDFS para uma tabela Hive particionada por município
*   ✅ Criar as 3 visualizações pelo Spark com os dados enviados para o HDFS
*   ✅ Salvar a primeira visualização como tabela Hive
*   ✅ Salvar a segunda visualização com formato Parquet e compressão Snappy
*   ✅ Salvar a terceira visualização em um tópico no Kafka


## Como Executar o Projeto

Para executar este projeto, é necessário ter um ambiente Big Data configurado com Apache Hadoop (HDFS), Apache Hive, Apache Spark e Apache Kafka. O Jupyter Notebook `Projeto_Final.ipynb` contém o código para todas as etapas do pipeline.

1.  **Configuração do Ambiente:** Certifique-se de que todas as dependências (Spark, Hive, Kafka) estejam instaladas e configuradas corretamente no seu ambiente.
2.  **Carregar Dados:** O arquivo `PAINEL_COVIDBR.rar` (localizado em `Dados/`) contém os dados brutos. Descompacte-o e carregue o arquivo CSV resultante para o HDFS.
3.  **Executar Jupyter Notebook:** Abra o `Projeto_Final.ipynb` em um ambiente Jupyter e execute as células sequencialmente. Certifique-se de que a `SparkSession` seja inicializada corretamente antes de qualquer operação Spark.

## Melhorias Futuras

*   **Concluir Integração com ElasticSearch/Kibana:** Finalizar a etapa de envio de dados para o ElasticSearch e a criação de dashboards no Kibana para visualização interativa.
*   **Otimização de Performance:** Explorar técnicas avançadas de otimização do Spark e Hive para datasets maiores.
*   **Automação do Pipeline:** Implementar ferramentas de orquestração (e.g., Apache Airflow) para automatizar a execução do pipeline.
*   **Monitoramento:** Adicionar monitoramento para o pipeline de dados e os serviços envolvidos.
*   **Documentação Detalhada:** Fornecer documentação mais aprofundada sobre cada etapa do processo, incluindo esquemas de dados e exemplos de consultas.

## Autor

**Carlos Henrique de Assis Junior**

*   **Instituição:** Semantix Academy
*   **Turma:** Big Data Engineer 08-2022
*   **Professor:** Rodrigo Rebouças
