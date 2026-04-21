# Pipeline de Dados

## 1. Visão geral

A pipeline seguirá o padrão de camadas Landing, Bronze, Silver e Gold.

Esse modelo foi escolhido para separar o dado bruto do dado estruturado, do dado tratado e do dado pronto para consumo analítico.

## 2. Landing

### O que é
Camada de aterrissagem dos dados brutos.

### Objetivo
Preservar os dados exatamente como chegam da origem.

### O que será armazenado
- arquivos CSV
- arquivos JSON
- arquivos de cadastros mestres
- arquivos de vendas e estoque

### Controles esperados
- data/hora de ingestão
- sistema de origem
- nome do arquivo
- partição lógica por data, quando aplicável

## 3. Bronze

### O que é
Primeira camada estruturada do lakehouse.

### Objetivo
Transformar arquivos brutos em tabelas Iceberg com schema definido e metadados técnicos.

### Regras principais
- aplicar schema explícito
- padronizar nomes de colunas
- incluir metadados técnicos
- manter proximidade com a origem

### Resultado esperado
Tabelas estruturadas, rastreáveis e consultáveis.

## 4. Silver

### O que é
Camada de dados tratados e integrados.

### Objetivo
Garantir qualidade mínima para consumo corporativo.

### Regras principais
- deduplicação
- tratamento de nulos
- tipagem correta
- validações de integridade
- enriquecimento com dimensões

### Resultado esperado
Base consistente e integrada entre domínios.

## 5. Gold

### O que é
Camada analítica final.

### Objetivo
Entregar dados prontos para SQL e BI.

### Regras principais
- construção de fatos e dimensões
- agregações
- indicadores
- tabelas orientadas a negócio

### Resultado esperado
Tabelas prontas para dashboards e análise.

## 6. Estratégia operacional

A pipeline será construída inicialmente em batch e com foco em reprodutibilidade.

## 7. Critérios de sucesso

Cada etapa da pipeline deve garantir:

- rastreabilidade
- padronização
- possibilidade de validação
- documentação atualizada
