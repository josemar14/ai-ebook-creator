# Celebro.md — Cérebro do projeto AI Ebook Creator

> Leia no início de sessões longas. Atualize em decisões de produto.  
> Fases → `ROADMAP.md` · Kit: https://github.com/josemar14/celebro

**Última atualização:** 2026-08-27  
**Dono:** josemar14  
**Repo:** https://github.com/josemar14/ai-ebook-creator  

---

## 1. Produto

App web HTML de criação de e-book com IA.  
Usuário envia texto/áudio/imagens → IA estrutura, gera sinopse + blurb → PDF baixável + sugestões de venda.

**Hoje já faz:** gravação de áudio, transcrição Whisper (OpenAI), geração com IA (capítulos + sinopse + texto de vendas), PDF com imagens.

---

## 2. Stack

| Camada | Tech |
|--------|------|
| Frontend | HTML + CSS + JS vanilla |
| PDF | jsPDF |
| Áudio | MediaRecorder + Whisper API |
| IA chat | OpenAI / xAI Grok / custom |

**Entrypoint:** `index.html`  
**Config IA:** `localStorage` (nunca no repo)

---

## 3. Regras

- Texto e/ou áudio; múltiplas imagens
- Com API Key → IA estrutura + sinopse + blurb
- Whisper só com OpenAI (ou endpoint compatible)
- Sem chave / erro → modo local
- Nunca commitar API keys
- Interface em PT-BR

---

## 4. Secrets (só nomes)

`OPENAI_API_KEY` · `XAI_API_KEY` / Grok key  
(ficam no localStorage do usuário)

---

## 5. Fluxo

1. (Opcional) Configurar API Key
2. Título + texto e/ou áudio (+ imagens)
3. Transcrever áudio (botão Whisper) se quiser
4. Gerar e-book → preview com sinopse + blurb + caps
5. Baixar PDF
6. Ver plataformas de venda

---

## 6. Decisões recentes

| Tema | Decisão |
|------|--------|
| Whisper | Botão dedicado + auto-transcribe se só áudio na geração |
| Blurb | Campo `blurb` no JSON da IA + página no PDF |
| Fase | Fase 2 quase fechada → próxima = Fase 3 (EPUB) ou proxy |
| CORS | Documentado; proxy na Fase 4 |

---

## 7. Arquivos-chave

`index.html` · `Celebro.md` · `ROADMAP.md` · `README.md` · `AGENTS.md`

---

## 8. Próximo

- EPUB
- Backend proxy
- Deploy

---

## 9. Como a IA trabalha aqui

1. Editar arquivos existentes  
2. Atualizar Celebro após decisões  
3. Sem secrets no arquivo  
4. Responder em português  
5. Seguir ROADMAP  
