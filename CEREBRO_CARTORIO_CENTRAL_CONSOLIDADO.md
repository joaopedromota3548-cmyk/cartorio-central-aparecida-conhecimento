# 🧠 CÉREBRO DO CARTÓRIO CENTRAL — Conhecimento Consolidado para Transplante
## Sala de Situação · Cartório Central · DPM Aparecida/SP (Cód. 1512 — DEINTER 1 · Seccional Guaratinguetá)

> **O que é este arquivo.** É a **consolidação integral do conhecimento reutilizável** ("o cérebro") acumulado
> na pasta do Cartório Central até **07/07/2026**, produzida pelo HUB (Opus) a partir da destilação de toda a
> governança-raiz, dos SOPs de gestão cartorária, dos módulos investigativos e jurídico-processuais e da
> memória viva de lições e entraves. Reúne **como o sistema pensa e opera** — protocolos, regras inegociáveis,
> estruturas de planilha, modelos de peças, fundamentos legais e armadilhas conhecidas — **sem dados de casos
> concretos** (números de BO reais, nomes de envolvidos, planilhas vivas ou PDFs de exemplo ficaram de fora).
>
> **Finalidade:** servir de base única e portátil para **transplante a outro ambiente** (nova pasta, nova
> máquina, novo projeto ou chat). Decisão final de qualquer ato é sempre do **Escrivão-Chefe/Delegado**
> (art. 2º, §6º, Lei 12.830/13).

---

## Como usar este documento

Este é um documento de **conhecimento**, não de dados. Ele condensa cinco camadas do sistema:

- **Parte I — Arquitetura e Governança do HUB:** o motor multiagente (HUB + subagentes), a fila de commit,
  o roteamento de modelos, o ciclo de vida dos dados, buscas, custódia e o roadmap de melhorias.
- **Parte II — Gestão do Cartório Central:** perfil funcional, estrutura das planilhas mestras, snapshots,
  estatística mensal, fluxo de entrada, formatação de documentos e o catálogo de modelos de peças.
- **Parte III — Módulos Investigativos:** triagem de BO, histórico/APFD, análise e conferência de inquéritos,
  análise aprofundada de BO e o modelo de resumo investigativo.
- **Parte IV — Módulos Jurídico-Processuais:** oitiva policial, portaria de instauração, relatório final,
  IPe, laudos e protocolo de objetos/custódia.
- **Parte V — Lições Operacionais e Entraves de Sistema:** a memória viva — sintomas, causas e contornos
  de cada sistema (SPJ, IPe, SPTC, Outlook, e-SAJ), métodos consolidados e armadilhas a evitar.

> Onde há divergência entre versões de um mesmo item (ex.: layout da aba `BOs`, telefone institucional),
> o texto **preserva ambas** e assinala qual é a canônica ou a regra "**o arquivo manda** — conferir o
> cabeçalho real antes de gravar".

---

## Índice

- **Parte I — Arquitetura e Governança do HUB**
  1. Arquitetura multiagente (HUB + subagentes) e fila de commit · carta de poderes e plano de varredura S1–S8
  2. Matriz de roteamento de modelos (Opus/Sonnet/Haiku; sem Fable) e Cláusula de Qualidade
  3. Catálogo de frentes (A–F) e catálogo de comandos/briefs
  4. Ciclo de vida dos dados em 3 camadas + índice mestre
  5. Protocolo de varredura contínua (checkpoint + compactação)
  6. Central de buscas (internet + sistemas via Chrome)
  7. Comando `clear` / Quarentena
  8. Padrão de citação-à-fonte
  9. Padrão de cadeia de custódia — ISO/IEC 27037 (append-only)
  10. Roadmap de melhorias e registro de expansão de frentes
- **Parte II — Gestão do Cartório Central (SOPs e Modelos de Peças)**
  1. Perfil funcional e tom · 2. Planilhas mestras e bases seccionais · 3. Snapshots · 4. Estatística mensal
  · 5. Fluxo único de entrada e conferência de BO · 6. Formatação de documentos Word · 7. POP triagem de e-mail
  e SOP de prazo · 8. Catálogo dos 13 modelos de peças
- **Parte III — Módulos Investigativos**
  1. Triagem de BO (árvore de decisão) · 2. Histórico de BO / APFD / captura / complemento · 3. Análise e
  conferência de inquéritos (correição 2026) · 4. Análise aprofundada de BO e resumo investigativo v2.0
- **Parte IV — Módulos Jurídico-Processuais**
  1. Oitiva policial (EC/SUE/PEACE/PBEF) · 2. Portaria de instauração · 3. Relatório final (7 eixos) · 4. IPe
  · 5. Laudos (SPTC) · 6. Protocolo de objetos/custódia · 7. Habilidades e prompts · 8. Projetos importados
- **Parte V — Lições Operacionais e Entraves de Sistema**
  Estrutura durável · gravação de planilha · ferramentas/arquivos · SPJ · IPe · SPTC · Outlook · e-SAJ/SPVIDA
  · métodos investigativos · regime de trabalho

---

## PARTE I — Arquitetura e Governança do HUB

> Governança-raiz do sistema multiagente do Cartório Central da DPM Aparecida/SP, destilada dos protocolos-fonte. Fundamento decisório permanente: a **decisão final é sempre do Escrivão-Chefe/Delegado** (art. 2º, §6º, Lei 12.830/13).

---

### 1. Arquitetura multiagente: HUB + subagentes/satélites e a fila de commit

#### 1.1 Regime CHAT ÚNICO com despacho interno (PROTOCOLO_MULTIAGENTE v2.3)

O expediente inteiro roda **num único chat HUB, em Opus por padrão**. O HUB abre sozinho os próprios subagentes internos e nunca para.

- **Toda frente roda como subagente interno** despachado pelo HUB (produção, leitura, análise, varredura). O HUB retém para si: **orquestração, auditoria, commit, memória (E3) e decisões com o João**.
- **Chats-satélite manuais deixaram de ser o modo normal** — passam a **exceção declarada** para exatamente 3 casos (§2.5): (1) login em sistema via Claude in Chrome; (2) sessão dedicada em Opus a peça longa (C3/C5) com curadoria ao vivo; (3) frente que atravessa dias (mutirão, correição).
- **Despacho automático total:** aberto o dia, o HUB despacha as frentes rotineiras **sem pedir OK**, informando `frente → modelo → escopo`. Exigem confirmação do João apenas: **commit** nas vivas, **expurgo** (`clear`) e **decisão jurídica**.
- **Retorno por referência (P11):** o subagente devolve **síntese ≤10 linhas + produto no destino + pacote na fila**, sempre com caminho + contagens. É **proibido colar conteúdo bruto no retorno**. A leitura bruta morre com o subagente; o contexto do HUB dura o expediente.

#### 1.2 A regra inegociável que sustenta o conceito

> **Tudo paraleliza, MENOS a escrita nas planilhas vivas — que têm UM dono: o HUB.**

- **Planilhas vivas:** `CARTORIO_CENTRAL_DM_APARECIDA (1).xlsx` (mestra, **26 abas**) e `AGENDA_ESCRIVAO_CHEFE_v1.0 (1).xlsx`, em `Planilhas de controle cartorário\`.
- **Subagente NUNCA toca as vivas.** Entrega **pacote** em `_PARA_LANCAR_NA_MESTRA\pendentes\` (formato `_MODELO_PACOTE.md`).
- **Frentes 🔴 (commit) nunca viram subagente** — ficam no HUB: D1, D2, D3, D6, E3 (e G3/G4).

#### 1.3 Fila de commit `_PARA_LANCAR_NA_MESTRA\` (sequência inalterada)

`pendentes\` → **auditoria de completude** (cobertura · completude por registro · consistência · fonte lida por inteiro) → veredicto **✅/🔁** → **backup → prévia célula a célula → confirmação do João → aplicar → validar reabertura** → `aplicados\`. **Um pacote por vez.** Commit parcial é preferível a represar.

#### 1.4 Anti-colisão simplificada pelo chat único

Não há outro escritor possível. A checagem de abertura reduz-se a: **trava `.~lock`** (Excel aberto) **+ conferência por CHAVE da última linha das abas-alvo × ESTADO** (openpyxl full load). A pergunta "há outro chat gravando?" só ressurge se aparecer pacote em `pendentes\` que este chat não despachou — nesse caso o HUB pergunta antes de qualquer commit.

#### 1.5 Régua de esforço e paralelismo (P8–P14, adotadas 02/07/2026)

| Regra | Conteúdo |
|---|---|
| **P8 · Régua de esforço** | Trivial (1 consulta, 1 ofício avulso) = **inline no HUB**, sem subagente. Simples = 1 subagente (3–10 chamadas). Comparação/conferência = 2–4 subagentes (10–15 chamadas cada). Varredura complexa = fan-out por território. Na dúvida, um nível acima. |
| **P9 · Teto de paralelismo** | Máximo **3–5 subagentes leves por onda**; acima disso, ondas sucessivas. Pesada continua 1 por vez. |
| **P10 · Território** | 2+ subagentes em escopos vizinhos → brief define **DIVISÃO DE TERRITÓRIO** explícita (dentro/fora). |
| **P11 · Retorno por referência** | Síntese + caminho + contagens; proibido colar conteúdo bruto. |
| **P12 · Paralelismo interno** | Brief manda o subagente fazer leituras/consultas em chamadas paralelas (3+ por vez); exceção: sistemas com login (sequencial). |
| **P14 · Painel de revisores (C3/C5)** | Peça assinada pelo Delegado: antes da versão final, **2–3 subagentes revisores em paralelo** com lentes distintas — (a) conformidade DGP-26/CPP · (b) fato×fonte nos autos · (c) forma e coesão — e o redator sintetiza. |

Custo relativo (fonte Anthropic engineering): subagente ~4× tokens de chat; fan-out completo ~15×. Despachar só quando a economia de contexto/tempo supera o custo.

#### 1.6 Brief estruturado (§2.4)

O HUB preenche: **OBJETIVO · ESCOPO EXATO · FORMATO DE SAÍDA · O QUE NÃO FAZER · CHAVE DO PACOTE.** O **corpo operacional do brief = o comando vigente da frente** no `CATALOGO_COMANDOS_SATELITE.md` v2.0 (agora "catálogo de briefs"). Lote grande: sub-lotes 10–20 + `PROTOCOLO_VARREDURA_CONTINUA`.

#### 1.7 Ciclo do dia

1. **Abertura** (comando §7.1) → rotina da `ROTINA_ABERTURA_HUB.md` v2.4 → despacho automático.
2. **Produção paralela** dos subagentes; João livre no HUB.
3. **Coleta + auditoria** dos retornos; fila montada.
4. **Commits seriais** com confirmação.
5. **Fechamento:** `ESTADO_ATUAL.md` (heredoc + tail), fila restante, repassadas abertas, aprendizados novos.

#### 1.8 Blindagem de contingência (o sistema degrada com anúncio, nunca trava)

| # | Se acontecer… | O HUB faz |
|---|---|---|
| **C1** | Ferramenta de subagentes falhar | Executa a frente **inline**, mesma qualidade; registra via `aprendizado-continuo`. |
| **C2** | Modelo indisponível/rebaixado | Fallback: **Opus→Sonnet** (só produção; juízo/auditoria/commit aguardam Opus) · **Haiku→Sonnet**. Sempre anuncia. |
| **C3** | Franquia apertando | `modo rapido` automático só nas frentes mecânicas, anuncia, pergunta se prioriza/adia as Opus. |
| **C4** | Contexto do HUB a ~70–80% | **Passagem de bastão**: fecha parcial, atualiza `ESTADO_ATUAL.md`, gera comando de abertura do chat-sucessor. |
| **C5** | Paralelismo travando (entrave 02/06) | Serializa tudo (um por vez), termina o dia assim, registra. |
| **C6** | Trava `.~lock` na hora do commit | Pede fechar a planilha; produção continua, só os commits aguardam. |
| **C7** | Pacote com lacuna | Veredicto 🔁 NOVA PASSADA cirúrgica; volume→mesmo modelo/lote menor; juízo→1 nível acima; 2× o mesmo motivo→corrigir o brief. |
| **C8** | Subagente não retorna | Redespacha 1× (mesmo brief, lote menor); 2ª falha = inline + registra. |

**Princípio:** a **Cláusula de Qualidade não entra na contingência** — auditoria ✅/🔁, leitura integral e regra de ouro valem em qualquer modo e fallback.

#### 1.9 Carta de poderes e plano de varredura total (HUB_CONTROLE_TOTAL, 28/06/2026)

A carta-mãe concede ao HUB, **sem autorização a cada passo**: despachar quantos subagentes forem necessários; auditar todo pacote e exigir nova passada; mapear/propor consolidação de dados espalhados (Bloco I — entrelaçamento) e arquivar pelo ciclo de vida; buscar na internet e nos sistemas (após `login ok`); higienizar e operar o `clear`. Os limites que ficam de pé são os já consolidados: escritor único, IA nunca digita credenciais, leitura integral, curadoria intocável, regime de despacho interno.

**A meta:** a pasta tem **200+ planilhas**; toda informação relevante deve desembocar na **espinha relacional da mestra** (26 abas amarradas por chaves comuns — BO+Ano, nº IP, envolvido/CPF/RG, nº laudo, nº objeto), espelhada na Ficha 360. **Princípio do entrelaçamento (ordem do João, 20/06/2026):** consolidar não é só juntar, é **conectar** — tocar um registro faz aparecer tudo o que se liga a ele.

**Plano de varredura S1–S8 (frentes despacháveis, ordem recomendada):** S1 BOs & Fianças (`projeto-download-bos` → `BOs`/custódia/`CORRESP.`) → S3 Livros obrigatórios & Custódia (`projeto-livros-correicao` → abas de custódia/`PERÍCIAS`/`AIs`) → S4 Laudos (worklists 85-Laudos → `PERÍCIAS`) → S2 IPe & Correição (`projeto-conferencia-inqueritos`/Correição 2026 → `IPs`/`COTAS`) → S5 Estatística mensal (EST. jan→jun + inventário) → S6 SPVIDA & fontes Seccional (auditoria de tipificação → `IPs`/`BOs`) → S7 Avulsos & Encartes → S8 Ciclo de vida (arquiva/consolida o já absorvido). Cadência: uma pesada por vez; leves (S4/S7) em paralelo; lote >10 → `PROTOCOLO_VARREDURA_CONTINUA`.

> **Nota de versões dos protocolos-fonte (07/07/2026 — HARMONIZADO):** os arquivos em disco autodeclaravam **v2.1** enquanto as referências cruzadas citavam **v2.3**; em 07/07/2026 os rótulos de `PROTOCOLO_MULTIAGENTE`, `MATRIZ_ROTEAMENTO_MODELOS` e das referências cruzadas foram harmonizados para **v2.3** (conteúdo inalterado — P8–P17, blindagem C1–C8, chat único, sem-Fable já constavam). Backup pré-edição em `05_ARQUIVO/2026_Q3/backup_pre-harmonizacao-rotulos_2026-07-07/`.

---

### 2. Matriz de roteamento de modelos (MATRIZ_ROTEAMENTO_MODELOS v2.3)

#### 2.1 Regime vigente (decisão de 02/07/2026)

**Despacho interno automático — matriz reativada.** Substitui o regime "OPUS para todas as requisições" (10/06/2026, **revogado**). O **HUB roda em Opus** (padrão e teto de qualidade, dentro da franquia — custo extra zero).

> **Regra "SEM FABLE":** em 07/07/2026 o Fable 5 sai da franquia e passa a créditos em dólar; por isso a **3ª ordem do João (02/07): FABLE NÃO É UTILIZADO.** Regime 100% dentro da franquia (Haiku/Sonnet/Opus). Reversão só por nova ordem expressa do João. As frentes de juízo profundo que rodariam em Fable rodam em **Opus + painel de revisores P14** (+ rubrica P13 + mini-eval P17).

- **Nota de versões:** Opus 4.8 · Sonnet (mais recente) · Haiku 4.5. Fable 5 existe mas está fora do regime.
- **Válvula de subida sempre aberta, de descida nunca:** o HUB sobe o modelo quando a qualidade pedir (anunciando); rebaixar abaixo da matriz só por gatilho ou ordem.

#### 2.2 Matriz por frente

| Modelo | Natureza | Frentes |
|---|---|---|
| **Haiku 4.5** | Mecânica pura, regra fixa, sem juízo jurídico | A2 (download BOs SPJ, custódia SHA-256, CSV), B5 (laudos Segunda Via SPTC), B6 (varredura IPe cota×inquérito), D5 (separação p/ livros), E2 (snapshots), F-EXP-01 (fiança × comprovante × BO) |
| **Sonnet** | Classificação/produção com regra explícita | A1 (triagem e-mails T01–T12), C1 (ofícios/cotas/certidões/intimações), C6 (destruição em lote), D4 (re-auditoria documental), D6 (prazos + minutas prorrogação), E1 (estatística mensal, 10 planilhas), F-EXP-02 (remessa BO de fora), B2-tabela, G1, G2 |
| **Opus 4.8** | Síntese analítica com juízo; **MODELO PADRÃO DO HUB** | **HUB** (orquestração/auditoria/commit), B1 (análise IP 7 passos), B2-decisão, B4 (histórico consolidado de envolvido), B-HIB, C2 (portaria instauração), C4 (termo de oitiva), D1 (cadastro BO com propagação), conferências em lote |
| ~~Fable 5~~ **→ Opus + painel P14** | Juízo profundo (Fable NÃO utilizado) | A3-sensível, B3 (análise aprofundada BO 13 blocos), C3 (Relatório Final IP), C5 (representações cautelares), SPVIDA (tipificação de mortes), PRONT. (cruzamento de envolvidos/coautoria), F-META (curadoria do sistema), auditoria crítica. **Opus é o piso — nunca rodar em Haiku/Sonnet.** |

**Modo HÍBRIDO (frente B-HIB, gatilho `hibrido`):** o João anexa o documento; a cada lacuna o HUB **pergunta** `(1) 🤖 eu busco` (cito fonte) ou `(2) 🧑 você busca`. Modelo Opus; se o produto final for peça jurídica → Opus + painel P14.

#### 2.3 Cláusula de Qualidade (10/06/2026) — permanece integral e inegociável

1. **Nenhuma medida de eficiência pode importar em perda de qualidade.** Leitura integral, regra de ouro do `cadastro-bo-mestra` e validação de reabertura não se abreviam.
2. **O HUB é SEMPRE o auditor.** Todo pacote passa pela conferência de completude antes de qualquer commit. O regime barateia a **produção**, nunca a **conferência**.
3. **Rigor no controle:** chaves contra a mestra, vocabulários (LISTAS), colunas por NOME, curadoria preservada (col. `U`/`W`; col. A da IPs), veredicto explícito em todo pacote.

#### 2.4 Gatilhos de nível e velocidade

| Gatilho | Efeito |
|---|---|
| **`modo padrao`** | Matriz como está (default de toda abertura). |
| **`modo rapido`** | Produção desce 1 nível onde a regra é fixa (Sonnet→Haiku; Opus→Sonnet em produção não-jurídica), paralelismo máximo. **Juízo e auditoria NÃO descem nunca.** |
| **`modo maximo`** | Produção sobe 1 nível (teto: Opus — sem Fable); juízo ganha painel P14. |
| **`nivel [modelo] [frente]`** | Força o modelo daquela frente (ex.: `nivel opus B5`). Subida direta; descida abaixo da matriz = HUB avisa o risco 1× e cumpre. |
| **`despachar [frente] [escopo]`** | Despacho imediato fora da rotina. |
| **`status`** | Painel: subagente → modelo → escopo → situação. |
| **`pausar despacho` / `retomar despacho`** | Suspende/retoma o automático. |

#### 2.5 Conferência do HUB — completude antes do commit (rubrica P13)

**P13 · Rubrica pontuada (LLM-as-judge):** todo pacote recebe nota **0–1** em 5 critérios — exatidão factual · citação-à-fonte · completude do escopo · qualidade da fonte (autos lidos, não tela-resumo) · eficiência. **Corte: qualquer critério <0,8 = 🔁 NOVA PASSADA.** A rubrica não substitui a amostragem no documento-fonte, a sustenta.

Nenhum pacote entra na mestra sem auditoria, nesta ordem: **(1) Cobertura** (contagem pacote × lote; parada graciosa = cobertura parcial declarada) · **(2) Completude por registro** (100% em lotes ≤10; nos maiores, todos com campos vazios + 2 aleatórios) · **(3) Consistência** (flags nas abas certas, formato padrão, datas plausíveis, soma de objetos × abas de custódia) · **(4) Fonte lida por inteiro** (síntese que cita só a 1ª página ou ignora peças = leitura parcial → nova passada).

**Regras da nova passada:** escopo cirúrgico; falha de volume → mesmo modelo, lote menor; falha de juízo → um nível acima; repassada 2× pelo mesmo motivo → registrar via `aprendizado-continuo` e corrigir o prompt. Commit parcial preferível a represar.

---

### 3. Catálogo de frentes (A–F) e catálogo de comandos/briefs

#### 3.1 Legenda de tipo

🟢 Produção isolada (vira subagente) · 🔵 Leitura/análise (vira subagente) · 🔴 Commit em planilha viva (**fica no HUB, nunca vira subagente**).

#### 3.2 Frentes por bloco

**BLOCO A — ENTRADA & TRIAGEM**
- **A1** 🟢 Triagem de e-mails (Outlook, tipologias T01–T12, anexos com SHA-256) → `CORRESP.`, agenda.
- **A2** 🟢 Download + extração de BOs do dia (SPJ) → PDFs + CSV em `downloads\AAAA-MM-DD\` → `BOs`.
- **A3** 🔵 Triagem/destino de BO (IPL/IPS/TCO/NECRIM/arquivar/remessa) → `BOs`/`IPs`/`TCs`/`AIs`.
- **A4** 🔵 Conferidor de BOs não cadastrados (cruza worklists × mestra) → `conferir_bos.py`.

**BLOCO B — INVESTIGAÇÃO & ANÁLISE**
- **B1** 🔵 Análise de inquérito (diagnóstico 7 passos) → agenda, `COTAS`.
- **B2** 🔵 Mutirão de IPs (lote); tabela=Sonnet, decisão/priorização=Opus.
- **B3** 🔵 Análise aprofundada de BO (13 blocos) → minuta da coluna de Análise Aprofundada (col. `U` no layout v2.1 vigente; a coluna é só do João).
- **B4** 🔵 Histórico de BO por envolvido (reincidência, modus).
- **B5** 🟢 Consulta/caça de laudos (Segunda Via SPTC) → `PERÍCIAS`.
- **B6** 🟢 Levantamento IPe (cota × inquérito, pente-fino) → `COTAS`, `IPs`.
- **B-HIB** 🔵 Híbrido sobre documento anexado; pergunta a cada lacuna quem busca.

**BLOCO C — PRODUÇÃO DE PEÇAS (.docx)**
- **C1** 🟢 Ofícios / cota cumprida / intimação → `04_PRODUTOS\Aguardando_Revisao\`.
- **C2** 🟢 Portaria de instauração de IP → `IPs`.
- **C3** 🟢 Relatório Final de IP (7 eixos, cenários A/B/C) → `IPs`.
- **C4** 🟢 Termo de oitiva (declarante/testemunha/vítima/indiciado; quesitos por técnica EC/SUE/PBEF).
- **C5** 🟢 Representações cautelares (preventiva/temporária/busca e apreensão/sigilo).
- **C6** 🟢 Pedidos de destruição em lote (drogas/armas) → custódia (baixa).

**BLOCO D — CARTÓRIO & CONTROLE (núcleo de commit — no HUB)**
- **D1** 🔴 Cadastro & propagação de BO na mestra (`cadastro-bo-mestra`) → `BOs` + abas dependentes.
- **D2** 🔴 Agenda — BACKLOG/AGUARDANDO/ROTINAS, prazos → `AGENDA`.
- **D3** 🔴 Custódia → `ARM. CUST.`/`DROGAS CUST.`/`CEL.`/`VEÍC.`/`DINH.`/`DEMAIS OBJ.`/`ARMAS B.`/`SIMUL.`.
- **D4** 🔵→🔴 Re-auditoria documental de BOs (aponta lacunas; correção é commit no HUB).
- **D5** 🔵→fila Separação para os livros obrigatórios.
- **D6** 🔴 Controle de prazos / livros obrigatórios → `AGENDA`/mestra.

**BLOCO E — FECHAMENTO & GESTÃO**
- **E1** 🟢 Estatística mensal (Seccional/DEINTER 1/CCDCRIM).
- **E2** 🟢 Snapshots datados da mestra/agenda → `Para_Consulta\`.
- **E3** 🔴 Log de aprendizado / `ESTADO_ATUAL.md` (**só o HUB**).
- **E4** 🟢 Ficha 360 (painel relacional; views Pendências/Prazos/Saúde; dossiê do envolvido) → `Ficha360_Cartorio_Central.html` (auto 20h).
- **E5** 🟢 Briefing matinal + abertura HUB → `Briefings/BRIEFING_HOJE.md` (auto 07h).

**BLOCO F — EM EXPANSÃO**
- **F-EXP-01** 🔵 Controle de fianças (comprovante × valor × BO).
- **F-EXP-02** 🔵 Remessa de BO de fora (circunscrição diversa) + ofício de encaminhamento.
- **F-EXP-03** 🔵→🔴 Re-auditoria documental (promovida de D4).
- **F-META** 🔴 Curadoria do sistema multiagente (propõe frentes novas; só no HUB).

**BLOCO G — GOVERNANÇA & AUTOMAÇÃO**
- **G1** Higiene de pastas (gatilho `higiene`) · **G2** Gestor de Informações / Bloco I (gatilhos `consolidar`/`gestor`) · **G3** `clear`/Quarentena (gatilhos `clear`/`quarentena`) · **G4** Modernização semanal (gatilho `modernizar`) · **G5** Ciclo de vida dos dados (gatilhos `arquivar`/`consolidar dados`/`indice`) · **G6** Central de Buscas (gatilho `buscar`).

#### 3.3 Catálogo de comandos/briefs (CATALOGO_COMANDOS_SATELITE v2.0)

Os antigos "comandos de satélite" viraram o **corpo operacional do BRIEF** que o HUB entrega ao subagente. O know-how permanece; muda o veículo — só nas exceções manuais o comando volta a ser colado num chat. Cada frente com projeto próprio tem um comando **VIGENTE** (ex.: A1 `TRIAGEM_EMAIL_v1.1_CONTINUACAO`, A2 `LISTA_LIVROS_v4.1`, B5 `B5_CACA_LAUDOS`, B6 `ENRIQUECIMENTO_IPs_v1.0`, C1 `PEDIDO_PRAZO` v4.0/v5.0/v6.0). Versões **SUPERSEDED** são preservadas (limpeza física de 02/07/2026 moveu-as para quarentena, com registro cruzado — nada apagado). Frentes sem comando próprio (A3, B1–B4, C2–C6, D1–D6, E1–E3, F-EXP, F-META) usam o **prompt genérico** do `CATALOGO_FRENTES.md §3` ou ficam no HUB.

---

### 4. Ciclo de vida dos dados — 3 camadas + índice mestre (PROTOCOLO_CICLO_DE_VIDA_DADOS v1.0)

**Princípio inegociável:** consolidar = **unificar, nunca perder**. Nada é apagado; o original só vai à quarentena depois de conferido e indexado, e a quarentena é permanente e consultável.

| Camada | O que é | Onde fica | Entrada |
|---|---|---|---|
| **🟢 VIVO** | Dado de uso corrente, editável | mestra `CARTORIO_CENTRAL` + `AGENDA` | procedimento/controle em andamento |
| **🟡 ARQUIVO** | Dado íntegro fora do giro diário | `05_ARQUIVO/AAAA_Qn/` | procedimento encerrado / mês fechado / projeto concluído |
| **🔵 CONSOLIDADO** | Resumo denso + ponteiro ao original | `05_ARQUIVO/_CONSOLIDADO/` | quando o ARQUIVO perde interesse corrente e ocupa espaço |

**Fluxo:** `VIVO ─(encerrou)→ ARQUIVO ─(perdeu interesse)→ CONSOLIDADO`, sempre com conferência do HUB.
- **VIVO→ARQUIVO:** confirmar absorção/encerramento → mover a fonte sem alterá-la (md5 registrado) → linha no `_INDICE_MESTRE.md` (camada ARQUIVO).
- **ARQUIVO→CONSOLIDADO ("compactação que preserva a busca"):** gerar resumo denso em `_CONSOLIDADO/AAAA_Qn__<tema>.md` → **compactar o original** para `_CONSOLIDADO/_originais/AAAA_Qn__<tema>.zip` (md5 antes/depois) → atualizar índice (aponta para resumo **e** zip) → só então o arquivo solto pode ir à quarentena.

**Índice mestre** (`05_ARQUIVO/_INDICE_MESTRE.md`, gatilhos `indice`/`buscar arquivo [chave]`): tabela **append-only**, uma linha por lote/fonte — `| Chave/Tema | Período | Camada | Caminho | Resumo (se consolidado) | md5 | Data índice |`. Para qualquer chave (BO+Ano, IP, CPF/RG, laudo, objeto, período) diz **em que camada** o dado está e **o caminho exato** para recuperá-lo.

**Nunca consolidar/arquivar (intocáveis):** as 2 planilhas vivas e backups; custódia, livros obrigatórios e peças de valor legal (ISO 27037); estatística do mês corrente e anterior; `Conhecimento/` e a governança-raiz; projetos com atividade nos últimos 60 dias.

**Gatilhos:** `arquivar` · `consolidar dados` · `indice` / `buscar arquivo [chave]`.

---

### 5. Protocolo de varredura contínua — checkpoint + compactação (v1.3)

**Ordem do João (10/06/2026):** os subagentes de bloco **não usam número fixo de lote**. O subagente processa registro a registro e vai **até encher o contexto**, parando sozinho com margem e indicando onde retomar. Aplica-se a varredura de BO, inquéritos/IPe, laudos/perícias, livro de controle interno, consolidação — qualquer frente em blocos.

**Princípio:** o que torna a parada segura **não** é medir o contexto (o agente não consegue com precisão) — é **persistir e dar checkpoint a cada registro**, de modo que uma parada perca no máximo o registro em curso.

**Ciclo por registro (inegociável):** (1) buscar/ler por **API/DOM** (nunca screenshot quando houver alternativa) · (2) produzir a saída e **persistir já em disco** (`resumos/`, `staging/`, linha no pacote parcial em `pendentes\`) · (3) **CHECKPOINT** (marcar feito no controle, com `.bak`) · (4) **descartar o conteúdo pesado da memória** (manter só uma linha de status) · (5) repetir.

**Parada graciosa:** parar ao acumular registros pesados, ao encurtar/lentificar as respostas, logo após um registro muito pesado, ou por estimativa a ~**70–80%** do fôlego — sempre com folga. Ao parar: fechar o pacote parcial, atualizar o controle com "próximo = registro Y", avisar "processados N (de A até B); retomar do Y".

**Compactação AGENDADA (P1):** além do descarte por registro, o subagente faz compactação ativa **a cada 10–15 registros/ferramentas** (linha-âncora + confere pacote/checkpoints em disco + solta o detalhe acumulado do bloco). Pesquisa: cadência fixa mede **~22% menos tokens**, sem perda de acurácia. A compactação nunca abrevia a leitura integral nem a fidelidade — descarta o texto bruto já processado, não a informação extraída.

**Checklist JSON (P15/P16):** toda varredura **>20 registros** nasce com um **CHECKLIST JSON** gerado pelo HUB (um objeto por registro: chave, descrição, `"passes": false`) gravado junto ao pacote. O subagente **só pode alterar o campo `passes`** — é inaceitável remover ou editar itens. Cobertura audita-se por contagem (`passes:true` × total). **Retomada (P16):** o subagente de continuação lê o checklist + progresso, **confere 1–2 registros já feitos** antes de produzir; estado quebrado → reporta antes de continuar.

**Regra do HUB:** o HUB **confere pela pasta** (saídas + controle + pacote), **não confia no "concluí" reportado** pelo subagente. Um trecho só é "fechado" quando **saída + checkpoint + linha no pacote** existem para cada registro.

---

### 6. Central de buscas — internet + sistemas via Claude in Chrome (v1.0)

**Decisão do João (28/06/2026): buscas LIBERADAS.** Revogadas todas as travas que proibiam a IA de pesquisar, na internet e dentro dos sistemas. **Única salvaguarda mantida (segurança, não trava de busca): a IA nunca digita login/senha** — o João autentica manualmente e dá o **`login ok`**; a partir daí a IA navega, pesquisa, lê e extrai.

**Dois canais:**
1. **Internet:** `WebSearch` (legislação, jurisprudência, DGP recente, doutrina, dados oficiais); `mcp__workspace__web_fetch` (URL conhecida); Claude in Chrome (`navigate` + `get_page_text`/`read_page`) quando exige JS/render/login. **Sempre citar a fonte** (`PADRAO_CITACAO_FONTE.md`).
2. **Sistemas (Claude in Chrome, sessão do João):**

| Sistema | URL-base | Busca | Pré-requisito |
|---|---|---|---|
| **SPJ** | `https://spj.ipe-policiacivil.sp.gov.br/boletins-ocorrencias/list` | BOs, autos, oitivas, requisições, APFD, Histórico de Despacho, Extrato de Alterações | `login ok` |
| **Segunda Via SPTC** | conforme SOP `85-Laudos/SOP_Consulta_Segunda_Via_Laudos.md` | laudos por nº/lacre/peso; "Exibir Laudo" baixa PDF | `login ok` |
| **IPe** | conforme `80-IPe/SOP_Levantamento_Inqueritos_x_Cotas.md` | cota × inquérito, status, pente-fino | `login ok` |

