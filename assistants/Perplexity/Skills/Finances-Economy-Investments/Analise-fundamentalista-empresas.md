---
name: fundamentalist-stock-analysis
description: "Análise fundamentalista de ações com 12 critérios objetivos (ROE, CAGR, dividendos, governança, valuation, endividamento, etc.), sistema de pontuação SIM/PARCIAL/NÃO e cálculo de 'força' da empresa. Use quando o usuário pedir análise fundamentalista, avaliação de ações, screening de empresas para carteira de longo prazo, ou perguntas como 'vale investir em X?', 'analise a empresa X', 'faça o checklist de X'."
metadata:
  author: nelson
  version: '1.0'
---

# Análise Fundamentalista de Ações

## Quando Usar Esta Skill

Use quando o usuário pedir:

- Análise fundamentalista de uma ou mais empresas
- Checklist de qualidade de ações
- Screening de empresas para carteira de longo prazo
- Avaliação se uma ação vale a pena ("vale investir em X?")
- Comparação fundamentalista entre empresas

## Instruções

### 1. Coleta de Dados

Antes de responder, busque dados atualizados da(s) empresa(s) usando ferramentas de pesquisa disponíveis. Priorize:

- ROE histórico (mínimo 5 anos)
- Receita líquida e lucro líquido históricos (mínimo 5 anos, para cálculo de CAGR)
- Histórico de pagamento de dividendos
- Setor de atuação e posição competitiva
- Ano de fundação
- Capitalização de mercado e liquidez
- Dívida Líquida e EBITDA (histórico de 5 anos)
- Preço atual vs. preço justo/preço-alvo (fontes: DCF, Graham, consenso de analistas)
- Histórico de governança (escândalos, fraudes, processos relevantes)
- Estrutura de controle (estatal, privado, concentração de clientes)

### 2. Avaliação dos 12 Critérios

Para cada critério, atribua: **SIM**, **NÃO** ou **PARCIAL**, seguido de uma justificativa objetiva em 1–3 linhas.

---

**Critério 1 — ROE**
> A empresa tem ROE historicamente maior que 5%?

- Usar ROE médio dos últimos 5+ anos, nunca um único trimestre isolado.
- SIM: média > 5% de forma consistente.
- PARCIAL: média próxima de 5% ou com alta volatilidade.
- NÃO: média abaixo de 5% ou consistentemente negativo.

---

**Critério 2 — Crescimento (CAGR)**
> A empresa tem crescimento de receitas ou lucros superior a 5% nos últimos 5 anos?

- Calcular CAGR de receita líquida ou lucro líquido no período disponível.
- SIM: CAGR > 5%.
- PARCIAL: CAGR entre 0% e 5%.
- NÃO: CAGR negativo ou crescimento estagnado.

---

**Critério 3 — Dividendos**
> A empresa tem histórico consistente de pagamento de dividendos?

- Constância importa mais que yield pontual.
- SIM: pagamento consistente nos últimos 5+ anos, sem interrupções relevantes.
- PARCIAL: histórico intermitente ou recente (menos de 5 anos).
- NÃO: não paga dividendos ou interrompeu por períodos longos sem justificativa clara.

---

**Critério 4 — Tecnologia e Pesquisa**
> A empresa investe em P&D/inovação e o setor não é obsoleto?

- Se o setor for claramente obsoleto (ex.: impressão gráfica tradicional, fax, mídia física), a resposta é **SEMPRE NÃO**, independente dos investimentos.
- SIM: setor perene e empresa com investimentos em inovação documentados.
- PARCIAL: setor em transição ou investimento em P&D baixo mas existente.
- NÃO: setor obsoleto ou empresa sem qualquer evidência de inovação.

---

**Critério 5 — Tempo de Mercado**
> A empresa tem mais de 30 anos de mercado?

- Contar desde a **fundação**, não desde o IPO.
- SIM: fundada há mais de 30 anos.
- NÃO: fundada há menos de 30 anos.
- (Não há PARCIAL neste critério — use julgamento se estiver próximo de 30 anos.)

---

**Critério 6 — Vantagens Competitivas**
> A empresa é líder nacional ou mundial no setor?

- Considerar apenas se for líder (1ª colocada) em market share ou relevância setorial.
- SIM: líder clara no seu setor nacional ou global.
- PARCIAL: entre as líderes (top 3), mas não a 1ª.
- NÃO: não é líder, posição competitiva fraca ou disputada sem diferencial claro.

---

**Critério 7 — Perenidade do Setor**
> O setor em que a empresa atua tem mais de 100 anos?

- Exemplos de setores perenes: bancos, energia elétrica, saneamento, consumo básico (alimentos, bebidas), saúde, seguros, transportes essenciais.
- SIM: setor existe há mais de 100 anos e continuará existindo.
- NÃO: setor novo ou cuja existência futura é incerta.

---

**Critério 8 — Tamanho (Blue Chip)**
> A empresa é uma blue chip?

