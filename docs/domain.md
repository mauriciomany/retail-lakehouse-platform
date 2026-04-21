# 🛒 Domínio de Negócio — Varejo

## 1. Objetivo

Definir o domínio de dados utilizado no projeto de plataforma de dados para varejo omnichannel.

---

## 2. Entidades principais

### Sales
Transação de venda.

### Sales Item
Item individual dentro de uma venda.

### Product
Catálogo de produtos.

### Store
Lojas físicas ou canais digitais.

### Customer
Clientes.

### Inventory
Estoque por produto e loja.

---

## 3. Granularidade

### Fato principal (sales_item)
- 1 linha por item vendido por pedido

### Estoque
- produto + loja + data

---

## 4. KPIs

- faturamento
- ticket médio
- margem
- vendas por canal
- vendas por categoria
- giro de estoque
- ruptura de estoque

---

## 5. Fontes de dados

- store_sales.csv
- ecommerce_orders.json
- inventory.csv
- products.csv
- stores.csv
- customers.csv

---

## 6. Regras de negócio

### Vendas
- valor total = quantidade * preço - desconto
- canal identificado

### Produtos
- categoria obrigatória

### Clientes
- podem ser anônimos

### Estoque
- não deve ser negativo

---

## 7. Domínios

- sales
- inventory
- product
- customer
- store