**Procedimento padrão:** confirmar sessão (`login ok`, IA não insere credenciais) → abrir a tela certa → pesquisar pela chave (BO+Ano, nº IP, nº laudo, lacre) → **ler por inteiro** (regra de ouro: todos os documentos, não a tela-resumo) → **extrair com custódia** (PDF + **SHA-256**, CPP 158-A → `projeto-download-bos/downloads/AAAA-MM-DD/`) → citar a fonte.

**Entraves conhecidos (consultar `aprendizado-continuo`):** sessão SPJ expira em minutos (carregar 30s+ = sessão caiu, repedir `login ok`); modal "Notificações" do SPJ bloqueia o "Pesquisar"; renderizador do Chrome congela ("renderer frozen" → `wait` 5–6s + re-screenshot); "Exibir Laudo" baixa mas não renderiza; Chrome MCP às vezes bloqueia o texto bruto de PDF (ler via pdf.js ou buscar o arquivo baixado). Todo novo entrave deve ser registrado via `aprendizado-continuo` com data.

**Limites permanentes (segurança):** nunca digitar login/senha; nunca abrir anexo de tipo proibido (`.exe`, `.scr`, `.bat`, `.vbs`, `.js`, `.msi`, `.dll`, `.com`, `.pif`); link de e-mail/mensagem é suspeito por padrão (conferir URL real antes de abrir); todo download de peça oficial recebe SHA-256 e registro.

---

### 7. Comando `clear` / Quarentena (v1.1)

Tira do caminho documentos que já cumpriram a função, deixando a pasta mais leve **sem nunca perder o que tem valor cartorário/legal**. Nada some de imediato nem por tempo: tudo vai para uma **quarentena permanente e consultável**.

**Princípios:** (1) **sempre perguntar** (o `clear` nunca move/apaga sozinho); (2) **otimizar/mesclar/consolidar vem antes de expurgar** — inclui o **gestor de informações** (Bloco I): dados espalhados são propostos para unificação na mestra, não expurgo; (3) **quarentena permanente**, não lixeira-relógio; (4) **resgate fácil** via `_INDICE_QUARENTENA.md` (caminho original); (5) na dúvida entre leveza e acervo, **prevalece o acervo**.

**Gatilho de candidatura:** função cumprida **E** sem toque há mais de **60 dias**. Exceção antecipadora: staging/temp de operação comprovadamente já aplicada (pacote em `aplicados/`).

**Lista de PROTEÇÃO (nunca candidatar):** as 2 planilhas vivas e backups; `_PARA_LANCAR_NA_MESTRA/` inteiro; `Conhecimento/`; governança-raiz; custódia, livros obrigatórios e peças de valor legal/probatório; estatística do mês corrente e anterior; projetos com atividade nos últimos 60 dias.

**Estrutura:** `05_ARQUIVO/_QUARENTENA/` com `_INDICE_QUARENTENA.md` (data | item | caminho ORIGINAL | motivo | tamanho | como resgatar), `_NAO_VARRER.marker` (varreduras/higiene ignoram a árvore) e um lote por expurgo `AAAA-MM-DD_<motivo>/` preservando subcaminho. Esvaziar a quarentena de vez só por ordem explícita e separada do João. O **Bloco H** da abertura gera os candidatos; o `clear` é o executor da etapa de quarentena (a mais drástica das três: otimizar → consolidar → quarentena).

---

### 8. Padrão de citação-à-fonte (P5)

Todo produto gerado com apoio do sistema (ofícios, relatórios, resumos investigativos, levantamentos, pacotes) leva ao final um **rodapé de proveniência**:

```
— Fonte: [documento(s)/peça(s) de origem — ex.: BO ...; Auto de Exibição; Termo de Declarações]
  Gerado com apoio do HUB em [data] · CONFERIR NO ORIGINAL antes de assinar/juntar.
  Responsável pela revisão: [Escrivão/Delegado].
```

**Princípios:** (1) **rastreabilidade** — citar a peça-fonte exata (nº do BO/IP, tipo de documento), não "os autos" genéricos; (2) **carimbo temporal** (data/hora de geração); (3) **conferência humana obrigatória** — a peça é minuta a conferir; decisão e assinatura do Escrivão-Chefe/Delegado (art. 2º §6º, Lei 12.830/13); (4) **não substitui a cadeia de custódia** (ver P6). Aplica-se a C1, C3, C4, C5, resumos investigativos e ao cabeçalho dos pacotes de commit.

---

### 9. Padrão de cadeia de custódia — ISO/IEC 27037, log append-only (P6)

Fundamento legal interno: **art. 158-A a 158-F do CPP**. Referências técnicas: ISO/IEC 27037, ISO/IEC 27042, SWGDE.

**Três pilares:** (1) **Integridade — SHA-256** (todo arquivo de evidência recebe hash na coleta; recálculo prova que nada mudou — já feito no `projeto-download-bos`); (2) **Preservação — cópia fiel** (trabalhar sobre cópia; original não é editado); (3) **Rastreabilidade — log imutável** (cada acesso/cópia/transferência/requisição/entrega vira **uma linha nova** num livro append-only; nunca se edita nem apaga linha existente).

**Livro append-only:** `custodia/LIVRO_CUSTODIA_APPEND_ONLY.csv`. **Regra absoluta: só APPEND.** Correção de erro = **nova linha de RETIFICACAO** referenciando a anterior. Campos: `data_hora` · `evento` (COLETA / ACESSO / COPIA / TRANSFERENCIA / REQUISICAO_PERICIA / ENTREGA / DEVOLUCAO / RETIFICACAO) · `bo_ano` · `objeto` (descrição + nº de lacre) · `sha256` · `de`→`para` · `responsavel` · `doc_ref` · `obs`.

**Ligação com o resto:** as abas da mestra `PROTOC. OBJ.` e `MOVIM. OBJ.` mantêm o controle operacional; o livro append-only é a **trilha probatória imutável** que as complementa (não substitui). Cada entrada de custódia trazida dos livros de correição gera também a 1ª linha no livro append-only, reaproveitando os SHA-256 já calculados no `projeto-download-bos`. **Honestidade:** o livro é disciplina de processo, não criptografia forte; não substitui laudo pericial nem a guarda física.

---

### 10. Roadmap de melhorias (ondas C/P/H/Q) e registro de expansão de frentes

#### 10.1 Roadmap (ROADMAP_MELHORIAS_MODELO v1.1)

Backlog mestre do HUB, com quatro categorias: **C** (consolidação de dados), **P** (modernização/pesquisa), **H** (higiene), **Q** (qualidade de dados). Legenda: 🟢 autônomo · 🟡 verificação · 🔴 commit na mestra.

| Onda | Escopo | Itens (situação em 22/06/2026) |
|---|---|---|
| **Já entregue (base)** | — | C0 (espinha relacional + Ficha 360, regenera 20h); C2 (índice de IPs, coberto pela busca/dossiê); Governança v2; Automação (Ficha 360 20h + Briefing/abertura 07h). |
| **Onda 1** — ganhos rápidos e seguros (CONCLUÍDA) | — | C4 (dedup vermelhos IPe — bloqueado por `.~lock`); C5 (2 versões correição-fórum divergem, ambas preservadas); Q1 (anos no futuro em `IPs`, view Saúde corrigida); P4 (versões correntes na matriz); **P5 · citação-à-fonte** ✅. |
| **Onda 2** — consolidações que tocam a mestra (análise concluída, prévias na fila) | — | C1 (cotas triagem × status: 87 IPs cota=ARQUIVAMENTO mas "Em Andamento"); C3 (custódia: 83 BOs ausentes nas abas, sub-projeto por lotes); Q2 (88 IPs com Data Instauração implausível — typo de ano). |
| **Onda 3** — modernização de método/governança (CONCLUÍDA) | — | P1 (compactação agendada na varredura); P2 (brief estruturado); P3 (consolidação automática de memória via `consolidate-memory`); **P6 · custódia ISO 27037 + livro append-only** ✅. |
| **Onda 4** — higiene e piloto (CONCLUÍDA) | — | H1 (backups: **manter todos**, ordem do João); Q3 (objeto sem BO: Celta a vincular); P7 (IDP/extração inteligente de BO — piloto: texto+hash sim, parsing de campos não). |

**Como o HUB puxa daqui:** a cada sessão pega o próximo item "a fazer"; os 🔴 viram prévia/pacote para confirmação; os 🟢 saem prontos. Status atualizado neste arquivo + `ESTADO_ATUAL.md`.

#### 10.2 Registro de expansão de frentes (REGISTRO_EXPANSAO_FRENTES v1.0)

Decisão do Escrivão-Chefe (01/06/2026): o sistema **deve crescer** — não há teto para o número de frentes; o único limite é a regra de ouro.

