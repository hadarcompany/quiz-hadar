# PROMPT PARA CLAUDE CODE — Quiz Funnel Agência Hadar

Cole o conteúdo abaixo dentro do Claude Code para gerar o quiz completo.

---

## 🎯 CONTEXTO

Você é um especialista em funis de conversão e desenvolvimento front-end. Vou te pedir pra construir um **Quiz Funnel completo em HTML, CSS e JavaScript puro** (sem frameworks, single-file) para a **Agência Hadar**, uma agência de marketing completa que atende empresas da região do Alto Paranaíba (Minas Gerais).

O objetivo do quiz é **qualificar leads e redirecioná-los pro WhatsApp** com uma mensagem pré-preenchida contendo as respostas, pra que o time comercial já receba o lead "aquecido".

---

## 🏢 SOBRE A EMPRESA

- **Nome:** Agência Hadar
- **Localização:** Alto Paranaíba, Minas Gerais
- **Serviços:** Agência de marketing completa — diagnóstico estratégico, roteiros, captação e edição de vídeos, tráfego pago, CRM, assessoria completa
- **Público-alvo:** Donos de empresas e gestores de marketing da região do Alto Paranaíba
- **Tom de voz:** Profissional, próximo, direto, sem clichês de marketing

---

## 📐 ESTRUTURA DO QUIZ (3 etapas)

### ETAPA 1 — Tela de Abertura (Capa)

- **Headline:** "Sua empresa do Alto Paranaíba está pronta pra escalar em 2026?"
- **Subheadline:** "Responda 7 perguntas rápidas e descubra em 60 segundos onde seu marketing está travando — e o que fazer pra desbloquear seu próximo nível de faturamento."
- **CTA principal:** "COMEÇAR DIAGNÓSTICO GRATUITO →"
- **Prova social abaixo do CTA:** Faixa horizontal com logos de clientes atendidos (deixe placeholders `<img src="logos/cliente-1.png">` até `cliente-8.png` que eu substituo depois)
- **Texto sobre os logos:** "Empresas que já transformaram seu marketing com a Hadar:"

### ETAPA 2 — As 7 Perguntas

Cada pergunta deve aparecer **uma de cada vez**, com transição suave (fade ou slide). Inclua uma **barra de progresso** no topo (ex: "Pergunta 3 de 7" + barra visual preenchendo).

**Pergunta 1 — Qual o seu papel na empresa?**
- Sou o(a) dono(a)/sócio(a)
- Sou gestor(a) de marketing
- Trabalho na equipe
- Ainda estou começando meu negócio

**Pergunta 2 — Há quanto tempo sua empresa está no mercado?**
- Menos de 1 ano
- 1 a 3 anos
- 3 a 10 anos
- Mais de 10 anos

**Pergunta 3 — Qual o faturamento médio mensal da sua empresa?**
- Até R$ 20 mil
- R$ 20 mil a R$ 50 mil
- R$ 50 mil a R$ 200 mil
- Acima de R$ 200 mil

**Pergunta 4 — Qual o maior desafio do seu marketing hoje?**
- Não consigo gerar leads suficientes
- Gero leads, mas não convertem em vendas
- Não sei medir o que está funcionando
- Não tenho tempo/equipe pra cuidar disso
- Faço tudo "no achismo", sem estratégia

**Pergunta 5 — O que você já tentou pra crescer?** (MÚLTIPLA ESCOLHA — permitir várias)
- Tráfego pago (Meta/Google Ads)
- Conteúdo orgânico (Instagram/TikTok)
- Indicações e boca a boca
- Contratei outra agência antes
- Ainda não tentei nada estruturado

**Pergunta 6 — Você já tem material de vídeo da sua empresa?**
- Sim, gravo com frequência
- Tenho alguns, mas amadores
- Não tenho nada
- Não gosto/tenho vergonha de aparecer

**Pergunta 7 — Quando você quer começar a ver resultados?**
- Pra ontem (urgente)
- Nos próximos 30 dias
- Nos próximos 90 dias
- Estou apenas pesquisando

### ETAPA 2.5 — Captura de Nome e WhatsApp (ANTES do resultado)

Após a pergunta 7, mostre uma tela curta:
- **Headline:** "Quase lá! Pra onde devemos enviar seu diagnóstico personalizado?"
- **Campo 1:** Nome (obrigatório)
- **Campo 2:** WhatsApp com DDD (obrigatório, com máscara `(XX) XXXXX-XXXX`)
- **CTA:** "VER MEU DIAGNÓSTICO →"
- **Texto pequeno embaixo:** "🔒 Seus dados estão seguros. Não enviamos spam."

