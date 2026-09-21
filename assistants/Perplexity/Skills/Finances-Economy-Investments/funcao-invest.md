---
name: functions
description: "Função para calcular a alocação de investimentos baseado nos critérios definidos pelo usuário."
metadata:
  author: nelson
  version: '1.0'
---

# Função INVEST

## Quando Usar Esta Skill

Use quando o usuário solicitar a função INVEST definida com um valor e lista de referência (opcional).
Exemplos:
- INVEST(1000)
- INVEST(500, IBOVESPA)

## Instruções

### 1. Coleta de Dados

Executar a análise fundamentalista definida na skill correspondente neste espaço, para a lista de ações desejada. Caso não seja informado o segundo parâmetro (referente a qual índice, lista, etc., levar em conta), considerar a lista provida pelo usuário, neste momento ou anteriormente no contexto da conversa. Não incluir nunca papéis cuja análise fundamentalista resulte em um valor negativo.

### 2. Avaliação dos Critérios

A seguir, organizar os aportes de acordo com os critérios a seguir, em ordem de importância:

---

**Critério 1 — Força**
> Preferir empresas que tenham maior "força" (ou seja, obtenham uma pontuação maior) na análise fundamentalista.

---

**Critério 2 — Perenidade e resiliência do setor**
> Priorizar aqui os papéis que pertençam a empresas de setores perenes e menos sensíveis a regulações ou variações de mercado.

**Critério 3 — Preço/Lucro**
> Preferir as ações que estejam com menor preço por lucro, ou que estejam "descontadas".

---

**Critério 4 — Dividendos**
> Priorizar aqui as empresas que pagam mais dividendos consistentemente; isso importa mais que dividend yields pontuais.

---

### 3. Estratégias de alocação

- Evitar alocação excessiva em poucos papéis, buscando diversificar mas respeitando os critérios anteriores
- Caso o usuário forneça uma lista de posições de sua carteira atual, evitar alocações excessivas em papéis que ele já possua. Não é estritamente proibido, mas sempre buscar balancear as quantidades para que ele não fique excessivamente exposto com determinados ativos

### 4. Formato de Resposta

Apresentar os resultados no seguinte formato para cada empresa analisada:

```
| # | Empresa                      | Quantidade | Valor total | Justificativa(s)              |
|---|------------------------------|------------|-------------|-------------------------------|
| 1 | [Ticker] [Nome da empresa]   |      N     | R$          | Explicar pontos fortes        |

```

### 5. Observações Importantes