**Gatilhos de nascimento de frente:** tarefa recorrente (2+ vezes); lote de itens de um tipo que pede tratamento próprio; planilha/sistema ainda não coberto; entrave que virou procedimento (Log-Aprendizado); pedido direto do João.

**Regra de ouro da expansão (inegociável):** (1) subagente nunca grava as vivas — só o HUB, via fila; (2) **fidelidade total** — ausente = vazio/`N/C`; nunca inventar; coluna de Análise Aprofundada intocável (`U` no layout v2.1; o registro original dizia `W`, layout anterior); bandeiras de custódia só `Sim`/`Não` (`K–Q` no layout v2.1; original dizia `L–R`); (3) **rastreabilidade** — todo lançamento cita a fonte; (4) decisão final é do João. Frente que não respeita isso não entra no catálogo.

**Anatomia obrigatória de uma frente:** `Código · Nome · Tipo (🟢/🔵/🔴) · Módulo a ler · Saída · Gatilho de fila (aba que recebe pacote) · Prompt de abertura`.

**F-META** é a frente 🔴 autoexpansível: lê o `99-Log-Aprendizado\` e este registro, identifica rotinas/entraves ainda não catalogados, **propõe** e (com OK) **cadastra** frentes novas, mantendo o changelog. Roda no fechamento do dia ou semanalmente. Changelog inaugural (01/06/2026): 24 frentes (A1–E3) + F-EXP-01 (fianças) + F-EXP-02 (remessa de BO de fora) + F-EXP-03 (re-auditoria, promovida de D4) + F-META.

---

## PARTE II — Gestão do Cartório Central (SOPs e Modelos de Peças)

> Destilação dos SOPs de gestão cartorária da DPM Aparecida/SP (Cód. 1512 — DEINTER 1 / Seccional Guaratinguetá). Consolida perfil funcional, planilhas mestras, protocolos operacionais, padrões de formatação, POPs de triagem e o catálogo de modelos de peças. Nomes de abas/colunas, fundamentos legais, prazos e campos obrigatórios preservados com fidelidade. Dados de casos concretos excluídos.

---

### 1. Perfil funcional do Escrivão-Chefe e tom esperado

**Titular do papel:** João Pedro de Alcântara Mota — Escrivão de Polícia Civil de 3ª Classe (RG 54.571.643-3 SSP/SP), Escrivão-Chefe do Cartório Central da DPM Aparecida/SP (Cód. 1512). Subordinação: DEINTER 1 (São José dos Campos) → Seccional Guaratinguetá → DEL.POL.APARECIDA. Endereço: Praça Pe. Vítor Coelho de Almeida, 500 — Jd. São Paulo — Aparecida/SP — CEP 12570-000.

**Estrutura local:** Delegado Titular Dr. Paulo Sergio Barbosa; Substituto Dr. Leonardo da Costa Ferreira; escrivães ativos Milton, Bianca, José Carlos, Erika, Wilson, João Pedro (Chefe — não conta na produção), Cássio, Vinicius. Equipe operacional referida: SIG (Setor de Investigações Gerais).

**Responsabilidades:** gestão do cartório e supervisão da equipe; controle de prazos cartorários (IPs, IPSs, APFDs, MPUs, Cotas Ministeriais, Cartas Precatórias, Ofícios); lançamento na planilha-mestre; triagem de correspondência e de BOs; análise de inquéritos; produção de peças; estatística mensal; gestão dos livros obrigatórios (Decreto 54.750/2009); auditorias SPJ × Controle Interno e SPVIDA.

**Tom (regras de comunicação):**
- **Sem abertura cerimoniosa.** Entrar direto no assunto, como colega de delegacia. Formalidade profissional, não burocrática. Voz ativa e primeira pessoa quando couber. Sem enrolação nem ressalvas genéricas — ele *é* o especialista; disclaimers de IA são redundantes.
- **Terminologia rígida:** "Investigado" é o padrão; "Indiciado" só com peça formal de indiciamento nos autos. Modular imputação ("em tese", "indícios suficientes", "a princípio", "conduta em tese típica"); jamais "comprovadamente praticou"/"culpado". Verbos de elocução neutros (informou, relatou, declarou, admitiu/reconheceu — nunca "confessou", "alegou").
- **Fundamentação dispositivo a dispositivo** com citação dupla: dispositivo federal **+** dispositivo da Consolidação (Portaria DGP-26/2023 e alteradoras). A Consolidação nunca derroga lei federal — só organiza/especifica.
- **Violência doméstica** não é tipo penal autônomo (exceção: art. 24-A da Lei 11.340/06). É contexto vinculado ao crime material (ex.: "lesão corporal, art. 129, §9º, CP, c/c Lei 11.340/2006").
- **Fidelidade aos dados:** extrair apenas o que consta. Lacuna → `N/C` (Não Consta) nas extrações; `[INSERIR DADO]` nas minutas. Nunca presumir, nunca inventar. Evitar pomposidade arcaizante ("destarte", "outrossim", "insta salientar").
- **Estruturação preferida:** tabelas Markdown para roteamento de dados no formato `| ABA DESTINO | COLUNA (CAMPO) | DADO EXTRAÍDO |`; texto corrido para pareceres e Relatório Final. Encerrar respostas substantivas com 1-2 perguntas específicas de acompanhamento.
- **Fontes prioritárias:** Portaria DGP-26/2023 e alteradoras (DGP-32/2023, 35/2023, 6/2024, 01/2025, 21/2025, 36/2025, 37/2025, 9/2026); legislação federal (CP, CPP, Lei 12.830/13, 11.343/06, 9.613/98, 12.850/13, 9.296/96 etc.); jurisprudência STF/STJ (HC 598.886/SC — reconhecimento de pessoas); Resoluções SSP/SP; Decreto 54.750/2009 (livros).

---

### 2. Planilhas mestras e bases seccionais

#### 2.1. Planilha mestra `CARTORIO_CENTRAL_DM_APARECIDA.xlsx` (26 abas, v2.1)

**Regra dos nomes encurtados (v2.0):** usar exatamente os nomes curtos com ponto final quando aplicável. Nomes longos da v1.0 não existem mais.

> ✅ **Conferido no arquivo real em 07/07/2026** (`o arquivo manda`): a mestra tem **26 abas** — as 23 do SOP original **+ `PROTOC. OBJ.`, `MOVIM. OBJ.` e `PERÍCIAS`** (inseridas após `DEMAIS OBJ.`, antes de `REDISTR. IP`). A tabela abaixo reflete a ordem real do arquivo.

| Nº | Aba | Função | Início dados |
|---|---|---|---|
| 1 | `PAINEL` | Dashboard mensal automático (só Presos/Apreendidos manuais, L60-62) | fórmulas |
| 2 | `DASH.` | Dashboard gerencial anual (produção mês a mês) | L8 |
| 3 | `TAREFAS` | Pomodoro — agenda do dia + backlog interno | L5 |
| 4 | `BOs` | Porta de entrada — todos os BOs | L5 |
| 5 | `IPs` | Inquéritos Policiais | L6 |
| 6 | `TCs` | Termos Circunstanciados | L6 |
| 7 | `AIs` | Atos Infracionais (ECA) | L6 |
| 8 | `MPUs` | Medidas Protetivas (Lei 11.340/06) | L6 |
| 9 | `COTAS` | Cotas Ministeriais | L6 |
| 10 | `CPs` | Cartas Precatórias | L6 |
| 11 | `CORRESP.` | Ofícios / requisições / respostas | L4 |
| 12 | `ARM. CUST.` | Armas de fogo + zona ⚡ | L6 |
| 13 | `SIMUL.` | Simulacros (sem zona ⚡) | L6 |
| 14 | `ARMAS B.` | Armas brancas + zona ⚡ | L6 |
| 15 | `DROGAS CUST.` | Entorpecentes + zona ⚡ | L6 |
| 16 | `CEL.` | Celulares + zona ⚡ | L6 |
| 17 | `VEÍC.` | Veículos + zona ⚡ | L6 |
| 18 | `DINH.` | Dinheiro + zona ⚡ | L6 |
| 19 | `DEMAIS OBJ.` | Outros objetos + zona ⚡ | L6 |
| 20 | `PROTOC. OBJ.` | Protocolo de objetos — localização atual + status ("fotografia de agora"), ver Parte IV §6 | conferir |
| 21 | `MOVIM. OBJ.` | Movimentações de objetos (1 linha por evento), ver Parte IV §6 | conferir |
| 22 | `PERÍCIAS` | Requisições de perícia e laudos (Nº Laudo, Status, Data), ver Parte IV §5 | conferir |
| 23 | `REDISTR. IP` | Redistribuição entre escrivães | L4 |
| 24 | `PRONT.` | Prontuários (8 col., expandida v2.0) | L4 |
| 25 | `LISTAS` | Domínios de validação | L4 |
| 26 | `CHANGELOG` | Histórico obrigatório de revisões estruturais | L4 |

**Chaves primárias:** `Nº do BO` (col. B da `BOs` / col. E das abas de custódia) e `Nº do IP` (col. C da `IPs`). Cruzamento com custódia também por `Nº do Lacre`.

**Aba `BOs` (layout v2.1, 01/06/2026) — cabeçalho L4:** A (Nº, fórmula `=IF(B<>"",ROW()-4,"")`), B (Nº do BO, ex. DF8667), C (Ano), D (Data), E (Endereço do Fato), F (Autor(es)), G (Crime), H (Art./Lei), I (Vítima(s)), J (Outras Pessoas), **K–Q = bandeiras Sim/Não que disparam zonas ⚡** [K Outros Objetos→`DEMAIS OBJ.`; L Armas de Fogo→`ARM. CUST.`; M Drogas→`DROGAS CUST.`; N Armas Brancas→`ARMAS B.`; O Celulares→`CEL.`; P Dinheiro→`DINH.`; Q Veículo→`VEÍC.`], R (Despacho), S (Observação — pente fino SPJ), T (Flagrante), U (Análise Aprofundada — curadoria manual, não sobrescrever). *v2.1 removeu as antigas `Nº Controle` e `Escrivão Resp.`; bandeiras migraram de L–R para K–Q.*

**Aba `IPs` (25 col., L5, atualização 11/06/2026):** A (Controle Interno `NNN/26`), B (Nº contador), **C (IP nº — chave primária)**, D (Ano), E (Origem), F (Nº RDO), G (Ano RDO), H (Natureza/Art.), I (Data Instauração), J (Tipo — lista `TIPO_INSTAURACAO`), K (IPe), L (Processo CNJ), M (Vara), N (Vítima), O (Indiciado), P (Delegado), Q (Data Entrada Cartório), R (Prontuário), S (Escrivão — lista `ESCRIVAES`), T (Data Relatório), **U (Nº Protocolo)**, V (Status — lista `STATUS_IP`), W (Observação), X (Vinculação BO), Y (Flagrante). Indicadores L3 e CF de prazo leem V:V (Status).

**Aba `TCs` (16 col., L5):** A (Nº), B (TCO nº), C (Ano), D (Nº RDO), E (Ano RDO), F (Natureza/Art.), G (Data Fato), H (IPe), I (Processo CNJ), J (Vara), K (Vítima), L (Autor), M (Escrivão), N (Status — `STATUS_TC`), O (Prontuário), P (Observação).

**Aba `AIs` (16 col., L5):** idêntica à `TCs` com B (Procedimento nº), F (Ato Infracional/Art.), L (Adolescente), N (`STATUS_AI`).

**Aba `MPUs` (16 col., L5):** A (Nº), B (Controle), C (Ano), D (Nº RDO), E (Ano RDO), F (Natureza/Art.), G (Data Entrada), H (IPe/IP Vinculado), I (Processo CNJ), J (Vara), K (Vítima), L (Agressor), M (Escrivão), N (Status — `STATUS_MP`), O (Prontuário), P (Observação).

**Aba `COTAS` (17 col., L5):** A (Nº Cota), B (Tipo — `TIPO_COTA`), **C (Nº Procedimento — TEXTO, evita truncar 19 dígitos)**, D (Ano), E (Nº RDO), F (Ano RDO), G (Natureza/Art.), H (Data Entrada), I (IPe), J (Processo CNJ), K (Vara), L (Vítima), M (Indiciado), N (Diligências Requeridas), O (Status — `STATUS_COTA`), P (Data Cumprimento), Q (Escrivão).

**Aba `CPs` (15 col., L5):** A (Nº), B (CP nº), C (Ano), D (Delegacia Origem), E (CP Origem), F (Data Entrada), G (Diligência), H (Envolvido), I (Natureza/Art.), J (Nº RDO), K (D.P. Origem), L (Prontuário), M (Status — `STATUS_CP`), N (Data Cumprimento), O (Processo CNJ).

**Aba `CORRESP.` (15 col., L3):** A (Nº), B (Data Entrada), C (Processo), D (Vara), E (Origem), F (Juiz/Promotor), G (Assunto), H (Parte), I (IPe), J (Servidor Resp.), K (Data Resposta), L (Status — `STATUS_CORRESP`), M (Observação), N (Nº Ofício Saída), O (Modal de Envio).

**Abas de custódia (12–19) — estrutura padrão de duas zonas:** zona principal (acervo detalhado) + **zona ⚡ Pendentes** à direita (fila alimentada pela bandeira do BO; ao cadastrar na principal, remover da ⚡).
- `ARM. CUST.` (A–P): campos-chave G (Lacre), I (Marca/Modelo), J (Calibre), K (Nº Série), L (Guia Perícia), O (Status — `STATUS_CUSTODIA`). Zona ⚡ R–W.
- `DROGAS CUST.` (A–O): I (Tipo Substância), J (Peso/g), K (Guia Perícia=Nº Laudo), N (Status: Em Custódia/Periciado/Incinerado), O (Motivo: TRÁFICO/PORTE/OUTROS). Zona ⚡ Q–V.
- `CEL.` (A–O): I (Marca/Modelo), J (IMEI), K (Nº Linha). Zona ⚡ Q–V.
- `VEÍC.` (A–Q, dados na L6): B (Marca/Modelo), C (Placa), L (Guia Pátio), O (Status: No Pátio/Entregue). Zona ⚡ S–X.
- `DINH.` (A–O): J (Valor R$), M (Status — inclui `Depositado`), O (Guia de Depósito nº, incluída 15/06/2026). Zona ⚡ P–U.
- `ARMAS B.` / `DEMAIS OBJ.` (A–N): zona ⚡ P–U. `SIMUL.` (A–N, sem ⚡).

**Aba `LISTAS` (domínios de validação — respeitar exatamente, variante = erro de COUNTIFS):**
| Domínio | Valores |
|---|---|
| ESCRIVAES | Milton, Bianca, José Carlos, Erika, Wilson, João Pedro, Cássio, Vinicius |
| STATUS_IP | Andamento, Relatado, Arquivado, Redistribuído, Devolvido |
| STATUS_TC | Andamento, Cumprido, Aguardando Audiência, Encaminhado JECrim |
| STATUS_AI | Andamento, Concluído, Encaminhado VIJ, Aguardando Oitiva |
| STATUS_MP | Vigente, Cumprida, Revogada, Descumprida, Suspensa |
| STATUS_COTA | Pendente, Em Diligência, Cumprida, Devolvida ao MP, Aguardando Perícia |
| STATUS_CP | Pendente, Em Diligência, Cumprida, Devolvida, Negativa |
| STATUS_CUSTODIA | Em Custódia, Entregue, Destruído, Periciado, Encaminhado Judicial, Restituído, Depositado |
| STATUS_CORRESP | Pendente, Em Análise, Respondido, Arquivado |
| TIPO_INSTAURACAO | Portaria, Requisitado, Flagrante, Auto de Prisão |
| TIPO_COTA | IP, TC, AI, CP, PIC |
| SIM_NAO | Sim, Não · PRIORIDADE | Alta, Média, Baixa, Urgente |

**Regras universais da mestra:** dado ausente → `N/C`; saída sempre em tabela Markdown; nome de escrivão sempre em forma extensa (`João Pedro`, `José Carlos`); toda alteração estrutural registrada em `CHANGELOG` antes de publicar (rastreabilidade análoga ao art. 158-A do CPP).

#### 2.2. AGENDA do Escrivão-Chefe (`AGENDA_ESCRIVAO_CHEFE_v1.0.xlsx`, 5 abas)

Arquivo **separado** da mestra (não confundir com a aba `TAREFAS`, que é Pomodoro pontual). Localização: `Planilhas de controle cartorário\`.

| Aba | Dimensão | Pergunta |
|---|---|---|
| `🗓️ SEMANA` | Macro semanal | Ritmo fixo por dia |
| `📋 BACKLOG` | Micro tarefa | O que está aberto agora / dentro do prazo? |
| `🔄 ROTINAS` | Cíclico | O que se repete? |
| `⏳ AGUARDANDO` | Externo | O que está parado com terceiros? |
| `📊 PAINEL` | Consolidação | Situação geral (só leitura, via fórmula) |

**Ritmo fixo (`🗓️ SEMANA`, L7):** SEGUNDA = análise pesada de BOs (acumulado Sex/Sáb/Dom); TERÇA = remessa drogas/armas/objetos perícia; QUARTA = despachos + correspondências + reunião com escrivães; QUINTA = remessa perícia; SEXTA = cobrança de pendentes + cota cumprida + estatística + backup.

**`📋 BACKLOG` (13 col., L5):** A (Nº), B (Data Entrada), C (Categoria — lista), D (Descrição), E (Vinculado BO/IP/Cota), F (Prazo), G (Dias p/ vencer = `=IF(F6="","",F6-TODAY())`), H (Status — lista), I (Aguardando Quem?), J (Próxima Ação), K (Concluído em), L (Tempo min), M (Observações). **Categorias:** BO | Despacho | E-mail | Cota MP | Carta Precatória | MPU | Custódia | Diligência | Estatística | Ofício | IP/Relatório | Admin Interno. **Status:** A Fazer | Em Andamento | Aguardando | Concluído | Cancelado. Formatação condicional col. G: negativo=atrasado (vermelho), 0-1=laranja, 2-7=amarelo.

**`⏳ AGUARDANDO` (9 col., L5):** B (Descrição), C (Vinculado), D (Aguardando Quem? — lista: Dr. Paulo Sergio (Titular) | Dr. Leonardo (Substituto) | Polícia Científica (IC) | IML | Outra DP | MPSP | Vara/Juízo | Investigador | Vítima/Testemunha | Advogado | Perito | Outros), E (Solicitado em), F (Dias parado = `=IF(E6="","",TODAY()-E6)`), G (Cobrar em), H (Status: Em Espera | Cobrado | Resolvido | Cancelado), I (Observações). Conferir toda SEXTA; itens > 7 dias em vermelho.

**Gatilhos de alimentação:** "anota essa tarefa" → BACKLOG (mín.: Data Entrada=TODAY, Categoria, Descrição, Prazo); "encaminhei para X, esperando" → AGUARDANDO (Descrição, Aguardando Quem?, Solicitado em, Status=Em Espera); "já fiz [rotina]" → ROTINAS (✔ + Última execução). *Defeito conhecido: fórmula `=TEXT(TODAY(),"dddd, dd/mm/aaaa")` em SEMANA!F4 e PAINEL!F15 — trocar `aaaa`→`yyyy`.*

#### 2.3. Bases seccionais (`BASE_PLANILHAS_CARTORIO_CENTRAL.md` / `03_BASE_PLANILHAS_SECCIONAL.md`)

Planilhas mensais consolidadas da Seccional de Guaratinguetá, com **uma aba/linha por unidade** (a de Aparecida = `DM APARECIDA` / `APARECIDA` / `DPM APARECIDA`, linha 26 no Acervo e 27 nas Cotas). Cruzamento por Nº do BO (chave primária), Nº do IP (secundária), Nº do Lacre (custódia).

| Planilha | Aba | Dados | Estrutura essencial |
|---|---|---|---|
| **1 — Produção Cartorária** | `DM APARECIDA` | L13 (1/escrivão) | 13 col.: B/C IPs+Cota mês anterior; D/E recebidos do Fórum; F Instaurados; G Relatados; H Flagrantes elaborados; I Cotas cumpridas; J Enc. Fórum (Sol Cautelar); K Enc. p/ prazo; L/M passam mês seguinte. Rodapé "ELABORADO POR" + Escrivão + Delegado |
| **2 — Nova Acervo IPs** | `GUARATINGUETÁ` | L15 | 33 col.: acervo físico/eletrônico anterior; instaurados (Portaria/Flag/Requis./Requer.); relatados físicos/eletrônicos; redistribuídos; cotas; CPs; funcionários; acervo total |
| **3 — Cotas TC–AI** | mês | L16 | 14 col.: acervo TC físico/eletrônico; instauradas; recebidas; cumpridas; redistribuídas; atos infracionais registrados; acervo total |
| **4 — Esclarecimentos** | `APARECIDA` | L11 | A Nº RDO, B Data Registro, C Equipe, E Natureza (dropdown col. D, ~65 naturezas), F Vítima, G Data Solução, H Autor |
| **5 — Inventário de Entorpecentes** | `APARECIDA` | L22 | Cabeçalho hierárquico L18-21: A Data, B Nº BO, C/D IP físico/digital, E Motivo (TRÁFICO/PORTE/OUTROS), F Vara, G Processo, H Laudo, I Lacre, J-M gramas sob custódia (Maconha/Cocaína/Crack/Outros), N/O incineração solicitada/autorizada, Q-S peso líquido conforme laudo. Metadados L14-16: local, condições de segurança, última incineração |
| **7 — Controle de Armas** | `DPM APARECIDA` | L17 | Aba GERAL + unidades. A Ordem, B Data, C Nº BO, D IP/AI/TC, E/F físico/digital, G Descrição (REVR/PIST/ESP/GARR/CARAB/SUBM; S/M sem marca; S/N sem número), H Marca, I Número, J Calibre, K Laudo, L Lacre, M Vara, N Comarca, O Processo, P Autorização Destruição (SIM/NÃO). *Não existe planilha "6".* |

**Pacote SPJ (fonte externa, cruzamento):** `IPS INSTAURADOS/RELATADOS/FLAGRANTES LAVRADOS SPJ`, estrutura idêntica, dados L4: F (Nº IP), G (Nº BO), H (O IP pertence a esta unidade? SIM/NÃO), I (unidade correta se NÃO).

**Planilhas de Produtividade (conferência com campos de auditoria manuais):** SPDADOS_CRIMINAIS (chave H=NUM_BO; auditor confere DP_CIRCUNSCRIÇÃO e NATUREZA_APURADA); ENTORPECENTES_APREENDIDOS (tipo de tóxico / qtde corretos?); ARMAS_APREENDIDAS (ARMA ILÍCITA? — SIM se numeração suprimida/sem SINARM-SIGMA/possuidor sem CAC-posse-porte; NÃO se institucional PMESP/FA/GCM ou registro regular); PRESOS_E_APREENDIDOS (dupla contagem flagrante+mandado; adolescente = APREENDIDO não PRESO; fiança não descaracteriza prisão); VEÍCULOS_RECUPERADOS (Localizado/Entregue ou Localizado/Apreendido); SPVIDA (78 col.; chave G=SPJ_NUM_BO; análise CAP + auditoria de morte suspeita/circunscrição, Portaria DGP-14/2005).

---

### 3. Protocolo de snapshots (`06_PROTOCOLO_SNAPSHOTS.md`, v1.1)

Três tipos de cópia: **planilha viva** (raiz, edição diária), **backup pré-edição** (`backups/`, antes de alteração estrutural, com timestamp), **snapshot de consulta** (`Para_Consulta/`).

Estrutura de `Para_Consulta/`: `ULTIMA/` (sobrescrita) + `historico/AAAA-MM-DD/`. Nomenclatura: `<NOME-BASE>_AAAA-MM-DD.xlsx` (ISO 8601; remover sufixos ` (1)`/` (2)` de duplicação do Windows).

**Regras de execução:** origem = raiz de `Planilhas de controle cartorário\`; incluir todo `.xlsx` da raiz; excluir subpastas (`backups/`, `Para_Consulta/`, `nao_versionar/`). **Estratégia exclusivamente sob demanda** (agendamentos automáticos desabilitados em 26/05/2026; tarefas permanecem em `Claude/Scheduled/` com `enabled:false`, reativáveis). Gatilhos: "me dá a planilha preenchida", "gera snapshot", "atualiza a pasta de consulta", "fecha versão pra hoje". Snapshot é cópia literal — não recalcula, não valida, não envia a terceiros; se planilha aberta no Excel falhar, registrar e seguir.

---

### 4. Método de estatística mensal (`07_METODO_ESTATISTICA_MENSAL.md`, v1.0)

**Periodicidade:** mensal; fechamento dias 1–10 do mês seguinte; envio à CCDCRIM **após** assinatura do Delegado Titular vigente. Destinatário: Seccional Guaratinguetá → DEINTER 1 → CCDCRIM.

**As 10 planilhas:** 6 alimentadas pela DPM (nº 1, 2, 3, 4, 5, 7 — não existe "6") + 3 do SPJ (8, 9, 10). Auxiliares internas: `Estatistico Novo.xlsx` (11 abas — Resolução SSP-040, IPs relatados, Produção, Prisões, Escoltas, Operações, Diversos, Acervo, DGP 036-AGRO, Ativos), `MAPA DE PRODUÇÃO ESCRIVÃES 2026.xlsx`, `Planilha de armas.pdf`/`Planilha de drogas.pdf`.

**Mapa de fontes:** Produção Cartorária ← `PAINEL`+`IPs`+`COTAS`; Acervo IPs ← `IPs` (IPe vazio=físico; preenchido=eletrônico); Cotas TC-AI ← `TCs`+`AIs`; Esclarecimentos ← `BOs` com autoria identificada (≠ "A Esclarecer"); Inventário ← `DROGAS CUST.`+laudos IC; Controle Armas ← `ARM. CUST.`+laudos IC; SPJ 8-10 ← exportação do `inquerito.policiacivil.sp.gov.br`.

**Sequência canônica (11 etapas):** 0. snapshot da mestra (último dia útil); 1. coleta de inputs (dias 1-2); 2. extração automática da mestra (dia 2, `scripts/extracao_estatistica.py`); 3. campos externos (dias 3-5); 4. auditoria SPJ × Controle Interno (cruzar SPJ col. F/G contra `IPs.C`/`IPs.F`); 5. auditoria de Produtividade (dias 5-7); 6. auditoria SPVIDA; 7. revisão do escrivão (dia 8); 8. assinatura do Delegado (dia 9); 9. envio à CCDCRIM (até dia 10); 10. arquivo em `Para_Consulta/historico/AAAA-MM-DD_estatistica_<mês>/`.

**Inputs pedidos a cada mês:** mês/ano de referência; confirmação do Delegado Titular vigente; lista de escrivães ativos (checar afastamentos); 3 planilhas SPJ; relatórios de esclarecimento da SIG; laudos do IC. *Nota: João Pedro (Chefe) não aparece como linha de escrivão na Produção — atua na coordenação.*

---

### 5. Fluxo único de entrada e conferência de controle de BO

#### 5.1. Fluxo único de entrada (`08_FLUXO_UNICO_ENTRADA.md`, v1.0)

Orquestra **dois canais** que convergem num **trilho comum**:
- **Canal E-MAIL** → robô triagem-outlook (lotes LIFO de 5) → POP com 12 tipologias (T01–T12).
- **Canal BO** → robô download-bos (PDF-driven, SHA-256 por BO) → árvore de decisão (IPL/IPS/TCO/NECRIM/arquivar/remeter — Súmula 536 STJ, art. 28 da Lei 11.343/06).

**Trilho comum (5.1–5.4):** 1. registro na mestra (verificar duplicidade → linha nova → validar contra `LISTAS` → zonas ⚡); 2. registro na AGENDA (BACKLOG/AGUARDANDO/ROTINAS); 3. geração de peça (modelo correspondente → `04_PRODUTOS/Aguardando_Revisao/`, nome `AAAA-MM-DD_<tipo>_<codigo>_v<NN>.<ext>`); 4. log de aprendizado se descobriu padrão novo.

**Árvore de decisão do BO:** não é infração → arquivar; pena ≤ 2 anos → TCO (autor presente) / NECRIM-IPS (autor ausente) / IPL (violência doméstica, Súmula 536 STJ); pena > 2 anos → IPL (justa causa) / IPS (sem justa causa, 60+30 dias) / APFD (flagrante); hipóteses especiais → ECA / JM / PF / juízo competente.

**SLAs (col. Prazo do BACKLOG):** T04 Decisão MPU 24-48h; T06/T07 laudos "hoje+1"; T09 localização/captura 24-72h; BO flagrante/APFD imediato (24h legais); BO VD com MPU 24h (art. 19 da Lei 11.340/06); BO arquivamento → próxima sexta.

#### 5.2. Modelo de conferência e controle aprofundado de BO (`08_MODELO_CONFERENCIA_CONTROLE_BO.md`, v1.0)

**Princípio:** um BO não é uma linha — é um **procedimento**. Conferir = abrir e ler **TODOS** os documentos e **anexos** (Auto de Exibição e Apreensão, Termo de Declarações, despacho, laudos, fotos). "A tela-resumo do SPJ pode mentir; o documento manda." Modelo **não-econômico** (completude vence custo).

**Salvaguardas do modo "zerar e recadastrar" (inegociáveis):** 1. backup datado completo (`CARTORIO_CENTRAL_pre-rebuild_AAAA-MM-DD_HHMM.xlsx`); 2. exportar coluna U curada para `_colunaU_curada_AAAA-MM-DD.csv` (chave=Nº BO, reinjetada com OK); 3. zerar só por fase; 4. recadastro via fila + commit no HUB (nunca dois escritores); 5. fórmulas preservadas.

**8 dimensões do controle por BO:**
- **D1** Identificação → `BOs` B–J (todas as naturezas concomitantes).
- **D2** Pente-fino documental → `BOs` col. S (bloco `[Pente fino SPJ]`) + minuta col. U.
- **D3** Classificação e destino → árvore de decisão → aba de destino (`IPs`/`TCs`/`AIs`/arquivar/remeter). Ato infracional **nunca** vai para `IPs`.
- **D4** Procedimento, CNJ e despacho (com atualizações) → nº do IP sem sufixo `.1512`; reconsultar Histórico de Despacho.
- **D5** Custódia e rastreamento (CPP art. 158-A a 158-F) → abas próprias; caminho completo Entrada→Trânsito→Saída→Presença física; `[confirmar no físico]` só quando o destino documental já foi apurado e resta a presença no cofre.
- **D6** Perícias e laudos → aba `PERÍCIAS` (caçar em 4 lugares: Segunda Via SPTC + SPJ Documentos + SPJ Anexos + dentro do IP).
- **D7** Distribuição e livros → `IPs` col. O/R/P + livros obrigatórios (Registro de IPL / Carga aos escrivães).
- **D8** Prazos e correspondência → AGENDA + `CORRESP.`; reincidência → cruzar `PRONT.`.

**Fontes autorizadas para resolução ativa de dúvidas:** SPJ, IPe novo (SPJ), IPe antigo, Segunda Via de Laudos (SPTC). Fluxo de sub-lote: HUB faz backup + exporta col. U → satélite varre 10-20 BOs e monta pacote → HUB grava (backup → prévia célula a célula → confirmação → aplica) → anota livros + reinjeta col. U + CHANGELOG.

---

### 6. Diretrizes e padrão de formatação de documentos Word (`04_DIRETRIZES_DOCUMENTOS_WORD.md`, v1.0 + `PADRAO_FORMATACAO_DOCUMENTOS.md`)

**Pré-requisito absoluto:** brasão oficial da PC-SP (PNG fundo branco, ~600px). Sem brasão, **não gerar** — solicitar ao usuário. Biblioteca: `docx` (npm) ≥ 9.6.1; validar com `validate.py`; converter a PDF para preview; entregar via `present_files`.

**Página A4:** 11906 × 16838 DXA; margens superior 720, inferior/laterais 1134, header/footer 360 (1440 DXA = 1 pol.; cm × 567).

**Cabeçalho institucional (obrigatório, imutável):** tabela 2 colunas (1500 | 8706 DXA), borda inferior SINGLE 8 preto. Célula 1: brasão 70×90pt centralizado. Célula 2: borda esquerda SINGLE 6 preto + 5 linhas Arial: (1) "Secretaria de Segurança Pública" 10pt; (2) "POLÍCIA CIVIL DO ESTADO DE SÃO PAULO" 11pt **negrito**; (3) "DEPARTAMENTO DE POLÍCIA JUDICIÁRIA DO INTERIOR – DEINTER 1" 10pt; (4) "DELEGACIA SECCIONAL DE POLÍCIA DE GUARATINGUETÁ" 10pt; (5) "DELEGACIA DE POLÍCIA DO MUNICÍPIO DE APARECIDA" 10pt. `size` em half-points (20=10pt). Usar travessão `–` (U+2013), **nunca** hífen.

**Rodapé (obrigatório):** borda superior SINGLE 6 preto; L1 endereço; L2 "Telefone: (12) 3105-1650 – E-mail: dp.aparecida@policiacivil.sp.gov.br"; L3 "Página [CURRENT] de [TOTAL_PAGES]" — Arial 8pt, centralizado. *(Divergência preservada: `PADRAO_FORMATACAO` registra telefone (12) 3105-2333.)*

**Corpo:** fonte default **Liberation Serif 13pt**. Título 15pt negrito+sublinhado centralizado; rótulos 13pt negrito; corpo justificado, recuo 1ª linha 1134 DXA (2 cm), espaçamento 1,5 (line 360); data à direita; assinatura centralizada (nome negrito + cargo). **Ordem obrigatória do corpo:** espaçamento pós-cabeçalho → título → bloco de campos de referência → data → assunto (ofícios) → vocativo → corpo → fecho → assinatura → testemunhas (autos) → bloco destinatário (ofícios/CP).

**Autoridade assinante por documento:** Ofício/Pedido de Prazo/Cota Cumprida → Dr. Paulo Sergio Barbosa (Titular); Ordem de Serviço/Intimação → Dr. Leonardo da Costa Ferreira; Requisição IC → Delegado de plantão; Requisição IML → Declarante; Certidão → João Pedro (Escrivão); Autos (Avaliação/Reconhecimento) → Delegado + peritos/testemunhas + Escrivão.

**Regras invioláveis:** nunca gerar sem brasão; nunca alterar cabeçalho/rodapé; nunca hífen no lugar de travessão; nunca fonte diferente; sempre validar; jamais inventar dados (manter `[COLCHETES]`). O boilerplate `docx-js` traz `buildInstitutionalHeader/Footer`, `buildTitle/Field/BodyParagraph/Line/Signature` — só o `bodyChildren` varia entre os 13 documentos.

---

### 7. POP de triagem de e-mail e SOP de pedido de prazo

#### 7.1. POP de triagem de e-mail — dois regimes

**Regime detalhado (`POP_TRIAGEM_EMAIL.md`, v1.0):** frase-gatilho "Triagem de e-mail conforme POP" → resposta padronizada em 11 blocos (Classificação; campos universais; campos específicos; análise jurídico-cartorária; roteamento Pasta Outlook + Aba; roteamento coluna a coluna; flags de custódia; prazos com fundamento; checklist; sugestão de peça — só sugerir, nunca gerar sem comando; alertas). Campos universais: remetente (e-mail/órgão), data/hora, assunto, anexos, trecho-chave.

**12 tipologias e roteamento:**
| Tipo | Origem | Aba mestra | Pasta Outlook |
|---|---|---|---|
| T01 Cota Ministerial | MPSP/Vara | `COTAS` | 01-FÓRUM/01_Cotas |
| T02 Requisição Judicial | TJSP/Vara | `CORRESP.` | 01-FÓRUM/02_Requisições |
| T03 Carta Precatória | Outras Comarcas | `CPs` | 01-FÓRUM/03_CP a Cumprir |
| T04 Decisão MPU | Vara Maria da Penha | `MPUs` | 01-FÓRUM/05_MPU (URGENTE) |
| T05 Comunicação de IP | Outras DPs | `IPs`/`CORRESP.` | 03-INQUÉRITOS/01 |
| T06 Laudo IC | Polícia Científica | custódia (⚡) | 04-CUSTÓDIA/01 |
| T07 Laudo IML | IML | `IPs` (juntada) | 04-CUSTÓDIA/02 |
| T08 Denúncia/Notícia-Crime | Cidadão/181 | **NÃO CADASTRAR** (sigilo) → SIG | 02-INVESTIGAÇÕES/01 |
| T09 Localização/Captura | DPs/Polinter | **NÃO CADASTRAR** até cumprir | 02-INVESTIGAÇÕES/02 |
| T10 Seguradora | Seguradoras | `CORRESP.` | 05-EXTERNOS/03 |
| T11 Administrativo | Chefia/DGP | não vai à mestra | 06-GESTÃO |
| T12 Outros | Diverso | caso a caso | manter na caixa |

Regras de ouro: fidelidade (`N/C`); classificar antes de extrair; roteamento duplo (Outlook + Aba) por nome E letra; prazos com fundamento; sigilo de T08; sugerir peça com modelo `.docx`, nunca gerar sem comando.

**Regime vigente (`Procedimento_Padrao_Triagem_Email_DPM_Aparecida.md`, a partir de 09/06/2026):** o Cowork **deixou de ler/triar/mover e-mails no Outlook**. Novo fluxo: (1) João lê e separa; (2) envia `.eml` no chat (Cowork lê cabeçalhos/corpo/anexos, decodifica PDFs, SHA-256 se custódia); (3) Cowork pode abrir Outlook só para conferir; (4) Cowork prepara pacote em `_PARA_LANCAR_NA_MESTRA/pendentes/` (aba-alvo + NOVA×ENRIQUECE×CORRIGE), HUB grava. **Regras de movimentação:** denúncia Ligue 180 / Monitoramento de Apuração DEINTER / mandado de prisão / ofício de paradeiro / requisição para qualificar-localizar pessoa → mover para **SIG**, manter **NÃO LIDO**; permuta → **Arquivo Morto**; DDM ONLINE → simplesmente arquivar. Salvaguardas: não acessar links externos nem inserir chaves de acesso; nenhum envio externo sem confirmação (clique final é do usuário).

#### 7.2. SOP de pedido de dilação de prazo (`SOP_PEDIDO_DE_PRAZO.md`, v2.0)

**Fundamento:** art. 10, *caput* e §3º, do CPP; Lei 12.830/13; Consolidação DGP-26/2023. **Sistema:** IPe antigo (`inquerito.policiacivil.sp.gov.br/inquerito/`). **Gatilho:** pedir prazo para **tudo que está "vermelho"** (linha vermelha = "Data Prevista p/ Conclusão" vencida; branca = no prazo). Reconcilia a regra de 17/06 (`>30 dias sem movimentação`). Réu preso/relatado não aparecem vermelhos (tratamento próprio — art. 10, 10 dias). Abas a trabalhar: **Em Cartório** e **Cotas**.

**Criar o pedido (por procedimento, sem assinar):** abrir vermelho → Procedimento ▸ Documentos → "Criar Documento a Partir de Modelo" → filtrar "prazo" → **"DESPACHO PRAZO"** → manter Inquérito marcado → **Integrantes: marcar apenas Paulo Sergio Barbosa (DELEGADO) + João Pedro (ESCRIVAO)** → Utilizar → nome do documento "PEDIDO DE PRAZO" → Salvar. Texto genérico já pronto (art. 10 §3º CPP), sem diligência específica.

**Assinar e enviar — SOMENTE o João (agente nunca assina nem digita senha):** Assinatura Digital ▸ Pendentes ▸ "Assinar Documento(s)" (senha pessoal, fila acumula → assinar em bloco). Enviar TJ (ícone martelo) ▸ "Complementar Procedimento TJ" → 🔴 selecionar **exatamente `Pedido de Prazo`** (não `Pedido Exclusivo de Dilação`, nem `com Diligência`) → gera protocolo de Envio TJ.

**Regra do martelo (checkpoint):** procedimento cuja barra começa em "Pasta Digital TJ" (sem martelo) → **PULAR e anotar** em `PROCEDIMENTOS_SEM_ENVIAR_TJ_A_CONFERIR.md`. **Mapa de rosters** (marcar Paulo + João): Cartório 06 Bianca/05 José Carlos = pág. 1 linhas 1 e 4; Cartório 07 Milton = pág. 1 linhas 1 e **2**; Cartório 01 Plantão = Paulo pág. 2, João pág. 5. Armadilhas: tipo de petição errado; ordenação da lista reseta ao voltar; criar/salvar não remove o vermelho (só sai quando João assina+envia — rastrear por nº); IP com Carta Precatória exige selecionar Associação IP antes dos integrantes.

---

### 8. Catálogo dos modelos de peças (`modelos/`, 00–12)

Todos partem do mesmo **cabeçalho institucional** (tabela brasão + texto SSP → PCSP → DEINTER 1 → Seccional Guaratinguetá → DPM Aparecida) e rodapé com paginação. Formatação conforme §6. O placeholder de dado ausente é `[COLCHETES]`.

| Nº | Modelo | Título | Campos de referência | Fecho / assinatura | Fundamento / regra |
|---|---|---|---|---|---|
| **00** | Modelo Padrão Universal | `[TÍTULO DO DOCUMENTO]` | IP, BO, Natureza, Vítima(s), Investigado(s) | fecho variável; assinatura conforme o caso | Base para qualquer peça sem modelo próprio; traz guia de formatação (remover 2ª página ao usar) |
| **01** | Pedido de Dilação de Prazo | `PEDIDO DE DILAÇÃO DE PRAZO` + subtítulo `DESPACHO` | IP, Natureza, Vítima(s), Investigado(s) | "Cumpra-se." / Delegado Titular | **art. 10º, §3º, CPP.** Texto fechado/genérico. Modelo oficial = `MODELO_PEDIDO_DE_PRAZO_PADRAO.pdf`; via IPe = modelo nativo "DESPACHO PRAZO" |
| **02** | Ofício | `Ofício nº [N]/2026 – Delpol Aparecida` | IP, Processo CNJ, RDO | "Aproveito... / Atenciosamente," / Delegado Titular + bloco destinatário | Assunto e vocativo obrigatórios (Excelentíssimo/Ilustríssimo conforme destinatário) |
| **03** | Ordem de Serviço | `ORDEM DE SERVIÇO Nº ____/2026` + `NATUREZA DA INVESTIGAÇÃO` | IP, BO, Natureza, Vítima(s), Investigado(s) | "Sr. Policial Civil, proceda..." / **Leonardo da Costa Ferreira** | Determina diligência investigativa; anexa BO e peças |
| **04** | Intimação | `INTIMAÇÃO` + `INTIMAÇÃO Nº ____/2026` | Para, Endereço, BO, IP | de ordem de Leonardo da Costa Ferreira; assinada pelo Escrivão | **art. 330 do CP (Desobediência).** Linha de ciência: "RECEBI ESTA INTIMAÇÃO EM __/__/__ + CIENTE:". "Não damos informações por telefone" |
| **05** | Auto de Avaliação Indireta | `AUTO DE AVALIAÇÃO INDIRETA` | abertura "Aos [DIA] dias do mês de [MÊS]..." | Delegado + 1º Perito + 2º Perito + Escrivão | Compromisso formal dos peritos + descrição do objeto avaliado |
| **06** | Requisição IC | `REQUISIÇÃO IC-[TIPO]` | dest. Diretor do Instituto de Criminalística; BO, Naturezas, Local, Circunscrição, datas, Objetos | Delegado(a) de plantão | Quesitos: `intra.policiacivil.sp.gov.br/.../quesitos_PJ-1.pdf`; "O laudo deverá ser enviado a: DEL.POL.APARECIDA" |
| **07** | Requisição IML-Pessoa | `REQUISIÇÃO IML-PESSOA` | dest. Diretor do IML; Passou pelo P.S.?, BO, Flagrante, DADOS DA PESSOA | **Declarante** (não o Delegado) | Cláusula de autorização de divulgação de prontuário médico p/ exame de corpo de delito |
| **08** | Certidão | `CERTIDÃO` | abertura "Eu, João Pedro... Escrivão de Polícia de 3ª Classe..." | "O referido é verdade e dou fé." / **JOÃO PEDRO** (Escrivão) | "CERTIFICO que [...]" |
| **09** | Cota Cumprida | `COTA CUMPRIDA` | IP, Processo CNJ; vocativo "MM. Juiz," | "Respeitosamente," / Delegado Titular | Referência à cota ministerial (fls.) + juntada + "retornem os autos ao Ministério Público" |
| **10** | Carta Precatória | `CARTA PRECATÓRIA DISTRIBUÍDA` | Inquérito, Dependência, CP nº, Deprecante, Deprecada | Delegado(a) | Fórmula "FAZ SABER... DEPRECA a Vossa Excelência"; fecho **ASSIM O DEPRECA / REGISTRA-SE e CUMPRA-SE / PRAZO: [N] dias** |
| **11** | Auto de Reconhecimento de Pessoa | `AUTO DE RECONHECIMENTO DE PESSOA` | abertura "Aos [DIA] dias..." | Delegado + 2 Testemunhas + Reconhecedor + Escrivão | **CPP art. 226** (procedimento de reconhecimento; cf. HC 598.886/SC do STJ) |
| **12** | Auto de Reconhecimento de Objeto | `AUTO DE RECONHECIMENTO DE OBJETO` | idem, substituindo pessoa por objeto | Delegado + 2 Testemunhas + Reconhecedor + Escrivão | Estrutura idêntica ao 11, objeto entre coisas semelhantes |

*Modelos auxiliares na pasta: `MODELO_PEDIDO_DE_PRAZO_PADRAO.pdf` e `PEDIDO_DE_PRAZO_PADRAO_OFICIAL_2026-06-18.pdf` (PDF timbrado padrão para todos os procedimentos de prazo).*

> **Anomalias preservadas (do próprio SOP):** (1) o `POP_TRIAGEM_EMAIL` v1.0 usa nomes longos das abas (planilha de 20 abas) — desatualizado frente à mestra v2.1 (23 abas, nomes curtos); prevalece a v2.1. (2) Delegado Titular registrado = Dr. Paulo Sergio Barbosa, mas a Produção de abril/26 foi assinada por Dr. Ernani Ronaldo Giannelli (confirmar o vigente a cada estatística). (3) Telefone institucional diverge entre fontes (3105-1650 × 3105-2333).

---

## PARTE III — Módulos Investigativos (Triagem, Histórico e Análise de BO; Análise de Inquéritos)

> Contexto permanente: DPM Aparecida/SP (cód. 1512 — DEINTER 1 / Seccional Guaratinguetá). Tom impessoal, técnico-jurídico. Terminologia precisa (Indiciado × Autor; Vítima × Ofendido). Regra transversal: **dado faltante → `[INSERIR DADO]` ou `N/C`; nunca inventar** dados, leis ou fatos. Decisão final é sempre do Escrivão-Chefe/Delegado (art. 2º, §6º, Lei 12.830/13). Sigilo funcional (Lei 12.830/13, art. 25) e finalidade (LGPD, art. 6º); CPF/RG redigidos; autos sob segredo de justiça: registrar a existência, tratar com sigilo, sem expor conteúdo protegido.

---

### 1. TRIAGEM DE BO EM LOTE — ÁRVORE DE DECISÃO

Cobre a **decisão de destino** dos BOs (IPL/IPS/TCO/NECRIM/arquivamento/remessa). O lançamento na planilha após a decisão pertence ao módulo GCC. Para cada BO da pilha determinar: há tipicidade e qual; cabe IPL, IPS, TCO, NECRIM, arquivamento ou remessa; há prazo crítico (decadência/prescrição/dilação); há flagrante (que muda o tratamento para APFD).

#### 1.1 Árvore de decisão

```
BO ingressado na unidade
│
├── É infração penal? (Há tipicidade?)
│   ├── NÃO → Arquivar (Livro IV)
│   └── SIM →
│       │
│       ├── Pena máxima ≤ 2 anos (IMPO — art. 61, L. 9.099/95)?
│       │   ├── SIM, Autor conhecido e presente → TCO
│       │   ├── SIM, Autor ausente/desconhecido → NECRIM / IPS
│       │   └── SIM, Violência doméstica (Lei 11.340/06, Súmula 536 STJ)
│       │            → NÃO cabe JECRIM → IPL
│       │
│       ├── Pena máxima > 2 anos?
│       │   ├── Justa causa fundamentada (indícios mínimos de
│       │   │   autoria e materialidade)?
│       │   │   ├── SIM → IPL (portaria inaugural)
│       │   │   └── NÃO → IPS (despacho; até 60+30 dias)
│       │   └── Flagrante? → APFD (independente de decisão anterior)
│       │
│       └── Hipóteses especiais:
│           ├── ECA (adolescente infrator) → procedimento próprio
│           ├── Crime militar → remeter à JM
│           ├── Crime federal → remeter à PF
│           └── Prerrogativa de função → remeter ao juízo competente
```

#### 1.2 Checklist rápido por BO

| Item | Observação |
|---|---|
| Tipificação correta | Checar subsunção. BO inicial costuma trazer tipificação provisória. |
| Competência | PC/SP? Federal? Militar? JECRIM? |
| Autor identificado? | Muda o destino (TCO só com autor conhecido e presente). |
| Vítima quer representar? | Ação penal pública condicionada (estelionato pós-13.964/19; ameaça; lesão leve). Sem representação → arquivar. |
| Flagrante? | Se sim, não é "destino do BO", é APFD — prioridade absoluta. |
| Violência doméstica (Lei 11.340/06)? | Súmula 536 STJ — não cabe JECRIM mesmo com pena ≤ 2. IPL direto. |
| Prescrição consumada? | Arquivar — extinção da punibilidade. |
| Fato insignificante? | Princípio da insignificância — verificar jurisprudência; se claramente incidente, sugerir arquivamento. |

#### 1.3 Output padrão — triagem em lote

Tabela de decisão em série (uma linha por BO): `Nº BO · Data fato · Tipificação proposta · Autor? · Vítima representou? · Destino sugerido · Prazo crítico · Observação`. Destino **IPL/IPS** → acionar módulo Portaria. Lançamento na mestra → módulo GCC.

#### 1.4 Pontos de atenção (jurisprudência e legislação)

- **Violência doméstica:** Súmula 536 STJ exclui JECRIM (não cabe TCO em VD mesmo com pena ≤ 2 anos); IPL ou medidas protetivas (Lei 11.340/06). **Não existe "crime de violência doméstica"** como tipo autônomo (única exceção: descumprimento de MPU — art. 24-A da Lei 11.340/06). VD é **contexto** vinculado ao crime material: lesão corporal (art. 129, §9º, CP, c/c Lei 11.340/06); ameaça (art. 147 CP c/c Lei 11.340/06).
- **Estelionato:** Lei 13.964/19 alterou o art. 171 do CP — ação penal pública **condicionada à representação**. Sem representação, arquivar. Prazo de 6 meses do conhecimento da autoria (art. 103 CP).
- **Porte para consumo (art. 28 da Lei 11.343/06):** não é hipótese de APFD (art. 48, §§ 2º e 3º da Lei); TCO ou procedimento específico. Acompanhar o RE 635.659/STF.
- **Insignificância (STF, critérios cumulativos):** (1) mínima ofensividade; (2) ausência de periculosidade social; (3) reduzido grau de reprovabilidade; (4) inexpressividade da lesão jurídica. Reincidente habitual, pela jurisprudência majoritária, não se beneficia.
- **Ação penal pública condicionada:** prazo decadencial de 6 meses do conhecimento da autoria (art. 103 CP).
- **Crimes contra a honra:** calúnia, difamação, injúria — em regra ação penal privada (queixa-crime); a PC não instaura IPL, orienta a vítima a advogado. Exceções: contra funcionário público em razão da função (representação) e racial/preconceito (Lei 7.716/89, ação pública incondicionada).

#### 1.5 Output consolidado de fim de ciclo

Resumo por data: BOs triados (N); instaurados IPL / IPS / encaminhados TCO-NECRIM / arquivados / remetidos; **Alertas** (reincidências pelo cruzamento com PRONT.; prazo crítico de prescrição/decadência; indício de organização criminosa por coautoria recorrente; VDs sem MPU); próximas peças a produzir; pendências escaladas ao Delegado Titular.

---

### 2. ELABORAÇÃO DE HISTÓRICO DE BO E PEÇAS CORRELATAS

Padrão é redigir o BO "do zero"; ao notar versão finalizada, seguir o rito de **complemento** (2.4). **SEMPRE perguntar a fase antes de redigir.** Regras de ouro: dado faltante → `[INSERIR DADO]` (nunca inventar); **nunca alterar as "Frases de Início Obrigatório"**; "veículo apreendido" = tratar como já no sistema; "drogas" = assumir necessidade de laudo químico.

#### 2.1 Redação do campo Histórico

Texto **impessoal, técnico-jurídico, cronológico, sem tópicos**, unindo as narrativas em relato coeso. Detalhar **lesões** (natureza/local), **danos** (o quê/valor) e **objetos** (descrição + destino/lacre). Não emitir juízo de valor.

**Frases de início obrigatório (NUNCA alterar):**
| Cenário | Abertura |
|---|---|
| **BO comum** | "Comparece a este plantão policial, [Nome], informando que..." |
| **Flagrante (APFD)** | "Comparece a este plantão policial, o Condutor [Nome]..." — narrar Patrulhamento → Abordagem → Prisão → Delegacia |
| **Captura de procurado** | Base no mandado de prisão (ver 2.3) |

**Estrutura:** (1) abertura obrigatória + qualificação sumária; (2) dinâmica cronológica; (3) detalhamento de lesões/danos/objetos; (4) providências do plantão; (5) orientações por crime (2.6); em APFD, orientações + **despacho da autoridade**.

#### 2.2 Lavratura de APFD (CPP arts. 301–310; Portaria DGP-26/2023)

**Cronologia (histórico do condutor):** Patrulhamento (motivo/ROTA) → Abordagem (fundada suspeita/denúncia) → Prisão (conduta flagrancial, **art. 302 CPP**) → Apresentação na Delegacia.

**Sequência do auto:** 1. oitiva do **Condutor**; 2. **Testemunhas** (mínimo duas; senão, de apresentação); 3. **Vítima** (se houver); 4. **Interrogatório** com aviso de direitos (art. 5º, LXIII, CF; silêncio); 5. **Despacho:** homologa/relaxa; **fiança** (arts. 322/323 CPP); comunicações (Juiz, MP, DP, família/advogado — **art. 306 CPP**); **audiência de custódia**. Armas/drogas/objetos → lacre + guia de perícia + abas de custódia. **Nota de culpa** ao preso; APF comunicado em **24h**; réu preso = IP em **10 dias** (art. 10 CPP).

#### 2.3 Captura de Procurado (cumprimento de mandado)

Gera **histórico** + **texto do mandado cumprido**. Fonte = o mandado apresentado (dados do capturado, processo/CNJ, juízo, tipo — preventiva/temporária/definitiva, validade). **Histórico:** origem da informação → abordagem → **conferência da identidade** e do mandado → voz de prisão → condução → comunicações. **Texto do mandado cumprido:** nº do mandado e processo (CNJ); juízo; nome/qualificação; data/hora/local; autoridade que cumpriu; destino do preso; comunicação ao juízo. **Confirmar mandado ATIVO** antes de consignar; seguir fielmente, não presumir.

#### 2.4 Complemento / Retificação de BO (segunda versão)

**Frases obrigatórias (NUNCA alterar):** Início "Versão elaborada para acrescentar/alterar..."; Fechamento "Nada mais, sendo a presente versão elaborada para [resumo das alterações]". **Conteúdo:** (1) início; (2) **justificativa técnica** do motivo; (3) o aditamento/correção impessoal; (4) fechamento com resumo. **Casos típicos:** retirada de queixa/representação; deslacração/relacração; correção de local; alteração de natureza (ex.: homicídio doloso); reclassificação (armas de pressão); devolução de veículo/objeto; erro material em lacres.

#### 2.5 Análise e Perícias — Checklist ("PONTOS DE ATENÇÃO E REQUISIÇÕES")

Para cada gatilho, **perguntar** se a requisição já foi expedida: sim → juntar o laudo; não e vital → gerar a **minuta**.

| Se houver... | Requisitar | Destino |
|---|---|---|
| **Lesão corporal** | **IML** (corpo de delito) | IML |
| **Arrombamento / local / dano** | **IC-Local** | IC |
| **Drogas** | **IC-Constatação** + laudo químico definitivo | IC |
| **Arma de fogo** | **IC** (eficiência/procedência); conferir numeração | IC |
| **Veículo / adulteração de sinal** | **IC** (identificação veicular) | IC |
| **Objeto p/ avaliação** | Auto de Avaliação (direta/indireta) | Cartório |

**Regra de ouro:** não requisitar perícia nova não pedida no BO (salvo urgência); a regra é **juntar os laudos das requisições já expedidas**. Registrar em `PERÍCIAS`/custódia + protocolo de objetos quando houver apreensão.

#### 2.6 Orientações Dinâmicas de BO (por natureza)

| Natureza | Orientações |
|---|---|
| **Lesão / VD** | IML; verificar **MPU** (Lei 11.340/06); juntar antecedentes + outros BOs das partes; vincular ao crime material. |
| **Furto/Roubo** | *res furtiva* e valor; recuperação; CFTV; qualificadoras (art. 155 §4º / 157 §2º CP). |
| **Dano** | IC-Local; Auto de Avaliação Indireta. |
| **Drogas (Lei 11.343/06)** | IC-Constatação + laudo definitivo; custódia por lacre; tráfico × uso. |
| **Arma de fogo (Lei 10.826/03)** | IC de eficiência; alertar **numeração suprimida**; custódia. |
| **Estelionato (art. 171 CP)** | Representação (§5º); documentar o meio fraudulento. |
| **Ameaça (art. 147 CP)** | Representação; contexto de VD. |
| **Homicídio / morte suspeita** | IML necroscópico; IC de local; **Portaria DGP-14/2005**; circunscrição. |
| **Vulneráveis (criança/adolescente)** | Escuta especializada (**Lei 13.431/17**); Conselho Tutelar/CREAS. |

---

### 3. ANÁLISE E CONFERÊNCIA DE INQUÉRITOS POLICIAIS

#### 3.1 Análise/Triagem de IP — Máquina de dois estados

Persona: Escrivão sênior e Analista de Inteligência Policial. **Nunca** executar o Estado 2 sem comando explícito.

**ESTADO 1 — ANÁLISE E TRIAGEM** (gatilho: documento ou `/analisar`). Estrutura obrigatória: 1. **Resumo Fático e Tipificação** (natureza, subsunção preliminar, circunstâncias); 2. **Síntese de Oitivas e Provas Documentais**; 3. **Controle de Diligências (Cumpridas e Pendentes/Importantes)** — dois tópicos distintos; para cada pendente, informar a **ORIGEM** (Portaria / Despacho / Cota MP / Lógica Investigativa); 4. **Menu de Diligências (checklist numerado)**; 5. **PAUSA OBRIGATÓRIA** — encerrar com "Quais itens do Menu de Diligências o senhor deseja expedir? (Responda com o número do item ou '/executar tudo')".

**ESTADO 2 — EXECUÇÃO** (gatilho `/item [N]` ou `/executar tudo`): buscar o **modelo exato** da peça; preencher com os dados do Estado 1; peças múltiplas separadas por `---`; lacuna → `[DADOS NÃO INFORMADOS]`.

#### 3.2 Modelo de Conferência de Inquérito (chat)

Espelho do Modelo de Resumo Investigativo de BO (v2.0), aplicado ao acervo de IPs. Confere andamentos em **dois sistemas (IPe + e-SAJ, pelo CNJ)**, cruza com a mestra. **Critério João:** existe **Relatório Final** nas peças → **cota**; não existe → **inquérito**. O documento manda, não o status do sistema. Ausente = `N/C`. Convenção: `📄` peça/auto · `⚖️` andamento e-SAJ · `🖥` tela/status IPe · `❔` a confirmar.

**§0. TRIAGEM PRIORITÁRIA** — marcar 🔴 quando: indiciado **preso** (10 dias, art. 10 CPP); **prescrição iminente** (art. 109 CP); vítima/autor **vulnerável** (ECA; Lei 10.741/03; Lei 11.340/06; Lei 13.146/15); **determinação judicial/MP com prazo vencido**.

**As 8 seções:** 1. Identificação & cadastro (campos da aba `IPs`); 2. Situação processual — auditoria cruzada IPe × e-SAJ × mestra (apontar divergências; cota × inquérito); 3. Prazos & Prescrição; 4. Diligências cumpridas × pendentes (com ORIGEM); 5. Cadeia de custódia & perícias; 6. Distribuição & livros; 7. Menu de diligências (numerado); 8. Pendências/decisões para o Escrivão-Chefe + Inteligência. **Rodapé:** tags correição/estatística.

**Regras da conferência:**
- **A — Auditoria cruzada** (IPe × e-SAJ × mestra): fonte de verdade = peças/autos; e-SAJ pelo CNJ; registrar divergência e propor correção; sem CNJ → pendência.
- **B — Prazos & Prescrição:**

| Situação | Prazo | Base |
|---|---|---|
| IP com **indiciado preso** | **10 dias improrrogáveis** | art. 10 CPP |
| IP com **indiciado solto** | **30 dias** + prorrogações | art. 10 CPP; DGP-26 |
| **IPS** | **60 + 30 dias** | DGP-26/23 |
| **Cota/diligência do MP / decisão judicial** | prazo fixado | despacho/cota |
| **Prescrição** | pena máxima → art. 109 CP (termo inicial 111; suspensivas/interruptivas 116/117; reduções 115 — < 21 ou > 70) | arts. 109–117 CP |

  Sinalizar 🔴: preso; parado além do prazo; **prescrição a < 12 meses**.
- **C — Proatividade + cruzamento:** resolver dúvidas ativamente (IPe peças + e-SAJ + Segunda Via/SPTC); ao Chefe só o que o sistema não responde; cruzar indiciado/vítima/CNJ/BO contra `IPs`/`BOs`/`MPUs`/`AIs` e roster; consolidar por escrivão os IPs com pendência.
- **D — Tags correição/estatística:** classe · preso S/N · prazo crítico S/N + data · prescrição (ano-limite) · última movimentação · escrivão · vara/CNJ.
- **E — Persistência + merge na aba `IPs`:** persistir em `projeto-conferencia-inqueritos/conferencias/<ANO>_IP-<nº>.md`; merge por **IP nº + Ano** (inexistente → nova linha preservando fórmula col A; existente → enriquece só vazios; Observação preserva trecho humano; curadoria intocável; status/escrivão/tipo validados contra `LISTAS`); só o **HUB grava**; pacote marca NOVA × ENRIQUECE × CORRIGE.
- **F — Fonte única:** conferência no chat e pacote nascem do mesmo objeto extraído.
- **G — Campos obrigatórios da correição:** a conferência reúne todos os campos da correição; camada investigativa por cima.
- **H — Nº de Prontuário (Relatado):** número que o procedimento ganha **quando é relatado**; só existe para relatados; ausente = vazio, nunca inventar; fonte primária = caderno do escrivão anterior.

**Boas práticas:** não usar o Status do IPe como atalho (Pasta Digital → Ordenar Peças, rolar até o fim); e-SAJ complementa o IPe; IPe usa frameset (travou → F5 e relocalizar o frame); procedimentos de outra unidade tratar à parte.

#### 3.3 Correição 2026 — Estrutura Obrigatória

Organiza os procedimentos em **quatro quadrantes** por **escrivão contável** (Bianca, José Carlos, Milton), + Cartas Precatórias e Roteiro da unidade. João Pedro = Chefe, **não conta**.

| Eixo | Valores |
|---|---|
| **Suporte** | **Eletrônico** (digital/IPe) × **Físico** (papel) |
| **Local** | **Em Cartório** × **No Fórum** |
| **Tipo** | IP · TC · AI (e CP à parte) |
| **Situação** | *Em Cartório* → **CARTÓRIO/COTA** · *No Fórum* → **PRAZO/COTA** (cota = tem Relatório Final) |

Cada aba: cabeçalho **UNIDADE POLICIAL · ESCRIVÃO · DELEGADO**.

**Colunas obrigatórias por tipo:** IP eletrônico — `Nº IP(e)` · `Nº IP CONTROLE` · `ANO IP` · `NATUREZA` · `VÍTIMA` · `AVERIGUADO/INDICIADO` · `CARTÓRIO/COTA`(ou `PRAZO/COTA`) · `FÓRMULA`. IP físico: sem Nº Controle/Ano. TC eletrônico/físico: `AUTOR` no lugar de indiciado. AI: `ADOLESCENTE INFRATOR`. CP: `CP Nº (UNIDADE)` · `CP Nº (ORIGEM)` · `DATA ENTRADA` · `UNIDADE ORIGEM` · `REFERÊNCIA (IP/TC/AI/BO)` · `FÓRMULA`. `FÓRMULA` = coluna **auto** (concatenação p/ conferência), não digitada.

**Roteiro da unidade** (`ROTEIRO CORREIÇÃO - 2026.xlsx`): abas administrativas — `DADOS GERAIS`, `EQUIP. INFORMÁTICA`, `BENS E UTENSÍLIOS`, `ESTOQUE`, `PROTOCOLADOS`, `VEÍCULOS APREENDIDOS` (cruza com a aba `VEÍC.`).

**Controle da conferência = fonte única** (superset: campos da correição + `CNJ`, `Andamento_eSAJ`, `Prazo_prescricao`, `Diligencias_pendentes`, `Distribuicao_livro`, `Vulneravel`, `Custodia_pericias`, `Observacao_investigativa`). Mapeia para a aba `IPs` e as demais. **Entrega final:** por escrivão, preencher os formulários em branco (`modelos_correicao/DPM APARECIDA/...`) nos 4 quadrantes + CPs.

#### 3.4 Geração de peças no Estado 2

**Ordem de Serviço ao SIG** — quando a elucidação depende de diligência de campo. Estrutura: cabeçalho (DP, nº IP/BO, CNJ, Delegado) → determinação "Expeça-se Ordem de Serviço ao SIG para..." com objeto vital → detalhamento telegráfico → prazo/retorno → data/assinatura. Só diligências **vitais**, vinculando cada uma à sua **origem**.

**Ofício (máscara):** `Ofício nº [N]/2026 – Delpol Aparecida` + `IP nº` + `Processo CNJ nº` + `RDO nº` + data + `Assunto:` + vocativo por destinatário (Excelentíssimo Juízes/Promotores; Ilustríssimo Delegados/Peritos; Senhor(a) civis) + corpo (1º parágrafo direto, 2º detalhamento) + fecho "Aproveito... / Atenciosamente," + Delegado Titular + bloco destinatário. Registrar na aba `CORRESP.`. Caixa: `dp.aparecida@policiacivil.sp.gov.br`.

**Intimação:** intimado + endereço; nº IP/BO/CNJ; **data, hora e local**; finalidade; advertência de condução coercitiva quando cabível; autoridade e data.

**Requisições de perícia:** IML (pessoa) — corpo de delito, quesitos por lesão; IC (objeto/local/arma/veículo/constatação de droga). Regra: só o **vital**; se já expedida, apenas **juntar o laudo**.

---

### 4. ANÁLISE APROFUNDADA DE BO (sob demanda — SPJ/PC-SP)

Skill investigativa **sob demanda** que abre TODAS as peças do BO, produz análise completa e — **só sob comando** ("consolida na planilha") — grava síntese densa na coluna de Análise Aprofundada da aba `BOs`. **Não lança nada automaticamente.** Rodar em Opus. Gatilhos: "analisa o BO X a fundo", "análise completa dos BOs do dia".

> ⚠️ **Canônico:** para o resumo investigativo de BO, o documento vigente e mais completo é o **Modelo de Resumo Investigativo (v2.0)** (§4.5). O Protocolo de Análise Aprofundada (v2.0) permanece como referência do fluxo de 13 blocos.

#### 4.1 Fonte das peças — Modo híbrido

| # | Fonte | Origem | Cobre | Quando |
|---|---|---|---|---|
| **A** | **PDF consolidado baixado** | `projeto-download-bos\downloads\AAAA-MM-DD\BO-...pdf` | Cabeçalho, histórico, partes, naturezas, objetos/armas/drogas/veículos | **Sempre primeiro** (offline, SHA-256) |
| **B** | **SPJ ao vivo (Claude in Chrome)** | `spj.ipe-policiacivil.sp.gov.br/boletins-ocorrencias/list` | Documentos anexos (autos, oitivas, requisições, APFD, nota de culpa), Histórico de Despacho, Extrato de Alterações | Quando faltar peça ou conferir a edição vigente |

Registrar a fonte (`[PDF]`/`[SPJ]`); ausente em ambas → `N/C`. A **edição vigente governa**.

#### 4.2 Passo 1 — Varredura total das peças

SPJ: **Detalhar BO** (Histórico, Pessoa Física/Jurídica, Naturezas, Cargas, Objetos, Entorpecentes, Veículos, Armas, Vídeos/Áudios); **Documentos** (Auto de Exibição e Apreensão; Auto de Arrecadação; Auto de Entrega; APFD; Nota de Culpa/Recibo de Entrega de Preso — art. 304 CPP; Requisições IC/IML → sempre à aba `PERÍCIAS`; Termo de Oitiva → síntese; Extrato de Qualificação, Certidões, Ofícios); **Histórico de Despacho**; **Extrato de Alterações BO**.

#### 4.3 Passo 2 — Análise nos 13 blocos + Apontamentos

| Bloco | Conteúdo |
|---|---|
| 1. Identificação | BO nº/ano, edições, procedimento/CNJ, circunscrição, data/hora, despacho/solução. |
| 2. Local e circunstâncias | Endereço, tipo de local, contexto, horário, condições (luz, câmeras). |
| 3. Vítima(s) | Qualificação, vínculo, lesões/prejuízo, vulnerabilidades (Lei 10.741/03; ECA; Lei 11.340/06; MPU). |
| 4. Autor(es)/indiciado(s) | Qualificação, antecedentes, papel, autoria conhecida/desconhecida, preso/solto/foragido. |
| 5. Dinâmica / modus operandi | Meios, instrumentos, abordagem, fuga, divisão de tarefas, indícios de reiteração/organização. |
| 6. Apreensões e cadeia de custódia | Tabela item · lacre · natureza · destino · aba. Alertas (numeração suprimida, chassi/placa adulterados, droga sem laudo, divergência de quantidade). |
| 7. Prova oral | O que cada vítima/testemunha/indiciado/condutor declarou — convergências e contradições. |
| 8. Elementos de prova / materialidade | Vídeos, imagens, laudos pendentes, documentos, perícias requisitadas (cruzar `PERÍCIAS`). |
| 9. Tipificação | Enquadramento com **citação dupla** (federal + Consolidação DGP-26/23); qualificadoras, concurso, competência. |
| 10. Linhas de investigação | Oitivas faltantes; representações (busca e apreensão, preventiva/temporária, quebra de sigilo); requisições IC/IML; reconhecimento (art. 226 CPP); vinculação a outros casos. |
| 11. Pendências | Laudos; oitivas; peças a juntar; prazos (risco prescricional — art. 109 CP). |
| 12. Inconsistências / alertas | Divergências BO × autos; erros de endereçamento; circunscrição diversa (BO de fora → remessa); atrasos; edições conflitantes. |
| 13. Conexões | Ligação com outros BOs/IPs/indiciados (mesmos nomes, lacres, locais, modus). |

Encerrar com **★ APONTAMENTOS DO ANALISTA** (3–6 conclusões acionáveis). Síntese para a coluna de Análise Aprofundada (só sob comando): Local · Modus operandi · Autor · Vítima · Apreensões/lacres · Tipificação · Linhas de investigação/pendências · Alertas.

#### 4.4 Lote diário e consolidação

**Lote diário:** listar PDFs (deduplicado); triagem rápida (nº · natureza · circunscrição · flagrante · prioridade; BO de fora → remessa); rodar Passos 1–2 para os da circunscrição (DELPOLAPARECIDA); índice no topo + análises; **não** lançar. **Consolidar** (só sob comando): backup pré-edição → localizar linha por **B (Nº BO) + C (Ano)** → preencher a coluna de Análise Aprofundada → análise longa vai à parte (`.docx`/`.md` em `04_PRODUTOS\Aguardando_Revisao\`) → custódia/perícia às abas próprias → registrar no `CHANGELOG`.

> **Nota de layout (divergência RESOLVIDA em 07/07/2026):** o Protocolo de Análise Aprofundada (v2.0, 30/05) apontava a Análise Aprofundada na **coluna W** com mapa que incluía F=Nº Controle; o Modelo de Resumo Investigativo (v2.0, 07/06) registra o layout **v2.1** sem Nº Controle, com a Análise Aprofundada na **coluna U**. **Conferido no cabeçalho real (L4) do arquivo em 07/07/2026: vale o v2.1 — bandeiras K–Q, R Despacho, S Observação, T Flagrante, U Análise Aprofundada (intocável, curadoria manual).** A regra permanece: **o arquivo manda** — reconferir o cabeçalho antes de gravar.

#### 4.5 Modelo de Resumo Investigativo de BO (v2.0) — estrutura

**Obrigatório para TODO BO** (07/06/2026); "modo resumido" vedado. Não transcreve o BO: vai atrás do que falta (SPJ, IPe novo/antigo, Segunda Via/SPTC) e cruza com o acervo. **Regra-mãe:** leitura íntegra do BO + TODOS os documentos e anexos; imagens sensíveis (sobretudo de criança/adolescente) **NUNCA** abertas/descritas — só registrar a existência e preservação (CPP 158-A; ECA). Ausente = N/C. **A tela-resumo do SPJ mente** — idade da vítima, destino do objeto e tipificação real só nos autos e oitivas.

**§0. TRIAGEM DE VULNERABILIDADE** (1ª passada): havendo vulnerável, 🔴 no cabeçalho, levar ao Delegado de imediato e disparar comunicações:

| Gatilho | Roteamento | Comunicações | Base |
|---|---|---|---|
| **Criança/adolescente** | vítima → IP prioritário + escuta especializada; autor → **ato infracional** (`AIs`), nunca `IPs` | Conselho Tutelar + MP; abuso sexual infantil → **preservar sem abrir** | ECA (Lei 8.069/90) arts. 241-A/B/D; Lei 13.431/17 |
| **Mulher em VD** | `MPUs` + `IPs`; Formulário de Risco | **MPU ao Judiciário em 48h**; comunicar a vítima | Lei 11.340/06 (art. 12, III); DGP-26/23 |
| **Idoso (≥60)** | IP/registro + encaminhamento | rede de proteção; MP se maus-tratos/abandono | Lei 10.741/03 |
| **Pessoa com deficiência** | atenção à hipossuficiência na prova | apoio adequado; MP se exploração | Lei 13.146/15 (LBI) |

**As 10 seções:** 1. Classificação e procedimento (NOSSO × FORA por `idDelegaciaInquerito` + Local do Fato; IP/IPS/TC/APFD/AI e CNJ; VD S/N pelas naturezas/autos, **nunca** pelo `flagViolenciaDomestica` do JSON); 2. Partes (VD/vulnerável → iniciais); 3. Os fatos (relato integral); 4. O que as pessoas disseram (CADA oitiva — coração do resumo); 5. Apreensão e destino (Regra A); 6. Perícias e laudos; 7. Documentos e anexos; 8. Enquadramento e diligências (citação dupla); 9. Prazos & Prescrição (Regra B); 10. Pendências/decisões (cruzamento Regra C). Rodapé: tags estatísticas (Regra D).

**Regra A — Tabela-verdade da bandeira de custódia** (gate determinístico; colunas K–Q são bandeiras `Sim`/`Não`, jamais texto):

| Situação (origem no auto) | Bandeira | Aba |
|---|---|---|
| **Apreendido** (Auto de Exibição e Apreensão) | **Sim** | conforme o tipo |
| **Arrecadado** (Auto de Arrecadação) | **Sim** | conforme o tipo |
| **Restituído** (Auto de Entrega) | **Sim** | aba do tipo · Status *Restituído* + data/recebedor |
| **Localizado/Encontrado** sob custódia | **Sim** | conforme o tipo |
| **Subtraído/Furtado/Roubado NÃO recuperado** | **Não** | nenhuma — só Observação |
| **Objeto de BO de fora** (remetido) | **Não** | custódia de outra unidade |

  Um objeto = uma bandeira/uma aba; detalhe (tipo, qtd, marca, **lacre**, situação) vai à Observação e à aba de custódia. Lacre nunca presumido. Base: CPP 158-A a 158-F.

**Regra B — Prazos** (lançar na AGENDA): APFD (nota de culpa 24h, art. 306 CPP); IP preso 10d (art. 10); IP solto 30d; IPS 60+30 (DGP-26); VD c/ MPU 48h (art. 12 III, Lei 11.340/06); ação condicionada/privada decadência 6 meses (art. 38 CPP; art. 103 CP); prescrição (art. 109 CP; termo inicial 111; reduções 115).

**Regra C — Cruzamento obrigatório** contra `BOs`/`IPs`/`MPUs`/`AIs` e roster por nome/vulgo, CPF (redigido), placa, telefone, PIX, endereço, modus — reincidência, MO seriado, conexões na seção 10. **Regra D — Tags:** mês de competência = mês da **1ª edição**; preso S/N (adolescente = APREENDIDO); arma lícita × ilícita; entorpecente tipo + gramagem; veículo Localizado/Entregue × Apreendido; morte suspeita (DGP-14/2005). **Regra E — Persistência + merge idempotente** por Nº BO + Ano (col A fórmula intocável; K–Q recalculadas pela Regra A; Análise Aprofundada INTOCÁVEL). **Regra F — Fonte única.** **Regra G — 🔔 Objeto apreendido + requisição de IC → lançar em `PROTOC. OBJ.` + lembrete.**

---

### 5. Comando diário — Análise Aprofundada dos BOs do dia

Pré-requisito: PDFs do dia em `projeto-download-bos\downloads\AAAA-MM-DD\`; rodar em Opus. Passos: (1) listar PDFs (deduplicado); (2) triagem rápida (sinalizar não-DELPOLAPARECIDA p/ remessa); (3) abrir todas as peças (PDF primeiro; faltante → SPJ após `login ok`); (4) 13 blocos + Apontamentos; (5) índice no topo + análises; (6) **não** lançar — aguardar "consolida na planilha". Avulsos: BO único; consolidar na coluna de Análise Aprofundada (backup, localização por B+C, roteamento de custódia/perícia, `CHANGELOG`); gerar `.docx` em `04_PRODUTOS\Aguardando_Revisao\`.

---

## PARTE IV — Módulos Jurídico-Processuais (Oitiva, Portaria, Relatório Final, IPe, Laudos, Objetos)

> Dados institucionais fixos: Delegado Titular Dr. Paulo Sergio Barbosa; Substituto Dr. Leonardo da Costa Ferreira; Escrivão-Chefe João Pedro de Alcântara Mota (RG 54.571.643-3 SSP/SP, 3ª Classe). Decisão final é sempre do Escrivão-Chefe/Delegado (art. 2º, §6º, Lei 12.830/13). Regra-mãe transversal: **ausente = N/C, nunca inventar; cada arquivo é prova estanque; CPF/RG redigidos (LGPD, art. 6º, I)**.

---

### 1. Oitiva Policial — condução e lavratura do termo

**Natureza.** Oitiva por meio audiovisual: **todos os quesitos gerados de uma só vez**. Conduta profissional, formal, terminologia técnica ("instado a narrar", "sob a égide", "capitulação legal").

**Fase 1 — Identificação de cenário:**

| Elemento | Cenário A (BO) | Cenário B (IP) |
|---|---|---|
| Delegado | extrair do documento | Dr. Leonardo da Costa Ferreira (ou Titular Dr. Paulo Sergio Barbosa) |
| Escrivão | João Pedro de Alcântara Mota | João Pedro de Alcântara Mota |
| Unidade | extrair do documento | Delegacia de Polícia de Aparecida |
| Numeração | nº do BO | nº do IP |

**Fase 2 — Quem será ouvido.** Perguntar quem será ouvido e se haverá **entrevista preliminar** (as respostas dela **devem depois constar na oitiva gravada**). Nada informado → oitiva normal direta.

**Fase 3 — Estruturação do Termo:**
- **Cabeçalho padrão (literal):** *"Hoje é dia [DIA], são [HORÁRIO]. Estou na [UNIDADE], sob a autoridade policial supervisora, [DELEGADO], eu sou João Pedro de Alcântara Mota, Escrivão de Polícia."*
- **Qualificação e contexto:** qualificação (nome, nascimento, filiação) + resumo dos fatos (nº do procedimento, data, local, crimes).
- **Advertências legais por status:**

| Status | Advertência / fundamento |
|---|---|
| **Testemunha / Condutor** | Compromisso legal; **art. 342 do CP** (falso testemunho). |
| **Vítima** | Responsabilidade legal; **instada a dizer a verdade** (não presta compromisso de testemunha). |
| **Investigado / Indiciado** | Direitos constitucionais — silêncio, não autoincriminação, advogado — **art. 5º, LXIII, CF**. Sem compromisso com a verdade; silêncio não gera prejuízo. |

- **Técnica do Funil:** Abertura (pergunta aberta, narrativa livre) → Aprofundamento (O quê? Quem? Quando? Onde? Como? Por quê?) → Confrontação (com evidências dos autos) → Fechamento (coação, adicional). **Sem limite de quesitos.**

**Metodologias científicas obrigatórias:**

| Técnica | Aplica-se a | Núcleo |
|---|---|---|
| **Entrevista Cognitiva (EC)** — Fisher & Geiselman | Testemunhas e vítimas | 4 mnemônicos: (1) Restabelecimento do Contexto Mental; (2) Relato de Tudo (hipermnésia); (3) Mudança de Ordem (cronológica inversa); (4) Mudança de Perspectiva (só localização espacial, com cautela). EC Aprimorada: rapport, transferência de controle, abertas antes das específicas, não interromper, silêncios úteis. |
| **Uso Estratégico da Evidência (SUE)** — Granhag & Hartwig | Suspeitos resistentes | Explora a **assimetria de informação**. Prova *específica* × *de contexto*. **Divulgação tardia**: "trancar" o suspeito numa versão verificável, esgotar a narrativa, só após a **negativa absoluta** confrontar. Valor probatório = discrepância declaração × prova, documentada. |
| **Modelo PEACE + TED'S PIE** | Todos (arquitetura) | **P** Planejamento (Pontos a Provar; provas Dependentes × Independentes); **E** Engajamento (rapport + aviso art. 5º LXIII CF); **A** Account/Relato (livre + confronto); **C** Closure; **E** Evaluation. **TED'S PIE**: Tell, Explain, Describe / Show me, Precisely, In detail, Exactly. |
| **PBEF + Lei 13.431/2017** | Crianças e adolescentes — **acionamento automático** | Escuta especializada / depoimento especial. *Ground rules*: "Regra do Não Sei", "Não Entendi", "corrigir o entrevistador", compromisso com a verdade em linguagem acessível. Fases NICHD/PBEF: rapport → prática narrativa → regras → substantiva ("me conte tudo…") → fechamento neutro. **Só perguntas abertas.** |

**Restrições negativas de segurança jurídica (sobrepõem-se a qualquer estratégia):**
- **Vedada a Técnica Reid** (maximização/minimização) e toda pressão psicológica agressiva — risco de confissão falsa e prova imprestável (incompatível com art. 5º, LXIII, CF).
- **Veto ao engano:** **não blefar** sobre provas inexistentes. O SUE trabalha com **prova real dos autos**, só divulgada no tempo certo (lícito); blefar com prova inexistente é o vedado.
- **Vulnerável** → migrar imediatamente ao PBEF/Lei 13.431/17; nunca SUE/confronto.

> **Acionamento:** memória (testemunha/vítima) → EC; suspeito → SUE; arquitetura geral → PEACE/TED'S PIE; menor → PBEF (automático); sempre sob as restrições acima.

---

### 2. Portaria de Instauração de Inquérito Policial (frente C2)

**Assinatura:** Dr. Leonardo da Costa Ferreira. **Fundamento:** arts. **144 da CF/88** e **5º, inciso I, do CPP**.

**Protocolo de fidelidade:** basear-se só nos documentos carregados; cada arquivo é prova estanque (não cruzar casos); conferir nomes, datas, artigos, endereços. **Endereço:** *"na [Rua/Av], nº [Número], Bairro [Nome], [Cidade]/SP"*.

**Filtro de diligências (regra central):** listar **apenas diligências de vital importância**; proibido genéricas/"encher linguiça".
- **Oitivas:** só de qualificados/mencionados no BO, fundamentais e **ainda não ouvidos**.
- **Perícias (regra de ouro):** **NÃO** requisitar novas não pedidas no BO (salvo urgência gritante); a regra é **só juntar os laudos das requisições já expedidas** (Lesão → IML; Dano → IC).
- **Ofícios/avaliações:** só se necessários (ex.: preservação de imagens; Auto de Avaliação Indireta).
- **Vulneráveis:** Escuta Especializada e/ou Conselho Tutelar/CREAS.
- **VD (obrigatório):** verificar se a vítima pediu **MPU** → juntar requerimento + decisão + intimação; e **sempre** ordenar pesquisa/juntada de **antecedentes + outros BOs das mesmas partes**.
- **Dúvida de autoria / campo:** Ordem de Serviço ao **SIG**.

**Estrutura de saída (texto único, contínuo, pronto para copiar):**
```
PORTARIA
Tendo chegado ao meu conhecimento fato noticiado no boletim de ocorrência nº [BO], lavrado [LOCAL], versando sobre a natureza de [NATUREZA/ART.], no qual se apura [RESUMO DO NÚCLEO PENAL], ocorrido no dia [DATA], [HORA], na [ENDEREÇO COMPLETO], onde [INVESTIGADO ou "AUTORIA DESCONHECIDA"] teria, em tese, [CONDUTA SUCINTA].
Considerando a necessidade de melhor apuração dos fatos e suas circunstâncias, com espeque nos arts. 144 da CF/88 e 5º, inciso I, do CPP, INSTAURO o presente procedimento de polícia judiciária [...] vez que a conduta [...] amolda-se, em tese, à figura típica descrita no art. [TIPIFICAÇÃO].
Determino ao Sr. Escrivão [...] promova a juntada aos autos:
- BO nº [BO];
- [SOMENTE documentos já existentes — declarações; requisições já expedidas (Lesão→IML; Dano→IC)].
E, desde já, cumpram-se as seguintes diligências vitais:
- Digitalize-se eventuais documentos físicos e promova-se o respectivo upload no sistema; [PEÇA SEMPRE]
- [Junte-se laudos de IML/IC já expedidas];
- [Proceda-se à oitiva de [CITADO NÃO OUVIDO]];
- [Intime-se o investigado para prestar esclarecimentos];
- [Expeça-se ofício a [ÓRGÃO] solicitando [INFORMAÇÃO]];
- [Elabore-se Auto de Avaliação Indireta];
- [Oficie-se Conselho Tutelar/CREAS — vulneráveis];
- [VD: antecedentes + BOs das partes; cópia do pedido de MPU e decisão];
- [Expeça-se Ordem de Serviço ao SIG];
- [APENAS SE URGENTE: Requisite-se perícia [TIPO] para [FINALIDADE]].
Devidamente cumpridas as diligências, tornem os autos conclusos para ulteriores deliberações.
Aparecida/SP, [DATA POR EXTENSO].
LEONARDO DA COSTA FERREIRA
Delegado de Polícia
```

**Formatação (.docx):** A4, fonte **Century** (corpo 10,5pt; "PORTARIA" 14pt negrito), justificado, recuo 1ª linha 3402 DXA; cabeçalho Arial 10pt; listas de juntada e providências em **numeração contínua** (mesma reference); "upload" em itálico; nome do delegado centralizado em negrito. Nenhum item de lista é fixo — a quantidade decorre da análise do caso.

---

### 3. Relatório Final de Inquérito Policial (frente C3)

**Papel da IA:** Assistente Cartorário de Inteligência, subordinado ao Delegado. **Prioridade:** Regras Invioláveis > 7 Eixos > Templates/Exemplos > Princípios.

**Regras invioláveis de estilo (violação invalida o relatório):**
- **Texto corrido**, só parágrafos. **PROIBIDO** tópicos, marcadores, numeração, subtítulos, títulos de seção, caixas, tabelas no corpo oficial; proibido nomes dos eixos, meta-textos, introduções ("Segue abaixo…") ou despedidas. Começa no cabeçalho, termina na assinatura.
- **Proibida paginação** ("fls. 12") — ancorar pelo **título da peça** ("o Laudo Pericial nº…", "o Termo de Declarações de…").
- **Negrito** só em palavras-chave vitais (armas, horários, valores, drogas, datas, locais, quantidades). **Aspas** só em transcrições literais de alto valor probatório.
- **Verbos neutros** (informou, relatou, detalhou, declarou, atestou, constatou, apontou). **Proibidos:** confessou (usar "admitiu"/"reconheceu"), alegou, bradou, gritou, chorou. **Tratamento:** "investigado" por padrão; "indiciado" só com indiciamento formal. **Modulação:** "em tese", "indícios suficientes"; proibido "comprovadamente", "é o autor", "culpado".
- **VD:** não existe "crime de violência doméstica" autônomo (exceção: descumprimento de MPU, art. 24-A da Lei 11.340/06). Vincular ao crime material (art. 129, §9º, CP c/c Lei 11.340/06).
- **Peças de instauração × de prova:** **B.O., APF e Portaria só no Eixo 3**; **jamais** para fundamentar materialidade/autoria (Eixo 4) — que vêm só de laudos, oitivas/interrogatórios e relatórios de investigação.

**Estrutura — os 7 Eixos** (guias internos; nomes nunca aparecem no texto):

| Eixo | Conteúdo | Fundamentos |
|---|---|---|
| **1 — Cabeçalho** | `IP. Nº / RDO. Nº / NATUREZA / VÍTIMA / INDICIADO` | dados reais da capa |
| **2 — Introdução padrão** (texto inalterável) | Invoca **art. 144, §4º, CF**; **art. 2º, §1º, Lei 12.830/13**; **art. 140, §3º, Const. Estadual/SP**; **arts. 4º e ss. do CPP**; oferta nos moldes do **art. 10, §1º, CPP** | dirigida ao "EXMO(A). SR(A). DR(A). JUIZ DE DIREITO" |
| **3 — Instauração e Resumo dos Fatos** | "Consta deste procedimento… instaurado por [portaria/APF], que no dia [data], em [local]…, o investigado [nome]… praticou [conduta]." + tipificação + dinâmica | base restrita a BO/portaria/APF |
| **4 — Síntese Probatória** | 1 parágrafo materialidade + 1 autoria; cada elemento com razão de relevância; crime a crime | **escolher UM cenário** |
| **5 — Oitivas** | Transcrição indireta, ordem: **condutor/autoridade → vítima(s) → testemunha(s) → interrogatório**. "**[NOME EM MAIÚSCULAS]**, ora [qualidade], informou…" | silêncio → art. 5º, LXIII, CF |
| **6 — Análise de Documentos/Provas Técnicas** | Cada laudo/exame/relatório/mídia em parágrafo próprio ("O Laudo Toxicológico Definitivo nº X concluiu…") | ancorar pelo nome/número |
| **7 — Fechamento padrão** (texto inalterável) | **art. 10, §1º, CPP**, oferta do RELATÓRIO FINAL; local/data; Delegado | — |

**Mapa de decisão do cenário (Eixo 4) — apenas um:**
- Sem materialidade / atípico → **Cenário C** (prejudicada a autoria).
- Materialidade + indícios suficientes de autoria → **Cenário A** (autoria "em tese" sobre [NOME]).
- Materialidade + autoria desconhecida apesar de esgotadas as diligências → **Cenário B** (autoria "permanece elidida/desconhecida", elencando o esforço).

**Glossário:** materialidade (o crime ocorreu) × autoria (quem praticou); **indícios suficientes de autoria** = standard do inquérito (inferior à "prova além da dúvida razoável"); indiciamento = ato formal do Delegado; elementos de informação ≠ provas judiciais. **Lacunas:** solicitar complementação ou placeholder `[inserir …]` — jamais inventar.

---

### 4. IPe — Inquérito Policial Eletrônico (fluxo e entraves)

**Sistema:** `inquerito.policiacivil.sp.gov.br` (frameset). **Critério João:** possui documento "**Relatório Final**" → **COTA**; não possui → **INQUÉRITO** (não é o status do sistema que decide).

**Onde:** Menu → Procedimento → Inquéritos Policiais. Abas: `Em Cartório` | `Para Prazo` | `Relatado` | `Cotas` | `Procedimento Físico`. **Conferir:** Em Cartório + Para Prazo. **Ignorar:** Relatado, Cotas, Físico. Escrivão = coluna **Equipe** (ex.: `CARTORIO 06 - BIANCA`).

**Por procedimento (~25s):** "Consultar Meus Inquéritos" (`+`) → Nº + Ano → Buscar → clicar no **número** → "Abrir Inquérito" → **Pasta Digital → Ordenar Peças** → **rolar até o FIM** → procurar "**Relatório Final**" na coluna Tipo → voltar pelo brasão.

**Entraves:**

| Armadilha | O que fazer |
|---|---|
| Usar a coluna **Status** como atalho | Abrir cada um. |
| Ler **movimentações** para achar o RF | Usar **Pasta Digital → Ordenar Peças** (lista única). |
| Ler a lista de peças **cedo demais** | Carrega progressivamente; **rolar até o fim** (13 peças dizia "inquérito"; com 55 era cota). |
| "Buscar Procedimento" do menu | Dá erro; usar "Consultar Meus Inquéritos". |
| Abrir sem selecionar a linha | "Abrir Inquérito" só após clicar no número. |
| Página em branco / frameset | **F5** limpa o estado; relocalizar o frame dinamicamente. |

**Padrão:** antigos/relatados tendem a cota; recentes em cartório tendem a inquérito — mas há exceções: **conferir um a um**. **Automação:** colher roteiro (nº+equipe+status) e classificar por laço assíncrono, gravando em `localStorage` (resiliente a F5). Linha de base 22-23/05/2026: 592 procedimentos → **248 cotas + 343 inquéritos**.

---

### 5. Laudos — Frente B5 (SPTC: worklist, caça, conferência)

**Sistema "Segunda Via de Laudos" (SPTC — ≠ SPJ):** intranet `http://10.78.1.6/SegundaViaDeLaudos`, unidade DEL.POL.APARECIDA. **Login sempre manual — o Cowork NUNCA insere credenciais.**

