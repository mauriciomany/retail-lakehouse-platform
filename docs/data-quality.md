# Qualidade de Dados

## 1. Objetivo

Definir controles mínimos de qualidade para cada camada da plataforma.

## 2. Princípios

- qualidade é responsabilidade da pipeline
- cada camada possui um nível diferente de exigência
- toda regra relevante deve ser documentada

## 3. Regras por camada

### Landing
Controles mínimos:
- arquivo recebido
- estrutura legível
- metadado de origem identificado

### Bronze
Controles esperados:
- schema definido
- tipos básicos válidos
- colunas técnicas presentes
- volume carregado conhecido

### Silver
Controles esperados:
- duplicidade tratada
- chaves obrigatórias válidas
- nulos tratados
- integridade entre domínios
- regras de negócio aplicadas

### Gold
Controles esperados:
- indicadores reconciliáveis
- agregações corretas
- métricas consistentes
- nomes compreensíveis para negócio

## 4. Tipos de validação

- completude
- unicidade
- conformidade de tipos
- integridade referencial
- consistência temporal
- reconciliação de volume

## 5. Evidências

Sempre que possível, validar por meio de:
- contagem de registros
- comparação entre origem e destino
- queries de conferência
- testes simples por camada

## 6. Resultado esperado

O projeto deve demonstrar que qualidade de dados não é apenas tratamento técnico, mas parte central da confiabilidade da solução.
