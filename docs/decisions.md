# Decisões Técnicas

## ADR-001 — Uso de MinIO
### Decisão
Usar MinIO como armazenamento local S3-compatible.

### Motivo
Permite simular um Data Lake próximo ao padrão de mercado sem depender de nuvem pública.

## ADR-002 — Uso de Apache Spark
### Decisão
Usar Spark como engine principal de processamento.

### Motivo
É uma tecnologia amplamente utilizada em pipelines modernas e adequada para transformação em escala.

## ADR-003 — Uso de Apache Iceberg
### Decisão
Usar Iceberg como formato de tabela do lakehouse.

### Motivo
Melhora governança, evolução de schema, organização e leitura analítica em comparação com arquivos soltos.

## ADR-004 — Uso de Project Nessie
### Decisão
Usar Nessie como catálogo da plataforma.

### Motivo
Permite separar metadados do armazenamento físico e aproxima o projeto de arquiteturas modernas.

## ADR-005 — Uso de Trino
### Decisão
Usar Trino como motor SQL independente da transformação.

### Motivo
Demonstra desacoplamento entre processamento e consumo, padrão comum em plataformas modernas.

## ADR-006 — Uso de Superset
### Decisão
Usar Superset como camada de visualização.

### Motivo
Ferramenta open source, adequada para demonstrar consumo analítico e dashboards.

## ADR-007 — Modelo Bronze / Silver / Gold
### Decisão
Adotar arquitetura em camadas.

### Motivo
Melhora organização, rastreabilidade, governança e clareza das transformações.