**Consulta por BO:** Menu Consulta → **CONSULTA POR ORIGEM** → Tipo de Origem `BO / RDO / TC` (filtrar por "RDO" é o seguro) → Número (alfanumérico, ex. `GQ8779`) + Ano → **Pesquisar**: começar em **IC** e repetir em **IML** (necropsia, lesão, ECD, toxicológico). Trocar a base **reseta** o Tipo de Origem.

**Status (coluna Ações):** "Exibir Laudo" (cinza) = **concluído** → baixar PDF; "Laudo em Elaboração" (laranja) = nº atribuído mas **não concluído** → registrar só nº/natureza; "Não foram encontrados resultados" = **não emitido** → marcar `NAO_EMITIDO`, reconsultar.

**Método (2 camadas + lotes):** Camada 1 (localizar): achar item, anotar status/nº/data (>30s = sessão caiu, re-logar). Camada 2 (extrair): baixar PDF (**SHA-256**, CPP 158-A/F), **persistir texto integral** em `85-Laudos\laudos_texto\`, gerar **resumo investigativo** em `85-Laudos\resumos\`, marcar worklist, projetar no **pacote** (satélite **não grava** na mestra). **Ritmo:** **lotes de 5** (11/06); checkpoint a cada laudo; parada graciosa a ~70-80%.

**Extração da conclusão:** Drogas — substância **confirmada** (reconferir contra o auto — "crack" pode ser cocaína); massa **bruta × líquida**; contraprova retida. Arma — eficiência (apta × inapta), calibre, numeração (íntegra × **suprimida** = ilícita), SINARM/SIGMA. IML-pessoa (ECD) — **grau** da lesão (art. 129 §§), instrumento, nexo; **vítima menor:** achado clínico em termos técnicos, **imagem NUNCA aberta** (CPP 158-A; ECA). Necroscópico — causa mortis, meio, toxicológico. Veículo — chassi/motor (art. 311 CP).

> **REGRA DE PESO PARA A ESTATÍSTICA (João, 01/06/2026):** entra **só o peso que VOLTA à unidade = massa líquida (laudo) − contraprova**, por item/substância. "amostra de ~N g" → subtrair N; "todo o material retido" → **0 g**. **O peso bruto do BO é IGNORADO.** Em apreensão grande, o DEFINITIVO analisa só ~2 g/item; a massa líquida real está na **CONSTATAÇÃO PROVISÓRIA**.

**Roteamento a jusante:** `PERÍCIAS` (Nº Laudo, Status, Data, Observação), custódia (Guia, Lacre, Status→"Periciado", peso) e estatística (peso que volta). **Fonte única:** resumo ↔ texto persistido ↔ pacote têm de bater célula a célula.

---

### 6. Protocolo de Objetos / Cadeia de Custódia (frente 86 · CPP arts. 158-A a 158-F)

**Duas abas da mestra (após `DEMAIS OBJ.`):**
- **`PROTOC. OBJ.`** — 1 linha por objeto, com **LOCALIZAÇÃO ATUAL** + Status ("fotografia de agora"). Localização: Cartório/Cofre · Na Perícia (IC) · Na Perícia (IML) · Pátio · Fórum/Vara · Restituído · Incinerado/Destruído · Entregue · Em trânsito · Outro órgão. Status: Em Custódia · Aguardando Perícia · Em Perícia · Periciado/Retornou · Restituído · Encaminhado Vara · Descartado.
- **`MOVIM. OBJ.`** — 1 linha por movimentação. Tipo: SAÍDA · ENTRADA/RETORNO · TRANSFERÊNCIA · RESTITUIÇÃO · DESTRUIÇÃO.

Ligam-se pelo **Nº Protocolo** (`NNN/AA`, ex. `001/26`; um objeto = um protocolo, vários eventos); cruzam por Nº BO+Ano / IP / lacre.

> **Regra do lembrete (João, 11/06/2026 — gatilho automático):** BO com objeto **APREENDIDO** (Auto de Exibição/Arrecadação) **E requisição de exame ao IC** → (1) avisar `🔔 OBJETO P/ PERÍCIA: [objeto] do BO [nº/ano] tem requisição de IC — encaminhar e protocolar`; (2) lançar na `PROTOC. OBJ.` (Status "Aguardando Perícia"); (3) na remessa, SAÍDA na `MOVIM. OBJ.`; (4) no retorno com laudo, ENTRADA/RETORNO + Status→"Periciado" + Nº Laudo. Nenhum objeto com requisição de IC fica fora do `PROTOC. OBJ.`.

**POP — texto de protocolo de remessa (v1.1, 30/06/2026):** o Cowork **responde só com o texto final**. Máscara:
```
Enc. Req. BO [Nº SPJ] – [CRIME, ART./LEI]; autor: [NOME]; acompanha [OBJETO/DROGA] – LACRE [Nº].
```
Múltiplos objetos → conjunção `E`; objeto de terceiro → `relacionado a [NOME]`; autoria ignorada → `autor: A Esclarecer`. **Regras:** objeto/droga em **CAIXA ALTA**, só o **tipo** (sem peso/marca/calibre/IMEI/cor); Nº do BO = o do **SPJ**; um lacre por objeto; travessão `–` separa BO/crime e objeto/lacre, `;` separa blocos; sem cabeçalho/assinatura. Um autor = o **principal ou possuidor efetivo** (pela leitura do Auto). Campo ausente → "N/C"/"LACRE N/C". Roteamento paralelo (não no texto): registrar na aba de custódia (col. G = Lacre).

---

### 7. Habilidades Originais e Prompts de Inicialização Cowork

**Skill `pente-fino-bo-api` (v1.2)** — pente fino de BO do SPJ pelo caminho de menor custo, via **APIs autenticadas** (base `api.ipe-policiacivil.sp.gov.br`, header `Authorization: Bearer <token>`, **sem cookies** — cookie → 504; token expira em minutos). Por BO: `boletins?...&numero={BO}` → `id` · `getPdf/{id}` (pessoas, naturezas, objetos, drogas/armas/veículos+lacres) · `findByIdOcorrencia/{id}` (instaurações, cnjs, cartorioDespacho, flagViolenciaDomestica) · `documentos/?idOcorrencia={id}`. **SHA-256** por arquivo. Destino: aba `BOs` v2.1 (K–Q bandeiras; detalhe/lacre → Observação S; coluna de Análise Aprofundada é do Escrivão-Chefe — automação NUNCA grava). **Modo profundo:** ler **TODOS** os documentos e anexos; lacre nunca presumido (`[conferir no Auto]`). **Companheiras (locais, .zip):** `joao-pedro-policia`, `pecas-pc-sp`, `portaria-dgp-26`.

**Prompts de inicialização Cowork:**
- **Prompt 0 — Inicialização universal (SEMPRE primeiro):** ler `00-Perfil\perfil-escrivao-chefe.md` e confirmar o perfil em 3 linhas.
- **Prompt 1 — GCC** · **2 — Triagem de BO** · **3 — Histórico de BO** · **4/5 — Análise de Inquérito** (7 passos, 2 estados) · **6 — Oitiva** · **7 — Portaria** · **8 — Relatório Final** · **9 — Prontuário (PRONT.)** · **10 — Estatística mensal** · **11 — Destruição em lote** (drogas: art. 50, §3º e art. 32, Lei 11.343/06; armas: art. 25, Lei 10.826/03; demais: art. 124 CPP).
- **Boas práticas:** começar pelo Prompt 0; ler o módulo antes do pedido; `[INSERIR DADO]`/`N/C`; revisar antes de assinar; atualizar a mestra após cada ciclo.

---

### 8. Mapa dos Projetos Claude Importados

Importados do Claude.ai em 06/07/2026 (reconstrução nativa equivalente). **Regra:** as cartas são fonte do **método**; o **dado** vive na mestra local; onde há sobreposição, as **skills locais prevalecem**.

| # | Projeto | Frente | O que faz |
|---|---|---|---|
| **01** | **Gestor Cartorário Central (GCC)** | A1/D1/B-múltiplas | Projeto-mãe. 7 módulos: M1 Acervo (BO/IP → planilha, flags → zona ⚡); M2 Custódia/laudos (peso final = líquido − contraprova; alerta numeração suprimida); M3 Auditoria (SPJ × interno, SPVIDA/DGP-14, produtividade); M4 Redação oficial; M5 Livro de Inquérito físico; M6 13 modelos Word; M7 Triagem de e-mail (T01–T12). |
| **02** | **Relatório Final** | C3 | 7 eixos, cenários A/B/C, texto corrido (seção 3). |
| **03** | **PORTARIA (Leonardo)** | C2 | Portaria + filtro de diligências vitais; assina Dr. Leonardo (seção 2). |
| **04** | **Análise de Inquéritos** | B1 | Máquina de **2 estados**; Estado 1 triagem + Menu numerado + PAUSA; Estado 2 só com `/item [N]` ou `/executar tudo`. Faltante = `[DADOS NÃO INFORMADOS]`. |
| **05** | **Oitiva Policial** | C4 | Termo audiovisual — EC/SUE/PEACE/PBEF (seção 1). |
| **06** | **Histórico de BO** | B3/histórico | Redação do Histórico (frases obrigatórias imutáveis) + "PONTOS DE ATENÇÃO E REQUISIÇÕES" + complemento/retificação. |

**Cartas:** `00-Projetos-Claude-Importados/01..06_*.md`, `_INDICE.md`, `_MAPA_MESTRE.md`. **Gatilho:** `importar projetos` re-varre os 6.

---

## PARTE V — Lições Operacionais e Entraves de Sistema (memória viva)

> Conhecimento durável destilado do Log de Aprendizado (mai–jul/2026). Organizado por tema, não por data. Foco no reutilizável: entraves de sistema (sintoma → causa → contorno), métodos consolidados e armadilhas a evitar. Casos concretos e pendências datadas omitidos. **Fonte viva de entraves = skill `aprendizado-continuo`**; a skill é somente-leitura no Cowork e só se atualiza reimportando via Settings ▸ Capabilities.

---

### V.1 — Acervo e estrutura durável

- **Arquitetura HUB + satélites** (regime = **chat único com despacho interno**; satélites manuais = exceção para login, sessão dedicada ou frente multi-dia). Blindagem: **degrada anunciando, nunca trava**.
- **Escritor único inegociável:** só o HUB grava as vivas. Satélite larga pacote em `_PARA_LANCAR_NA_MESTRA/pendentes/`. Ciclo: **backup `pre-<ação>` → prévia → confirmação → aplicar → validar reabertura → CHANGELOG no mesmo commit**.
- **Mestra `CARTORIO_CENTRAL_DM_APARECIDA.xlsx`** (~0,9–1 MB, **26 abas** — conferido no arquivo em 07/07/2026). Planilha irmã: `AGENDA_ESCRIVAO_CHEFE`.
- **Coluna Nº (col A)** de BOs/custódia tem fórmula `=IF(B<>"",ROW()-n,"")`. **Nunca escrever na col A.** Deixar B vazio tira a linha da contagem.
- **Zonas ⚡ Pendentes** são ArrayFormula: puxam BOs com flag "Sim" e removem quando o nº do BO aparece na coluna D. Nunca escrever manualmente nelas.
- **Bandeiras K–Q (BOs)** só recebem `Sim`/`Não`. Lacre nunca presumido. **Coluna de Análise Aprofundada intocável.**
- **Status de custódia** (`STATUS_CUSTODIA`): Em Custódia, Entregue, Destruído, Periciado, Encaminhado Judicial, Restituído, **Depositado**.

---

### V.2 — Entraves de gravação de planilha (os mais graves)

| Sintoma | Causa | Contorno |
|---|---|---|
| `openpyxl save` **estoura o timeout de 45s**; às vezes grava **2×** | Mestra grande não cabe em 45s; o save conclui mas o `validate` estoura (exit 124) → parece "não salvou" → re-run duplica. Background morre ao fim de cada `bash` | **Editar o XML interno do `.xlsx`** (é ZIP): `unzip` → mapear aba→sheetN por `workbook.xml.rels` → substituir célula vazia preservando `s=` → `zip` só as abas tocadas → validar. Determinístico/idempotente. Se usar openpyxl, separar `save` de `validate` e **conferir o estado real antes de re-executar** |
| Mestra **corrompe no save** — `BadZipFile / EOCD not found` | Save grande grava arquivo truncado (assinatura `PK` sem EOCD final) | **Após TODO save, verificar que reabre** (`openpyxl.load_workbook`) antes de mover/encerrar. Restaurar o `pre-` backup. Preservar o corrompido. Saves grandes: gravar por aba, validando a cada passo |
| Leitura por chave **"não acha" linhas que existem** | `openpyxl read_only=True` confia na tag `<dimension>`; se defasada, **trunca silenciosamente** | Conferência/contagem/guarda anti-colisão → **SEMPRE full load** (sem `read_only`) |
| Excel **pede "reparar"** ao abrir | `append` de linha nova **depois** das linhas-fantasma pré-formatadas cria `r=` duplicado e não-ascendente; openpyxl tolera, o Excel é estrito | **Inserir = sobrescrever a primeira linha vazia EXISTENTE** após a última com conteúdo, nunca `append`. Validação inclui: `r` **único e estritamente ascendente**. Abas com fantasmas: `CORRESP.`, `CHANGELOG` |
| XML passa em `zip -t`/read_only mas quebra no Excel | `<sheetData>` mal fechado não é pego | Validar com `ET.fromstring` **+** reabertura `openpyxl` full load |
| **Colisão de escrita entre sessões** | Dois chats gravaram as mesmas linhas; pacote em `aplicados/` + CHANGELOG "parecia" cadastrado | **UM escritor por vez.** Guarda de estado (aborta se a âncora divergir). **`aplicados/` + CHANGELOG NÃO são prova** — conferir por chave na própria aba |
| **Localizar por nº de linha grava no registro errado** | Linhas mudam após reorder | **Localizar SEMPRE por CHAVE** (Nº BO+Ano, IP nº+Ano) |

**Transversal:** dedup por **chave dupla** (IP nº+Ano **e** IPe; Nº BO+Ano) após todo commit em lote.

---

### V.3 — Entraves de ferramenta/arquivo (dual filesystem)

| Sintoma | Causa | Contorno |
|---|---|---|
| **Write/Edit truncam silenciosamente .md/scripts grandes** | O Read mostra o **cache**, não o disco; a gravação corta o fim | Criar/editar via **bash heredoc** (`cat > arq << 'EOF'`). **Sempre conferir o disco** com `tail -1`/`wc -l`/`wc -c` |
| Vista do **shell do sandbox truncada/defasada** | Mount pode mostrar cópia cortada | Editar pelas ferramentas de arquivo, não por shell de leitura+regravação; comparar `wc -c` antes. Para executar, **o disco/bash é a verdade** |
| `javascript_tool` (Chrome) **bloqueia o retorno** (`[BLOCKED: Cookie/Base64]`) | Payload com e-mails/URLs/query strings/hashes/base64 | Nunca devolver cru. Guardar em `window.__x` e retornar texto ultra-limpo (URLs→`[url]`, sem `?&=`, JSON por vírgula). Montar CSV no sandbox |
| `javascript_tool` corta em **~1 KB** | Truncamento do display | Guardar em `window.__x`, devolver em fatias (`.slice`) |
| Função **async retorna `{}`** (após navegação/AJAX) | A Promise "morre" no meio, mas os efeitos persistem em `window` | **Processador em segundo plano**: grava em `window.__acc`/`__final` + flag `__done`; ler o progresso em chamadas síncronas seguintes. Cada fetch com `AbortController` próprio |

---

### V.4 — SPJ (BOs via API) — método consolidado

- Frontend: `spj.ipe-policiacivil.sp.gov.br/boletins-ocorrencias/list` (SSO realm **dipol**, client `dipol-rpj`). O app IPe-inquérito **NÃO serve** (cookie próprio).
- **Host da API = `https://api.ipe-policiacivil.sp.gov.br`** (NÃO o host `spj` → devolve HTML do SPA → `Unexpected token '<'`).
- **Chamadas: Bearer SEM cookie** (`credentials:'omit'`). Com cookie → **504**.
- **Token vivo NÃO fica no localStorage** (adapter Keycloak em memória). Capturar interceptando `setRequestHeader`+`fetch` e disparando uma busca real pela UI; expira ~1h → pedir "login ok", reinstalar interceptor + reinjetar pdf.js/rotinas.
- **Campo de busca:** `form_input` não dispara o Angular → digitar com teclado real. Chamar `read_network_requests` **antes** da busca.

