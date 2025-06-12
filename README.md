
# Challenge_TelecomX-BR

## Visão Geral

Este projeto faz parte do desafio proposto na formação **"Aprendendo a fazer ETL - G8"** do programa **ONE - Oracle Next Education** em parceria com a **Alura**. Seu objetivo é analisar os fatores que contribuem para a evasão (churn) de clientes em uma empresa de telecomunicações, utilizando ferramentas e técnicas de análise de dados.

## Objetivos

- Compreender os fatores que levam ao cancelamento de clientes.
- Aplicar práticas de ETL (Extração, Transformação e Carga).
- Realizar análise exploratória de dados (EDA).
- Construir visualizações e relatórios com insights estratégicos.

## Andamento do Projeto

### Etapas Concluídas

1. **Extração de Dados**
   - Fonte: JSON público da Alura ([link](https://raw.githubusercontent.com/alura-cursos/challenge2-data-science/refs/heads/main/TelecomX_Data.json))
   - Uso do Google Colab com bibliotecas `pandas` e `requests`.
   - Expansão de colunas aninhadas (`customer`, `phone`, `internet`, `account`) com `pd.json_normalize`.
   - Verificação da estrutura final: 7267 registros e 21 colunas, sem valores nulos.

2. **Transformação dos Dados**
   - Análise de valores ausentes com substituição de padrões como "", "None", etc., por `np.nan`.
   - Remoção de 224 registros com `Churn` ausente (variável alvo).
   - Preenchimento de 11 valores ausentes em `Charges.Total` com `0` quando `tenure == 0`.
   - Conversão da coluna `Charges.Total` para `float64`.
   - Verificação de duplicatas por `customerID` e por linha completa (nenhuma duplicata encontrada).
   - Inspeção manual dos valores únicos por coluna para garantir consistência.
   - Criação da coluna `Contas.Diarias` como `Charges.Monthly / 30`, arredondada para duas casas decimais.

## Próximos Passos

- Carga e análise  
- Relatório Final

## Autor

Paulo M. P. Patricio

## Créditos

Desenvolvido como parte da formação **"Aprendendo a fazer ETL - G8"** do programa **ONE - Oracle Next Education** em parceria com a **Alura**.

---

*Acompanhe o progresso do projeto neste repositório!*
