<img width="2096" height="1524" alt="Gemini_Generated_Image_9eki4y9eki4y9eki" src="https://github.com/user-attachments/assets/cea6ef3a-9307-4bf4-95ff-521ae87b418d" /># 📊 UFC 329: Análise de Performance e Análise Preditiva de Ritmo de Luta
## Conor McGregor vs. Max Holloway II (Agosto de 2026)

Este projeto apresenta uma infraestrutura completa de dados (Data Pipeline) que integra engenharia e análise de dados para prever e analisar cenários de performance para a revanche histórica entre Conor McGregor e Max Holloway no UFC 329. 

O projeto demonstra competência em extração de regras de negócio, modelagem em nuvem utilizando **Google BigQuery (SQL)** e desenvolvimento de inteligência de negócios visual no **Power BI**.

---

## 🛠️ Arquitetura do Projeto

1. **Camada de Processamento Histórico:** Estruturação dos dados brutos de performance atlética dos combatentes (Idade, Média de Golpes por Minuto, Precisão Histórica e Tempo de Inatividade).
2. **Data Warehouse (Cloud):** Persistência dos dados e criação de tabelas otimizadas via Google Cloud Platform (GCP) utilizando **Google BigQuery**.
3. **Data Visualization & Analytics:** Desenvolvimento de um painel executivo (Dashboard) focado em KPIs de combate, volumes e análise preditiva de "Ring Rust" (ferrugem de ringue) conectado via DirectQuery/Import ao BigQuery.

---

## 💾 Modelagem de Dados & SQL (Google BigQuery)

A tabela de análise preditiva foi consolidada e persistida no projeto em nuvem utilizando a seguinte estrutura SQL:

```sql
CREATE OR REPLACE TABLE `estudos-499418.ufc.analise_mcgregor` AS (
  SELECT 
    'Conor McGregor' AS lutador, 
    25 AS idade_2013, 
    55.79 AS precisao_golpes_2013_porcentagem, 
    5.0 AS anos_inatividade_mma, 
    5.32 AS media_golpes_por_minuto, 
    'ALTO' AS risco_ritmo_luta
  UNION ALL
  SELECT 
    'Max Holloway' AS lutador, 
    21 AS idade_2013, 
    29.49 AS precisao_golpes_2013_porcentagem, 
    0.0 AS anos_inatividade_mma, 
    7.14 AS media_golpes_por_minuto, 
    'BAIXO' AS risco_ritmo_luta
);
<img width="2096" height="1524" alt="ufc1" src="https://github.com/user-attachments/assets/a59622f1-bd27-4ac7-acff-b6e813a63b73" />