**Endpoints (host api, Bearer sem cookie):**
- Busca: `/cadastros/ocorrencias/boletins?tipoBusca=R&rdo=false&ano={A}&numero={BO}&...` — já traz `content[0].idCircunscricao`/`nomeCircunscricao`. **O id do detalhe é `content[0].id`, NÃO `idOcorrencia`.**
- Detalhe: `/.../findByIdOcorrencia/{id}` — `instaucoes[].numero`, `idDelegaciaInquerito`, `cnjs`, `solucao`, `delegado`, `flagViolenciaDomestica`, `locais[0]`. NÃO traz naturezas/pessoas/objetos expandidos.
- PDF: `/.../getPdf/{id}` (arraybuffer) → **SHA-256** (`crypto.subtle.digest`) antes de parsear → texto via **pdf.js** (cdnjs 3.11.174/4.x).
- Documentos: lista `/cadastros/documentos/?idOcorrencia={id}` (tipo em `item.modelo.nome`); conteúdo `/cadastros/documentos/{idDoc}` → campo `texto` (HTML — decodificar entidades).
- Anexos: `/cadastros/anexos/?idOcorrencia={id}`.

**Entraves:** abas do "Detalhar BO" **renderizam vazias/lazy** → não confiar (a tela mente; o Auto e o PDF mandam). PDFs travam ao abrir → **F5** e reabrir por "Visualizar". Oitivas em vídeo → usar a **transcrição textual**, nunca abrir o vídeo.

