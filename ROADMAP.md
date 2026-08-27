# ROADMAP — AI Ebook Creator

Última atualização: 2026-08-27

---

## Fase 0 — Fundação ✅

- [x] Repositório criado
- [x] Celebro instalado
- [x] README inicial
- [x] Protótipo HTML com upload (texto, áudio, imagens)
- [x] Detecção básica de capítulos
- [x] Geração real de PDF no navegador
- [x] Sugestões de plataformas de venda

---

## Fase 1 — Core útil ✅

- [x] Campo de título do e-book
- [x] Detecção de capítulos mais inteligente
- [x] Download de PDF funcional
- [x] Gravação de áudio direto no navegador (MediaRecorder)
- [x] Incluir imagens no PDF
- [x] Preview mais rico dos capítulos (stats + contagem de palavras)
- [ ] Melhorar capa do PDF (polish opcional)

---

## Fase 2 — Inteligência real 🚧

**Objetivo:** a IA de fato escreve e organiza o conteúdo.

- [x] Integração com API de IA (OpenAI + Grok/xAI + custom OpenAI-compatible)
- [x] Configuração de API Key salva no localStorage
- [x] Estruturação e melhoria de capítulos pela IA
- [x] Geração de sinopse automática
- [x] Fallback para modo local se não houver chave ou der erro
- [ ] Transcrição de áudio automática (Whisper)
- [ ] Reescrita/expansão mais profunda por capítulo
- [ ] Posicionamento inteligente de imagens na narrativa
- [ ] Geração de texto de vendas / blurb

---

## Fase 3 — Formatos e publicação

- [ ] Exportar EPUB além de PDF
- [ ] Template de capa editável
- [ ] Metadados do e-book (autor, ISBN placeholder, etc.)
- [ ] Checklist de publicação por plataforma
- [ ] Links diretos / instruções passo a passo

---

## Fase 4 — Produto

- [ ] Decidir stack definitiva
- [ ] Backend leve (proxy de API + histórico) — recomendado por causa de CORS
- [ ] Login / salvar projetos
- [ ] Histórico de e-books gerados
- [ ] Deploy (Vercel / Netlify / Cloudflare Pages)

---

## Fase 5 — Polimento e escala

- [ ] Temas claro/escuro
- [ ] Múltiplos idiomas
- [ ] Templates de gênero
- [ ] Analytics básico
- [ ] Monetização (se fizer sentido)

---

## Decisões em aberto

| Tema | Status |
|------|--------|
| Modelo de IA preferido | Usuário escolhe (OpenAI / Grok / custom) |
| Backend vs só front-end | Front-end primeiro; backend recomendado para CORS e segurança da key |
| Formato prioritário | PDF primeiro, EPUB depois |
| Nome final do produto | AI Ebook Creator (provisório) |

---

## Nota técnica importante

Chamadas diretas à API de OpenAI/xAI a partir do navegador podem ser bloqueadas por **CORS**.  
Para uso em produção, o ideal é um backend/proxy simples que guarda a chave no servidor.

*Atualize este arquivo sempre que uma fase for concluída ou prioridade mudar.*