### ETAPA 3 — Tela de Resultado

Esta é a tela mais importante. Deve conter:

**Bloco 1 — Diagnóstico personalizado:**
- Headline: "✅ Diagnóstico pronto, [NOME]!"
- Texto: "Identificamos 3 pontos críticos que estão travando o crescimento da sua empresa hoje:"
- 3 cards vermelhos com as dores identificadas (use lógica condicional baseada nas respostas — ver seção "LÓGICA DE DIAGNÓSTICO" abaixo)

**Bloco 2 — Prova social com VÍDEOS de cases:**
- Headline: "Veja o que conseguimos pra empresas como a sua:"
- Grid responsivo com **3 vídeos de cases de clientes** (use placeholders `<video>` com `src="videos/case-1.mp4"` até `case-3.mp4`, com `controls`, `poster="videos/case-1-thumb.jpg"`)
- Embaixo de cada vídeo: nome do cliente + 1 linha de resultado (ex: "Padaria Silva — +180% em vendas no delivery")

**Bloco 3 — Faixa de logos (de novo):**
- "Mais empresas que confiaram na Hadar:" + faixa de logos

**Bloco 4 — CTA final pro WhatsApp:**
- Headline: "Quer um plano de ação personalizado pra sua empresa?"
- Texto: "Nosso time vai te enviar uma proposta sob medida no WhatsApp, sem compromisso."
- **Botão GRANDE verde WhatsApp:** "📲 RECEBER MEU PLANO NO WHATSAPP"
- Selo de garantia: "✓ Atendimento humano  ✓ Sem compromisso  ✓ Resposta em até 1 hora útil"

---

## 🧠 LÓGICA DE DIAGNÓSTICO (3 dores personalizadas)

Use esta lógica em JavaScript pra montar as 3 dores:

**Dor 1 — Baseada na pergunta 4 (desafio principal):**
- "Não consigo gerar leads suficientes" → "🔴 Falta de previsibilidade na geração de leads — você depende da sorte ao invés de um sistema."
- "Gero leads, mas não convertem" → "🔴 Vazamento no funil de vendas — você atrai pessoas, mas perde dinheiro na conversão."
- "Não sei medir o que está funcionando" → "🔴 Decisões no escuro — sem métricas claras, cada real investido é uma aposta."
- "Não tenho tempo/equipe" → "🔴 Operação sobrecarregada — marketing virou mais um peso na sua agenda, não um motor de crescimento."
- "Faço tudo no achismo" → "🔴 Estratégia inexistente — sem direção, qualquer caminho parece certo (e nenhum leva longe)."

**Dor 2 — Baseada na pergunta 5 (o que já tentou):**
- Se marcou "Contratei outra agência antes" → "🔴 Frustração com agências que prometem e não entregam — você precisa de parceiros, não fornecedores."
- Se marcou "Ainda não tentei nada estruturado" → "🔴 Crescimento orgânico tem teto — sem estratégia paga e dados, sua empresa estaciona."
- Se marcou apenas "Tráfego pago" → "🔴 Tráfego pago sem estratégia de conteúdo é dinheiro queimado — anúncio sem autoridade não converte no Alto Paranaíba."
- Se marcou apenas "Indicações" → "🔴 Depender só de indicação é frágil — basta um mês ruim pra travar o caixa."
- Default → "🔴 Esforços fragmentados — você faz várias coisas, mas nada conversa entre si."

**Dor 3 — Baseada na pergunta 6 (vídeo):**
- "Não tenho nada" → "🔴 Ausência de prova social em vídeo — em 2026, quem não aparece, não vende."
- "Tenho alguns, mas amadores" → "🔴 Material de vídeo sem padrão profissional — passa a impressão errada do tamanho real da sua empresa."
- "Não gosto/tenho vergonha" → "🔴 O dono que não aparece transfere autoridade pra concorrência — e a vergonha custa caro."
- "Sim, gravo com frequência" → "🔴 Volume sem estratégia — gravar muito sem roteiro e edição profissional pulveriza o resultado."

---

## 🔗 INTEGRAÇÃO COM WHATSAPP