---

### V.5 — IPe (dois inquéritos eletrônicos) — regra de ouro

**A PC/SP tem DOIS sistemas — SEMPRE buscar nos dois** antes de concluir "não instaurado". `NNNNNNN/ANO` = novo; `NNNNNNN-DD` (hífen) = antigo.

| | IPe NOVO | IPe ANTIGO |
|---|---|---|
| URL | `https://inquerito.ipe-policiacivil.sp.gov.br` | `http://inquerito.policiacivil.sp.gov.br/inquerito/` (**http, sem "s"**) |
| Tecnologia | Angular | JSF/PrimeFaces em **frameset** (`window.frames[1]`, name=`body`) |
| Guarda | Recentes; a aba "Inquéritos Policiais" lista **SÓ FLAGRANTES** | Antigos/migrados |

**Novo — abas de status** = universo por escrivão. "Em Cartório – Enviado TJ" **não** é relatório final (é o APF ao Juiz das Garantias, 24h). **Antigo — método de capa:** buscar em `formMeusInqueritos` → **selecionar o `<tr>`** (obrigatório) → `btnPresidirInq` → ler por DOM. Delegado = coluna "Usuário que Criou" da linha Tipo "Portaria".

**Entraves:**

| Sistema | Sintoma | Contorno |
|---|---|---|
| Novo | Modal "Notificações" reabre e **bloqueia a busca** | Fechar pelo botão "Fechar"; `Escape` nem sempre pega |
| Novo | Bearer não capturável (Zone.js); fetch → 504 | Trabalhar pela UI (`get_page_text`); ou `sessionStorage.access_token` do SPJ |
| Novo | Coluna "Ano" ≠ ano do procedimento; laço JS de paginação **congela o renderer** | Buscar só pelo número; não fazer laço numa chamada; operar o paginador índice [1] |
| Antigo | Guia nova cold-load trava (timeout 180s) | Usar a **guia válida**; operar por DOM/JS no `frames[1]`, **nunca screenshot** |
| Antigo | Paginação PrimeFaces instável | Monitorar "Página X de N" por regex; acumular por chave; conferir contra "Total" |
| Antigo | SSO expira no meio (frame → `sgu/login.faces`) | Novo login; `frames[1].location` volta a `meusInqueritos`; esperar "Bem-vindo(a)…DEL.POL.APARECIDA" |

