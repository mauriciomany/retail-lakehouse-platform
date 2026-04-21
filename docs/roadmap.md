# Roadmap do Projeto

## Etapa 0 — Base documental e governança
- [x] Estruturar documentação inicial
- [x] Definir visão arquitetural
- [x] Definir princípios de governança
- [x] Definir regras iniciais de qualidade

## Etapa 1 — Definição do domínio de negócio
- [ ] Definir entidades do varejo
- [ ] Definir granularidade dos dados
- [ ] Definir KPIs principais
- [ ] Definir fontes simuladas

## Etapa 2 — Landing e Bronze
- [ ] Organizar estrutura de entrada
- [ ] Criar primeira tabela Iceberg Bronze
- [ ] Registrar metadados técnicos
- [ ] Validar leitura via Spark e Trino

## Etapa 3 — Silver
- [ ] Aplicar limpeza
- [ ] Deduplicar dados
- [ ] Integrar domínios
- [ ] Validar qualidade

## Etapa 4 — Gold
- [ ] Criar fatos e dimensões
- [ ] Criar agregações
- [ ] Publicar indicadores

## Etapa 5 — Consumo analítico
- [ ] Consultar via Trino
- [ ] Conectar Superset
- [ ] Criar dashboards iniciais

## Etapa 6 — Evolução
- [ ] Automatizar geração de dados
- [ ] Criar testes de qualidade
- [ ] Implementar observabilidade
- [ ] Avaliar orquestração
