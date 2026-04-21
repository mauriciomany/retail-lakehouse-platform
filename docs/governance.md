# Governança de Dados

## 1. Objetivo

Estabelecer princípios e controles mínimos de governança para a plataforma de dados, mesmo em ambiente local e de portfólio.

## 2. Domínios de dados

Os domínios iniciais do projeto são:

- vendas
- estoque
- produtos
- clientes
- lojas

Cada domínio deve ter definição clara, propósito e responsabilidade lógica.

## 3. Papéis lógicos

### Data Owner
Responsável pelo significado e uso do dado no contexto de negócio.

### Data Steward
Responsável pela definição de regras de qualidade, nomenclatura e conformidade.

### Data Engineer
Responsável pela ingestão, transformação, observabilidade e operação da pipeline.

## 4. Classificação dos dados

Os dados do projeto devem ser classificados em três níveis:

- público
- interno
- sensível

No contexto deste projeto, dados de clientes devem ser tratados com mais atenção, mesmo que simulados.

## 5. Nomenclatura

### Schemas
- bronze
- silver
- gold

### Tabelas
- dim_<entidade>
- fact_<evento>
- stg_<origem> quando aplicável

### Colunas
- snake_case
- nomes claros
- evitar abreviações desnecessárias

## 6. Linhagem

Toda transformação relevante deve permitir responder:

- de onde o dado veio
- o que foi transformado
- para onde o dado foi publicado
- quem consome o dado

## 7. Auditoria

Cada carga deve registrar, sempre que possível:

- data/hora
- origem
- quantidade de registros
- status da execução
- mensagem de erro, se houver

## 8. Controle de acesso

Mesmo em ambiente local, a política recomendada é:

- segredos fora do repositório
- arquivos sensíveis ignorados pelo Git
- credenciais separadas de código

## 9. Retenção e descarte

Como princípio, manter:

- landing para rastreabilidade
- camadas analíticas conforme necessidade do caso
- arquivos temporários fora do versionamento

## 10. Resultado esperado

A governança deve garantir que o projeto tenha clareza técnica, rastreabilidade e postura profissional.