**Integridade:** **Natureza deriva das Capitulações** (capa), **NUNCA do "Assunto Principal"** (genérico). **Correição — pedido de prazo por inatividade:** última movimentação > 30 dias, em andamento (não relatado, não réu preso) → `PEDIR PRAZO` + Pedido de Dilação (art. 10, §3º CPP). Deduplicar correição por chave antes de commitar.

---

### V.6 — SPTC / Segunda Via de Laudos

**Regime:** login manual em `http://10.78.1.6/SegundaViaDeLaudos` (intranet — o sandbox **não alcança** o 10.78.1.6). Autentica por **cookie** → `credentials:'include'`, sem Bearer.

**Endpoints:** IC `POST api_ic/GetLaudosByOrigem` (JSON, `CodigoTipoOrigem:"2"` p/ BO/RDO/TC); IML `POST api_iml/BuscarPorOrigemPC` (urlencoded, `2,7` p/ BO/TC; `3` p/ IP). Trocar a base reseta o Tipo de Origem. **Status:** `plem` false/0 = concluído; true/1 = em elaboração. **Download:** `GET api_ic/ArquivoDownload?numero=&ano=&nome=<usuário>&codRep=<IdREP>`. **`codRep`=`IdREP` OBRIGATÓRIO** (sem ele o PDF vem com **0 bytes**). Fetch arraybuffer → `%PDF-` → pdf.js. **Extrair na própria página.**