Quando o usuário clicar no botão final, abrir WhatsApp com:
- **Número:** Use o placeholder `5534XXXXXXXXX` (eu substituo depois)
- **Mensagem pré-preenchida** (URL encoded):

```
Olá! Acabei de fazer o diagnóstico no site da Hadar.

👤 Nome: [NOME]
🏢 Papel: [RESPOSTA 1]
⏱️ Tempo de empresa: [RESPOSTA 2]
💰 Faturamento: [RESPOSTA 3]
🎯 Maior desafio: [RESPOSTA 4]
🚀 Já tentei: [RESPOSTAS 5]
🎥 Vídeo: [RESPOSTA 6]
⏰ Urgência: [RESPOSTA 7]

Quero receber meu plano de ação personalizado!
```

Use `https://wa.me/5534XXXXXXXXX?text=` + `encodeURIComponent(mensagem)`.

---

## 🎨 DESIGN SYSTEM

**Paleta de cores:**
- Primária (verde Hadar — substituir depois): `#0F4C3A`
- Secundária/destaque: `#F4A300` (laranja vibrante pros CTAs)
- WhatsApp verde: `#25D366`
- Fundo claro: `#FAFAF7`
- Texto principal: `#1A1A1A`
- Texto secundário: `#6B6B6B`
- Vermelho dor: `#D64545`
- Borda suave: `#E5E5E0`

**Tipografia:**
- Headlines: `'Inter', system-ui, -apple-system, sans-serif` — peso 800
- Corpo: `'Inter', system-ui, sans-serif` — peso 400/500
- Importar do Google Fonts

**Estilo visual:**
- Mobile-first (a maioria vai responder pelo celular vindo do Facebook)
- Cards com bordas arredondadas (16px)
- Sombras suaves (não exagerar)
- Espaçamentos generosos
- Botões grandes (mínimo 56px de altura) com hover em escala 1.02
- Microanimações em transições entre perguntas (fade + slide-up sutil)
- Barra de progresso animada no topo durante o quiz

---

## 📱 REQUISITOS TÉCNICOS

1. **Single-file HTML** — todo CSS e JS embutidos
2. **Mobile-first responsivo** — testar em 375px, 768px, 1280px
3. **Sem frameworks** — HTML, CSS e JS vanilla
4. **Performance:** carregamento <2s, sem dependências pesadas
5. **Acessibilidade:** labels nos inputs, contraste AA, navegação por teclado
6. **State management:** guardar respostas em objeto JS (`quizState`)
7. **Validação:** não avançar sem resposta selecionada; validar formato do WhatsApp
8. **Tracking:** incluir placeholders pra Meta Pixel e Google Analytics 4 (GA4) com eventos:
   - `quiz_started` (clique no CTA inicial)
   - `quiz_question_answered` (cada resposta, com `question_number`)
   - `quiz_completed` (finalizou as 7 perguntas)
   - `lead_generated` (preencheu nome/whatsapp)
   - `whatsapp_redirect` (clique no botão final)

---

## 📂 ESTRUTURA DE ARQUIVOS ESPERADA

```
quiz-hadar/
├── index.html              (arquivo único com tudo)
├── assets/
│   ├── logos/              (placeholders cliente-1.png até cliente-8.png)
│   ├── videos/             (case-1.mp4 a case-3.mp4 + thumbs .jpg)
│   └── logo-hadar.png      (logo da agência no header)
└── README.md               (instruções de como substituir os placeholders)
```

---

## ✅ ENTREGÁVEIS

1. `index.html` completo e funcional
2. `README.md` explicando:
   - Onde colocar os logos de clientes (formato, tamanho recomendado)
   - Onde colocar os vídeos de cases (formato MP4, peso máximo, dimensões)
   - Como trocar o número de WhatsApp
   - Como adicionar IDs do Meta Pixel e GA4
   - Como hospedar (sugestão: Cloudflare Pages, Netlify ou Vercel — todos grátis)

---

## 🚀 EXECUTE

Construa o quiz seguindo TODAS as especificações acima. Priorize:
1. **Conversão** — cada elemento deve empurrar pro próximo passo
2. **UX mobile** — vai rodar no Facebook, então 80%+ vem do celular
3. **Velocidade** — sem peso desnecessário
4. **Código limpo** — comentado nas seções principais pra facilitar manutenção

Comece pelo HTML estrutural, depois CSS, depois JavaScript com a lógica completa. No final, gere o README.
