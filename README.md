# Tech Challenge FIAP – Análise do E-commerce Brasileiro (Olist)

**Pós-Tech em Data Analytics · FIAP**

---

## Objetivo

Este projeto tem como objetivo analisar o desempenho do e-commerce brasileiro utilizando dados reais da Olist, com foco em identificar padrões de comportamento, eficiência operacional e fatores que impactam a geração de receita.

A partir dessa análise, busca-se gerar insights acionáveis para apoiar a tomada de decisão estratégica e orientar recomendações de negócio para investidores e executivos.

---

## Contexto do Dataset

Foi utilizado o dataset público da Olist, contendo aproximadamente **100 mil pedidos** realizados entre 2016 e 2018 em diferentes regiões do Brasil. O dataset oferece uma visão completa da jornada de compra: do cadastro do cliente à avaliação pós-entrega.

Fonte: [Olist – Brazilian E-Commerce Public Dataset (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

## Estrutura dos Dados

### Tabelas originais utilizadas

| Arquivo | Descrição |
|---|---|
| `olist_customers_dataset.csv` | Dados dos clientes (localização e identificação) |
| `olist_orders_dataset.csv` | Informações dos pedidos (status e datas) |
| `olist_order_items_dataset.csv` | Itens por pedido (produto, vendedor e preço) |
| `olist_order_payments_dataset.csv` | Formas e valores de pagamento |
| `olist_order_reviews_dataset.csv` | Avaliações e comentários dos clientes |
| `olist_products_dataset.csv` | Dados dos produtos (categoria e dimensões) |
| `olist_sellers_dataset.csv` | Informações dos vendedores |
| `olist_geolocation_dataset.csv` | Coordenadas geográficas por CEP |
| `product_category_name_translation.csv` | Tradução das categorias para o inglês |

## Metodologia

A análise foi conduzida em etapas estruturadas:

- **Integração** — cruzamento das tabelas do dataset por chaves de relacionamento (pedido, cliente, produto, vendedor)
- **Tratamento** — padronização de tipos de dados, remoção de inconsistências e normalização de campos geográficos
- **Construção de métricas** — cálculo de receita líquida, ticket médio, proxy de rentabilidade e indicadores logísticos
- **Análise exploratória (EDA)** — visualizações e estatísticas descritivas para identificar padrões e anomalias

O objetivo foi garantir consistência, qualidade e reprodutibilidade dos resultados.

---

## Principais Análises

As análises foram organizadas em quatro dimensões de negócio:

- **Receita e crescimento por categoria** — quais categorias geram mais valor e apresentam maior potencial de expansão
- **Ticket médio e rentabilidade por estado** — comparativo entre regiões, identificando onde o negócio é mais lucrativo
- **Eficiência logística** — tempo médio de entrega por região e impacto na satisfação do cliente
- **Avaliação do cliente e valor do pedido** — relação entre nota de satisfação e comportamento de compra

Essas dimensões foram analisadas de forma integrada para identificar os principais drivers de performance do negócio.

---

## Principais Insights

- **Concentração no Sudeste:** a região concentra o maior volume de vendas, mas o Norte e o Nordeste apresentam ticket médio mais elevado
- **Trade-off logístico:** regiões mais distantes dos centros de distribuição têm prazos de entrega significativamente maiores, impactando a satisfação e a recorrência de compra
- **Avaliação como alavanca de receita:** pedidos com nota igual ou superior a 4 apresentam valor médio até **6% maior**, indicando que a experiência do cliente influencia diretamente o gasto
- **Oportunidade regional:** estados do Norte e Nordeste, apesar do menor volume, apresentam ticket médio elevado — potencial de rentabilidade com investimento em infraestrutura logística

---

## Recomendações Estratégicas

### Curto prazo (0 a 6 meses)
- Implementar ações para elevar a nota média dos produtos para o patamar de 4 ou mais (resposta rápida, qualidade de embalagem, comunicação pós-venda)
- Otimizar a logística de última milha nas regiões de maior volume (SP, RJ, MG)
- Concentrar esforços de marketing nas categorias líderes de receita para maximizar retorno imediato

### Médio prazo (6 a 18 meses)
- Expandir o portfólio nas categorias com maior crescimento no período analisado
- Desenvolver estratégias de precificação para aumentar o ticket médio nas regiões de maior volume
- Investir em parcerias logísticas regionais para reduzir o prazo de entrega no Norte e Nordeste

### Longo prazo (acima de 18 meses)
- Fortalecer centros de distribuição nas regiões estratégicas
- Desenvolver segmentos premium com produtos de maior valor agregado
- Evoluir a capacidade analítica para uso preditivo dos dados (demanda, retenção e precificação dinâmica)

---

## Estrutura do Repositório

```
tech_challenge_data_analytics/
│
├── notebooks/
│   ├── analise_logistica_rentabilidade_regioes_Caio_Bosnic.ipynb
│   ├── analise_Receita_Olist_TechChallenge_Alexandre_Amorim.ipynb
│   ├── analise_precos_por_nota_Gusthavo_Soares.ipynb
│   └── regioes_maiores_rentabilidade_Allison_Lima.ipynb
│
├── data/
│   ├── olist_customers_dataset.csv
│   ├── olist_orders_dataset.csv
│   ├── olist_order_items_dataset.csv
│   ├── olist_order_payments_dataset.csv
│   ├── olist_order_reviews_dataset.csv
│   ├── olist_products_dataset.csv
│   ├── olist_sellers_dataset.csv
│   ├── olist_geolocation_dataset.csv
│   └── product_category_name_translation.csv
│
└── README.md
```

---

## Como Executar o Projeto

**Pré-requisitos:** Python 3.8+, Jupyter Notebook ou JupyterLab

1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   cd tech_challenge_data_analytics
   ```

2. Instale as dependências necessárias:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

3. Abra o ambiente Jupyter:
   ```bash
   jupyter notebook
   ```

4. Execute os notebooks na pasta `notebooks/` na seguinte ordem sugerida:
   - `analise_logistica_rentabilidade_regioes_Caio_Bosnic.ipynb`
   - `analise_Receita_Olist_TechChallenge_Alexandre_Amorim.ipynb`
   - `analise_precos_por_nota_Gusthavo_Soares.ipynb`
   - `regioes_maiores_rentabilidade_Allison_Lima.ipynb`

> Os arquivos de dados já estão disponíveis na pasta `data/` e são referenciados diretamente pelos notebooks.

---

## Autores

| Nome | RM | Área de Análise |
|---|---|
| Alexandre de Souza Amorim | 372077 | Receita e Crescimento por Categoria |
| Allison Lima | 372648 | Regiões de Maior Rentabilidade |
| Caio Rodrigues Bosnic Barbosa | 372603 | Logística e Rentabilidade por Região |
| Gusthavo Lourenço Rios Soares | 371911 | Preços e Avaliações de Clientes |

**FIAP – Pós-Tech em Data Analytics**