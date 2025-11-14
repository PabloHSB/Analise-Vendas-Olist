# 📊 Análise de Vendas E-commerce (Olist)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458)
![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-orange)
![Status](https://img.shields.io/badge/Status-Concluído-green)

## 📝 Sobre o Projeto

Este é um projeto de **Análise Exploratória de Dados (EDA)** realizado sobre o dataset público do **Olist** (maior departamento de e-commerce do Brasil), abrangendo cerca de 100 mil pedidos feitos entre 2016 e 2018.

O objetivo não foi apenas limpar os dados, mas agir como um **Analista de Dados** para responder perguntas estratégicas de negócio, validando hipóteses sobre comportamento do consumidor, performance logística e concentração de receita.

---

## 🔍 Principais Descobertas (Insights)

A análise revelou 4 pontos chave sobre a operação:

### 1. Concentração Geográfica do Faturamento 📍
O faturamento é massivamente concentrado na **Região Sudeste**.
* **São Paulo (SP)** é o líder absoluto, gerando quase **R$ 6 milhões** em receita.
* Isso representa mais que o dobro do segundo colocado (**Rio de Janeiro**), indicando uma forte dependência logística e comercial de um único estado.

### 2. A "Batalha" das Categorias: Volume vs. Valor 🛍️
**Hipótese Inicial:** Categorias de tecnologia (`informatica_acessorios`) gerariam maior faturamento devido ao alto valor agregado.
**Realidade dos Dados:** A hipótese foi refutada. A categoria **`cama_mesa_banho`** é a campeã absoluta, liderando tanto em **quantidade de vendas** (11.1k itens) quanto em **faturamento total** (R$ 1.7M). Isso sugere um perfil de consumidor focado em utilidades domésticas.

### 3. Estratégia Logística e Gestão de Expectativa 🚚
A Olist entrega, em média, **11 dias antes** do prazo prometido.
* **O Insight:** Em estados do Norte (como **AC, AM, RR**), essa "antecedência" chega a **20 dias**.
* **A Causa:** Não é que a entrega seja mais rápida (esses estados têm o maior tempo real de trânsito, ~28 dias). A empresa utiliza uma estratégia de **prazos de segurança estendidos** para essas regiões, garantindo a satisfação do cliente mesmo com a complexidade logística.

### 4. Preferência de Pagamento 💳
O **Cartão de Crédito** domina as transações com **73.9%** de participação, seguido pelo Boleto (19%). Isso reforça a importância de oferecer opções competitivas de parcelamento para manter a conversão.

---

## 🛠️ Tecnologias Utilizadas

* **Python:** Linguagem principal.
* **Pandas:** Para manipulação, limpeza (cleaning), junção de tabelas (merge) e agregações (groupby).
* **Matplotlib:** Para criação de visualizações de dados e relatórios gráficos.
* **KaggleHub:** Automação do download do dataset diretamente via código.

---

## 📂 Estrutura do Projeto

O projeto foi desenvolvido em um **Jupyter Notebook**, seguindo um fluxo lógico de *Data Storytelling*:

1.  **Ingestão de Dados:** Download automatizado e carregamento de 5 datasets relacionais.
2.  **Tratamento de Dados:** Conversão de tipos temporais, tradução de colunas e tratamento de valores nulos.
3.  **Análise de Faturamento:** Junção de tabelas de Pedidos, Clientes e Pagamentos.
4.  **Análise Logística:** Engenharia de atributos para calcular `tempo_real_entrega` e `atraso`.
5.  **Análise de Produtos:** Comparativo entre categorias de alto giro vs. alto ticket.
6.  **Visualização:** Gráficos formatados para apresentação executiva.

---

## 🚀 Como Executar

Este projeto utiliza a biblioteca `kagglehub` para baixar os dados automaticamente. Não é necessário baixar os CSVs manualmente.

1. Clone o repositório:
```bash
git clone [https://github.com/PabloHSB/Analise-Vendas-Olist.git](https://github.com/PabloHSB/Analise-Vendas-Olist.git)
