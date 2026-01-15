# 🚨 ETL para Detecção de Fraudes Bancárias

## 📌 Visão Geral

Este projeto implementa um **pipeline de ETL (Extract, Transform, Load)** aplicado à **detecção de fraudes bancárias**, utilizando **Python** e a biblioteca **Pandas**.

O objetivo é demonstrar, de forma prática e didática, como dados transacionais bancários podem ser extraídos, transformados com regras de negócio e carregados para análise, apoiando processos de **prevenção a fraudes financeiras**.

---

## 🎯 Objetivos do Projeto

* Simular dados de transações bancárias
* Aplicar conceitos fundamentais de ETL
* Identificar padrões suspeitos de fraude
* Preparar dados para análise e visualização
* Servir como projeto acadêmico e de portfólio

---

## 🏗️ Arquitetura do ETL

```text
CSV de Transações
       ↓
   Extração
       ↓
 Transformação
       ↓
CSV Analítico (Fraudes)
```

---

## 📂 Estrutura do Projeto

```text
├── transacoes_bancarias.csv        # Dados brutos (Extract)
├── etl_fraudes_bancarias.py        # Script principal do ETL
├── fraudes_bancarias_analise.csv   # Dados tratados (Load)
└── README.md                       # Documentação do projeto
```

---

## 📥 Etapa 1 – Extração (Extract)

* Leitura de dados a partir de um arquivo CSV
* Simula um sistema transacional bancário
* Dados incluem:

  * Cliente
  * Data e hora da transação
  * Valor
  * Tipo de transação
  * Canal e localização

---

## 🔄 Etapa 2 – Transformação (Transform)

Durante a transformação, são aplicadas **regras de negócio** para identificar possíveis fraudes:

### 🔍 Regras Implementadas

* **Transações na madrugada** (00h às 05h)
* **Valores elevados** (acima de R$ 5.000)
* **Múltiplas transações em curto intervalo** (≤ 5 minutos)
* Criação de **flag final de suspeita de fraude**

### 🧠 Novas Colunas Criadas

| Coluna                     | Descrição                             |
| -------------------------- | ------------------------------------- |
| transacao_madrugada        | Indica transação em horário atípico   |
| valor_alto                 | Indica valor acima do limite definido |
| muitas_transacoes_seguidas | Indica comportamento suspeito         |
| suspeita_fraude            | Flag final de fraude                  |

---

## 📤 Etapa 3 – Carga (Load)

* Os dados transformados são salvos em um novo arquivo CSV
* Prontos para uso em:

  * Excel
  * Power BI
  * Bancos de dados relacionais
  * Modelos de Machine Learning

---

## 🛠️ Tecnologias Utilizadas

* **Python 3**
* **Pandas**
* **CSV**
* **Jupyter Notebook / VS Code (opcional)**

---

## ▶️ Como Executar o Projeto

1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/etl-banking-fraud-detection.git
```

2. Instale as dependências:

```bash
pip install pandas
```

3. Execute o script:

```bash
python etl_fraudes_bancarias.py
```

4. O arquivo `fraudes_bancarias_analise.csv` será gerado automaticamente.

---

## 📊 Resultados Esperados

* Identificação de transações suspeitas
* Dados organizados e prontos para análise
* Base sólida para dashboards ou modelos de fraude

---

## 📚 Aplicações do Projeto

* Engenharia de Dados
* Prevenção a Fraudes Bancárias
* Estudos de ETL
* Análise de Dados
* Projetos acadêmicos
* Portfólio profissional

---

## 📌 Observações

> Os dados utilizados são **totalmente fictícios** e foram criados apenas para fins educacionais.

---

## 👤 Autor

Projeto desenvolvido para fins **acadêmicos e didáticos**, com foco em **ETL, dados bancários e detecção de fraudes**.
