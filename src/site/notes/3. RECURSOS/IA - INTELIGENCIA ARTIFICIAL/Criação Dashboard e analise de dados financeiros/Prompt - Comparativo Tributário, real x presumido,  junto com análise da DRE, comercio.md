---
{"dg-publish":true,"permalink":"/3-recursos/ia-inteligencia-artificial/criacao-dashboard-e-analise-de-dados-financeiros/prompt-comparativo-tributario-real-x-presumido-junto-com-analise-da-dre-comercio/","dgPassFrontmatter":true,"noteIcon":"","created":"2026-05-18T10:58:48.730-03:00","updated":"2026-05-18T14:07:51.226-03:00"}
---

**OBJETIVO:**

Este prompt tem como objetivo orientar a análise da DRE e elaborar um comparativo entre os regimes de Lucro Real e Lucro Presumido, voltado aos nossos clientes do **comércio** que atualmente estão enquadrados no Lucro Real e desejam avaliar uma eventual comparação tributária.
A conta “Outras Despesas” deve ser considerada como o conjunto de ajustes realizados para reduzir o lucro contábil e apurar um lucro tributável mais adequado, conforme alinhamento feito com o cliente e a diretoria. 

Esse detalhe deve ser apresentado de forma complementar na análise, permitindo demonstrar ao cliente a relevância dessa conta e acompanhar sua evolução ao longo do tempo.

**Sempre revise o resultado final.**

**COPIE E COLE A PARTIR DAQUI: 👇**

Você é um analista financeiro sênior especializado em tributação de empresas do comércio.

**Arquivos de entrada:**

- DRE Analítica com acumulado (exportada do sistema Domínio)
- Planilha de PIS e COFINS no Lucro Real (mensal e trimestral)
- CNPJ(s):

---

**Passo 1 — Análise da DRE**

Extraia e apresente os principais indicadores: receita bruta, deduções, receita líquida, CMV, lucro bruto, despesas operacionais, EBITDA estimado e lucro antes dos tributos.

Destaque a conta **"Outras Despesas"** separadamente. Ela representa ajustes contábeis realizados para redução da base tributável. Mostre sua evolução mensal e o impacto acumulado no lucro tributável.

---

**Passo 2 — Comparativo tributário: Lucro Real × Lucro Presumido**

Impostos a comparar: PIS, COFINS, IRPJ e CSLL.

- **PIS e COFINS no Lucro Real:** use os valores da planilha anexada (mensal e trimestral)
- **PIS e COFINS no Lucro Presumido:** calcule com alíquotas cumulativas (0,65% e 3%) sobre a receita bruta
- **IRPJ e CSLL no Lucro Real:** calcule com base no lucro tributável da DRE (15% + adicional 10% para IRPJ; 9% para CSLL)
- **IRPJ e CSLL no Lucro Presumido:** aplique os percentuais de presunção sobre a receita (8% comércio para IRPJ, 12% para CSLL), depois as alíquotas nominais

Apresente o comparativo em tabela mensal, trimestral e acumulado. Mostre a diferença absoluta e percentual entre os regimes. Indique qual regime resulta em menor carga em cada período.

---

**Passo 3 — Dashboard HTML**

Gere um arquivo HTML único, autossuficiente, com:

- Fundo azul-marinho, texto branco/cinza claro, destaques em dourado
- Cards de KPI: receita bruta, lucro líquido, carga tributária total por regime, economia/custo adicional do regime atual
- Gráfico de barras: comparativo mensal de carga tributária (Lucro Real vs Presumido)
- Gráfico de pizza: composição dos tributos por regime
- Tabela com filtro por mês/trimestre
- Seção de alerta: se o Lucro Presumido for mais vantajoso em algum período, sinalize em vermelho/âmbar com o valor da diferença

---



