# Arquitetura da Plataforma

## 1. Visão geral

A solução foi concebida como uma plataforma moderna de dados para varejo omnichannel, com separação clara entre ingestão, processamento, armazenamento analítico, consulta e visualização.

O projeto utiliza um modelo Data Lake + Lakehouse, permitindo preservar dados brutos, aplicar transformações em camadas e disponibilizar dados confiáveis para análise.

## 2. Objetivo arquitetural

Os principais objetivos da arquitetura são:

- desacoplar armazenamento, processamento e consumo
- permitir evolução incremental da pipeline
- manter rastreabilidade entre origem e consumo
- demonstrar uma solução próxima ao mercado
- suportar governança e qualidade de dados desde o início

## 3. Componentes

### MinIO
Responsável pelo armazenamento S3-compatible local. Atua como Data Lake para dados brutos e como base física do warehouse do lakehouse.

### Apache Spark
Responsável pelo processamento dos dados, incluindo leitura de arquivos, padronização, validação e transformação entre camadas.

### Apache Iceberg
Formato de tabela analítica utilizado para armazenar as camadas Bronze, Silver e Gold com mais governança, evolução de schema e melhor gestão de arquivos.

### Project Nessie
Catálogo da plataforma, responsável por manter metadados e referências do lakehouse.

### Trino
Motor de consulta SQL desacoplado da camada de processamento. Permite consumo analítico sobre as tabelas Iceberg.

### Superset
Camada de visualização e BI. Será utilizada para dashboards e consumo analítico.

## 4. Fluxo de alto nível

1. Dados são gerados ou recebidos em formatos brutos, como CSV e JSON.
2. Esses dados são armazenados na camada landing no MinIO.
3. O Spark lê os dados brutos e cria tabelas Bronze em Iceberg.
4. O Spark trata e integra os dados para gerar a camada Silver.
5. O Spark consolida agregações e indicadores na camada Gold.
6. O Trino consulta as tabelas analíticas.
7. O Superset consome o Trino para dashboards.

## 5. Princípios adotados

- separação em camadas
- dados brutos preservados
- transformações rastreáveis
- nomenclatura padronizada
- preocupação com governança desde o início
- documentação como parte do produto

## 6. Escopo inicial

O domínio inicial cobre varejo com foco em:

- vendas
- estoque
- produtos
- clientes
- lojas

## 7. Resultado esperado

A arquitetura deve permitir a evolução do projeto de um laboratório técnico para uma solução demonstrável, com narrativa clara de engenharia de dados e arquitetura de dados.