**Negócio (droga):** substância pelo **resultado químico** (COCAÍNA; THC = maconha), nunca pela descrição física. **Não certifica "crack"** (item petrificado testa COCAÍNA). Peso que volta = líquida − contraprova. Definitivo analisa só ~2 g/item; massa líquida real na **CONSTATAÇÃO PROVISÓRIA**. Dedup por (item, lacre, liq).

**Entraves:**

| Sintoma | Causa | Contorno |
|---|---|---|
| **503** antes do login | Servidor SPTC fora do ar | Aguardar; não é sessão |
| Login abre mas 1ª consulta gira + recargas 503 | Servidor degradado | Parar (não relogar em loop); retomar depois; acionar SPTC |
| **IC** "Falha na comunicação"; **IML funciona** | `api_ic` indisponível | Marcar IC como `IC_INDISPONIVEL`; fechar só os IML |
| `ArquivoDownload` série 21xxxx/22xxxx retorna HTML "Runtime Error" 500 | Bug do servidor | Nº/status existem; peso/lacre por "Exibir Laudo" |
| Laudos de arma são **imagem/escaneados** | — | OCR do lacre ou cruzar com o lacre da apreensão do SPJ |

**Sessão caída × servidor fora:** carregando 30s+ depois de logado = sessão caiu; 503 sem tela de login = servidor fora.

---

### V.7 — Outlook institucional (triagem de e-mail)

**Modelo vigente:** o **João lê todos os e-mails**, separa e informa as diligências; o Cowork transforma cada uma em pacote para o HUB. Entrada preferencial = `.eml` anexado (MIME; PDF base64 → texto; SHA-256 quando custódia). O Cowork **não conecta ao Outlook para triar de rotina**.

**Roteamento durável:**
- **Qualificar / localizar pessoa** (inclui reiteração) → **SIG** + **NÃO LIDO**.
- **Monitoramento Apuração / Disque-180 / Denúncia** → SIG, não-lido.
- **DDM Online** → arquivar.
- **SEMPRE ler o ofício anexo, não o assunto** ("ARQUIVA IP" pode mascarar extinção de punibilidade / revogação de MPU / adolescente).

**Entraves "novo Outlook" (`outlook.cloud.microsoft`):**

| Sintoma | Contorno |
|---|---|
| Caixa **virtualizada** (~12–15 no DOM); IDs re-renderizam no scroll | Capturar por **scroll-accumulate + dedup** (Map por aria-label; passo ~160px); abrir por **assinatura (remetente+assunto)**, não por id |
| Loops de scroll estouram 45s | Fatiar em várias chamadas |
| Anexo PDF abre em **CANVAS** (sem texto) | Ler por **screenshot/zoom** |
| **Abrir marca como LIDO** | Reverter todos a não-lido ao final (o toggle é toggle — conferir o badge) |
| **Mover 1 e-mail:** painel só aparece com **2+ marcados** | Marcar checkbox de 2+; ou menu de contexto (instável) |
| Busca só acha no **assunto** | Buscar por **remetente** e desambiguar por data; escopo "Todas as pastas". Enter nativo submete; `dispatchEvent` sintético não |
| Mapa de pastas real ≠ documentado (nbsp/espaços invisíveis) | Casar por regex/índice do treeitem, não `textContent===` |

---

### V.8 — Outros sistemas

- **e-SAJ Pasta Digital (TJSP):** texto das peças em **canvas** (`get_page_text` traz só a árvore de peças — ótima para achar Relatório Final/Manifestação MP); ler PDF por **screenshot/zoom**. **Não clicar no zoom durante o carregamento** (corrompe o visualizador → abrir aba nova). Domínio `esaj.tjsp.jus.br` exige **permissão da extensão por domínio/sessão**. **Alternativa nativa:** confirmar RF por **Monitorar Envios TJ** do IPe (aba "Sucesso" → Tipo "Relatório Final").
- **SPVIDA:** colunas do cartório **deslocadas** vs o README (79 col., cabeçalho na linha 2). Casar **por NOME de cabeçalho, nunca por letra cega**.
- **Extensão Claude-in-Chrome pareada mas sem controle:** `tabs_context` responde mas `navigate`/`computer` expiram (180s). Contorno: trazer o Chrome ao primeiro plano; recarregar/reabilitar a extensão; re-parear.

---

### V.9 — Métodos investigativos e de cadastro (consolidados)

- **Regra de ouro (INEGOCIÁVEL):** ao tocar num BO, **abrir e ler TODOS os documentos e anexos** — não só a linha do Livro de BO, não só a 1ª página, não só os campos JSON. Ausente = `N/C`, **nunca inventado**.
- **Modelo NÃO econômico:** o "menor custo" serve só para triagem; na conferência, **completude > custo**. Testemunho: um "estelionato art. 171" na tela era **sextorsão de criança de 13 anos** — a idade só apareceu na transcrição da oitiva em vídeo. Sem leitura íntegra, seria arquivado como golpe comum.
- **Cruzar BO × Documentos × Custódia antes de lançar:** a aba Objetos/Entorpecentes do BO **não basta** (omite lacres, diverge de quantidade). Lacres/destino/restituições estão nos **Autos** (Exibição/Apreensão / Arrecadação / Entrega). Distinguir **Apreendido** × **Arrecadado** × **Restituído/Entregue**.
- **Custódia — o que manda é ONDE A CUSTÓDIA FICA**, não a região do fato nem quem digitou o BO. Aparecida **lavra BOs para Roseira e Potim**: BO de circunscrição Roseira/Potim → "de fora / remessa", custódia não é nossa. Droga de fora **remetida a** Aparecida = custódia nossa. `idDelegaciaInquerito`: **1512/130201 = Aparecida**; 130206 = Roseira; 130214/130215 = Potim (confirmar mapa). **Local do Fato + delegaciaInquerito são mais confiáveis que o campo "circunscrição".**
- **CNJ e nº do IP saem do PDF do BO** (edições pós-instauração): "Procedimentos Instaurados" (IP, ex. `2532974-71.2026.1512`) e "Número do Processo CNJ". Para estatística, IP **sem** o sufixo `.1512`.
- **Fonte limpa da qualificação** = documento "EXTRATO DE QUALIFICAÇÃO DAS PARTES". **Autoridade/fiança do flagrante** = corpo/assinatura do APF.
- **Flagrantes réu-preso (aba IPs):** col C (IP nº) = col K (IPe) = nº do procedimento.
- **LGPD/ECA:** redigir CPF/RG antes de qualquer uso; imagens sensíveis de criança → **não abrir/expor**, só registrar existência sob custódia; nunca reconhecimento facial.

---

### V.10 — Método/regime de trabalho

- **Uma frente pesada por vez.** Vários satélites pesados em paralelo **estouram a memória do Cowork → congela tudo**. Serializar as pesadas; sub-lotes de 10–20; **um chat novo por sub-lote**; nunca despejar JSON/PDF cru no chat; HUB fica leve; chat travado → abrir novo lendo só o `ESTADO_ATUAL.md`.
- **Varredura contínua** (registro a registro com checkpoint; parar a 70–80%) em vez de lote fixo.
- **Resumo Investigativo v2.0 obrigatório para TODO BO.**
- **Conferência do HUB (4 eixos):** cobertura → completude → consistência → fonte lida por inteiro. Eficiência **nunca** reduz qualidade. Nova passada do satélite quando houver lacuna, antes do commit.
- **Estatística mensal:** 6 planilhas à Seccional (1–5 e 7, não há 6) + 3 de cruzamento SPJ. Aba do João = "DM APARECIDA"; ele não entra na contagem de produção (coordenação); casar por nome de aba/cabeçalho.

---

**Regra transversal de decisão:** a decisão final é sempre do Escrivão-Chefe/Delegado (art. 2º, §6º, Lei 12.830/13). Ao registrar novo entrave/lição, gravar log datado em `99-Log-Aprendizado/`, classificar no `INDICE_LICOES.md` e, se entrave de sistema, adicionar a `_MIGRAR_PARA_SKILL_entraves.md` para reimportar em `aprendizado-continuo`.

---

## Fecho — Nota de transplante

Este documento condensa o **conhecimento reutilizável** do Cartório Central até **07/07/2026**, destilado pelo HUB a partir de: a governança-raiz (16 protocolos), os SOPs de gestão (`Conhecimento/10-GCC` + perfil), os módulos investigativos (`20`/`30`/`40`/`45`) e jurídico-processuais (`50`/`60`/`70`/`80`/`85`/`86`/`90`/`01`/`00-Projetos-Importados`) e a memória viva (`99-Log-Aprendizado`).

**O que NÃO está aqui (por escopo):** dados de casos concretos — números de BO reais, nomes de envolvidos, planilhas vivas (`CARTORIO_CENTRAL`, `AGENDA`), resumos investigativos de casos, PDFs de exemplo, backups e as skills empacotadas (`.skill`/`.zip`). Estes seguem nos seus arquivos de origem e podem ser transplantados à parte, se desejado.

**Fidelidade:** preservados com precisão os artigos de lei (CF, CP, CPP, Leis 8.069/90, 9.099/95, 9.296/96, 10.741/03, 10.826/03, 11.340/06, 11.343/06, 12.830/13, 12.850/13, 13.146/15, 13.431/17, 13.964/19, LGPD), a Portaria DGP-26/2023 e alteradoras, súmulas e HCs, os nomes de abas/colunas/chaves, prazos, estruturas de peças e gatilhos. Onde as fontes divergiam, ambas as versões foram mantidas com a marca "**o arquivo manda**".

*Consolidado pelo HUB (Opus) · Cartório Central · DPM Aparecida/SP · 07/07/2026.*

*Conferido e revisado em **Fable 5** por ordem expressa do João (07/07/2026) — auditoria de completude contra os protocolos-fonte, a pasta `Conhecimento/` e as planilhas vivas. Correções aplicadas nesta revisão: (1) tabela da mestra atualizada para **26 abas** conferidas no arquivo real (+`PROTOC. OBJ.`, `MOVIM. OBJ.`, `PERÍCIAS`); (2) divergência de layout da aba `BOs` **resolvida** pelo cabeçalho real — Análise Aprofundada na col. **U**, bandeiras **K–Q**; (3) referências residuais à col. `W`/`L–R` corrigidas (§I.3.2-B3 e §I.10.2); (4) incluída a seção **I.1.9** — carta de poderes e plano de varredura S1–S8 do `HUB_CONTROLE_TOTAL` (lacuna da consolidação original); (5) nota sobre a defasagem de rótulo de versão dos protocolos-fonte — **harmonizada em 07/07/2026** (v2.3 em disco); (6) criado o produto derivado **`PROMPTS_COPILOT/`** — kit de 14 prompts autocontidos + LEIA-ME que portam as frentes-satélite para Copilot M365/Claude API/ChatGPT, mantendo o João como HUB e escritor único das vivas (manter o kit sincronizado com este consolidado). Decisão final é do Escrivão-Chefe/Delegado (art. 2º, §6º, Lei 12.830/13).*
