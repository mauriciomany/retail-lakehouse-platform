# 🏗️ Arquitetura da Plataforma

## Visão Geral

A plataforma segue o modelo moderno de Data Lake + Lakehouse.

## Fluxo

1. Dados brutos são ingeridos no MinIO (S3-compatible)
2. Spark processa e transforma os dados
3. Iceberg armazena tabelas analíticas
4. Nessie gerencia catálogo/versionamento
5. Trino consulta os dados via SQL
6. Superset consome os dados para visualização

## Princípios

- Separação entre armazenamento e processamento
- Camadas Bronze, Silver e Gold
- Dados imutáveis na ingestão
- Processamento incremental

## Tecnologias

- MinIO → armazenamento
- Spark → processamento
- Iceberg → lakehouse
- Nessie → catálogo
- Trino → query engine
- Superset → BI