- Verificar: alta liquidez média diária, grande capitalização de mercado, peso relevante no índice principal do mercado (ex.: Ibovespa, S&P 500).
- SIM: claramente uma blue chip pelo mercado de referência.
- PARCIAL: midcap com boa liquidez mas não blue chip.
- NÃO: small cap, baixa liquidez ou irrelevante no índice.

---

**Critério 9 — Governança**
> A empresa tem boa gestão e boa governança?

- Histórico de corrupção ou fraudes relevantes = **SEMPRE NÃO**, independentemente de melhorias recentes.
- SIM: sem histórico de fraudes, gestão bem avaliada, boas práticas ESG/governança.
- PARCIAL: governança razoável, sem grandes escândalos mas com pontos de atenção.
- NÃO: envolvimento em fraudes, corrupção, ou gestão reconhecidamente problemática.

---

**Critério 10 — Independência**
> A empresa é livre de controle estatal relevante e de concentração em único cliente?

- Controle estatal relevante: governo como controlador direto com interferência política documentada.
- Concentração: mais de 30–40% da receita de um único cliente.
- SIM: privada, controle pulverizado ou familiar sem interferência política; base de clientes diversificada.
- PARCIAL: alguma influência estatal ou concentração moderada de clientes, mas não dominante.
- NÃO: empresa estatal com histórico de interferência política ou altamente dependente de um único cliente.

---

**Critério 11 — Endividamento**
> Dívida Líquida/EBITDA é menor que 2x nos últimos anos?

- Avaliar os últimos 5 anos de forma consistente.
- SIM: Dívida Líquida/EBITDA < 2x de forma consistente.
- PARCIAL: entre 2x e 3x, ou abaixo de 2x em alguns anos mas não todos.
- NÃO: acima de 3x de forma consistente, ou estrutura de capital muito alavancada.

---

**Critério 12 — Preço / Valuation**
> A ação está com desconto relevante em relação ao preço justo?

- Usar preço justo de fontes reconhecidas: DCF, Fórmula de Graham, consenso de analistas, relatórios de corretoras sérias.
- **SIM**: preço atual ≤ 70% do preço justo (desconto ≥ 30%).
- **PARCIAL**: preço atual entre 70% e 120% do preço justo.
- **NÃO**: preço atual ≥ 120% do preço justo (sobrevalorizado).
- Se não houver preço justo disponível de fonte confiável, indicar como **INCONCLUSIVO** e explicar.

---

### 3. Sistema de Pontuação ("Força")

Após avaliar todos os critérios, calcular a pontuação:

| Resultado | Pontos |
|-----------|--------|
| SIM       | +1     |
| PARCIAL   | 0      |
| NÃO       | −2     |

**Força = soma dos pontos de todos os 12 critérios**

Pontuação máxima possível: **+12** (todos SIM)
Pontuação mínima possível: **−24** (todos NÃO)

**Interpretação:**

| Faixa de Força | Interpretação |
|----------------|---------------|
| +8 a +12       | Empresa excelente — candidata forte ao núcleo da carteira de longo prazo |
| +5 a +7        | Empresa boa — pode compor a carteira com monitoramento |
| +1 a +4        | Empresa mediana — exige análise adicional antes de incluir |
| 0              | Empresa neutra — não recomendada para carteira core sem gatilhos claros |
| Negativa       | Empresa fraca — evitar no núcleo; só manter conscientemente em lista separada |

---

### 4. Formato de Resposta

Apresentar os resultados no seguinte formato para cada empresa analisada:

```
## [NOME DA EMPRESA] ([TICKER])

| # | Critério              | Resultado | Justificativa                        |
|---|-----------------------|-----------|--------------------------------------|
| 1 | ROE                   | SIM/NÃO/PARCIAL | ...                            |
| 2 | Crescimento (CAGR)    | ...       | ...                                  |
| 3 | Dividendos            | ...       | ...                                  |
| 4 | Tecnologia/Inovação   | ...       | ...                                  |
| 5 | Tempo de Mercado      | ...       | ...                                  |
| 6 | Vantagens Competitivas| ...       | ...                                  |
| 7 | Perenidade do Setor   | ...       | ...                                  |
| 8 | Tamanho (Blue Chip)   | ...       | ...                                  |
| 9 | Governança            | ...       | ...                                  |
|10 | Independência         | ...       | ...                                  |
|11 | Endividamento         | ...       | ...                                  |
|12 | Valuation             | ...       | ...                                  |

**Força total: X pontos**
**Conclusão:** [resumo em 2–3 linhas sobre se a empresa é candidata à carteira ou não]
```

Se múltiplas empresas forem analisadas, apresentar cada uma em sua seção e, ao final, uma tabela comparativa de força.

### 5. Observações Importantes

- Sempre citar as fontes dos dados usados (relatórios de resultados, sites de RI, Bloomberg, Refinitiv, consenso de analistas, etc.).
- Se dados forem insuficientes para um critério, marcar como **INCONCLUSIVO** e explicar o que está faltando.
- Não inventar dados financeiros. Se não houver dados disponíveis, dizer claramente.
- Esta análise é para fins informativos e educacionais — não constitui recomendação de investimento.
