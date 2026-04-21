# 🔄 Pipeline de Dados

## Camadas

### Landing
Dados brutos recebidos sem transformação.

### Bronze
- Estruturação
- Schema definido
- Metadados de ingestão

### Silver
- Limpeza
- Deduplicação
- Enriquecimento

### Gold
- KPIs
- Agregações
- Dados prontos para BI

## Estratégia

- Batch incremental
- Idempotência
- Versionamento via Iceberg
