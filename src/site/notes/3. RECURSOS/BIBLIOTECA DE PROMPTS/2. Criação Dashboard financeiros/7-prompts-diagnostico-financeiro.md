---
{"dg-publish":true,"permalink":"/3-recursos/biblioteca-de-prompts/2-criacao-dashboard-financeiros/7-prompts-diagnostico-financeiro/","dgPassFrontmatter":true,"noteIcon":"","created":"2026-05-22T08:52:57.640-03:00","updated":"2026-05-21T09:13:08.046-03:00"}
---

# 💰 7 Prompts de IA para Diagnóstico Financeiro do Negócio

> Criado por **Lucas Rebouças**, CEO e Founder do Zetelkasten.IA.
> [@lucasreboucas.oficial


---

## 📌 Antes de começar

A maioria dos empresários acha que tá no controle do financeiro porque olha o DRE todo mês. **DRE é foto.** Mostra que você teve lucro, não mostra de onde ele veio, qual produto deu prejuízo, qual cliente custou caro, qual assinatura tá sangrando há meses.

Esse buraco entre *"vi o lucro"* e *"entendi o lucro"* é onde o dinheiro vaza.

Esses 7 prompts foram montados pra fechar esse buraco. Cada um foi escrito como se um controller sênior tivesse sentado pra analisar seus números. Profundidade, estrutura, regra de saída e ordem de leitura.

### 📋 Separa esses dados antes de começar:

- [ ] DRE dos últimos 12 meses
- [ ] Receita por produto ou serviço
- [ ] Lista de despesas mensais (fixas e variáveis)
- [ ] Lista de clientes ativos com ticket médio e frequência
- [ ] Dívidas em aberto, prazos e juros

> ⚠️ **Sem dado real, qualquer IA te devolve resposta bonita e vazia.** Tão simples quanto isso.

Roda no Claude ou no ChatGPT. Mão na massa.

---

## Prompt 1 — Análise de Margem Real por Produto ou Serviço

**Quando usar:** quando você não sabe ao certo qual produto ou serviço dá lucro de verdade depois de considerar todos os custos, não só os diretos.

**O que vai sair:** ranking dos seus produtos por margem real, identificação dos que dão prejuízo escondido e recomendação direta do que cortar, do que manter e do que dobrar a aposta.

### Dados que você precisa juntar antes:

- [ ] Lista de produtos ou serviços com receita total dos últimos 12 meses
- [ ] Custo direto de cada um (matéria-prima, comissão, frete, taxa de cartão, fornecedor)
- [ ] Custo indireto a ser rateado (estrutura, marketing, time)
- [ ] Tempo médio de produção ou entrega de cada um
- [ ] Volume vendido no período

### O prompt:

```
Você é um controller financeiro sênior com 15 anos de experiência em análise de rentabilidade de pequenas e médias empresas no Brasil. Sua especialidade é desmontar contabilidade superficial e mostrar onde o dinheiro realmente entra e sai. Você é brutal nos cortes e nunca deixa empresário manter produto por carinho.

Vou te passar os dados financeiros do meu negócio. Sua missão é fazer uma análise de margem real por produto ou serviço considerando 4 camadas:

1. Margem de contribuição: receita menos custo direto
2. Margem líquida: considerando o rateio proporcional dos custos indiretos (estrutura, time, marketing)
3. ROI por tempo: margem líquida dividida pelo tempo médio de produção ou entrega (em horas)
4. Custo de oportunidade: o que cada produto está bloqueando de capacidade da operação

Estrutura obrigatória da sua resposta:

- Tabela com cada produto e suas 4 métricas (margem de contribuição em %, margem líquida em %, ROI por hora em R$, e nota de custo de oportunidade de 1 a 10)
- Ranking do mais lucrativo pro menos lucrativo, baseado em margem líquida
- Sinalização explícita dos produtos que dão prejuízo real (margem líquida negativa)
- 3 produtos pra cortar imediatamente, com justificativa numérica
- 3 produtos pra dobrar a aposta, com justificativa numérica
- 1 armadilha escondida: produto que parece bom em margem de contribuição mas afunda na margem líquida ou no ROI por tempo

Não use linguagem corporativa. Não dê resposta diplomática. Se o produto não faz sentido, fala que não faz e mostra o número.

Dados do meu negócio:

[COLE AQUI A LISTA DE PRODUTOS COM RECEITA, CUSTOS DIRETOS, CUSTOS INDIRETOS RATEADOS, VOLUME E TEMPO MÉDIO DE ENTREGA]
```

### Como ler a resposta

A coluna que mais importa é **margem líquida**. Margem de contribuição alta com margem líquida baixa significa que o rateio de estrutura tá comendo o produto. A decisão muda: ou aumenta preço, ou aumenta volume, ou enxuga estrutura. **Margem líquida negativa significa que cada venda te custa dinheiro. Cortar é o caminho.**

### ➡️ Próximo passo

Pega os 3 produtos com pior margem líquida e responde uma de três perguntas pra cada um: Aumento preço? Corto? Reestruturo o custo? **Decisão tem que sair dessa análise nessa semana.**

---

## Prompt 2 — Diagnóstico de Fluxo de Caixa e Gargalos

**Quando usar:** quando o caixa aperta todo mês e você não consegue explicar exatamente por quê. Quando o lucro do DRE não bate com o saldo do banco. Quando você sente que falta dinheiro mesmo o mês fechando no positivo.

**O que vai sair:** análise mês a mês de entradas e saídas dos últimos 12 meses, identificação dos dias e semanas críticos do ciclo, cálculo do gap entre prazo médio de recebimento e prazo médio de pagamento, 3 ajustes operacionais pra destravar caixa em 30 dias.

### Dados que você precisa juntar antes:

- [ ] Entradas mensais dos últimos 12 meses, separadas por canal ou produto
- [ ] Saídas mensais dos últimos 12 meses, separadas por categoria (fixo, variável, fornecedor, folha, impostos)
- [ ] Prazo médio de recebimento atual (PMR)
- [ ] Prazo médio de pagamento atual (PMP)
- [ ] Lista das 10 maiores contas a receber em aberto com vencimento
- [ ] Lista das 10 maiores contas a pagar em aberto com vencimento
- [ ] Saldo de caixa inicial de cada mês

### O prompt:

```
Você é um controller financeiro sênior especializado em capital de giro e gestão de fluxo de caixa de pequenas e médias empresas. Sua especialidade é encontrar o momento exato em que o caixa quebra e explicar por que isso acontece de forma estrutural, não pontual.

Vou te passar 12 meses de fluxo de caixa do meu negócio. Sua missão é diagnosticar a saúde do ciclo financeiro em 4 frentes:

1. Padrão sazonal: em quais meses o caixa aperta de forma recorrente e por qual razão estrutural (pico de fornecedor, queda de receita, concentração de impostos, folha)
2. Ciclo financeiro real: gap entre prazo médio de recebimento e prazo médio de pagamento, e o impacto disso na necessidade de capital de giro
3. Concentração de saída: quais dias do mês concentram a maior parte das saídas e se isso bate com os dias de maior entrada
4. Pontos de ruptura: dias específicos do mês em que o saldo fica negativo ou abaixo do mínimo de segurança

Estrutura obrigatória da sua resposta:

- Tabela de fluxo mensal com saldo inicial, entradas, saídas e saldo final dos 12 meses
- Gráfico em ASCII (ou descrição clara) dos 3 meses mais críticos do ciclo
- Cálculo do ciclo financeiro em dias (PMR menos PMP) e leitura do que isso significa pro negócio
- Mapa dos dias do mês com maior pressão de caixa
- 3 ajustes operacionais pra resolver os gargalos identificados, em ordem de impacto, com prazo estimado de implementação
- 1 risco estrutural que vai estourar nos próximos 90 dias se nada mudar

Seja direto. Se o ciclo tá ruim, fala. Se o problema é estrutural e não vai melhorar sozinho, fala. Não dê dicas genéricas tipo "renegocie com fornecedores", entrega ação específica baseada nos meus dados.

Dados do meu negócio:

[COLE AQUI ENTRADAS E SAÍDAS MENSAIS DOS 12 MESES, PMR, PMP, CONTAS A RECEBER E A PAGAR EM ABERTO]
```

### Como ler a resposta

O número mais importante é o **ciclo financeiro em dias**. Se for positivo (você paga antes de receber), você está bancando o cliente com o seu caixa. Cada dia desse gap custa capital de giro. Resolver ciclo financeiro normalmente dá mais resultado do que cortar custo.

### ➡️ Próximo passo

Dos 3 ajustes propostos, escolha o de menor atrito e implementa nessa semana. Os outros dois agendam pra rodar nos próximos 60 dias. Reabre o prompt no próximo trimestre com dados atualizados pra ver se mexeu o ponteiro.

---

## Prompt 3 — Auditoria de Custos Invisíveis

**Quando usar:** quando você suspeita que tem dinheiro saindo sem ninguém perceber. Quando o custo cresceu mas você não consegue apontar onde. Quando entra empresa nova e descobre que tem assinatura ativa há anos que ninguém abre.

**O que vai sair:** mapeamento dos 5 tipos mais comuns de custo invisível no seu negócio, lista priorizada de cortes por impacto e facilidade de execução, estimativa de economia mensal e anual.

### Dados que você precisa juntar antes:

- [ ] Planilha completa de despesas dos últimos 12 meses, com fornecedor, valor e categoria
- [ ] Lista de todos os contratos ativos com prazo, valor e cláusula de renovação
- [ ] Lista de todas as assinaturas mensais e anuais (software, serviços, mídia, ferramentas)
- [ ] Lista de fornecedores recorrentes com histórico de reajustes nos últimos 3 anos
- [ ] Lista de clientes ativos com receita anual e estimativa de tempo de time consumido por cada um

### O prompt:

```
Você é um auditor financeiro sênior especializado em identificar custos invisíveis em pequenas e médias empresas. Sua experiência mostra que toda empresa tem entre 5% e 15% do custo total saindo em despesas que ninguém autoriza, ninguém revê e ninguém percebe. Sua missão é caçar esses custos.

Vou te passar os dados de despesas do meu negócio. Faça uma auditoria nas 5 categorias de custo invisível mais comuns:

1. Assinaturas zumbi: software, ferramenta ou serviço que continua sendo cobrado e ninguém usa há mais de 90 dias
2. Contratos com renovação automática: serviços onde o preço subiu sem renegociação ou onde a cláusula automática preservou um valor que hoje está acima de mercado
3. Reajustes de fornecedor não auditados: fornecedores recorrentes que aplicaram reajuste acima da inflação nos últimos 3 anos sem que ninguém comparasse com o mercado
4. Cliente caro disfarçado: cliente que paga ticket razoável mas consome volume desproporcional de tempo do time, transformando uma receita aparentemente boa em margem real negativa
5. Capital parado: dinheiro em conta corrente sem rendimento, estoque parado, contas a receber não cobradas

Estrutura obrigatória da sua resposta:

- Tabela com os custos identificados em cada uma das 5 categorias, valor mensal e valor anual
- Estimativa do total invisível em R$ por mês e por ano
- Lista priorizada de cortes ranqueada por (a) impacto financeiro e (b) facilidade de execução. Use uma matriz 2x2 simples
- 5 cortes pra executar nas próximas 2 semanas (alto impacto, baixa dificuldade)
- 3 renegociações que precisam de mais tempo mas têm impacto grande
- 1 cliente caro disfarçado que parece bom mas tá comendo margem (se houver)

Não inventa dado. Se faltar informação pra avaliar alguma categoria, fala o que falta e o que eu preciso te trazer.

Dados do meu negócio:

[COLE AQUI A PLANILHA DE DESPESAS, LISTA DE CONTRATOS, ASSINATURAS, FORNECEDORES E CLIENTES COM CONSUMO DE TEMPO]
```

### Como ler a resposta

O número que importa primeiro é o **total invisível anual**. Esse é o dinheiro que tá saindo do bolso sem você ter aprovado uma decisão de gastar ele. Os 5 cortes de execução rápida normalmente já recuperam metade desse valor em 30 dias.

### ➡️ Próximo passo

Delega os 5 cortes rápidos pra alguém da operação com prazo de 15 dias. As 3 renegociações precisam de você direto — agenda na agenda. O cliente caro disfarçado, se aparecer, é assunto pra outra reunião de decisão (rever escopo, reajustar preço ou desligar).

---

## Prompt 4 — Stress Test do Negócio em 4 Cenários

**Quando usar:** antes de tomar decisão grande (contratação, investimento, expansão de operação, novo canal). Em momento de incerteza de mercado. Quando você quer dormir mais tranquilo sabendo até onde o negócio aguenta.

**O que vai sair:** simulação de 4 cenários adversos, ponto exato em que o negócio quebra em cada um, plano de contingência específico pra cada cenário.

### Dados que você precisa juntar antes:

- [ ] DRE atual com receita e custos detalhados
- [ ] Mix de receita por canal (qual % vem de cada fonte de aquisição)
- [ ] Mix de receita por cliente (top 10 clientes e % que representam do faturamento)
- [ ] Estrutura de custos: separado em fixo e variável
- [ ] Dívidas atuais e prazos
- [ ] Saldo de caixa atual
- [ ] Capital de giro disponível

### O prompt:

```
Você é um CFO sênior especializado em planejamento de cenários e gestão de risco em pequenas e médias empresas. Sua experiência mostra que toda empresa tem pelo menos um cenário adverso que parece pouco provável mas é capaz de quebrar a operação em 60 dias. Sua missão é encontrar esses cenários e me mostrar o ponto exato em que eu quebro.

Vou te passar a estrutura financeira atual do meu negócio. Rode 4 cenários de stress:

1. Queda de 20% na receita por 3 meses (recessão, perda de mercado, sazonalidade ruim)
2. Atraso de 60 dias no recebimento do maior cliente ou maior canal
3. Aumento de 15% nos custos variáveis (alta de fornecedor, câmbio, insumo crítico)
4. Perda do principal canal de aquisição (anúncio que parou de performar, parceiro que rompeu, indicação que secou)

Pra cada cenário, calcula e me mostra:

- Impacto mensal em receita
- Impacto mensal em margem
- Qual o ponto exato (em meses) em que o caixa zera, considerando saldo atual e capital de giro
- Qual o ponto em que a operação fica inviável (não consegue cobrir folha e custo fixo)
- Plano de contingência específico pra esse cenário, em 3 níveis: ações imediatas (semana 1), ações de médio prazo (mês 1 a 2), ações estruturais (mês 3 em diante)

Estrutura obrigatória da resposta:

- Resumo dos 4 cenários em tabela única com impacto em receita, margem, mês de ruptura de caixa
- Para cada cenário: análise detalhada, ponto de quebra e plano de contingência em 3 níveis
- Ranking dos 4 cenários do mais ao menos perigoso pro meu negócio específico
- 1 cenário "fora da caixa" que eu não pedi mas que pelos meus dados representa um risco real que eu deveria estar acompanhando

Não suaviza. Se algum cenário quebra o negócio rápido, fala. Se a empresa aguenta bem, fala também.

Dados do meu negócio:

[COLE AQUI DRE, MIX DE RECEITA POR CANAL, TOP 10 CLIENTES, ESTRUTURA DE CUSTOS, DÍVIDAS, SALDO E CAPITAL DE GIRO]
```

### Como ler a resposta

O cenário mais perigoso é aquele em que o **mês de ruptura de caixa é o mais próximo**. Esse é o seu calcanhar de Aquiles. Ação de mitigação desse cenário entra como prioridade dos próximos 90 dias.

### ➡️ Próximo passo

Do cenário mais perigoso, implementa pelo menos as ações imediatas (semana 1) mesmo que o cenário não esteja acontecendo. Reserva, redundância de fornecedor ou diversificação de canal, conforme o caso. **Stress test que fica no papel não vale nada.**

---

## Prompt 5 — Projeção de Runway e Pontos de Decisão

**Quando usar:** quando você precisa saber exatamente quanto tempo de operação ainda tem se nada mudar. Quando está pensando em captar, cortar ou virar a chave de modelo. Quando o sócio ou investidor pergunta "até quando a gente aguenta" e você não sabe responder com precisão.

**O que vai sair:** linha do tempo com runway atual, ponto exato em que precisa agir, gatilhos numéricos pra cada decisão (cortar, captar, mudar de modelo).

### Dados que você precisa juntar antes:

- [ ] Saldo de caixa atual
- [ ] Queima mensal média dos últimos 6 meses (burn rate)
- [ ] Capital de giro disponível
- [ ] Receita mensal média e tendência de crescimento ou queda dos últimos 6 meses
- [ ] Linha de crédito disponível e custo dela
- [ ] Folha mensal e custo fixo mensal
- [ ] Investimentos previstos pros próximos 6 meses

### O prompt:

```
Você é um CFO sênior especializado em planejamento financeiro e gestão de runway de empresas em diferentes estágios de maturidade. Sua experiência mostra que empresário normalmente descobre que tá sem caixa 60 dias antes de quebrar, e aí é tarde. Sua missão é me mostrar o ponto exato em que eu preciso agir, com gatilhos numéricos claros.

Vou te passar o cenário financeiro atual do meu negócio. Calcula e estrutura a seguinte análise:

1. Runway base: quantos meses de operação o negócio sustenta no ritmo atual, considerando saldo, capital de giro e burn rate dos últimos 6 meses
2. Runway otimista: o mesmo cálculo considerando que a receita cresce conforme a tendência dos últimos 6 meses
3. Runway pessimista: o mesmo cálculo considerando queda de 15% na receita
4. Pontos de decisão: em que mês exatamente eu preciso (a) cortar custo, (b) buscar captação ou crédito, (c) virar a chave do modelo de negócio se nada mudou

Estrutura obrigatória da resposta:

- Linha do tempo dos próximos 18 meses com saldo projetado mês a mês nos 3 cenários
- Identificação visual ou clara do ponto em que cada cenário fica negativo
- Tabela de pontos de decisão com gatilhos numéricos. Exemplo: "quando o saldo cair abaixo de R$ X, ativar ação Y"
- Lista de 3 alavancas de aumento de runway por ordem de facilidade de execução (cortar custo X, antecipar receita Y, reduzir folha Z)
- 1 cenário em que o runway atual já é insuficiente mesmo no caso otimista (se for o caso). Aí o gatilho é hoje, não daqui a 3 meses

Não embeleza. Se o runway tá curto, fala. Empresário precisa do número real pra tomar decisão real.

Dados do meu negócio:

[COLE AQUI SALDO ATUAL, BURN RATE, CAPITAL DE GIRO, RECEITA E TENDÊNCIA, LINHA DE CRÉDITO, FOLHA E CUSTO FIXO, INVESTIMENTOS PREVISTOS]
```

### Como ler a resposta

O **runway pessimista é o que importa pra decisão**. Otimista é pra apresentação de board. Operação real se planeja no pessimista. Se o runway pessimista for inferior a 6 meses, você já precisa estar implementando a alavanca de maior impacto.

### ➡️ Próximo passo

Define qual gatilho numérico vai ativar cada decisão e coloca isso num lugar onde você olhe toda semana. Decisão pré-definida com gatilho objetivo evita que você adie até o ponto em que não dá mais pra reverter.

---

## Prompt 6 — Análise Estratégica de Precificação

**Quando usar:** quando suspeita que tá com preço errado. Antes de qualquer reajuste. Quando margem caiu sem motivo claro. Quando entra concorrente novo no mercado. Quando o cliente premium tá reclamando demais ou aceitando demais.

**O que vai sair:** tabela de preços recomendados com justificativa, ordem de implementação do reajuste pra não perder cliente bom, segmentação de clientes por sensibilidade a preço.

### Dados que você precisa juntar antes:

- [ ] Tabela de preços atuais por produto ou serviço
- [ ] Custos diretos e indiretos por produto
- [ ] Margem atual por produto
- [ ] Posicionamento de mercado (premium, médio, popular)
- [ ] Dados de churn por faixa de preço, se tiver
- [ ] Ticket médio atual e variação dos últimos 12 meses
- [ ] Preço dos 3 principais concorrentes pra cada produto comparável

### O prompt:

```
Você é um estrategista de precificação sênior com experiência em pequenas e médias empresas brasileiras. Sua especialidade é encontrar a margem que o empresário tá deixando na mesa por medo de subir preço, e estruturar reajustes que aumentam receita sem queimar base de cliente.

Vou te passar os dados de preço, custo e margem do meu negócio. Analise em 4 frentes:

1. Margem atual vs margem ideal: pra cada produto, calcule a margem hoje e a margem mínima saudável (considerando custo direto, indireto, capacidade e posicionamento). Mostre o gap
2. Posicionamento vs preço: pra cada produto, avalie se o preço atual condiz com o posicionamento declarado. Tem produto premium sendo cobrado preço de médio. Tem produto popular sendo cobrado preço de premium.
3. Sensibilidade da base: com base no churn por faixa de preço (se houver), estime quanto de cliente eu perco com reajuste de 5%, 10% e 15%. Calcula o efeito líquido (perda de cliente vs ganho de margem)
4. Ordem de implementação: produtos onde dá pra subir preço imediatamente, produtos que precisam de comunicação ou ajuste de oferta antes, produtos onde reajuste seria suicídio comercial

Estrutura obrigatória da resposta:

- Tabela com cada produto, preço atual, preço recomendado, percentual de reajuste, margem antes e margem depois
- Justificativa específica pra cada novo preço (baseado em custo, posicionamento ou comparação de mercado)
- Simulação de efeito líquido do reajuste considerando churn estimado
- Ordem de implementação: o que reajustar primeiro, segundo e terceiro, com prazo e racional
- 1 produto que parece estar subprecificado mas tem alguma armadilha (alta sensibilidade, concorrente forte, valor percebido baixo)
- 1 produto que parece estar com preço ok mas que pela margem real precisa de reajuste urgente

Não dê resposta genérica de "suba 10% no geral". Cada produto é uma decisão.

Dados do meu negócio:

[COLE AQUI TABELA DE PREÇOS, CUSTOS, MARGEM, POSICIONAMENTO, CHURN POR FAIXA, TICKET MÉDIO, PREÇOS DE CONCORRENTES]
```

### Como ler a resposta

O produto com **maior gap entre margem atual e margem ideal** é onde tá o maior dinheiro deixado na mesa. Reajuste bem comunicado e bem segmentado tem efeito líquido positivo quase sempre. Medo de perder cliente é o que mantém empresário com margem ruim.

### ➡️ Próximo passo

Implementa o primeiro reajuste recomendado nos próximos 30 dias. Comunica antes pra base ativa, mantém preço antigo pros 10 maiores clientes por mais 60 dias pra dar tempo de adaptação. Os outros reajustes seguem o cronograma da ordem de implementação.

---

## Prompt 7 — Mapa de Risco Financeiro

**Quando usar:** uma vez por trimestre, pra olhar a saúde do negócio de cima. Antes de planejamento estratégico. Em qualquer momento de mudança de cenário externo (regulamentação, política, câmbio, juros).

**O que vai sair:** matriz de risco em 4 quadrantes (impacto x probabilidade), top 3 riscos pra resolver em 90 dias com plano específico.

### Dados que você precisa juntar antes:

- [ ] Concentração de clientes (% de receita dos top 5 e do maior cliente)
- [ ] Concentração de fornecedores (% de custo direto vindo dos top 3 fornecedores)
- [ ] Exposição a câmbio (se tiver receita ou custo em outra moeda)
- [ ] Sazonalidade da receita (variação entre melhor e pior trimestre)
- [ ] Dívidas atuais, prazos e taxas
- [ ] Dependência de canal único de aquisição (% que vem do principal canal)
- [ ] Concentração de conhecimento (operação depende de uma pessoa específica?)

### O prompt:

```
Você é um consultor sênior de gestão de risco financeiro especializado em pequenas e médias empresas no Brasil. Sua experiência mostra que toda empresa tem 2 ou 3 riscos críticos que o dono enxerga, e 1 ou 2 que ele não vê porque virou parte da rotina e ninguém questiona mais. Sua missão é mapear todos.

Vou te passar a estrutura atual do meu negócio. Monte uma análise de risco financeiro em 7 dimensões:

1. Risco de concentração de cliente: quanto da receita depende dos top 5 e do maior cliente
2. Risco de concentração de fornecedor: quanto do custo direto vem dos top 3 fornecedores e qual o impacto se um deles cair
3. Risco de exposição cambial: se houver receita ou custo em outra moeda, o impacto de variação de 20% no câmbio
4. Risco de sazonalidade: variação entre melhor e pior trimestre e o impacto disso na previsibilidade de caixa
5. Risco de endividamento: nível de alavancagem atual, taxa média da dívida e capacidade de pagamento em cenário pessimista
6. Risco de canal único: dependência do principal canal de aquisição e o que acontece se ele cair
7. Risco de pessoa-chave: se a operação depende de uma pessoa específica (eu incluso) e o que acontece se ela sair ou ficar fora por 60 dias

Estrutura obrigatória da resposta:

- Matriz 2x2 de risco com cada um dos 7 riscos posicionado por impacto (baixo, médio, alto) e probabilidade (baixa, média, alta)
- Descrição específica de cada risco com o número que justifica a posição na matriz
- Top 3 riscos pra resolver nos próximos 90 dias (os de maior impacto e maior probabilidade)
- Pra cada um dos top 3: plano de mitigação em 3 ações específicas com prazo
- 1 risco que eu não pedi mas que pelos meus dados representa exposição real (risco oculto)
- 1 risco que eu pareço estar superestimando (pelos meus dados, é menor do que parece)

Não dá resposta genérica de "diversifique sua base". Diversificar como, em que canal, em que ordem, com que prazo. Plano específico.

Dados do meu negócio:

[COLE AQUI DADOS DE CONCENTRAÇÃO DE CLIENTE E FORNECEDOR, EXPOSIÇÃO CAMBIAL, SAZONALIDADE, DÍVIDAS, DEPENDÊNCIA DE CANAL E PESSOA-CHAVE]
```

### Como ler a resposta

O **quadrante crítico é alto impacto e alta probabilidade**. Risco que cai aí precisa de ação imediata, não plano de longo prazo. Os outros entram em fila de execução. O risco oculto, se aparecer, normalmente é o mais perigoso justamente porque você ainda não tinha mapeado.

### ➡️ Próximo passo

Dos top 3 riscos, escolhe o de menor atrito pra implementar e arranca nessa semana. Os outros dois entram no planejamento dos próximos 90 dias com responsável e prazo. **Reabre o prompt no fim do trimestre pra recalibrar a matriz.**

---

## 🎯 Como tirar o máximo do material

Esses 7 prompts funcionam isolados, mas **o ganho real aparece quando você roda os 7 em sequência num final de semana**, com os mesmos dados, e cruza as respostas.

| Prompt | Cruza com |
|--------|-----------|
| Produto com pior margem (P1) | → Problema de precificação (P6) |
| Cliente caro disfarçado (P3) | → Fator de concentração de risco (P7) |
| Gargalo de caixa (P2) | → Runway e pontos de decisão (P5) |

> **A IA não substitui análise crítica. Ela acelera.** Quem cola os 7 prompts sem olhar pros números recebe relatório bonito. Quem cola os 7 prompts e questiona cada resposta cruzando com a próxima recebe diagnóstico real.

**Mão na massa.**
