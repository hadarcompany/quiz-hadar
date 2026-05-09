# Quiz Funnel — Agência Hadar

Quiz de diagnóstico de marketing para qualificação de leads via WhatsApp.

---

## Estrutura de arquivos

```
Quiz hadar/
├── index.html
└── assets/
    ├── logo-hadar.png          ← logo da agência (cabeçalho)
    ├── logos/
    │   ├── cliente-1.png       ← logos dos clientes (faixa de prova social)
    │   ├── cliente-2.png
    │   ├── ...
    │   └── cliente-8.png
    └── videos/
        ├── case-1.mp4          ← vídeo do case 1
        ├── case-1-thumb.jpg    ← thumbnail do case 1
        ├── case-2.mp4
        ├── case-2-thumb.jpg
        ├── case-3.mp4
        └── case-3-thumb.jpg
```

---

## Como substituir os placeholders

### Logo da agência
Salve o arquivo como `assets/logo-hadar.png`.  
Tamanho recomendado: **200 × 60 px**, fundo transparente (PNG).  
Se o arquivo não existir, o nome "AGÊNCIA HADAR" aparece automaticamente como fallback.

### Logos de clientes
Salve em `assets/logos/` com os nomes `cliente-1.png` até `cliente-8.png`.  
Tamanho recomendado: **200 × 80 px** (proporção livre), fundo branco ou transparente.  
As imagens aparecem em escala de cinza e revelam cor no hover.

### Vídeos de cases
Salve os arquivos em `assets/videos/`:

| Arquivo | Descrição |
|---|---|
| `case-1.mp4` | Vídeo do case 1 |
| `case-1-thumb.jpg` | Thumbnail (capa) do vídeo 1 |
| `case-2.mp4` / `case-2-thumb.jpg` | Case 2 |
| `case-3.mp4` / `case-3-thumb.jpg` | Case 3 |

Recomendações:
- Formato: **MP4 (H.264)**
- Resolução: **1280 × 720** (16:9)
- Peso máximo: **20 MB por vídeo** (para carregamento rápido em mobile)
- Thumbnails: **1280 × 720 px**, JPEG, ~100 KB

Para editar o nome do cliente e o resultado embaixo de cada vídeo, busque no `index.html` por `"Substitua o nome aqui"` e troque o texto.

### Número de WhatsApp
O número já está configurado como `5534999386446`.  
Para alterar, busque no `index.html` por `WHATSAPP_NUMBER` e troque o número na linha seguinte.

### Textos dos cases
No `index.html`, busque por `Substitua o nome aqui` para encontrar os 3 blocos de case e editar nome do cliente e resultado.

---

## Como ativar rastreamento

### Meta Pixel
1. Abra `index.html`
2. Encontre o bloco comentado `<!-- META PIXEL -->`
3. Descomente e substitua `YOUR_PIXEL_ID` pelo ID do seu pixel

**Eventos disparados:**
- `quiz_started` — clique no CTA inicial
- `quiz_question_answered` — cada resposta (com `question_number`)
- `quiz_completed` — finalizou as 7 perguntas
- `lead_generated` — preencheu nome e WhatsApp
- `whatsapp_redirect` — clique no botão final

### Google Analytics 4
1. Encontre o bloco comentado `<!-- GA4 -->`
2. Descomente e substitua `G-XXXXXXXXXX` pelo seu Measurement ID

Os mesmos eventos acima também são enviados ao GA4.

---

## Como hospedar (grátis)

### Opção 1 — Netlify (mais simples)
1. Acesse [netlify.com](https://netlify.com) e crie uma conta gratuita
2. Arraste a pasta `Quiz hadar` para a área de deploy
3. Pronto — você recebe um link público em segundos
4. Conecte um domínio personalizado nas configurações

### Opção 2 — Cloudflare Pages
1. Acesse [pages.cloudflare.com](https://pages.cloudflare.com)
2. Faça upload direto ou conecte um repositório GitHub
3. Ideal para quem já usa Cloudflare no domínio

### Opção 3 — Vercel
1. Acesse [vercel.com](https://vercel.com)
2. Deploy via arrastar pasta ou GitHub
3. Domínio personalizado gratuito incluso

---

## Cor primária da marca

A cor principal atual é `#0F4C3A` (verde escuro).  
Para trocar, abra `index.html` e altere a variável CSS no topo:

```css
--c-primary: #0F4C3A;
```

---

## Checklist antes de publicar

- [ ] Logo da agência (`assets/logo-hadar.png`)
- [ ] 8 logos de clientes (`assets/logos/cliente-1.png` … `cliente-8.png`)
- [ ] 3 vídeos de cases + thumbnails (`assets/videos/`)
- [ ] Nomes e resultados dos cases atualizados no HTML
- [ ] Número de WhatsApp correto (`5534999386446`)
- [ ] Meta Pixel ID configurado (opcional)
- [ ] GA4 Measurement ID configurado (opcional)
- [ ] Cor primária da marca ajustada (se necessário)
- [ ] Testado no celular (Chrome/Safari mobile)
